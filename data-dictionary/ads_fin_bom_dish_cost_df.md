# ads_fin_bom_dish_cost_df

## 表描述
OLAP - 菜品BOM成本表，用于计算菜品成本结构

## 数据量
- 总记录数：12,832 条

## 字段信息

| 字段名称 | 数据类型 | 是否可空 | 默认值 | 字段描述 |
|---------|----------|----------|--------|----------|
| bom_code | VARCHAR(255) | 是 |  | BOM编码 |
| bom_name | VARCHAR(255) | 是 |  | BOM名称 |
| cup_sepc | VARCHAR(255) | 是 |  | 杯型规格 |
| item_code | VARCHAR(255) | 是 |  | 物料编码 |
| item_name | VARCHAR(255) | 是 |  | 物料名称 |
| use_quantity | DECIMAL(16,2) | 是 |  | 物料数量 |
| use_unit | VARCHAR(255) | 是 |  | 物料单位 |
| sale_unit | VARCHAR(255) | 是 |  | 销售单位，仅RAW(原料)有效 |
| raw_usage_qty | DECIMAL(16,2) | 是 |  | 用量数量，仅RAW(原料)有效 |
| raw_usage_unit | VARCHAR(255) | 是 |  | 用量单位，仅RAW(原料)有效 |
| spec_id | VARCHAR(255) | 是 |  | 规格 |
| spec_name | VARCHAR(255) | 是 |  | 规格名称 |
| cup_code | VARCHAR(255) | 是 |  | 杯型编码 |
| cup_name | VARCHAR(255) | 是 |  | 杯型名称 |
| temperature_name | VARCHAR(255) | 是 |  | 温度 |
| sweetness_name | VARCHAR(255) | 是 |  | 甜度 |
| region_name | VARCHAR(255) | 是 |  | 区域名称 |
| item_cate_code | VARCHAR(255) | 是 |  | 物料分类编码 |
| item_cate_name | VARCHAR(255) | 是 |  | 区域分类名称 |
| purc_price | DECIMAL(16,2) | 是 |  | 报货原价 |
| dish_price | DECIMAL(16,2) | 是 |  | 菜品价格 |
| pt | VARCHAR(255) | 是 |  | 天分区 |

## 业务说明

### BOM结构说明
- **BOM编码**：唯一标识一个菜品或产品的配方
- **物料编码**：组成菜品的原材料编码
- **物料分类**：将物料按类别分组管理
- **杯型规格**：不同杯型对应不同的物料用量

### 成本计算逻辑
- **物料成本** = 物料数量 × 报货原价
- **菜品总成本** = 所有物料成本之和
- **成本占比** = 物料成本 / 菜品售价

## 使用场景

### 1. 成本分析
```sql
-- 查询某菜品的成本构成
SELECT 
    bom_name,
    item_name,
    use_quantity,
    use_unit,
    purc_price,
    (use_quantity * purc_price) as item_cost
FROM ads_fin_bom_dish_cost_df 
WHERE bom_name = '经典珍珠奶茶'
ORDER BY item_cost DESC;
```

### 2. 物料用量分析
```sql
-- 查询某物料在所有菜品中的用量
SELECT 
    item_name,
    bom_name,
    use_quantity,
    use_unit,
    cup_name,
    temperature_name
FROM ads_fin_bom_dish_cost_df 
WHERE item_name = '珍珠'
ORDER BY use_quantity DESC;
```

### 3. 区域成本对比
```sql
-- 按区域分析菜品成本差异
SELECT 
    region_name,
    bom_name,
    AVG(dish_price) as avg_dish_price,
    SUM(use_quantity * purc_price) as total_material_cost
FROM ads_fin_bom_dish_cost_df 
GROUP BY region_name, bom_name
ORDER BY region_name, total_material_cost DESC;
```

## 常用查询示例

```sql
-- 查询最新数据
SELECT * FROM ads_fin_bom_dish_cost_df 
ORDER BY pt DESC 
LIMIT 10;

-- 查询数据总量
SELECT COUNT(*) FROM ads_fin_bom_dish_cost_df;

-- 查询某日数据
SELECT * FROM ads_fin_bom_dish_cost_df 
WHERE pt = '20240101';

-- 查询某BOM的所有物料
SELECT 
    bom_code,
    bom_name,
    item_code,
    item_name,
    use_quantity,
    purc_price,
    (use_quantity * purc_price) as item_cost
FROM ads_fin_bom_dish_cost_df 
WHERE bom_code = 'BOM001'
ORDER BY item_cost DESC;
```

## 注意事项

1. **时间格式**：pt字段为分区字段，格式为YYYYMMDD
2. **金额单位**：所有金额字段单位为分，需要除以100转换为元
3. **物料分类**：item_cate_code和item_cate_name对应物料的分类体系
4. **杯型差异**：不同杯型(cup_code)对应不同的物料用量(use_quantity)
5. **温度甜度**：temperature_name和sweetness_name影响最终的物料配置
6. **区域差异**：region_name可能导致价格和用量的区域差异

## 数据更新频率
- **更新周期**：每日更新
- **更新时间**：凌晨2:00-4:00
- **历史数据**：保留最近2年数据