# ads_fin_fee_bx_detail_di

## 表描述
OLAP

## 数据量
- 总记录数：44,195 条

## 字段信息

| 字段名称 | 数据类型 | 是否可空 | 默认值 | 字段描述 | 示例 |
|---------|----------|----------|--------|----------|------|
| business_date | BIGINT | 是 |  | 业务日期 | 20240907 |
| biz_no | VARCHAR(255) | 是 |  | 业务单号 | CL2040202409050191 |
| receipt_no | VARCHAR(255) | 是 |  | 单据号 | CL2000240911001630 |
| initiator | VARCHAR(128) | 是 |  | 制单人 | 徐涛 |
| account_in_company | VARCHAR(128) | 是 |  | 入账公司 | 安徽汇旺餐饮管理有限公司 |
| apply_dept | VARCHAR(64) | 是 |  | 申请部门 | 市场运营中心-北方战区-山河大区-山河五组 |
| notes | VARCHAR(500) | 是 |  | 备注 |  |
| center_name | VARCHAR(128) | 是 |  | 中心名称 | 信息科技中心 |
| submitter | VARCHAR(50) | 是 |  | 实际报销人 | 李小青 |
| fee_type | VARCHAR(128) | 是 |  | 费用类型 | 办公费-其他办公费 |
| occur_time | VARCHAR(128) | 是 |  | 发生时间 | 2024-08-16 13:30:00 |
| inclusive_tax_amt | DECIMAL(20,2) | 是 |  | 含税金额 | 289.50 |
| settlement_amt | DECIMAL(20,2) | 是 |  | 结算金额 | 317.00 |
| pay_status | VARCHAR(50) | 是 |  | 支付状态 | 已支付 |
| complete_time | VARCHAR(128) | 是 |  | 支付完成时间 | 2024-09-10 17:06:32 |
| payment_reason | VARCHAR(256) | 是 |  | 付款事由 | 酒水，麻将，水果，香烟，餐饮费用 |
| pt | VARCHAR(8) | 是 |  | 天分区 | 20240909 |

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
