# `dim_sup_srm_goods_df`

--- 

- 报货产品信息

| 字段                  | 类型          | 说明                                                  | 示例                        |
| --------------------- | ------------- | ----------------------------------------------------- | --------------------------- |
| id                    | BIGINT        | 主键ID                                                | 860561446084350776          |
| goods_name            | VARCHAR(255)  | 商品名称                                              | 香辣味脆爽魔芋-18g*100袋/箱 |
| goods_code            | VARCHAR(255)  | 商品编码                                              | 108000007                   |
| specs                 | VARCHAR(255)  | 规格                                                  | 18g*100袋/箱                |
| unit                  | VARCHAR(255)  | 单位                                                  | JAN                         |
| default_price         | DECIMAL(10,2) | 默认价格                                              | 55                          |
| status                | INT           | 状态（0: 停用，1: 启用）                              | 1                           |
| area_price_status     | INT           | 区域价格状态（0: 未设置，1: 已设置）                  | 0                           |
| area_sell_status      | INT           | 区域售卖状态（0: 未设置，1: 已设置）                  | 0                           |
| up_down_status        | INT           | 上下架状态（0: 未设置，1: 已设置）                    | 1                           |
| goods_category        | VARCHAR(255)  | 商品品类                                              | 108                         |
| goods_classify        | INT           | 商品分类（0:常规商品，1：组合商品，2:BOM组合商品）    | 0                           |
| goods_type            | VARCHAR(255)  | 商品类型（10: 实物类商品，30:虚拟商品,20:服务类商品） | 10                          |
| creator               | VARCHAR(255)  | 创建人                                                |                             |
| updater               | VARCHAR(255)  | 修改人                                                |                             |
| create_time           | VARCHAR(255)  | 创建时间                                              | 2024/8/29 14:56             |
| modify_time           | VARCHAR(255)  | 修改时间                                              | 2025/4/8 13:47              |
| spu_code              | VARCHAR(255)  | SPU编码                                               | 108000007                   |
| spu_name              | VARCHAR(555)  | SPU名字                                               | 香辣味脆爽魔芋-18g*100袋/箱 |
| delete_flag           | INT           | 是否删除（0: 否 1: 是）                               | 0                           |
| make_goods            | INT           | 是否组装商品（0: 否 1: 是）                           | 0                           |
| organization          | VARCHAR(255)  | 组织                                                  | 1000                        |
| tenant_id             | BIGINT        | 租户ID                                                | 854339203348044495          |
| belong_org_id         | BIGINT        | 所属组织ID                                            |                             |
| tenant_org_id         | BIGINT        | 租户组织ID                                            |                             |
| remark                | VARCHAR(255)  | 备注                                                  |                             |
| create_user_id        | BIGINT        | 记录创建者ID                                          | 0                           |
| modify_user_id        | BIGINT        | 记录最后更新者ID                                      | 0                           |
| audit_data_version    | INT           | 锁版本                                                |                             |
| sec_bu_id             | BIGINT        | 数据归属组织id                                        |                             |
| sec_user_id           | BIGINT        | 数据归属雇员id                                        |                             |
| sec_ou_id             | BIGINT        | 数据归属公司id                                        |                             |
| pid                   | BIGINT        | 上级ID                                                |                             |
| sub_item_code         | VARCHAR(255)  | 子件商品编码                                          |                             |
| product_type          | VARCHAR(255)  | 商品类型                                              | XC                          |
| guarantee_days        | VARCHAR(255)  | 保质期时长                                            | 12                          |
| guarantee_period_unit | VARCHAR(255)  | 保质期时长                                            | MONTH                       |

- 分类

| 类型 | 名称 |
| ---- | ---- |
| PT   | 普通 |
| XC   | 宣传 |
| ZY   | 直运 |
| SD   | 速冻 |
| SG   | 水果 |


- 单位

| 单位  | 名称 |
| ----- | ---- |
| JAN   | 件   |
| PCS   | 个   |
| TAO   | 套   |
| TAI   | 台   |
| BAG   | 包   |
| POT   | 罐   |
| ROL   | 卷   |
| KG    | 千克 |
| XIANG | 箱   |
| BOT   | 瓶   |