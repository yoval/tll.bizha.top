# ads_dbs_trade_shop_pay_channel_di


## 字段信息

| 字段名称 | 数据类型 | 是否可空 | 默认值 | 字段描述 | 示例 |
|---------|----------|----------|--------|----------|------|
| pt | VARCHAR(20) | 是 |  | 分区时间 | 20240106 |
| shop_id | VARCHAR(20) | 是 |  | 门店id(标准化) | ZYD00206 |
| payment_channels | VARCHAR(50) | 是 |  | 结账方式名称 | 美团外卖 |
| order_cnt | INT | 是 |  | 订单量 | 6 |
| income | DECIMAL(16,2) | 是 |  | 收入金额 | 171.39 |
| discount | DECIMAL(16,2) | 是 |  | 优惠金额 | 214.99 |
| amount | DECIMAL(16,2) | 是 |  | 流水金额 | 774.50 |
| total_order_cnt | INT | 是 |  | 订单量 | 187 |
| pay_way_created_time | VARCHAR(20) | 是 |  | 支付创建时间 | 20240106 |