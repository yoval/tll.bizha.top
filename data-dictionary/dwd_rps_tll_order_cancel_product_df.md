# dwd_rps_tll_order_cancel_product_df


## 字段信息

| 字段名称 | 数据类型 | 是否可空 | 默认值 | 字段描述 | 示例 |
|---------|----------|----------|--------|----------|------|
| id | BIGINT | 是 |  | 主键ID，使用雪花算法生成的自定义long类型 | 484254501395120128 |
| serial_no | VARCHAR(255) | 是 |  | 流水号，从订单商品明细继承过来 | 327484 |
| product_code | VARCHAR(255) | 是 |  | 商品编码 | 010000001 |
| product_name | VARCHAR(255) | 是 |  | 商品名称 | 8L保温桶 |
| product_specification | VARCHAR(255) | 是 |  | 商品规格 | 5kg*2包/件 |
| product_unit | VARCHAR(255) | 是 |  | 单位编码，当前下单对应的单位编码+名称 | 个 |
| is_gift | INT | 是 |  | 是否赠品，默认0:否  1:是 | 0 |
| cancel_quantity | INT | 是 |  | 取消数量 | 12 |
| refund_unit_price | DECIMAL(10,3) | 是 |  | 退款单价，对应订单中原折后含税单价 | 200.000 |
| subtotal | DECIMAL(10,3) | 是 |  | 小计 | 9.000 |
| discount_amount | DECIMAL(10,3) | 是 |  | 优惠金额，商品单价和折后单价的差乘以数量 | 1.000 |
| actual_refund_amount | DECIMAL(10,3) | 是 |  | 银行卡实退金额 | 198.760 |
| pt_discount_amount | DECIMAL(10,3) | 是 |  | 平台优惠退的金额 | 1.610 |
| agent_amount | DECIMAL(10,3) | 是 |  | 代理商代收代付款 | 0.000 |
| business_discount | DECIMAL(10,3) | 是 |  | 招商优惠 | 0.000 |
| customer_discount | DECIMAL(10,3) | 是 |  | 客户往来款 | 0.000 |
| house_subsidy | DECIMAL(10,3) | 是 |  | 房租优惠 | 0.000 |
| cancel_order_id | BIGINT | 是 |  | 退款单id | 484249094496862208 |
| create_time | VARCHAR(255) | 是 |  | 创建时间 | 2024-08-29 14:56:25 |
| update_time | VARCHAR(255) | 是 |  | 更新时间 | 2024-08-28 23:37:42 |
| create_by | VARCHAR(255) | 是 |  | 创建者 |  |
| update_by | VARCHAR(255) | 是 |  | 修改者 |  |
| order_id | BIGINT | 是 |  | 订单ID，long类型 | 484300110244102144 |
| product_id | BIGINT | 是 |  | 商品ID，long类型 | 483962582345060352 |
| product_price | DECIMAL(10,3) | 是 |  | 商品单价 | 270.000 |
| tenant_id | VARCHAR(255) | 是 |  | 租户id | tll |
| discount_unit_price | DECIMAL(10,3) | 是 |  | 商品折后单价 | 575.000 |
| is_combination_children_product | INT | 是 |  | 是否是组合子商品(1-是,2-否) | 2 |
| pt | VARCHAR(255) | 是 |  | 天分区 | 20250817 |
