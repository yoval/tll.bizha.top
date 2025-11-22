# dwd_rps_tll_order_details_di

## 字段信息

| 字段名称 | 数据类型 | 是否可空 | 默认值 | 字段描述 | 示例 |
|---------|----------|----------|--------|----------|------|
| pt | VARCHAR(255) | 是 |  | 天分区 | 20240915 |
| id | VARCHAR(255) | 是 |  | 明细ID | 172416 |
| order_id | VARCHAR(255) | 是 |  | 订单号 | 492720459084218368 |
| product_info | VARCHAR(255) | 是 |  | 商品信息 | 收银机软件系统-美团 |
| product_specification | VARCHAR(255) | 是 |  | 商品规格 | 15.6寸(美团) |
| product_id | VARCHAR(255) | 是 |  | 商品ID | 483962583154561024 |
| sku_code | VARCHAR(255) | 是 |  | SKU代码 | 100001551 |
| supplier | VARCHAR(255) | 是 |  | 供应商 | 未知 |
| unit_price | DECIMAL(10,2) | 是 |  | 单价 | 2276.00 |
| quantity | INT | 是 |  | 购买数量 | 2 |
| cancel_quantity | INT | 是 |  | 取消数量 | 0 |
| payable_amount | DECIMAL(10,2) | 是 |  | 应付金额 | 2276.00 |
| discount_amount | DECIMAL(10,2) | 是 |  | 优惠金额 | 0.00 |
| actual_amount | DECIMAL(10,2) | 是 |  | 实付金额 | 2276.00 |
| status | INT | 是 |  | 状态 | 1 |
| tenant_id | VARCHAR(255) | 是 |  | 租户ID | tll |
| create_time | VARCHAR(255) | 是 |  | 创建时间 | 2024-09-15 23:54:48 |
| product_type | VARCHAR(255) | 是 |  | 商品类型 | PT |
| warehouse_id | INT | 是 |  | 发货仓库 | 234123 |
| warehouse_batch_no | VARCHAR(255) | 是 |  | 仓库批次号 |  |
| discount_unit_price | DECIMAL(10,2) | 是 |  | 折后单价 | 158.00 |
| category_id | BIGINT | 是 |  | 类目id | 857214796288825395 |
| tax_rate | DECIMAL(10,2) | 是 |  | 税率 | 0.13 |
| is_freebies | INT | 是 |  | 是否为赠品：0：否  1：是 |  |
| packaging_unit | VARCHAR(255) | 是 |  | 包装单位 | 套 |
| unit_code | VARCHAR(255) | 是 |  | 单位编码 | JAN |
| serial_no | VARCHAR(255) | 是 |  | 流水号 | 999998 |
| out_quantity | INT | 是 |  | 出库数量 | 1 |
| customer_discount_amount | DECIMAL(10,2) | 是 |  | 客户优惠 | 0.00 |
| rent_subsidy_amount | DECIMAL(10,2) | 是 |  | 房租优惠 | 0.00 |
| agent_amount | DECIMAL(10,2) | 是 |  | 代理商代收代付款 | 0.00 |
| bank_actual_amount | DECIMAL(10,2) | 是 |  | 银行实付金额 | 263.26 |
| pt_discount_amount | DECIMAL(10,2) | 是 |  | 平台优惠金额 | 0.00 |
| is_combination_children_product | INT | 是 |  | 是否是组合子商品(1-是,2-否) | 2 |
| final_pay_amount | DECIMAL(10,2) | 是 |  | 最终支付金额，包含银行和平台付款，折后单价乘以出库数量 | 2276.00 |
| cancel_order_num | VARCHAR(2147483643) | 是 |  | 退款单号 | TK090641534147 |
| created_at | VARCHAR(2147483643) | 是 |  | 退款时间 | 2024-08-28 23:37:42 |
| warehouse_name | VARCHAR(2147483643) | 是 |  | 仓库名称 | 汇旺蚌埠仓工厂通用库 |
| refund_fee | DECIMAL(10,2) | 是 |  | 退单金额 | 0.00 |
| modify_time | VARCHAR(255) | 是 |  | 更新时间 | 2024-09-26 10:26:15 |
| activity_id | VARCHAR(255) | 是 |  | 活动id |  |
| combination_code | VARCHAR(255) | 是 |  | 组合商品编码 |  |
| logistic_fee_amount | DECIMAL(10,2) | 是 |  |  | 0.00 |
| has_logistic_fee | INT | 是 |  |  | 0 |
| delivery_method | INT | 是 |  | 配送方式,1:物流,2:快递,3:上门自提 | 0 |
| shipping_method | INT | 是 |  | 送货方式,0:起订,1:包邮,2:送货上门 | 0 |
