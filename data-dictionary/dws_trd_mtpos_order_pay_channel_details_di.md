# dws_trd_mtpos_order_pay_channel_details_di

## 表描述
订单支付渠道详情表


## 字段信息

| 字段名称 | 数据类型 | 是否可空 | 默认值 | 字段描述 |
|---------|----------|----------|--------|----------|
| pt | VARCHAR(100) | 是 |  | 分区时间 |
| order_id | VARCHAR(100) | 是 |  | 订单id |
| shop_id | VARCHAR(100) | 是 |  | 门店id(标准化) |
| data_source | VARCHAR(100) | 是 |  | 数据来源(instore 店内；mt 美团外卖；ele 饿了么外卖；self 自营外卖) |
| source_name | VARCHAR(100) | 是 |  | 订单来源名称 |
| status_name | VARCHAR(100) | 是 |  | 订单状态名称 |
| payment_channels | VARCHAR(100) | 是 |  | 支付渠道名称 |
| pay_way_pay_type | INT | 是 |  | 支付方式Id，大于1000的属于自定支付方式 |
| pay_way_pay_type_name | VARCHAR(100) | 是 |  | 结账方式名称 (格式:一级结账方式名称-二级结账方式名称）注：当一级和二级名称相同时，展示格式为：二级结账方式名称。 |
| income | DECIMAL(16,2) | 是 |  | 收入金额 |
| discount | DECIMAL(16,2) | 是 |  | 优惠金额 |
| amount | DECIMAL(16,2) | 是 |  | 流水金额 |
| refund_status | INT | 是 |  | 退单状态,0-未退单, 1-退单中, 2-已退单, 3-退单部分失败 |
| pay_way_created_time | VARCHAR(100) | 是 |  | 支付订单创建时间 |
| pay_way_refund_time | VARCHAR(100) | 是 |  | 支付订单退款时间 |
| pay_way_status | INT | 是 |  | 状态：-1 未支付,1 已支付,2 已撤销,3 支付中,4 退款中,5 支付失败,6 退款失败 |
| pay_way_type | INT | 是 |  | 支付类型 1-支付、2-找零、3-退款、4-找零撤销 |

## 使用说明

### 常用查询示例

```sql
-- 查询最新数据
SELECT * FROM dws_trd_mtpos_order_pay_channel_details_di 
ORDER BY business_date DESC 
LIMIT 10;

-- 查询数据总量
SELECT COUNT(*) FROM dws_trd_mtpos_order_pay_channel_details_di;

-- 查询某日数据
SELECT * FROM dws_trd_mtpos_order_pay_channel_details_di 
WHERE business_date = 20240101;
```

