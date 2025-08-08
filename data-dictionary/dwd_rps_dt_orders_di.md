# dwd_rps_dt_orders_di

## 表描述
OLAP

## 数据量
- 总记录数：611,040 条

## 字段信息

| 字段名称 | 数据类型 | 是否可空 | 默认值 | 字段描述 |
|---------|----------|----------|--------|----------|
| uuid | VARCHAR(255) | 是 |  | uuid |
| billno | INT | 是 |  | 自增ID |
| order_no | VARCHAR(255) | 是 |  | 订单号 |
| pd_no | VARCHAR(255) | 是 |  | pd_no |
| user_id | VARCHAR(255) | 是 |  | 用户ID |
| businessid | VARCHAR(255) | 是 |  | 用户名 |
| payment_id | INT | 是 |  | 支付方式 |
| payment_fee | DECIMAL(9,3) | 是 |  | 支付手续费 |
| refund_fee | DECIMAL(14,2) | 是 |  | refund_fee |
| payment_status | INT | 是 |  | 支付状态1未支付2已支付 |
| payment_initiationtime | VARCHAR(255) | 是 |  | payment_initiationtime |
| payment_time | VARCHAR(255) | 是 |  | 支付时间 |
| accept_name | VARCHAR(255) | 是 |  | 收货人姓名 |
| post_code | VARCHAR(255) | 是 |  | 邮政编码 |
| telphone | VARCHAR(255) | 是 |  | 联系电话 |
| area | VARCHAR(255) | 是 |  | 所属省市区 |
| address | VARCHAR(455) | 是 |  | 地址 |
| message | VARCHAR(255) | 是 |  | 订单留言 |
| remark | VARCHAR(255) | 是 |  | 订单备注 |
| is_invoice | INT | 是 |  | 是否索要发票 |
| invoice_title | VARCHAR(255) | 是 |  | 发票抬头 |
| invoice_taxes | DECIMAL(9,3) | 是 |  | 税金 |
| discount_amount | DECIMAL(14,3) | 是 |  | 应付商品总金额 |
| real_amount | DECIMAL(14,3) | 是 |  | 实付商品总金额 |
| order_amount | DECIMAL(14,3) | 是 |  | 订单总金额 |
| onlineamount | DECIMAL(14,3) | 是 |  | onlineamount |
| bonusamount | DECIMAL(14,3) | 是 |  | bonusamount |
| discountapportion | DECIMAL(14,3) | 是 |  | discountapportion |
| point | INT | 是 |  | 积分_正数赠送_负数消费 |
| status | INT | 是 |  | 订单状态1生成订单_2确认订单_3完成订单_4取消订单_5作废订单_7已收货 |
| add_time | VARCHAR(255) | 是 |  | 下单时间 |
| source | VARCHAR(255) | 是 |  | source |
| decaribe | VARCHAR(255) | 是 |  | decaribe |
| login_id | INT | 是 |  | login_id |
| is_integral | VARCHAR(255) | 是 |  | is_integral |
| entid | VARCHAR(255) | 是 |  | entid |
| postage | DECIMAL(14,2) | 是 |  | postage |
| free | VARCHAR(255) | 是 |  | free |
| upstatustime | VARCHAR(255) | 是 |  | upstatustime |
| order_date | VARCHAR(255) | 是 |  | order_date |
| order_time | VARCHAR(255) | 是 |  | order_time |
| iscriticism | VARCHAR(255) | 是 |  | 是否评论 |
| expressname | VARCHAR(255) | 是 |  | expressname |
| expressnum | VARCHAR(255) | 是 |  | expressnum |
| shipmentstime | VARCHAR(255) | 是 |  | shipmentstime |
| ywyid | VARCHAR(255) | 是 |  | ywyid |
| fpshtx | VARCHAR(255) | 是 |  | fpshtx |
| psfs | VARCHAR(255) | 是 |  | psfs |
| fhfs | VARCHAR(255) | 是 |  | fhfs |
| lineamount | DECIMAL(14,2) | 是 |  | lineamount |
| payid | VARCHAR(255) | 是 |  | payid |
| is_pt | VARCHAR(255) | 是 |  | 是否为拼团 |
| producer | VARCHAR(255) | 是 |  | 制单人 |
| areacode | VARCHAR(255) | 是 |  | areacode |
| audit_time | VARCHAR(255) | 是 |  | 审核时间 |
| use_balance | DECIMAL(14,2) | 是 |  | use_balance |
| use_fanli | DECIMAL(14,2) | 是 |  | use_fanli |
| cancel_time | VARCHAR(255) | 是 |  | cancel_time |
| is_chaizhang | INT | 是 |  | is_chaizhang |
| is_received | INT | 是 |  | 是否收货 |
| order_type | VARCHAR(255) | 是 |  | 订单类型 |
| generate | VARCHAR(255) | 是 |  | generate |
| thirdparty | VARCHAR(255) | 是 |  | thirdparty |
| storcode | VARCHAR(255) | 是 |  | storcode |
| storname | VARCHAR(255) | 是 |  | storname |
| is_refund | INT | 是 |  | is_refund |
| agent_id | VARCHAR(255) | 是 |  | 代理id |
| agent_name | VARCHAR(255) | 是 |  | 代理名称 |
| agent_ratio | DECIMAL(8,2) | 是 |  | 代理系数 |
| data_source | VARCHAR(255) | 是 |  | 1普通物料2宣传物料 |
| pt | VARCHAR(255) | 是 |  | 天分区 |

## 使用说明

### 常用查询示例

```sql
-- 查询最新数据
SELECT * FROM dwd_rps_dt_orders_di 
ORDER BY business_date DESC 
LIMIT 10;

-- 查询数据总量
SELECT COUNT(*) FROM dwd_rps_dt_orders_di;

-- 查询某日数据
SELECT * FROM dwd_rps_dt_orders_di 
WHERE business_date = 20240101;
```

### 注意事项
- 时间字段通常为bigint类型，格式为YYYYMMDD
- 金额字段单位为分，需要除以100转换为元
- 字符类型字段需要注意大小写敏感问题
