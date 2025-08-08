# dwd_spc_report_sales_di

## 表描述
OLAP

## 数据量
- 总记录数：190,712 条

## 字段信息

| 字段名称 | 数据类型 | 是否可空 | 默认值 | 字段描述 |
|---------|----------|----------|--------|----------|
| csaleid | VARCHAR(255) | 是 |  | 销售主表ID |
| pk_corp | VARCHAR(255) | 是 |  | 公司ID |
| vreceiptcode | VARCHAR(255) | 是 |  | 单据号 |
| creceipttype | VARCHAR(255) | 是 |  | 单据类型 |
| cbiztype | VARCHAR(255) | 是 |  | 业务类型 |
| order_no | VARCHAR(255) | 是 |  | 订单编号 |
| bill_date | VARCHAR(255) | 是 |  | 单据日期 |
| bill_time | VARCHAR(255) | 是 |  | 单据时间 |
| sale_cust_id | VARCHAR(255) | 是 |  | 客户ID |
| cust_code | VARCHAR(255) | 是 |  | 客商编码 |
| region_Manager_name | VARCHAR(255) | 是 |  | 大区经理名称 |
| prov_Manager_name | VARCHAR(255) | 是 |  | 省经理名称 |
| district_Manager_name | VARCHAR(255) | 是 |  | 区域经理名称 |
| report_amount | DECIMAL(20,2) | 是 |  | 订货金额合计 |
| status | INT | 是 |  | 状态 |
| bretinv_flag | VARCHAR(255) | 是 |  | 退货标记 |
| load_time | VARCHAR(255) | 是 |  | 数据生成时间 |
| report_type | VARCHAR(255) | 是 |  | 来源类型：1.正常 2.代客下单（首批报货） 3.代客下单（首批大机器） 4.代客下单（翻新） 5.代客下单（其他） |
| cwarehouseid | VARCHAR(255) | 是 |  | 仓库主键id |
| audit_time | VARCHAR(255) | 是 |  | 审批时间 |
| receive_address | VARCHAR(500) | 是 |  | 收货地址 |
| pt | VARCHAR(255) | 是 |  | 天分区 |
| operator_name | VARCHAR(400) | 是 |  |  |
| remark | VARCHAR(2147483643) | 是 |  | 备注 |

## 使用说明

### 常用查询示例

```sql
-- 查询最新数据
SELECT * FROM dwd_spc_report_sales_di 
ORDER BY business_date DESC 
LIMIT 10;

-- 查询数据总量
SELECT COUNT(*) FROM dwd_spc_report_sales_di;

-- 查询某日数据
SELECT * FROM dwd_spc_report_sales_di 
WHERE business_date = 20240101;
```

### 注意事项
- 时间字段通常为bigint类型，格式为YYYYMMDD
- 金额字段单位为分，需要除以100转换为元
- 字符类型字段需要注意大小写敏感问题
