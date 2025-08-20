# ads_fin_bom_dish_cost_df

## 表描述
OLAP

## 数据量
- 总记录数：12,832 条

## 字段信息

| 字段名称 | 数据类型 | 是否可空 | 默认值 | 字段描述 | 示例 |
|---------|----------|----------|--------|----------|------|
| bom_code | VARCHAR(128) | 是 |  | BOM编码 | 10000016 |
| bom_name | VARCHAR(128) | 是 |  | BOM名称 | 清风茉白鲜奶茶 |
| cup_sepc | VARCHAR(128) | 是 |  | 杯型规格 | 700ml |
| item_code | VARCHAR(128) | 是 |  | 物料编码 | 030001006 |
| item_name | VARCHAR(128) | 是 |  | 物料名称 | 调味糖浆-6kg*4瓶/箱 |
| use_quantity | DECIMAL(20,8) | 是 |  | 物料数量 | 2.12766000 |
| use_unit | VARCHAR(32) | 是 |  | 物料单位 | ML |
| sale_unit | VARCHAR(32) | 是 |  | 销售单位，仅RAW(原料)有效 | JAN |
| raw_usage_qty | DECIMAL(20,4) | 是 |  | 用量数量，仅RAW(原料)有效 | 18000.0000 |
| raw_usage_unit | VARCHAR(32) | 是 |  | 用量单位，仅RAW(原料)有效 | ML |
| spec_id | VARCHAR(128) | 是 |  | 规格 | 964199882636203630 |
| spec_name | VARCHAR(128) | 是 |  | 规格名称 | 海南-标准-热-三分糖 |
| cup_code | VARCHAR(128) | 是 |  | 杯型编码 | common |
| cup_name | VARCHAR(128) | 是 |  | 杯型名称 | 标准 |
| temperature_name | VARCHAR(32) | 是 |  | 温度 | 热 |
| sweetness_name | VARCHAR(32) | 是 |  | 甜度 | 不额外加糖 |
| region_name | VARCHAR(32) | 是 |  | 区域名称 | 海南 |
| item_cate_code | VARCHAR(128) | 是 |  | 物料分类编码 | 205 |
| item_cate_name | VARCHAR(128) | 是 |  | 区域分类名称 | 水果制品类 |
| purc_price | DECIMAL(20,4) | 是 |  | 报货原价 | 650.0000 |
| dish_price | DECIMAL(20,4) | 是 |  | 菜品价格 | 4.0000 |
| pt | VARCHAR(8) | 是 |  | 天分区 | 20250819 |

## 使用说明

### 常用查询示例

```sql
-- 查询最新数据
SELECT * FROM ads_fin_bom_dish_cost_df 
ORDER BY business_date DESC 
LIMIT 10;

-- 查询数据总量
SELECT COUNT(*) FROM ads_fin_bom_dish_cost_df;

-- 查询某日数据
SELECT * FROM ads_fin_bom_dish_cost_df 
WHERE business_date = 20240101;
```

### 注意事项
- 时间字段通常为bigint类型，格式为YYYYMMDD
- 金额字段单位为分，需要除以100转换为元
- 字符类型字段需要注意大小写敏感问题
