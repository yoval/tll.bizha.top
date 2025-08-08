# dim_oas_formmain_0145_all_df

## 表描述
OLAP

## 数据量
- 总记录数：4,115,156 条

## 字段信息

| 字段名称 | 数据类型 | 是否可空 | 默认值 | 字段描述 |
|---------|----------|----------|--------|----------|
| shop_oneid | VARCHAR(255) | 是 |  | 门店唯一编码 |
| shop_id | VARCHAR(255) | 是 |  | 门店id |
| shop_name | VARCHAR(255) | 是 |  | 门店名称 |
| oa_shop_code | VARCHAR(255) | 是 |  | OA门店编号 |
| oa_shop_name | VARCHAR(255) | 是 |  | OA门店名称 |
| shop_type | VARCHAR(255) | 是 |  | 门店类型 |
| shop_status | VARCHAR(255) | 是 |  | 门店状态 |
| busi_status | VARCHAR(255) | 是 |  | 运营状态 |
| open_date | VARCHAR(255) | 是 |  | 开业日期 |
| shop_open_time | VARCHAR(255) | 是 |  | 营业时间 |
| region_name | VARCHAR(255) | 是 |  | 所属大区 |
| region_manager_name | VARCHAR(255) | 是 |  | 大区经理名称 |
| prov_manager_name | VARCHAR(255) | 是 |  | 省经理名称 |
| district_manager_name | VARCHAR(255) | 是 |  | 区域经理名称 |
| supervisor_name | VARCHAR(255) | 是 |  | 督导 |
| shop_addr | VARCHAR(255) | 是 |  | 门店地址 |
| prov_name | VARCHAR(255) | 是 |  | 所属省份 |
| prov_id | VARCHAR(255) | 是 |  | 所属省份id |
| city_name | VARCHAR(255) | 是 |  | 所属城市 |
| city_id | VARCHAR(255) | 是 |  | 所属城市id |
| district_name | VARCHAR(255) | 是 |  | 所属区县 |
| district_id | VARCHAR(255) | 是 |  | 所属区县id |
| area_division | VARCHAR(255) | 是 |  | 所属行政区划 |
| busi_area_type | VARCHAR(255) | 是 |  | 商圈类型 |
| busi_area_level | VARCHAR(255) | 是 |  | 商圈等级 |
| send_whse | VARCHAR(255) | 是 |  | 发货仓库 |
| cont_status | VARCHAR(255) | 是 |  | 合同状态(初签、过户、迁址等) |
| shop_area | VARCHAR(255) | 是 |  | 经营面积 |
| license_name | VARCHAR(255) | 是 |  | 营业执照名称 |
| license_person | VARCHAR(255) | 是 |  | 营业执照法人 |
| license_phone | VARCHAR(255) | 是 |  | 法人号码 |
| license_addr | VARCHAR(255) | 是 |  | 营业执照地址 |
| u8c_cus_id | VARCHAR(255) | 是 |  | U8C客商编码 |
| regist_date | VARCHAR(255) | 是 |  | 登记日期 |
| close_shop_date | VARCHAR(255) | 是 |  | 闭店日期 |
| contract_sign_date | VARCHAR(255) | 是 |  | 签约日期 |
| contract_id | VARCHAR(255) | 是 |  | 合同编号 |
| contract_start_date | VARCHAR(255) | 是 |  | 合同开始日期 |
| contract_end_date | VARCHAR(255) | 是 |  | 合同结束日期 |
| load_time | VARCHAR(255) | 是 |  | 中台数据加工时间 |
| pt | VARCHAR(255) | 是 |  | 天分区 |
| shop_level | VARCHAR(5) | 是 |  | 门店等级 |
| rps_discount | VARCHAR(255) | 是 |  | 报货等级 |

## 使用说明

### 常用查询示例

```sql
-- 查询最新数据
SELECT * FROM dim_oas_formmain_0145_all_df 
ORDER BY business_date DESC 
LIMIT 10;

-- 查询数据总量
SELECT COUNT(*) FROM dim_oas_formmain_0145_all_df;

-- 查询某日数据
SELECT * FROM dim_oas_formmain_0145_all_df 
WHERE business_date = 20240101;
```

### 注意事项
- 时间字段通常为bigint类型，格式为YYYYMMDD
- 金额字段单位为分，需要除以100转换为元
- 字符类型字段需要注意大小写敏感问题
