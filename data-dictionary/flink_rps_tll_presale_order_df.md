# flink_rps_tll_presale_order_df

## 表描述
OLAP

## 数据量
- 总记录数：43,167 条

## 字段信息

| 字段名称 | 数据类型 | 是否可空 | 默认值 | 字段描述 | 示例 |
|---------|----------|----------|--------|----------|------|
| id | BIGINT | 是 |  |  | 1844196781305966594 |
| activity_id | BIGINT | 是 |  |  | 1840337065095979010 |
| presale_order_num | VARCHAR(255) | 是 |  |  | YS101053915757 |
| order_time | VARCHAR(255) | 是 |  |  | 2024-10-10 10:01:31 |
| actual_amount | DECIMAL(10,2) | 是 |  |  | 1182.00 |
| store_id | BIGINT | 是 |  |  | 6095 |
| store_code | VARCHAR(255) | 是 |  |  | TLL02428 |
| store_name | VARCHAR(255) | 是 |  |  | 吉林松原市宁江区中山大街状元府B5102号商企 |
| store_level | VARCHAR(255) | 是 |  |  | D |
| warehouse_id | BIGINT | 是 |  |  | 711449 |
| warehouse_code | VARCHAR(255) | 是 |  |  | CKHWZZCGCTYK01 |
| warehouse_name | VARCHAR(255) | 是 |  |  | 汇旺蚌埠仓工厂通用库 |
| order_status | INT | 是 |  |  | 0 |
| tenant_id | BIGINT | 是 |  |  | -1 |
| belong_org_id | BIGINT | 是 |  |  |  |
| tenant_org_id | BIGINT | 是 |  |  |  |
| remark | VARCHAR(255) | 是 |  |  |  |
| create_user_id | BIGINT | 是 |  |  |  |
| creator | VARCHAR(255) | 是 |  |  |  |
| create_time | VARCHAR(255) | 是 |  |  | 2024-10-10 10:05:47 |
| modify_user_id | BIGINT | 是 |  |  |  |
| updater | VARCHAR(255) | 是 |  |  |  |
| modify_time | VARCHAR(255) | 是 |  |  | 2024-11-23 13:52:00 |
| delete_flag | INT | 是 |  |  | 0 |
| audit_data_version | INT | 是 |  |  |  |
| sec_bu_id | BIGINT | 是 |  |  |  |
| sec_user_id | BIGINT | 是 |  |  |  |
| sec_ou_id | BIGINT | 是 |  |  |  |

## 使用说明

### 常用查询示例

```sql
-- 查询最新数据
SELECT * FROM flink_rps_tll_presale_order_df 
ORDER BY business_date DESC 
LIMIT 10;

-- 查询数据总量
SELECT COUNT(*) FROM flink_rps_tll_presale_order_df;

-- 查询某日数据
SELECT * FROM flink_rps_tll_presale_order_df 
WHERE business_date = 20240101;
```

### 注意事项
- 时间字段通常为bigint类型，格式为YYYYMMDD
- 金额字段单位为分，需要除以100转换为元
- 字符类型字段需要注意大小写敏感问题
