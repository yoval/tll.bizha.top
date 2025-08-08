# dwd_rps_tll_order_cancel_df

## 表描述
OLAP

## 数据量
- 总记录数：809,648 条

## 字段信息

| 字段名称 | 数据类型 | 是否可空 | 默认值 | 字段描述 |
|---------|----------|----------|--------|----------|
| id | BIGINT | 是 |  | 主键ID，使用雪花算法生成的自定义long类型 |
| cancel_order_num | VARCHAR(255) | 是 |  | 退款单编号 |
| refund_status | INT | 是 |  | 退款状态，0：待审核 1：退款中 2：已完成 3：退款失败 4：已关闭 |
| order_id | BIGINT | 是 |  | 原订单id |
| refund_type | INT | 是 |  | 退款类型，1：差异退 2：取消出库（支持部分取退、整单取消） |
| store_code | VARCHAR(255) | 是 |  | 门店编码 |
| store_name | VARCHAR(255) | 是 |  | 门店名称 |
| settlement_currency | INT | 是 |  | 结算币种，不填默认CNY，1：CNY |
| refund_price | DECIMAL(10,3) | 是 |  | 退款金额 |
| cancel_time | VARCHAR(255) | 是 |  | 退款日期，单据创建日期 |
| created_at | VARCHAR(255) | 是 |  | 创建时间 |
| update_time | VARCHAR(255) | 是 |  | 更新时间 |
| create_by | VARCHAR(255) | 是 |  | 创建者 |
| update_by | VARCHAR(255) | 是 |  | 修改者 |
| review_reason | VARCHAR(255) | 是 |  | 审核原因 |
| order_status | INT | 是 |  | 订单状态 |
| refund_progress | VARCHAR(255) | 是 |  | 退款进度 |
| refund_reason | VARCHAR(255) | 是 |  | 退款理由 |
| refund_count | INT | 是 |  | 退商品数量 |
| product_price_sum | DECIMAL(10,3) | 是 |  | 商品总金额 |
| service_fee | DECIMAL(10,3) | 是 |  | 手续费 |
| tenant_id | VARCHAR(255) | 是 |  | 租户id |
| is_compare_end | INT | 是 |  | 差异比较是否完成，0：否 1：是 |
| cancel_type | INT | 是 |  | 订单审核前(待确认)取退， |
| pt | VARCHAR(255) | 是 |  | 天分区 |

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
