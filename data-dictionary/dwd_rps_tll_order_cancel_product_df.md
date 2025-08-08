# dwd_rps_tll_order_cancel_product_df

## 表描述
**业务层级**: DWD层 - 订单取消商品明细表  
**数据用途**: OLAP分析  
**数据量**: 10,187,466条记录  
**更新频率**: 每日更新  

## 表结构说明
该表存储订单取消时的商品级详细信息，包含取消商品的基本信息、取消数量、退款金额、优惠分摊等关键字段。每个取消订单对应多条商品记录。

## 字段详情

| 字段名称 | 数据类型 | 是否可空 | 默认值 | 字段说明 |
|---------|----------|----------|--------|----------|
| id | bigint | 否 | - | 主键ID，使用雪花算法生成的自定义long类型 |
| serial_no | varchar | 是 | NULL | 流水号，从订单商品明细继承过来 |
| product_code | varchar | 是 | NULL | 商品编码 |
| product_name | varchar | 是 | NULL | 商品名称 |
| product_specification | varchar | 是 | NULL | 商品规格 |
| product_unit | varchar | 是 | NULL | 单位编码，当前下单对应的单位编码+名称 |
| is_gift | int | 是 | 0 | 是否赠品，默认0:否 1:是 |
| cancel_quantity | int | 是 | NULL | 取消数量 |
| refund_unit_price | decimal | 是 | NULL | 退款单价，对应订单中原折后含税单价 |
| subtotal | decimal | 是 | NULL | 小计 |
| discount_amount | decimal | 是 | NULL | 优惠金额，商品单价和折后单价的差乘以数量 |
| actual_refund_amount | decimal | 是 | NULL | 银行卡实退金额 |
| pt_discount_amount | decimal | 是 | NULL | 平台优惠退的金额 |
| agent_amount | decimal | 是 | NULL | 代理商代收代付款 |
| business_discount | decimal | 是 | NULL | 招商优惠 |
| customer_discount | decimal | 是 | NULL | 客户往来款 |
| house_subsidy | decimal | 是 | NULL | 房租优惠 |
| cancel_order_id | bigint | 是 | NULL | 退款单id |
| create_time | varchar | 是 | NULL | 创建时间 |
| update_time | varchar | 是 | NULL | 更新时间 |
| create_by | varchar | 是 | NULL | 创建者 |
| update_by | varchar | 是 | NULL | 修改者 |
| order_id | bigint | 是 | NULL | 订单ID，long类型 |
| product_id | bigint | 是 | NULL | 商品ID，long类型 |
| product_price | decimal | 是 | NULL | 商品单价 |
| tenant_id | varchar | 是 | NULL | 租户id |
| discount_unit_price | decimal | 是 | NULL | 商品折后单价 |
| is_combination_children_product | int | 是 | NULL | 是否是组合子商品(1-是,2-否) |
| pt | varchar | 是 | NULL | 天分区 |

## 业务说明

### 关键字段解释
- **cancel_quantity**: 商品取消的数量，正整数
- **refund_unit_price**: 商品取消时的退款单价，已考虑折扣
- **actual_refund_amount**: 实际退回给客户的银行卡金额
- **discount_amount**: 商品取消时优惠金额的分摊

### 金额计算逻辑
```
subtotal = refund_unit_price × cancel_quantity
discount_amount = (product_price - discount_unit_price) × cancel_quantity
```

### 使用场景
1. **取消商品分析**: 分析各商品的取消情况
2. **退款金额统计**: 统计各商品的实际退款金额
3. **优惠分摊计算**: 计算取消商品的优惠金额分摊
4. **商品维度分析**: 按商品维度分析取消订单

## 常用查询示例

### 1. 查询某日各商品的取消数量
```sql
SELECT 
    product_code,
    product_name,
    SUM(cancel_quantity) as total_cancel_qty,
    SUM(actual_refund_amount) as total_refund
FROM dwd_rps_tll_order_cancel_product_df
WHERE pt = '20241201'
GROUP BY product_code, product_name
ORDER BY total_cancel_qty DESC;
```

### 2. 查询某订单的取消商品详情
```sql
SELECT 
    product_code,
    product_name,
    cancel_quantity,
    refund_unit_price,
    actual_refund_amount,
    discount_amount
FROM dwd_rps_tll_order_cancel_product_df
WHERE order_id = 12345678
ORDER BY product_code;
```

### 3. 统计某时间段内取消金额TOP商品
```sql
SELECT 
    product_code,
    product_name,
    COUNT(*) as cancel_times,
    SUM(cancel_quantity) as total_cancel_qty,
    SUM(actual_refund_amount) as total_refund_amount
FROM dwd_rps_tll_order_cancel_product_df
WHERE pt BETWEEN '20241201' AND '20241231'
GROUP BY product_code, product_name
HAVING total_refund_amount > 1000
ORDER BY total_refund_amount DESC
LIMIT 20;
```

## 注意事项

1. **时间格式**: 所有时间字段均为字符串格式，格式为`YYYY-MM-DD HH:MM:SS`
2. **金额单位**: 所有金额字段单位均为**分**
3. **分区字段**: 使用`pt`字段作为时间分区，格式为`YYYYMMDD`
4. **关联关系**: 通过`cancel_order_id`关联到`dwd_rps_tll_order_cancel_df`表
5. **数据量**: 该表数据量较大，查询时建议使用分区过滤
