# ads_dbs_trade_shop_pay_channel_di

## 表描述

各支付渠道营业额


## 字段信息

| 字段名称 | 数据类型 | 是否可空 | 默认值 | 字段描述 |
|---------|----------|----------|--------|----------|
| pt | VARCHAR(20) | 是 |  | 分区时间 |
| shop_id | VARCHAR(20) | 是 |  | 门店id(标准化) |
| payment_channels | VARCHAR(50) | 是 |  | 结账方式名称 |
| order_cnt | INT | 是 |  | 订单量 |
| income | DECIMAL(16,2) | 是 |  | 收入金额 |
| discount | DECIMAL(16,2) | 是 |  | 优惠金额 |
| amount | DECIMAL(16,2) | 是 |  | 流水金额 |
| total_order_cnt | INT | 是 |  | 订单量 |
| pay_way_created_time | VARCHAR(20) | 是 |  | 支付创建时间 |

## 使用说明

### 常用查询示例

```sql
-- 查询最新数据
SELECT * FROM ads_dbs_trade_shop_pay_channel_di 
ORDER BY business_date DESC 
LIMIT 10;

-- 查询数据总量
SELECT COUNT(*) FROM ads_dbs_trade_shop_pay_channel_di;

-- 查询某日数据
SELECT * FROM ads_dbs_trade_shop_pay_channel_di 
WHERE business_date = 20240101;
```