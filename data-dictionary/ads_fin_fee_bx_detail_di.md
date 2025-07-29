# `ads_fin_fee_bx_detail_di`


---

- 费用报销明细表


| 字段               | 类型          | 说明         | 示例                     |
| ------------------ | ------------- | ------------ | ------------------------ |
| business_date      | BIGINT        |              | 20240914                 |
| biz_no             | VARCHAR(255)  | 业务单号     | BX1000202409110079       |
| receipt_no         | VARCHAR(255)  | 单据号       | BX1000240914d00596       |
| initiator          | VARCHAR(128)  | 制单人       | 金烨                     |
| account_in_company | VARCHAR(128)  | 入账公司     | 安徽汇旺餐饮管理有限公司 |
| apply_dept         | VARCHAR(64)   | 申请部门     | 销售业务部               |
| notes              | VARCHAR(500)  | 备注         |                          |
| center_name        | VARCHAR(128)  | 中心名称     | 供应链中心               |
| submitter          | VARCHAR(50)   | 实际报销人   | 金烨                     |
| fee_type           | VARCHAR(128)  | 费用类型     | 办公费-其他办公费        |
| occur_time         | VARCHAR(128)  | 发生时间     | 2024-09-11 15:48:00      |
| inclusive_tax_amt  | DECIMAL(20,2) | 含税金额     | 300                      |
| settlement_amt     | DECIMAL(20,2) | 结算金额     | 300                      |
| pay_status         | VARCHAR(50)   | 支付状态     | 已支付                   |
| complete_time      | VARCHAR(128)  | 支付完成时间 | 2024-09-18 15:03:02      |
| payment_reason     | VARCHAR(256)  | 付款事由     | 品控部实验室使用物品     |
| pt                 | VARCHAR(8)    |              | 20240914                 |