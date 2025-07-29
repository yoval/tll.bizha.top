# `dwd_rps_dt_orders_di`

---

- 报货历史订单查询


| 字段                   | 类型         | 说明                                                         | 示例                                                 |
| ---------------------- | ------------ | ------------------------------------------------------------ | ---------------------------------------------------- |
| billno                 | int          | 自增ID                                                       | 124506                                               |
| order_no               | string       | 订单号                                                       | BDD00000028062                                       |
| pd_no                  | string       | pd_no                                                        |                                                      |
| user_id                | string       | 用户ID                                                       | 2003105                                              |
| businessid             | string       | 用户名                                                       | 2003105                                              |
| payment_id             | int          | 支付方式                                                     | 100017                                               |
| payment_fee            | decimal(93)  | 支付手续费                                                   | 0                                                    |
| refund_fee             | decimal(142) | refund_fee                                                   | 0                                                    |
| payment_status         | int          | 支付状态1未支付2已支付                                       | 2                                                    |
| payment_initiationtime | string       | payment_initiationtime                                       |                                                      |
| payment_time           | string       | 支付时间                                                     |                                                      |
| accept_name            | string       | 收货人姓名                                                   | 巫阿龙                                               |
| post_code              | string       | 邮政编码                                                     |                                                      |
| telphone               | string       | 联系电话                                                     | 17681099609                                          |
| area                   | string       | 所属省市区                                                   |                                                      |
| address                | string       | 收货地址                                                     | 安徽省阜阳市颍州区安徽阜阳市颍州区京九办事处申寨社区 |
| message                | string       | 订单留言                                                     |                                                      |
| remark                 | string       | 订单备注                                                     |                                                      |
| is_invoice             | int          | 是否索要发票                                                 | 0                                                    |
| invoice_title          | string       | 发票抬头                                                     |                                                      |
| invoice_taxes          | decimal(93)  | 税金                                                         | 0                                                    |
| discount_amount        | decimal(143) | 应付商品总金额                                               | 0                                                    |
| real_amount            | decimal(143) | 实付商品总金额                                               | 920                                                  |
| order_amount           | decimal(143) | 订单总金额                                                   | 920                                                  |
| onlineamount           | decimal(143) | onlineamount                                                 | 920                                                  |
| bonusamount            | decimal(143) | bonusamount                                                  | 0                                                    |
| discountapportion      | decimal(143) | discountapportion                                            | 0                                                    |
| point                  | int          | 积分_正数赠送_负数消费                                       | 0                                                    |
| status                 | int          | 订单状态1生成订单_2确认订单_3完成订单_4取消订单_5作废订单_7已收货 | 3                                                    |
| add_time               | timestamp    | 下单时间                                                     | 2021/9/18 15:36                                      |
| source                 | string       | source                                                       | PC                                                   |
| decaribe               | string       | decaribe                                                     |                                                      |
| login_id               | int          | login_id                                                     | 0                                                    |
| is_integral            | string       | is_integral                                                  | N                                                    |
| entid                  | string       | entid                                                        | E26FMM0XNYQ                                          |
| postage                | decimal(142) | postage                                                      | 0                                                    |
| free                   | string       | free                                                         | N                                                    |
| upstatustime           | string       | upstatustime                                                 | 2021/9/18 15:36                                      |
| order_date             | string       | order_date                                                   | 2021/9/18                                            |
| order_time             | string       | order_time                                                   | 15:36:11                                             |
| iscriticism            | string       | 是否评论                                                     | N                                                    |
| expressname            | string       | expressname                                                  |                                                      |
| expressnum             | string       | expressnum                                                   |                                                      |
| shipmentstime          | string       | shipmentstime                                                |                                                      |
| ywyid                  | string       | ywyid                                                        |                                                      |
| fpshtx                 | string       | fpshtx                                                       |                                                      |
| psfs                   | string       | psfs                                                         | 物流                                                 |
| fhfs                   | string       | fhfs                                                         | 银行卡支付                                           |
| lineamount             | decimal(142) | lineamount                                                   | 0                                                    |
| payid                  | string       | payid                                                        |                                                      |
| is_pt                  | string       | 是否为拼团                                                   |                                                      |
| producer               | string       | 制单人                                                       | 19955260188                                          |
| areacode               | string       | areacode                                                     | 02140408                                             |
| audit_time             | timestamp    | 审核时间                                                     | 2021/9/18 15:39                                      |
| use_balance            | decimal(142) | use_balance                                                  | 0                                                    |
| use_fanli              | decimal(142) | use_fanli                                                    | 0                                                    |
| cancel_time            | string       | cancel_time                                                  | 2021/9/18 16:06                                      |
| is_chaizhang           | int          | is_chaizhang                                                 | 1                                                    |
| is_received            | int          | 是否收货                                                     | 1                                                    |
| order_type             | string       | 订单类型                                                     | 正常                                                 |
| generate               | string       | generate                                                     |                                                      |
| thirdparty             | string       | thirdparty                                                   |                                                      |
| storcode               | string       | storcode                                                     |                                                      |
| storname               | string       | storname                                                     |                                                      |
| is_refund              | int          | is_refund                                                    |                                                      |
| agent_id               | string       | 代理id                                                       |                                                      |
| agent_name             | string       | 代理名称                                                     |                                                      |
| agent_ratio            | decimal(82)  | 代理系数                                                     | 0                                                    |
| data_source            | string       | 1普通物料2宣传物料                                           | 1                                                    |
| area_manager           | string       | 区域经理                                                     | 20210918                                             |
| province_manager       | string       | 省经理                                                       |                                                      |
| big_area_manager       | string       | 大区经理                                                     |                                                      |


注：

- 中台u8c筛选以创建时间为准

- 筛选条件：`status = 3`

u8c渠道，已于2024年9月后弃用

