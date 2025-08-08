# ads_fin_shop_item_consume_di

## 表描述

门店物料消耗表


## 字段详情

| 字段名称 | 数据类型 | 是否可空 | 默认值 | 字段说明 |
|---------|----------|----------|--------|----------|
| shop_id | varchar | 是 | NULL | 门店编码 |
| item_cate_name | varchar | 是 | NULL | 物料类型名称 |
| item_code | varchar | 是 | NULL | 物料编码 |
| item_name | varchar | 是 | NULL | 物料名称 |
| use_quantity | decimal | 是 | NULL | 物料使用数量 |
| use_unit | varchar | 是 | NULL | 物料使用单位 |
| pack_qty | decimal | 是 | NULL | 包装数量 |
| pack_unit | varchar | 是 | NULL | 包装单位 |
| sale_quantity | decimal | 是 | NULL | 销售数量 |
| sale_unit | varchar | 是 | NULL | 销售单位 |
| pt | varchar | 是 | NULL | 天分区 |

## 业务说明

### 物料类型分类
- **食材类**: 各类食品原材料
- **包装类**: 包装材料、餐具
- **调料类**: 各类调味品
- **半成品**: 预加工食品
- **其他**: 辅助材料

### 关键指标计算
- **物料使用效率**: `sale_quantity / use_quantity`
- **单位销售消耗**: `use_quantity / sale_quantity`
- **包装转换率**: `use_quantity / pack_qty`

### 使用场景
1. **成本分析**: 统计各门店物料成本
2. **效率评估**: 分析物料使用效率
3. **库存预警**: 基于消耗预测库存需求
4. **异常监控**: 识别异常消耗情况
5. **供应商管理**: 评估物料采购需求

## 常用查询示例

### 1. 查询某日各门店物料消耗总量
```sql
SELECT 
    shop_id,
    item_cate_name,
    SUM(use_quantity) as total_use_qty,
    SUM(sale_quantity) as total_sale_qty,
    ROUND(SUM(use_quantity)/SUM(sale_quantity), 4) as unit_consumption
FROM ads_fin_shop_item_consume_di
WHERE pt = '20241201'
GROUP BY shop_id, item_cate_name
ORDER BY total_use_qty DESC;
```

### 2. 查询某物料在各门店的使用情况
```sql
SELECT 
    shop_id,
    item_name,
    use_quantity,
    use_unit,
    sale_quantity,
    sale_unit,
    ROUND(use_quantity/sale_quantity, 4) as consumption_rate
FROM ads_fin_shop_item_consume_di
WHERE item_code = 'ITEM001'
AND pt BETWEEN '20241201' AND '20241231'
ORDER BY use_quantity DESC;
```

### 3. 统计某时间段内消耗TOP的物料
```sql
SELECT 
    item_code,
    item_name,
    item_cate_name,
    SUM(use_quantity) as total_use,
    SUM(sale_quantity) as total_sale,
    COUNT(DISTINCT shop_id) as shop_count
FROM ads_fin_shop_item_consume_di
WHERE pt BETWEEN '20241201' AND '20241231'
GROUP BY item_code, item_name, item_cate_name
ORDER BY total_use DESC
LIMIT 20;
```

### 4. 分析各物料类型的消耗占比
```sql
SELECT 
    item_cate_name,
    SUM(use_quantity) as total_use,
    ROUND(SUM(use_quantity) * 100.0 / SUM(SUM(use_quantity)) OVER(), 2) as percentage
FROM ads_fin_shop_item_consume_di
WHERE pt = '20241201'
GROUP BY item_cate_name
ORDER BY percentage DESC;
```

### 5. 查询门店物料使用效率排名
```sql
SELECT 
    shop_id,
    item_cate_name,
    SUM(use_quantity) as total_use,
    SUM(sale_quantity) as total_sale,
    ROUND(SUM(sale_quantity)/SUM(use_quantity), 2) as efficiency_ratio
FROM ads_fin_shop_item_consume_di
WHERE pt BETWEEN '20241201' AND '20241231'
GROUP BY shop_id, item_cate_name
HAVING total_sale > 100
ORDER BY efficiency_ratio DESC
LIMIT 10;
```

## 包装单位转换

### 常见单位换算
```sql
-- 计算包装使用率
SELECT 
    item_name,
    pack_unit,
    use_unit,
    pack_qty,
    use_quantity,
    ROUND(use_quantity/pack_qty, 2) as pack_usage
FROM ads_fin_shop_item_consume_di
WHERE pt = '20241201'
ORDER BY pack_usage DESC;
```

### 库存预警查询
```sql
-- 基于历史消耗预测未来需求
SELECT 
    shop_id,
    item_code,
    item_name,
    AVG(use_quantity) as avg_daily_use,
    STDDEV(use_quantity) as use_variance,
    MAX(use_quantity) as max_daily_use
FROM ads_fin_shop_item_consume_di
WHERE pt >= DATE_SUB('20241201', INTERVAL 30 DAY)
GROUP BY shop_id, item_code, item_name
HAVING avg_daily_use > 0
ORDER BY avg_daily_use DESC;
```

## 数据质量检查

### 1. 检查异常消耗
```sql
SELECT * FROM ads_fin_shop_item_consume_di
WHERE use_quantity <= 0 OR sale_quantity <= 0;
```

### 2. 检查缺失物料信息
```sql
SELECT * FROM ads_fin_shop_item_consume_di
WHERE item_code IS NULL OR item_name IS NULL;
```

### 3. 检查单位不一致
```sql
SELECT DISTINCT item_code, use_unit, sale_unit
FROM ads_fin_shop_item_consume_di
WHERE use_unit != sale_unit;
```