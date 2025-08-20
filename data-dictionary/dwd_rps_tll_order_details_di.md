# dwd_rps_tll_order_details_di

## 表描述
OLAP

## 数据量
- 总记录数：3,364,778 条

## 字段信息

| 字段名称 | 数据类型 | 是否可空 | 默认值 | 字段描述 | 示例 |
|---------|----------|----------|--------|----------|------|
| pt | VARCHAR(255) | 是 |  | 天分区 | 20240905 |
| id | VARCHAR(255) | 是 |  | 明细ID | 223114 |
| order_id | VARCHAR(255) | 是 |  | 订单号 | 484019879599947776 |
| product_info | VARCHAR(255) | 是 |  | 商品信息 | 收银机软件系统-美团 |
| product_specification | VARCHAR(255) | 是 |  | 商品规格 | 15.6寸(美团) |
| product_id | VARCHAR(255) | 是 |  | 商品ID | 483962582462500864 |
| sku_code | VARCHAR(255) | 是 |  | SKU代码 | 100001551 |
| supplier | VARCHAR(255) | 是 |  | 供应商 | 未知 |
| unit_price | DECIMAL(10,2) | 是 |  | 单价 | 2276.00 |
| quantity | INT | 是 |  | 购买数量 | 1 |
| cancel_quantity | INT | 是 |  | 取消数量 | 0 |
| payable_amount | DECIMAL(10,2) | 是 |  | 应付金额 | 2276.00 |
| discount_amount | DECIMAL(10,2) | 是 |  | 优惠金额 | 0.00 |
| actual_amount | DECIMAL(10,2) | 是 |  | 实付金额 | 2276.00 |
| status | INT | 是 |  | 状态 | 1 |
| tenant_id | VARCHAR(255) | 是 |  | 租户ID | tll |
| create_time | VARCHAR(255) | 是 |  | 创建时间 | 2024-09-05 16:16:38 |
| product_type | VARCHAR(255) | 是 |  | 商品类型 | SD |
| warehouse_id | INT | 是 |  | 发货仓库 | 969798 |
| warehouse_batch_no | VARCHAR(255) | 是 |  | 仓库批次号 |  |
| discount_unit_price | DECIMAL(10,2) | 是 |  | 折后单价 | 270.00 |
| category_id | BIGINT | 是 |  | 类目id | 857214795298971583 |
| tax_rate | DECIMAL(10,2) | 是 |  | 税率 | 0.13 |
| is_freebies | INT | 是 |  | 是否为赠品：0：否  1：是 |  |
| packaging_unit | VARCHAR(255) | 是 |  | 包装单位 | 件 |
| unit_code | VARCHAR(255) | 是 |  | 单位编码 | JAN |
| serial_no | VARCHAR(255) | 是 |  | 流水号 | 11032 |
| out_quantity | INT | 是 |  | 出库数量 | 1 |
| customer_discount_amount | DECIMAL(10,2) | 是 |  | 客户优惠 | 0.00 |
| rent_subsidy_amount | DECIMAL(10,2) | 是 |  | 房租优惠 | 0.00 |
| agent_amount | DECIMAL(10,2) | 是 |  | 代理商代收代付款 | 0.00 |
| bank_actual_amount | DECIMAL(10,2) | 是 |  | 银行实付金额 | 0.00 |
| pt_discount_amount | DECIMAL(10,2) | 是 |  | 平台优惠金额 | 0.00 |
| is_combination_children_product | INT | 是 |  | 是否是组合子商品(1-是,2-否) | 2 |
| final_pay_amount | DECIMAL(10,2) | 是 |  | 最终支付金额，包含银行和平台付款，折后单价乘以出库数量 | 2276.00 |
| cancel_order_num | VARCHAR(2147483643) | 是 |  | 退款单号 | TK083132542404 |
| created_at | VARCHAR(2147483643) | 是 |  | 退款时间 | 2024-09-06 10:46:17 |
| warehouse_name | VARCHAR(2147483643) | 是 |  | 仓库名称 | 汇旺蚌埠仓工厂通用库 |
| refund_fee | DECIMAL(10,2) | 是 |  | 退单金额 | 0.00 |
| modify_time | VARCHAR(255) | 是 |  | 更新时间 | 2024-09-28 16:25:40 |
| activity_id | VARCHAR(255) | 是 |  | 活动id |  |
| combination_code | VARCHAR(255) | 是 |  | 组合商品编码 |  |
| logistic_fee_amount | DECIMAL(10,2) | 是 |  |  | 0.00 |
| has_logistic_fee | INT | 是 |  |  | 0 |
| delivery_method | INT | 是 |  | 配送方式,1:物流,2:快递,3:上门自提 | 0 |
| shipping_method | INT | 是 |  | 送货方式,0:起订,1:包邮,2:送货上门 | 0 |

## 使用说明

### 常用查询示例

```sql
-- 查询最新数据
SELECT * FROM dwd_rps_tll_order_details_di 
ORDER BY business_date DESC 
LIMIT 10;

-- 查询数据总量
SELECT COUNT(*) FROM dwd_rps_tll_order_details_di;

-- 查询某日数据
SELECT * FROM dwd_rps_tll_order_details_di 
WHERE business_date = 20240101;
```

### 注意事项
- 时间字段通常为bigint类型，格式为YYYYMMDD
- 金额字段单位为分，需要除以100转换为元
- 字符类型字段需要注意大小写敏感问题
