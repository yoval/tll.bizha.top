# ads_fin_shop_item_consume_di

## 表描述
OLAP

## 数据量
- 总记录数：22,929,230 条

## 字段信息

| 字段名称 | 数据类型 | 是否可空 | 默认值 | 字段描述 | 示例 |
|---------|----------|----------|--------|----------|------|
| shop_id | VARCHAR(128) | 是 |  | 门店编码 | TLL00001 |
| item_cate_name | VARCHAR(128) | 是 |  | 物料类型名称 | 冷冻类 |
| item_code | VARCHAR(128) | 是 |  | 物料编码 | 110000002 |
| item_name | VARCHAR(512) | 是 |  | 物料名称 | 咖啡粉-250g*40包/件 |
| use_quantity | DECIMAL(20,8) | 是 |  | 物料使用数量 | 580.00000000 |
| use_unit | VARCHAR(8) | 是 |  | 物料使用单位 | G |
| pack_qty | DECIMAL(20,8) | 是 |  | 包装数量 | 0.18000000 |
| pack_unit | VARCHAR(8) | 是 |  | 包装单位 | BOT |
| sale_quantity | DECIMAL(20,8) | 是 |  | 销售数量 | 0.01100000 |
| sale_unit | VARCHAR(8) | 是 |  | 销售单位 | JAN |
| pt | VARCHAR(8) | 是 |  | 天分区 | 20250808 |

## 使用说明

### 常用查询示例

```sql
-- 查询最新数据
SELECT * FROM ads_fin_shop_item_consume_di 
ORDER BY business_date DESC 
LIMIT 10;

-- 查询数据总量
SELECT COUNT(*) FROM ads_fin_shop_item_consume_di;

-- 查询某日数据
SELECT * FROM ads_fin_shop_item_consume_di 
WHERE business_date = 20240101;
```

### 注意事项
- 时间字段通常为bigint类型，格式为YYYYMMDD
- 金额字段单位为分，需要除以100转换为元
- 字符类型字段需要注意大小写敏感问题
