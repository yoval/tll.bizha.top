# ads_fin_fee_bx_detail_di

## 表描述
OLAP

## 数据量
- 总记录数：42,526 条

## 字段信息

| 字段名称 | 数据类型 | 是否可空 | 默认值 | 字段描述 |
|---------|----------|----------|--------|----------|
| business_date | BIGINT | 是 |  | 业务日期 |
| biz_no | VARCHAR(255) | 是 |  | 业务单号 |
| receipt_no | VARCHAR(255) | 是 |  | 单据号 |
| initiator | VARCHAR(128) | 是 |  | 制单人 |
| account_in_company | VARCHAR(128) | 是 |  | 入账公司 |
| apply_dept | VARCHAR(64) | 是 |  | 申请部门 |
| notes | VARCHAR(500) | 是 |  | 备注 |
| center_name | VARCHAR(128) | 是 |  | 中心名称 |
| submitter | VARCHAR(50) | 是 |  | 实际报销人 |
| fee_type | VARCHAR(128) | 是 |  | 费用类型 |
| occur_time | VARCHAR(128) | 是 |  | 发生时间 |
| inclusive_tax_amt | DECIMAL(20,2) | 是 |  | 含税金额 |
| settlement_amt | DECIMAL(20,2) | 是 |  | 结算金额 |
| pay_status | VARCHAR(50) | 是 |  | 支付状态 |
| complete_time | VARCHAR(128) | 是 |  | 支付完成时间 |
| payment_reason | VARCHAR(256) | 是 |  | 付款事由 |
| pt | VARCHAR(8) | 是 |  | 天分区 |

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
