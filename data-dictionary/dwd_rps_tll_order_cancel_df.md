# dwd_rps_tll_order_cancel_df

## 表描述
OLAP

## 数据量
- 总记录数：875,077 条

## 字段信息

| 字段名称 | 数据类型 | 是否可空 | 默认值 | 字段描述 | 示例 |
|---------|----------|----------|--------|----------|------|
| id | BIGINT | 是 |  | 主键ID，使用雪花算法生成的自定义long类型 | 484644868288299008 |
| cancel_order_num | VARCHAR(255) | 是 |  | 退款单编号 | TK083016685591 |
| refund_status | INT | 是 |  | 退款状态，0：待审核 1：退款中 2：已完成 3：退款失败 4：已关闭 | 2 |
| order_id | BIGINT | 是 |  | 原订单id | 484930295830167552 |
| refund_type | INT | 是 |  | 退款类型，1：差异退 2：取消出库（支持部分取退、整单取消） | 2 |
| store_code | VARCHAR(255) | 是 |  | 门店编码 | TLL00234 |
| store_name | VARCHAR(255) | 是 |  | 门店名称 | 甜啦啦喜迎门店 |
| settlement_currency | INT | 是 |  | 结算币种，不填默认CNY，1：CNY | 1 |
| refund_price | DECIMAL(10,3) | 是 |  | 退款金额 | 12012.000 |
| cancel_time | VARCHAR(255) | 是 |  | 退款日期，单据创建日期 | 2024-08-28 23:37:08 |
| created_at | VARCHAR(255) | 是 |  | 创建时间 | 2024-08-30 16:45:41 |
| update_time | VARCHAR(255) | 是 |  | 更新时间 | 2024-08-30 16:50:48 |
| create_by | VARCHAR(255) | 是 |  | 创建者 |  |
| update_by | VARCHAR(255) | 是 |  | 修改者 |  |
| review_reason | VARCHAR(255) | 是 |  | 审核原因 | 水果快递到付费用较高 |
| order_status | INT | 是 |  | 订单状态 | 3 |
| refund_progress | VARCHAR(255) | 是 |  | 退款进度 | 已完成 |
| refund_reason | VARCHAR(255) | 是 |  | 退款理由 | 测试 |
| refund_count | INT | 是 |  | 退商品数量 | 41 |
| product_price_sum | DECIMAL(10,3) | 是 |  | 商品总金额 | 1980.000 |
| service_fee | DECIMAL(10,3) | 是 |  | 手续费 |  |
| tenant_id | VARCHAR(255) | 是 |  | 租户id | tll |
| is_compare_end | INT | 是 |  | 差异比较是否完成，0：否 1：是 | 0 |
| cancel_type | INT | 是 |  | 订单审核前(待确认)取退， | 1 |
| pt | VARCHAR(255) | 是 |  | 天分区 | 20250818 |

## 使用说明

### 常用查询示例

```sql
-- 查询最新数据
SELECT * FROM dwd_rps_tll_order_cancel_df 
ORDER BY business_date DESC 
LIMIT 10;

-- 查询数据总量
SELECT COUNT(*) FROM dwd_rps_tll_order_cancel_df;

-- 查询某日数据
SELECT * FROM dwd_rps_tll_order_cancel_df 
WHERE business_date = 20240101;
```

### 注意事项
- 时间字段通常为bigint类型，格式为YYYYMMDD
- 金额字段单位为分，需要除以100转换为元
- 字符类型字段需要注意大小写敏感问题
