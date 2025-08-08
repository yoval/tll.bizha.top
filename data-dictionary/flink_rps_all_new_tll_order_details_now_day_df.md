# flink_rps_all_new_tll_order_details_now_day_df

## 表描述
订单详情表


## 字段信息

| 字段名称 | 数据类型 | 是否可空 | 默认值 | 字段描述 |
|---------|----------|----------|--------|----------|
| id | VARCHAR(255) | 是 |  | 明细ID |
| order_id | VARCHAR(255) | 是 |  | 订单号 |
| product_info | VARCHAR(255) | 是 |  | 商品信息 |
| product_specification | VARCHAR(255) | 是 |  | 商品规格 |
| product_id | VARCHAR(255) | 是 |  | 商品ID |
| sku_code | VARCHAR(255) | 是 |  | SKU代码 |
| supplier | VARCHAR(255) | 是 |  | 供应商 |
| unit_price | DECIMAL(10,2) | 是 |  | 单价 |
| quantity | INT | 是 |  | 购买数量 |
| cancel_quantity | INT | 是 |  | 取消数量 |
| payable_amount | DECIMAL(10,2) | 是 |  | 应付金额 |
| discount_amount | DECIMAL(10,2) | 是 |  | 优惠金额 |
| actual_amount | DECIMAL(10,2) | 是 |  | 实付金额 |
| status | INT | 是 |  | 状态 |
| tenant_id | VARCHAR(255) | 是 |  | 租户ID |
| create_time | VARCHAR(255) | 是 |  | 创建时间 |
| product_type | VARCHAR(255) | 是 |  | 商品类型 |
| warehouse_id | INT | 是 |  | 发货仓库 |
| warehouse_batch_no | VARCHAR(255) | 是 |  | 仓库批次号 |
| discount_unit_price | DECIMAL(10,2) | 是 |  | 折后单价 |
| category_id | INT | 是 |  | 类目id |
| tax_rate | DECIMAL(10,2) | 是 |  | 税率 |
| is_freebies | INT | 是 |  | 是否为赠品：0：否  1：是 |
| packaging_unit | VARCHAR(255) | 是 |  | 包装单位 |
| unit_code | VARCHAR(255) | 是 |  | 单位编码 |
| serial_no | VARCHAR(255) | 是 |  | 流水号 |
| out_quantity | INT | 是 |  | 出库数量 |
| customer_discount_amount | DECIMAL(10,2) | 是 |  | 客户优惠 |
| rent_subsidy_amount | DECIMAL(10,2) | 是 |  | 房租优惠 |
| agent_amount | DECIMAL(10,2) | 是 |  | 代理商代收代付款 |
| bank_actual_amount | DECIMAL(10,2) | 是 |  | 银行实付金额 |
| pt_discount_amount | DECIMAL(10,2) | 是 |  | 平台优惠金额 |
| is_combination_children_product | INT | 是 |  | 是否是组合子商品(1-是,2-否) |
| final_pay_amount | DECIMAL(10,2) | 是 |  | 最终支付金额，包含银行和平台付款，折后单价乘以出库数量 |
| modify_time | VARCHAR(64) | 是 |  | 修改时间 |
| activity_id | VARCHAR(32) | 是 |  | 预售活动id |
| combination_code | VARCHAR(64) | 是 |  | 组合商品编码 |
| pullstate | VARCHAR(255) | 是 |  | 新报货 |

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
