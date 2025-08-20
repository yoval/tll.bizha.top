# flink_rps_tll_presale_order_details_df

## 表描述
OLAP

## 数据量
- 总记录数：229,659 条

## 字段信息

| 字段名称 | 数据类型 | 是否可空 | 默认值 | 字段描述 | 示例 |
|---------|----------|----------|--------|----------|------|
| id | BIGINT | 是 |  |  | 1844196593610182657 |
| presale_order_num | VARCHAR(255) | 是 |  |  | YS101054796024 |
| product_info | VARCHAR(255) | 是 |  |  | 糯米麻薯粉(风味固体饮料) |
| product_specification | VARCHAR(255) | 是 |  |  | 500g*12包/箱 |
| product_id | BIGINT | 是 |  |  | 495404036200206336 |
| sku_code | VARCHAR(255) | 是 |  |  | 101000001 |
| unit_price | DECIMAL(10,2) | 是 |  |  | 318.00 |
| quantity | INT | 是 |  |  | 2 |
| product_type | VARCHAR(255) | 是 |  |  | 1 |
| tenant_id | BIGINT | 是 |  |  | -1 |
| belong_org_id | BIGINT | 是 |  |  |  |
| tenant_org_id | BIGINT | 是 |  |  |  |
| remark | VARCHAR(255) | 是 |  |  |  |
| create_user_id | BIGINT | 是 |  |  |  |
| creator | VARCHAR(255) | 是 |  |  | system |
| create_time | VARCHAR(255) | 是 |  |  | 2024-10-10 10:00:57 |
| modify_user_id | BIGINT | 是 |  |  |  |
| updater | VARCHAR(255) | 是 |  |  |  |
| modify_time | VARCHAR(255) | 是 |  |  |  |
| delete_flag | INT | 是 |  |  | 0 |
| audit_data_version | INT | 是 |  |  |  |
| sec_bu_id | BIGINT | 是 |  |  |  |
| sec_user_id | BIGINT | 是 |  |  |  |
| sec_ou_id | BIGINT | 是 |  |  |  |

## 使用说明

### 常用查询示例

```sql
-- 查询最新数据
SELECT * FROM flink_rps_tll_presale_order_details_df 
ORDER BY business_date DESC 
LIMIT 10;

-- 查询数据总量
SELECT COUNT(*) FROM flink_rps_tll_presale_order_details_df;

-- 查询某日数据
SELECT * FROM flink_rps_tll_presale_order_details_df 
WHERE business_date = 20240101;
```

### 注意事项
- 时间字段通常为bigint类型，格式为YYYYMMDD
- 金额字段单位为分，需要除以100转换为元
- 字符类型字段需要注意大小写敏感问题
