# dwd_rps_dt_orders_di

## 表描述
OLAP

## 数据量
- 总记录数：611,040 条

## 字段信息

| 字段名称 | 数据类型 | 是否可空 | 默认值 | 字段描述 | 示例 |
|---------|----------|----------|--------|----------|------|
| uuid | VARCHAR(255) | 是 |  | uuid | 0000e365-1cc1-49e0-8d70-a011267d4a5a |
| billno | INT | 是 |  | 自增ID | 186831 |
| order_no | VARCHAR(255) | 是 |  | 订单号 | BDD00000541785 |
| pd_no | VARCHAR(255) | 是 |  | pd_no | 10097 |
| user_id | VARCHAR(255) | 是 |  | 用户ID | 2003105 |
| businessid | VARCHAR(255) | 是 |  | 用户名 | 2002332 |
| payment_id | INT | 是 |  | 支付方式 | 100017 |
| payment_fee | DECIMAL(9,3) | 是 |  | 支付手续费 | 0.000 |
| refund_fee | DECIMAL(14,2) | 是 |  | refund_fee | 0.00 |
| payment_status | INT | 是 |  | 支付状态1未支付2已支付 | 2 |
| payment_initiationtime | VARCHAR(255) | 是 |  | payment_initiationtime |  |
| payment_time | VARCHAR(255) | 是 |  | 支付时间 | 2024-05-28 16:42:30 |
| accept_name | VARCHAR(255) | 是 |  | 收货人姓名 | 蚌埠鑫禾茂餐饮管理有限公司（丁柯） |
| post_code | VARCHAR(255) | 是 |  | 邮政编码 |  |
| telphone | VARCHAR(255) | 是 |  | 联系电话 | 13052648086 |
| area | VARCHAR(255) | 是 |  | 所属省市区 |  |
| address | VARCHAR(455) | 是 |  | 地址 | 江苏省苏州市常熟市 江苏苏州市常熟市沙家浜唐市三塘路78号店面甜啦啦奶茶店 |
| message | VARCHAR(255) | 是 |  | 订单留言 |  |
| remark | VARCHAR(255) | 是 |  | 订单备注 |  |
| is_invoice | INT | 是 |  | 是否索要发票 | 0 |
| invoice_title | VARCHAR(255) | 是 |  | 发票抬头 |  |
| invoice_taxes | DECIMAL(9,3) | 是 |  | 税金 | 0.000 |
| discount_amount | DECIMAL(14,3) | 是 |  | 应付商品总金额 | 0.000 |
| real_amount | DECIMAL(14,3) | 是 |  | 实付商品总金额 | 14520.000 |
| order_amount | DECIMAL(14,3) | 是 |  | 订单总金额 | 14520.000 |
| onlineamount | DECIMAL(14,3) | 是 |  | onlineamount | 9270.800 |
| bonusamount | DECIMAL(14,3) | 是 |  | bonusamount | 0.000 |
| discountapportion | DECIMAL(14,3) | 是 |  | discountapportion | 0.000 |
| point | INT | 是 |  | 积分_正数赠送_负数消费 | 0 |
| status | INT | 是 |  | 订单状态1生成订单_2确认订单_3完成订单_4取消订单_5作废订单_7已收货 | 3 |
| add_time | VARCHAR(255) | 是 |  | 下单时间 | 2024-08-23 19:38:50 |
| source | VARCHAR(255) | 是 |  | source | PC |
| decaribe | VARCHAR(255) | 是 |  | decaribe |  |
| login_id | INT | 是 |  | login_id | 0 |
| is_integral | VARCHAR(255) | 是 |  | is_integral | N |
| entid | VARCHAR(255) | 是 |  | entid | E26FMM0XNYQ |
| postage | DECIMAL(14,2) | 是 |  | postage | 0.00 |
| free | VARCHAR(255) | 是 |  | free | N  |
| upstatustime | VARCHAR(255) | 是 |  | upstatustime | 2023-10-14 14:18:51 |
| order_date | VARCHAR(255) | 是 |  | order_date | 2023-05-16 |
| order_time | VARCHAR(255) | 是 |  | order_time | 16:30:21 |
| iscriticism | VARCHAR(255) | 是 |  | 是否评论 | N  |
| expressname | VARCHAR(255) | 是 |  | expressname |  |
| expressnum | VARCHAR(255) | 是 |  | expressnum |  |
| shipmentstime | VARCHAR(255) | 是 |  | shipmentstime |  |
| ywyid | VARCHAR(255) | 是 |  | ywyid |  |
| fpshtx | VARCHAR(255) | 是 |  | fpshtx |  |
| psfs | VARCHAR(255) | 是 |  | psfs | 物流 |
| fhfs | VARCHAR(255) | 是 |  | fhfs | 银行卡支付 |
| lineamount | DECIMAL(14,2) | 是 |  | lineamount | 0.00 |
| payid | VARCHAR(255) | 是 |  | payid |                      |
| is_pt | VARCHAR(255) | 是 |  | 是否为拼团 | Y |
| producer | VARCHAR(255) | 是 |  | 制单人 | 19955260188 |
| areacode | VARCHAR(255) | 是 |  | areacode | 02050812 |
| audit_time | VARCHAR(255) | 是 |  | 审核时间 | 2021-09-18 15:39:28 |
| use_balance | DECIMAL(14,2) | 是 |  | use_balance | 0.00 |
| use_fanli | DECIMAL(14,2) | 是 |  | use_fanli | 0.00 |
| cancel_time | VARCHAR(255) | 是 |  | cancel_time | 2022-03-30 12:22:33 |
| is_chaizhang | INT | 是 |  | is_chaizhang | 1 |
| is_received | INT | 是 |  | 是否收货 | 1 |
| order_type | VARCHAR(255) | 是 |  | 订单类型 | 正常 |
| generate | VARCHAR(255) | 是 |  | generate | 223018152220240612162754768 |
| thirdparty | VARCHAR(255) | 是 |  | thirdparty |  |
| storcode | VARCHAR(255) | 是 |  | storcode | 01 |
| storname | VARCHAR(255) | 是 |  | storname | 蚌埠仓 |
| is_refund | INT | 是 |  | is_refund | 0 |
| agent_id | VARCHAR(255) | 是 |  | 代理id | 50000014 |
| agent_name | VARCHAR(255) | 是 |  | 代理名称 | 郭凯峰（邢台） |
| agent_ratio | DECIMAL(8,2) | 是 |  | 代理系数 | 0.00 |
| data_source | VARCHAR(255) | 是 |  | 1普通物料2宣传物料 | 1 |
| pt | VARCHAR(255) | 是 |  | 天分区 | 20240823 |

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
