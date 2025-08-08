# ads_mkt_fines_summary_df

## 表描述
罚款单汇总表

## 字段信息

| 字段名称 | 数据类型 | 是否可空 | 默认值 | 字段描述 |
|---------|----------|----------|--------|----------|
| ticket_number | VARCHAR(255) | 是 |  | 罚款单编号 |
| shop_id | VARCHAR(255) | 是 |  | 门店编号 |
| billing_person | VARCHAR(255) | 是 |  | 开单人 |
| department_lv6 | VARCHAR(255) | 是 |  | 开单人所在部门 |
| org_name_lv3 | VARCHAR(255) | 是 |  | 大部门 |
| license_phone | VARCHAR(255) | 是 |  | 店铺法人 |
| license_person | VARCHAR(255) | 是 |  | 法人电话 |
| penalty_amount | VARCHAR(255) | 是 |  | 罚款金额 |
| violations | VARCHAR(255) | 是 |  | 违规事项 |
| type_fine | VARCHAR(255) | 是 |  | 罚款类型 |
| province | VARCHAR(255) | 是 |  | 省 |
| city | VARCHAR(255) | 是 |  | 市 |
| district | VARCHAR(255) | 是 |  | 区 |
| busi_status | VARCHAR(255) | 是 |  | 运营状态 |
| storeaddr | VARCHAR(255) | 是 |  | 纤细地址 |
| penalty_date | VARCHAR(255) | 是 |  | 罚款日期 |
| penalty_pay_status | VARCHAR(255) | 是 |  | 是否缴纳罚款 |
| region_manager_name | VARCHAR(255) | 是 |  | 大区经理 |

## 使用说明

### 常用查询示例

```sql
-- 查询最新数据
SELECT * FROM ads_mkt_fines_summary_df 
ORDER BY business_date DESC 
LIMIT 10;

-- 查询数据总量
SELECT COUNT(*) FROM ads_mkt_fines_summary_df;

-- 查询某日数据
SELECT * FROM ads_mkt_fines_summary_df 
WHERE business_date = 20240101;
```

