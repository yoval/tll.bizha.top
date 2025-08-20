# dwd_rps_tll_order_cancel_product_df

## 表描述
OLAP

## 数据量
- 总记录数：10,729,982 条

## 字段信息

| 字段名称 | 数据类型 | 是否可空 | 默认值 | 字段描述 | 示例 |
|---------|----------|----------|--------|----------|------|
| id | BIGINT | 是 |  | 主键ID，使用雪花算法生成的自定义long类型 | 484254983291289600 |
| serial_no | VARCHAR(255) | 是 |  | 流水号，从订单商品明细继承过来 | 327484 |
| product_code | VARCHAR(255) | 是 |  | 商品编码 | 020000019 |
| product_name | VARCHAR(255) | 是 |  | 商品名称 | 速冻百香果浆-950g*12瓶/箱 |
| product_specification | VARCHAR(255) | 是 |  | 商品规格 | 5000个/件 |
| product_unit | VARCHAR(255) | 是 |  | 单位编码，当前下单对应的单位编码+名称 | 件 |
| is_gift | INT | 是 |  | 是否赠品，默认0:否  1:是 | 0 |
| cancel_quantity | INT | 是 |  | 取消数量 | 1 |
| refund_unit_price | DECIMAL(10,3) | 是 |  | 退款单价，对应订单中原折后含税单价 | 220.000 |
| subtotal | DECIMAL(10,3) | 是 |  | 小计 | 81.000 |
| discount_amount | DECIMAL(10,3) | 是 |  | 优惠金额，商品单价和折后单价的差乘以数量 | 18.000 |
| actual_refund_amount | DECIMAL(10,3) | 是 |  | 银行卡实退金额 | 228.580 |
| pt_discount_amount | DECIMAL(10,3) | 是 |  | 平台优惠退的金额 | 0.000 |
| agent_amount | DECIMAL(10,3) | 是 |  | 代理商代收代付款 | 0.000 |
| business_discount | DECIMAL(10,3) | 是 |  | 招商优惠 | 0.000 |
| customer_discount | DECIMAL(10,3) | 是 |  | 客户往来款 | 0.000 |
| house_subsidy | DECIMAL(10,3) | 是 |  | 房租优惠 | 0.000 |
| cancel_order_id | BIGINT | 是 |  | 退款单id | 484249094496862208 |
| create_time | VARCHAR(255) | 是 |  | 创建时间 | 2024-08-28 23:37:08 |
| update_time | VARCHAR(255) | 是 |  | 更新时间 | 2024-08-28 23:37:42 |
| create_by | VARCHAR(255) | 是 |  | 创建者 |  |
| update_by | VARCHAR(255) | 是 |  | 修改者 |  |
| order_id | BIGINT | 是 |  | 订单ID，long类型 | 484254901477064704 |
| product_id | BIGINT | 是 |  | 商品ID，long类型 | 483962582441529344 |
| product_price | DECIMAL(10,3) | 是 |  | 商品单价 | 90.000 |
| tenant_id | VARCHAR(255) | 是 |  | 租户id | tll |
| discount_unit_price | DECIMAL(10,3) | 是 |  | 商品折后单价 | 230.000 |
| is_combination_children_product | INT | 是 |  | 是否是组合子商品(1-是,2-否) | 2 |
| pt | VARCHAR(255) | 是 |  | 天分区 | 20250817 |

## 使用说明

### 常用查询示例

```sql
-- 查询最新数据
SELECT * FROM dwd_rps_tll_order_cancel_product_df 
ORDER BY business_date DESC 
LIMIT 10;

-- 查询数据总量
SELECT COUNT(*) FROM dwd_rps_tll_order_cancel_product_df;

-- 查询某日数据
SELECT * FROM dwd_rps_tll_order_cancel_product_df 
WHERE business_date = 20240101;
```

### 注意事项
- 时间字段通常为bigint类型，格式为YYYYMMDD
- 金额字段单位为分，需要除以100转换为元
- 字符类型字段需要注意大小写敏感问题
