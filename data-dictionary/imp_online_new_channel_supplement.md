# imp_online_new_channel_supplement

## 表描述
OLAP

## 数据量
- 总记录数：27,903 条

## 字段信息

| 字段名称 | 数据类型 | 是否可空 | 默认值 | 字段描述 | 示例 |
|---------|----------|----------|--------|----------|------|
| checkout_time | VARCHAR(255) | 是 |  | 结账时间 | 20250109 |
| store_code | VARCHAR(255) | 是 |  | 门店编码 | TLLBL003 |
| payment_channel | VARCHAR(255) | 是 |  | 支付渠道 | 线上新增快手团购 |
| order_count | INT | 是 |  | 订单量 | 3 |
| actual_amount | DECIMAL(16,2) | 是 |  | 实收金额 | 20.50 |
| discount_amount | DECIMAL(16,2) | 是 |  | 优惠金额 | 0.77 |
| transaction_amount | DECIMAL(16,2) | 是 |  | 流水金额 | 7.00 |
| total_order_count | INT | 是 |  | 总订单量 | 1 |
| payment_time | VARCHAR(255) | 是 |  | 支付时间 | 20250103 |
| ds | VARCHAR(255) | 是 |  | ds | 2025-07-01 |
| biz_table_result_id | VARCHAR(255) | 是 |  | biz_table_result_id | 1939883283961671682 |

## 使用说明

### 常用查询示例

```sql
-- 查询最新数据
SELECT * FROM imp_online_new_channel_supplement 
ORDER BY business_date DESC 
LIMIT 10;

-- 查询数据总量
SELECT COUNT(*) FROM imp_online_new_channel_supplement;

-- 查询某日数据
SELECT * FROM imp_online_new_channel_supplement 
WHERE business_date = 20240101;
```

### 注意事项
- 时间字段通常为bigint类型，格式为YYYYMMDD
- 金额字段单位为分，需要除以100转换为元
- 字符类型字段需要注意大小写敏感问题
