# imp_online_new_channel_supplement

## 表描述
新增渠道补充表

## 字段信息

| 字段名称 | 数据类型 | 是否可空 | 默认值 | 字段描述 |
|---------|----------|----------|--------|----------|
| checkout_time | VARCHAR(255) | 是 |  | 结账时间 |
| store_code | VARCHAR(255) | 是 |  | 门店编码 |
| payment_channel | VARCHAR(255) | 是 |  | 支付渠道 |
| order_count | INT | 是 |  | 订单量 |
| actual_amount | DECIMAL(16,2) | 是 |  | 实收金额 |
| discount_amount | DECIMAL(16,2) | 是 |  | 优惠金额 |
| transaction_amount | DECIMAL(16,2) | 是 |  | 流水金额 |
| total_order_count | INT | 是 |  | 总订单量 |
| payment_time | VARCHAR(255) | 是 |  | 支付时间 |
| ds | VARCHAR(255) | 是 |  | ds |
| biz_table_result_id | VARCHAR(255) | 是 |  | biz_table_result_id |

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

