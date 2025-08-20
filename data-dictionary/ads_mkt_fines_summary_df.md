# ads_mkt_fines_summary_df

## 表描述
OLAP

## 数据量
- 总记录数：4,405 条

## 字段信息

| 字段名称 | 数据类型 | 是否可空 | 默认值 | 字段描述 | 示例 |
|---------|----------|----------|--------|----------|------|
| ticket_number | VARCHAR(255) | 是 |  | 罚款单编号 | FKD-202108170001 |
| shop_id | VARCHAR(255) | 是 |  | 门店编号 | TLL01954 |
| billing_person | VARCHAR(255) | 是 |  | 开单人 | 陈冬冬 |
| department_lv6 | VARCHAR(255) | 是 |  | 开单人所在部门 |  |
| org_name_lv3 | VARCHAR(255) | 是 |  | 大部门 |  |
| license_phone | VARCHAR(255) | 是 |  | 店铺法人 | 18603420270 |
| license_person | VARCHAR(255) | 是 |  | 法人电话 | 刘洋 |
| penalty_amount | VARCHAR(255) | 是 |  | 罚款金额 | 2500 |
| violations | VARCHAR(255) | 是 |  | 违规事项 | 过期原物料、产品质量问题 |
| type_fine | VARCHAR(255) | 是 |  | 罚款类型 | 原物料 |
| province | VARCHAR(255) | 是 |  | 省 | 山东省 |
| city | VARCHAR(255) | 是 |  | 市 | 濮阳市 |
| district | VARCHAR(255) | 是 |  | 区 | 东平县 |
| busi_status | VARCHAR(255) | 是 |  | 运营状态 | 签约 |
| storeaddr | VARCHAR(255) | 是 |  | 纤细地址 | 江苏苏州市吴中区东吴北路98号 |
| penalty_date | VARCHAR(255) | 是 |  | 罚款日期 | 20210816 |
| penalty_pay_status | VARCHAR(255) | 是 |  | 是否缴纳罚款 | 否 |
| region_manager_name | VARCHAR(255) | 是 |  | 大区经理 | 刘向阳 |

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

### 注意事项
- 时间字段通常为bigint类型，格式为YYYYMMDD
- 金额字段单位为分，需要除以100转换为元
- 字符类型字段需要注意大小写敏感问题
