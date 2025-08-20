# ads_dbs_trade_shop_pay_channel_di

## 表描述
OLAP

## 数据量
- 总记录数：17,510,081 条

## 字段信息

| 字段名称 | 数据类型 | 是否可空 | 默认值 | 字段描述 | 示例 |
|---------|----------|----------|--------|----------|------|
| pt | VARCHAR(20) | 是 |  | 分区时间 | 20240103 |
| shop_id | VARCHAR(20) | 是 |  | 门店id(标准化) | ZYD00206 |
| payment_channels | VARCHAR(50) | 是 |  | 结账方式名称 | 美团外卖 |
| order_cnt | INT | 是 |  | 订单量 | 14 |
| income | DECIMAL(16,2) | 是 |  | 收入金额 | 190.41 |
| discount | DECIMAL(16,2) | 是 |  | 优惠金额 | 136.80 |
| amount | DECIMAL(16,2) | 是 |  | 流水金额 | 405.40 |
| total_order_cnt | INT | 是 |  | 订单量 | 187 |
| pay_way_created_time | VARCHAR(20) | 是 |  | 支付创建时间 | 20240103 |

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

### 注意事项
- 时间字段通常为bigint类型，格式为YYYYMMDD
- 金额字段单位为分，需要除以100转换为元
- 字符类型字段需要注意大小写敏感问题
