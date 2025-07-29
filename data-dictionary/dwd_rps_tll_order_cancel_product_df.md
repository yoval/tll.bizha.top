# dwd_rps_tll_order_cancel_product_df

---

- 订单取消商品明细


| 字段                            | 类型          | 说明                       | 示例                 |
| ------------------------------- | ------------- | -------------------------- | -------------------- |
| id                              | BIGINT        |                            | 484254501395120128   |
| serial_no                       | VARCHAR(255)  | 流水号，继承商品订单明细   | 128083               |
| product_code                    | VARCHAR(255)  | 商品编码                   | 020000019            |
| product_name                    | VARCHAR(255)  | 商品名称                   | 原味晶球-1kg*12包/箱 |
| product_specification           | VARCHAR(255)  | 商品规格                   | 1kg*12包/箱          |
| product_unit                    | VARCHAR(255)  | 单位                       | 件                   |
| is_gift                         | INT           | 是否是赠品                 |                      |
| cancel_quantity                 | INT           | 取消数量                   | 1                    |
| refund_unit_price               | DECIMAL(10,3) | 退款单价（折后含税单价）   | 81                   |
| subtotal                        | DECIMAL(10,3) | 小计                       | 81                   |
| discount_amount                 | DECIMAL(10,3) | 优惠金额                   | 9                    |
| actual_refund_amount            | DECIMAL(10,3) | 银行卡实退金额             | 81                   |
| pt_discount_amount              | DECIMAL(10,3) | 平台优惠退还金额           | 0                    |
| agent_amount                    | DECIMAL(10,3) | 代理商代收代付款           | 0                    |
| business_discount               | DECIMAL(10,3) | 招商优惠                   |                      |
| customer_discount               | DECIMAL(10,3) | 客户往来款                 | 0                    |
| house_subsidy                   | DECIMAL(10,3) | 房租优惠                   | 0                    |
| cancel_order_id                 | BIGINT        | 退款单ID                   | 484254501378342912   |
| create_time                     | VARCHAR(255)  | 创建时间                   | 2024-08-29 14:54:30  |
| update_time                     | VARCHAR(255)  | 更新时间                   | 2024-08-29 14:55:21  |
| create_by                       | VARCHAR(255)  | 创建者                     |                      |
| update_by                       | VARCHAR(255)  | 修改者                     |                      |
| order_id                        | BIGINT        | 订单ID                     | 484254412316360704   |
| product_id                      | BIGINT        | 商品ID                     | 483962582441529344   |
| product_price                   | DECIMAL(10,3) | 商品单价                   | 90                   |
| tenant_id                       | VARCHAR(255)  | 租户ID                     | tll                  |
| discount_unit_price             | DECIMAL(10,3) | 商品折后单价               | 81                   |
| is_combination_children_product | INT           | 是否是组合子商品（1是2否） | 2                    |
| pt                              | VARCHAR(255)  |                            | 20250725             |