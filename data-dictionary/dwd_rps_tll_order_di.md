# dwd_rps_tll_order_di

## 表描述
OLAP

## 数据量
- 总记录数：300,427 条

## 字段信息

| 字段名称 | 数据类型 | 是否可空 | 默认值 | 字段描述 | 示例 |
|---------|----------|----------|--------|----------|------|
| id | VARCHAR(255) | 是 |  | 订单号 | 1909773892702081025 |
| order_status | INT | 是 |  | 订单状态 1.待支付 2.已取消（支付超时） 3.待确认 5.已取消（驳回） 6.待确认（部分取消） 7.备货中 8.配送中 9.已完成（确认收货） 10:待递交 11:待推送 13.备货中（部分取消） | 9 |
| order_num | VARCHAR(255) | 是 |  | 订单编号 | DH040959714085 |
| order_type | INT | 是 |  |  1-普通 2-待客下单 | 1 |
| order_notes | VARCHAR(1024) | 是 |  | 订单备注 |  |
| order_time | VARCHAR(255) | 是 |  | 下单时间 | 2025-04-09 09:03:58 |
| payment_method | VARCHAR(255) | 是 |  | 支付方式 1.银行卡余额 2.平台余额 3.组合支付 | 3 |
| payable_amount | DECIMAL(10,2) | 是 |  | 应付金额 | 15.00 |
| discount_amount | DECIMAL(10,2) | 是 |  | 优惠金额 | 0.00 |
| actual_amount | DECIMAL(10,2) | 是 |  | 订单总金额 | 1802.00 |
| cancel_time | VARCHAR(255) | 是 |  | 取消时间 | 2025-04-09 13:52:40 |
| review_time | VARCHAR(255) | 是 |  | 审核时间 | 2025-04-09 09:22:18 |
| store_id | BIGINT | 是 |  | 门店ID | 6374 |
| delivery_method | INT | 是 |  | 配送方式,1:物流，2：快递。3上门自提 | 1 |
| manager_id | BIGINT | 是 |  | 客户经理ID | 0 |
| reviewer_name | VARCHAR(255) | 是 |  | 审核人姓名 | 宫丽婷 |
| reviewer_id | BIGINT | 是 |  | 审核人ID | 860514599395398081 |
| created_time | VARCHAR(255) | 是 |  | 创建时间 | 2025-04-09 09:03:58 |
| created_by | VARCHAR(255) | 是 |  | 创建人 | 闫立新 |
| updated_time | VARCHAR(255) | 是 |  | 更新时间 | 2025-04-10 09:05:22 |
| updated_by | VARCHAR(255) | 是 |  | 更新人 | 860522355472996436 |
| franchisee_rate | DECIMAL(10,2) | 是 |  | 加盟商费率折扣金额 | 0.00 |
| recipient_name | VARCHAR(255) | 是 |  | 收货人 | 郭成奇 |
| contact_number | VARCHAR(255) | 是 |  | 联系方式 | 15555897118 |
| delivery_address | VARCHAR(1024) | 是 |  | 收货地址 | 甘肃省兰州市皋兰县金城路160号 |
| tenant_id | VARCHAR(255) | 是 |  | 租户Id | tll |
| order_used_type | VARCHAR(255) | 是 |  | 订单用途类型 废弃 | 1 |
| free_shipping | INT | 是 |  | 1-包邮 2-不包邮 | 1 |
| cancel_reason | VARCHAR(1024) | 是 |  | 取消理由 | 不想要了 |
| region_manager | VARCHAR(255) | 是 |  | 大区经理 | 胡冰雪 |
| province_manager | VARCHAR(255) | 是 |  | 省区经理 | 韩善武 |
| area_manager | VARCHAR(255) | 是 |  | 区域经理 | 王宗杰 |
| agent_code | INT | 是 |  | 代理商code | 50000029 |
| ratio | DECIMAL(10,2) | 是 |  | 代理系数 | 0.05 |
| tll_user_id | VARCHAR(255) | 是 |  | 用户id | 2004096 |
| need_destruction | INT | 是 |  | 是否需要销毁物品  1 是需要  0 不需要 | 0 |
| store_code | VARCHAR(255) | 是 |  | 门店code | TLL03550 |
| store_name | VARCHAR(1024) | 是 |  | 门店名称 | 寿县安丰镇2店 |
| user_confirm_time | VARCHAR(255) | 是 |  | 用户确认收货时间 | 2025-04-20 00:09:19 |
| delivery_time | VARCHAR(255) | 是 |  | 发货时间 | 2024-08-01 17:08:42 |
| store_address | VARCHAR(1024) | 是 |  | 门店地址 |  |
| has_apply_after_sale | INT | 是 |  | 0：没申请过 1：申请过 | 0 |
| has_cancel | INT | 是 |  | 订单是否已经取消过 | 0 |
| pay_time | VARCHAR(255) | 是 |  | 支付时间 | 2025-04-09 09:01:08 |
| order_product_type | INT | 是 |  | 订单类型 1-纯水果订单 2-纯速冻订单 3混合型订单 | 2 |
| refund_amount | DECIMAL(10,2) | 是 |  | 退款金额 | 2591.00 |
| shipping_method | INT | 是 |  | 送货方式0起订，1包邮，2送货上门 | 0 |
| is_push_sap | INT | 是 |  | 是否推SAP  0：否  1：是 | 1 |
| order_source | VARCHAR(255) | 是 |  | 订单来源  如：1.甜掌柜 |  |
| sales_organization | VARCHAR(255) | 是 |  | 销售组织  默认 1000-汇旺 | 1000-汇旺 |
| salesman | VARCHAR(255) | 是 |  | 销售员   如：张三 |  |
| currency | VARCHAR(255) | 是 |  | 结算币种  默认CNY | CNY |
| order_category | INT | 是 |  | 订单类别  如 1：B2B  2：B2C | 1 |
| business_type | INT | 是 |  | 业务类型： 如1：首批大机器 | 1 |
| expected_time | VARCHAR(255) | 是 |  | 期望送达时间 |  |
| third_order_no | BIGINT | 是 |  | 第三方单号 |  |
| delivery_fee | DECIMAL(10,2) | 是 |  | 配送费 |  |
| packing_fee | DECIMAL(10,2) | 是 |  | 打包费 |  |
| cancel_type | VARCHAR(255) | 是 |  | 取消类型 |  |
| agent_name | VARCHAR(255) | 是 |  | 代理商名称 | 刘剑（衡水） |
| pt | VARCHAR(255) | 是 |  | 天分区 | 20250409 |

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

### 注意事项
- 时间字段通常为bigint类型，格式为YYYYMMDD
- 金额字段单位为分，需要除以100转换为元
- 字符类型字段需要注意大小写敏感问题
