# ads_fin_fee_bx_detail_di

## 表描述
OLAP

## 数据量
- 总记录数：44,195 条

## 字段信息

| 字段名称 | 数据类型 | 是否可空 | 默认值 | 字段描述 | 示例 |
|---------|----------|----------|--------|----------|------|
| business_date | BIGINT | 是 |  | 业务日期 | 20240911 |
| biz_no | VARCHAR(255) | 是 |  | 业务单号 | CL2000202409050216 |
| receipt_no | VARCHAR(255) | 是 |  | 单据号 | CL2000240911001630 |
| initiator | VARCHAR(128) | 是 |  | 制单人 | 付聪辉 |
| account_in_company | VARCHAR(128) | 是 |  | 入账公司 | 安徽汇旺餐饮管理有限公司 |
| apply_dept | VARCHAR(64) | 是 |  | 申请部门 | 销售业务部 |
| notes | VARCHAR(500) | 是 |  | 备注 |  |
| center_name | VARCHAR(128) | 是 |  | 中心名称 | 总经办 |
| submitter | VARCHAR(50) | 是 |  | 实际报销人 | 刘昊彬 |
| fee_type | VARCHAR(128) | 是 |  | 费用类型 | 办公费-其他办公费 |
| occur_time | VARCHAR(128) | 是 |  | 发生时间 | 2024-08-16 13:30:00 |
| inclusive_tax_amt | DECIMAL(20,2) | 是 |  | 含税金额 | 949.00 |
| settlement_amt | DECIMAL(20,2) | 是 |  | 结算金额 | 300.00 |
| pay_status | VARCHAR(50) | 是 |  | 支付状态 | 已支付 |
| complete_time | VARCHAR(128) | 是 |  | 支付完成时间 | 2024-09-13 10:47:09 |
| payment_reason | VARCHAR(256) | 是 |  | 付款事由 | 8月1日-8月31日差旅费 |
| pt | VARCHAR(8) | 是 |  | 天分区 | 20240903 |

## 使用说明

### 常用查询示例

```sql
-- 查询最新数据
SELECT * FROM ads_fin_fee_bx_detail_di 
ORDER BY business_date DESC 
LIMIT 10;

-- 查询数据总量
SELECT COUNT(*) FROM ads_fin_fee_bx_detail_di;

-- 查询某日数据
SELECT * FROM ads_fin_fee_bx_detail_di 
WHERE business_date = 20240101;
```

### 注意事项
- 时间字段通常为bigint类型，格式为YYYYMMDD
- 金额字段单位为分，需要除以100转换为元
- 字符类型字段需要注意大小写敏感问题
