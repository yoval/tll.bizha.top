# flink_rps_all_new_tll_order_details_now_day_df

## 表描述
OLAP

## 数据量
- 总记录数：181,421 条

## 字段信息

| 字段名称 | 数据类型 | 是否可空 | 默认值 | 字段描述 | 示例 |
|---------|----------|----------|--------|----------|------|
| id | VARCHAR(255) | 是 |  | 明细ID | 3373710 |
| order_id | VARCHAR(255) | 是 |  | 订单号 | 1952399786033315842 |
| product_info | VARCHAR(255) | 是 |  | 商品信息 | 调味糖浆-6kg*4瓶/箱 |
| product_specification | VARCHAR(255) | 是 |  | 商品规格 | 1kg*12瓶/箱 |
| product_id | VARCHAR(255) | 是 |  | 商品ID | 560646687530553344 |
| sku_code | VARCHAR(255) | 是 |  | SKU代码 | 040000026 |
| supplier | VARCHAR(255) | 是 |  | 供应商 | 未知 |
| unit_price | DECIMAL(10,2) | 是 |  | 单价 | 222.00 |
| quantity | INT | 是 |  | 购买数量 | 3 |
| cancel_quantity | INT | 是 |  | 取消数量 | 0 |
| payable_amount | DECIMAL(10,2) | 是 |  | 应付金额 | 345.00 |
| discount_amount | DECIMAL(10,2) | 是 |  | 优惠金额 | 0.00 |
| actual_amount | DECIMAL(10,2) | 是 |  | 实付金额 | 80.00 |
| status | INT | 是 |  | 状态 | 1 |
| tenant_id | VARCHAR(255) | 是 |  | 租户ID | tll |
| create_time | VARCHAR(255) | 是 |  | 创建时间 | 2025-08-05 00:02:26 |
| product_type | VARCHAR(255) | 是 |  | 商品类型 | PT |
| warehouse_id | INT | 是 |  | 发货仓库 | 969798 |
| warehouse_batch_no | VARCHAR(255) | 是 |  | 仓库批次号 |  |
| discount_unit_price | DECIMAL(10,2) | 是 |  | 折后单价 | 230.00 |
| category_id | INT | 是 |  | 类目id |  |
| tax_rate | DECIMAL(10,2) | 是 |  | 税率 | 0.13 |
| is_freebies | INT | 是 |  | 是否为赠品：0：否  1：是 |  |
| packaging_unit | VARCHAR(255) | 是 |  | 包装单位 | JAN |
| unit_code | VARCHAR(255) | 是 |  | 单位编码 | JAN |
| serial_no | VARCHAR(255) | 是 |  | 流水号 | 100003 |
| out_quantity | INT | 是 |  | 出库数量 | 1 |
| customer_discount_amount | DECIMAL(10,2) | 是 |  | 客户优惠 | 0.00 |
| rent_subsidy_amount | DECIMAL(10,2) | 是 |  | 房租优惠 | 0.00 |
| agent_amount | DECIMAL(10,2) | 是 |  | 代理商代收代付款 | 0.00 |
| bank_actual_amount | DECIMAL(10,2) | 是 |  | 银行实付金额 | 222.00 |
| pt_discount_amount | DECIMAL(10,2) | 是 |  | 平台优惠金额 | 0.00 |
| is_combination_children_product | INT | 是 |  | 是否是组合子商品(1-是,2-否) | 2 |
| final_pay_amount | DECIMAL(10,2) | 是 |  | 最终支付金额，包含银行和平台付款，折后单价乘以出库数量 | 280.00 |
| modify_time | VARCHAR(64) | 是 |  | 修改时间 | 2025-08-05 13:45:48 |
| activity_id | VARCHAR(32) | 是 |  | 预售活动id |  |
| combination_code | VARCHAR(64) | 是 |  | 组合商品编码 |  |
| pullstate | VARCHAR(255) | 是 |  | 新报货 | 3 |

## 使用说明

### 常用查询示例

```sql
-- 查询最新数据
SELECT * FROM flink_rps_all_new_tll_order_details_now_day_df 
ORDER BY business_date DESC 
LIMIT 10;

-- 查询数据总量
SELECT COUNT(*) FROM flink_rps_all_new_tll_order_details_now_day_df;

-- 查询某日数据
SELECT * FROM flink_rps_all_new_tll_order_details_now_day_df 
WHERE business_date = 20240101;
```

### 注意事项
- 时间字段通常为bigint类型，格式为YYYYMMDD
- 金额字段单位为分，需要除以100转换为元
- 字符类型字段需要注意大小写敏感问题
