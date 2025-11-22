# flink_rps_all_new_tll_order_now_day_df

## 字段信息

| 字段名称 | 数据类型 | 是否可空 | 默认值 | 字段描述 | 示例 |
|---------|----------|----------|--------|----------|------|
| id | BIGINT | 是 |  | 订单号 | 607748694435446800 |
| order_status | INT | 是 |  | 订单状态 1.待支付 2.已取消（支付超时） 3.待确认 5.已取消（驳回） 6.待确认（部分取消） 7.备货中 8.配送中 9.已完成（确认收货） 10:待递交 11:待推送 13.备货中（部分取消） | 9 |
| order_num | VARCHAR(255) | 是 |  | 订单编号 | DH250805111168 |
| order_type | INT | 是 |  |  1-普通 2-待客下单 | 2 |
| order_notes | VARCHAR(1024) | 是 |  | 订单备注 | 首批大机器全套机器利旧已申请不配，现需报货一套收银机软件系统 |
| order_time | VARCHAR(255) | 是 |  | 下单时间 | 2025-08-05 11:43:23 |
| payment_method | VARCHAR(255) | 是 |  | 支付方式 1.银行卡余额 2.平台余额 3.组合支付 | 1 |
| payable_amount | DECIMAL(10,2) | 是 |  | 应付金额 | 51300.00 |
| discount_amount | DECIMAL(10,2) | 是 |  | 优惠金额 | 0.00 |
| actual_amount | DECIMAL(10,2) | 是 |  | 订单总金额 | 20830.00 |
| cancel_time | VARCHAR(255) | 是 |  | 取消时间 | 2025-08-05 09:11:18 |
| review_time | VARCHAR(255) | 是 |  | 审核时间 | 2025-08-06 09:42:02 |
| store_id | BIGINT | 是 |  | 门店ID | 10290 |
| delivery_method | INT | 是 |  | 配送方式,1:物流，2：快递。3上门自提 | 1 |
| manager_id | BIGINT | 是 |  | 客户经理ID | 0 |
| reviewer_name | VARCHAR(255) | 是 |  | 审核人姓名 | 孙志 |
| reviewer_id | BIGINT | 是 |  | 审核人ID | 860516862209825658 |
| created_time | VARCHAR(255) | 是 |  | 创建时间 | 2025-08-05 17:11:33 |
| created_by | VARCHAR(255) | 是 |  | 创建人 | zhangyingchun |
| updated_time | VARCHAR(255) | 是 |  | 更新时间 | 2025-08-06 02:32:25 |
| updated_by | VARCHAR(255) | 是 |  | 更新人 | 860517233812577470 |
| franchisee_rate | DECIMAL(10,2) | 是 |  | 加盟商费率折扣金额 | 0.00 |
| recipient_name | VARCHAR(255) | 是 |  | 收货人 | 牛鲁宁 |
| contact_number | VARCHAR(255) | 是 |  | 联系方式 | 16521738888 |
| delivery_address | VARCHAR(1024) | 是 |  | 收货地址 | 辽宁省朝阳市凌源市沟门子镇百兴路121号 |
| tenant_id | VARCHAR(255) | 是 |  | 租户Id | 854339203348044495 |
| order_used_type | VARCHAR(255) | 是 |  | 订单用途类型 废弃 | 1 |
| free_shipping | INT | 是 |  | 1-包邮 2-不包邮 | 2 |
| cancel_reason | VARCHAR(1024) | 是 |  | 取消理由 | 超时未支付 |
| region_manager | VARCHAR(255) | 是 |  | 大区经理 | 严鹤 |
| province_manager | VARCHAR(255) | 是 |  | 省区经理 | 赵鹏 |
| area_manager | VARCHAR(255) | 是 |  | 区域经理 | 陈光太 |
| need_destruction | INT | 是 |  | 是否需要销毁物品  1 是需要  0 不需要 | 0 |
| store_code | VARCHAR(255) | 是 |  | 门店code | TLL10568 |
| store_name | VARCHAR(1024) | 是 |  | 门店名称 | 嘉善县罗星街道世纪大道570号向善商业中心店 |
| user_confirm_time | VARCHAR(255) | 是 |  | 用户确认收货时间 | 2025-08-11 15:31:00 |
| delivery_time | VARCHAR(255) | 是 |  | 发货时间 |  |
| store_address | VARCHAR(1024) | 是 |  | 门店地址 |  |
| has_apply_after_sale | INT | 是 |  | 0：没申请过 1：申请过 | 0 |
| has_cancel | INT | 是 |  | 订单是否已经取消过 | 0 |
| pay_time | VARCHAR(255) | 是 |  | 支付时间 | 2025-08-05 11:28:02 |
| order_product_type | INT | 是 |  | 订单类型 1-纯水果订单 2-纯速冻订单 3混合型订单 | 3 |
| refund_amount | DECIMAL(10,2) | 是 |  | 退款金额 | 0.00 |
| shipping_method | INT | 是 |  | 送货方式0起订，1包邮，2送货上门 | 2 |
| is_push_sap | INT | 是 |  | 是否推SAP  0：否  1：是 | 1 |
| order_source | VARCHAR(255) | 是 |  | 订单来源  如：1.甜掌柜 |  |
| sales_organization | VARCHAR(255) | 是 |  | 销售组织  默认 1000-汇旺 | 1000-汇旺 |
| salesman | VARCHAR(255) | 是 |  | 销售员   如：张三 |  |
| currency | VARCHAR(255) | 是 |  | 结算币种  默认CNY | CNY |
| order_category | INT | 是 |  | 订单类别  如 1：B2B  2：B2C | 1 |
| business_type | INT | 是 |  | 业务类型： 如1：首批大机器 |  |
| expected_time | VARCHAR(255) | 是 |  | 期望送达时间 |  |
| third_order_no | BIGINT | 是 |  | 第三方单号 |  |
| delivery_fee | DECIMAL(10,2) | 是 |  | 配送费
 |  |
| packing_fee | DECIMAL(10,2) | 是 |  | 打包费 |  |
| pullstate | VARCHAR(255) | 是 |  | 新老区分 | 3 |
