# dwd_rps_tll_order_di

## 表描述
订单表

## 字段信息

| 字段名称 | 数据类型 | 是否可空 | 默认值 | 字段描述 |
|---------|----------|----------|--------|----------|
| id | VARCHAR(255) | 是 |  | 订单号 |
| order_status | INT | 是 |  | 订单状态 1.待支付 2.已取消（支付超时） 3.待确认 5.已取消（驳回） 6.待确认（部分取消） 7.备货中 8.配送中 9.已完成（确认收货） 10:待递交 11:待推送 13.备货中（部分取消） |
| order_num | VARCHAR(255) | 是 |  | 订单编号 |
| order_type | INT | 是 |  |  1-普通 2-待客下单 |
| order_notes | VARCHAR(1024) | 是 |  | 订单备注 |
| order_time | VARCHAR(255) | 是 |  | 下单时间 |
| payment_method | VARCHAR(255) | 是 |  | 支付方式 1.银行卡余额 2.平台余额 3.组合支付 |
| payable_amount | DECIMAL(10,2) | 是 |  | 应付金额 |
| discount_amount | DECIMAL(10,2) | 是 |  | 优惠金额 |
| actual_amount | DECIMAL(10,2) | 是 |  | 订单总金额 |
| cancel_time | VARCHAR(255) | 是 |  | 取消时间 |
| review_time | VARCHAR(255) | 是 |  | 审核时间 |
| store_id | BIGINT | 是 |  | 门店ID |
| delivery_method | INT | 是 |  | 配送方式,1:物流，2：快递。3上门自提 |
| manager_id | BIGINT | 是 |  | 客户经理ID |
| reviewer_name | VARCHAR(255) | 是 |  | 审核人姓名 |
| reviewer_id | BIGINT | 是 |  | 审核人ID |
| created_time | VARCHAR(255) | 是 |  | 创建时间 |
| created_by | VARCHAR(255) | 是 |  | 创建人 |
| updated_time | VARCHAR(255) | 是 |  | 更新时间 |
| updated_by | VARCHAR(255) | 是 |  | 更新人 |
| franchisee_rate | DECIMAL(10,2) | 是 |  | 加盟商费率折扣金额 |
| recipient_name | VARCHAR(255) | 是 |  | 收货人 |
| contact_number | VARCHAR(255) | 是 |  | 联系方式 |
| delivery_address | VARCHAR(1024) | 是 |  | 收货地址 |
| tenant_id | VARCHAR(255) | 是 |  | 租户Id |
| order_used_type | VARCHAR(255) | 是 |  | 订单用途类型 废弃 |
| free_shipping | INT | 是 |  | 1-包邮 2-不包邮 |
| cancel_reason | VARCHAR(1024) | 是 |  | 取消理由 |
| region_manager | VARCHAR(255) | 是 |  | 大区经理 |
| province_manager | VARCHAR(255) | 是 |  | 省区经理 |
| area_manager | VARCHAR(255) | 是 |  | 区域经理 |
| agent_code | INT | 是 |  | 代理商code |
| ratio | DECIMAL(10,2) | 是 |  | 代理系数 |
| tll_user_id | VARCHAR(255) | 是 |  | 用户id |
| need_destruction | INT | 是 |  | 是否需要销毁物品  1 是需要  0 不需要 |
| store_code | VARCHAR(255) | 是 |  | 门店code |
| store_name | VARCHAR(1024) | 是 |  | 门店名称 |
| user_confirm_time | VARCHAR(255) | 是 |  | 用户确认收货时间 |
| delivery_time | VARCHAR(255) | 是 |  | 发货时间 |
| store_address | VARCHAR(1024) | 是 |  | 门店地址 |
| has_apply_after_sale | INT | 是 |  | 0：没申请过 1：申请过 |
| has_cancel | INT | 是 |  | 订单是否已经取消过 |
| pay_time | VARCHAR(255) | 是 |  | 支付时间 |
| order_product_type | INT | 是 |  | 订单类型 1-纯水果订单 2-纯速冻订单 3混合型订单 |
| refund_amount | DECIMAL(10,2) | 是 |  | 退款金额 |
| shipping_method | INT | 是 |  | 送货方式0起订，1包邮，2送货上门 |
| is_push_sap | INT | 是 |  | 是否推SAP  0：否  1：是 |
| order_source | VARCHAR(255) | 是 |  | 订单来源  如：1.甜掌柜 |
| sales_organization | VARCHAR(255) | 是 |  | 销售组织  默认 1000-汇旺 |
| salesman | VARCHAR(255) | 是 |  | 销售员   如：张三 |
| currency | VARCHAR(255) | 是 |  | 结算币种  默认CNY |
| order_category | INT | 是 |  | 订单类别  如 1：B2B  2：B2C |
| business_type | INT | 是 |  | 业务类型： 如1：首批大机器 |
| expected_time | VARCHAR(255) | 是 |  | 期望送达时间 |
| third_order_no | BIGINT | 是 |  | 第三方单号 |
| delivery_fee | DECIMAL(10,2) | 是 |  | 配送费 |
| packing_fee | DECIMAL(10,2) | 是 |  | 打包费 |
| cancel_type | VARCHAR(255) | 是 |  | 取消类型 |
| agent_name | VARCHAR(255) | 是 |  | 代理商名称 |
| pt | VARCHAR(255) | 是 |  | 天分区 |

## 使用说明

### 常用查询示例

```sql
-- 查询最新数据
SELECT * FROM dwd_rps_tll_order_di 
ORDER BY business_date DESC 
LIMIT 10;

-- 查询数据总量
SELECT COUNT(*) FROM dwd_rps_tll_order_di;

-- 查询某日数据
SELECT * FROM dwd_rps_tll_order_di 
WHERE business_date = 20240101;
```

