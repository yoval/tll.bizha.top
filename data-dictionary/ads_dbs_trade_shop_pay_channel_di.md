# ads_dbs_trade_shop_pay_channel_di


## 字段信息

| 列名              | 数据类型         | 注释           |
| ----------------- | ---------------- | -------------- |
| pt                | varchar(20)      | 时间分区       |
| shop_id           | varchar(20)      | 门店id(标准化) |
| payment_channels  | varchar(100)     | 结账方式名称   |
| order_cnt         | bigint(20)       | 订单量         |
| income            | decimalv3(16, 2) | 收入金额       |
| discount          | decimalv3(16, 2) | 优惠金额       |
| amount            | decimalv3(16, 2) | 流水金额       |
| total_order_cnt   | bigint(20)       | 订单量         |
| item_scrap_amount | decimalv3(16, 2) | 报废金额       |