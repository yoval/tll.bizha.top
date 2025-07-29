# `dwd_rps_dt_order_goods_di`

---

- 报货历史详单查询


| 字段               | 类型         | 说明         | 示例                   |
| ------------------ | ------------ | ------------ | ---------------------- |
| id                 | int          | 自增ID       | 11                     |
| order_id           | int          | 订单ID       | 100027                 |
| order_no           | string       | 订单编码     | XCD00000000012         |
| sortId             | int          | 序号         | 1                      |
| article_id         | int          | 文章ID       |                        |
| goods_no           | string       | 商品货号     | 120001041              |
| goods_title        | string       | 商品标题     | 摇摇杯宣传物料包 杯贴  |
| goods_price        | decimal(143) | 商品价格     | 85                     |
| real_price         | decimal(143) | 实际标题     | 85                     |
| quantity           | decimal(142) | 数量         | 1                      |
| taxAmount          | decimal(143) | 实际金额     | 85                     |
| point              | int          | 积分         | 0                      |
| discount           | int          | 折扣金额     | 100                    |
| derate             | decimal(142) | 利率         | 0                      |
| fabh               | string       | fabh         |                        |
| cxbs               | string       | cxbs         |                        |
| decaribe           | string       | 描述         |                        |
| entid              | string       | 企业代码     | E26FMM0XNYQ            |
| IsCriticism        | string       | 是否评论     | N                      |
| PromScenario       | string       | PromScenario |                        |
| Status             | int          | 状态         | 0                      |
| ReturnNum          | decimal(142) | 退货数量     | 0                      |
| PiHao              | string       | PiHao        |                        |
| timestamps         | string       | 创建时间     | 2023/6/15 12:23        |
| erp_orderno        | string       | U8C订单编号  |                        |
| erp_orderno_return | string       | U8C退单编号  |                        |
| storcode           | string       | 仓库编码     | 1001F8100000000001IZ   |
| storname           | string       | 仓库名称     | 蚌埠快递仓（原天津仓） |
| updatetime         | string       | 审核时间     | 2023/6/15 12:30        |
| data_source        | int          | 数据源类型   | 2                      |

- 备注：u8c渠道，已于2024年9月后弃用