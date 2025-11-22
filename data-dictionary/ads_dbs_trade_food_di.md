# ads_dbs_trade_food_di

## 字段信息

| 字段名称 | 数据类型 | 是否可空 | 默认值 | 字段描述 | 示例 |
|---------|----------|----------|--------|----------|------|
| business_date | BIGINT | 是 |  | 日期 | 20230101 |
| oper_center_name | VARCHAR(255) | 是 |  | 营运中心 | 全部 |
| prov_id | VARCHAR(64) | 是 |  | 省份编码 | 650000 |
| prov_name | VARCHAR(255) | 是 |  | 省份名称 | 新疆维吾尔自治区 |
| city_id | VARCHAR(64) | 是 |  | 城市编码 | 其它 |
| city_name | VARCHAR(255) | 是 |  | 城市名称 | 其它 |
| city_level | VARCHAR(64) | 是 |  | 城市等级 | 五线 |
| district_id | VARCHAR(64) | 是 |  | 区县编码 |  |
| district_name | VARCHAR(255) | 是 |  | 区县名称 |  |
| busi_area_type | VARCHAR(64) | 是 |  | 商圈 | 普通沿街商铺店 |
| bussiness_type | VARCHAR(64) | 是 |  | 业务类型 | 外卖自提 |
| channel_name | VARCHAR(255) | 是 |  | 订单渠道 | 美团外卖 |
| anal_type | VARCHAR(64) | 是 |  | 分析类型(到家、到店) | 到家 |
| platform | VARCHAR(64) | 是 |  | 平台(到家：美团、饿了么、其它 到店：POS、小程序、其它) | 美团 |
| cust_type | VARCHAR(64) | 是 |  | 用户类型 | 其它 |
| time_name | VARCHAR(255) | 是 |  | 时段 | 其它 |
| food_category_name | VARCHAR(255) | 是 |  | 商品分类 | 水果茶派对 |
| food_oneid | VARCHAR(64) | 是 |  | 商品oneid | e7231302649f38b453255dbdc63c3b6e |
| item_name | VARCHAR(500) | 是 |  | 商品名称 | 雪顶咖啡 |
| new_flag | VARCHAR(64) | 是 |  | 是否新品 | 否 |
| cup_type | VARCHAR(64) | 是 |  | 杯型 | 其它 |
| ice_type | VARCHAR(64) | 是 |  | 温度 | 冰 |
| sugar_type | VARCHAR(64) | 是 |  | 甜度 | 正常糖 |
| dp_total_amount | DECIMAL(16,2) | 是 |  | 商品流水金额 | 0.00 |
| dp_total_amount_last_day | DECIMAL(16,2) | 是 |  | 上一天商品流水金额 | 0.00 |
| dp_total_amount_last_week | DECIMAL(16,2) | 是 |  | 上一周商品流水金额 | 0.00 |
| dp_total_amount_last_year | DECIMAL(16,2) | 是 |  | 去年同期商品流水金额 | 6.93 |
| dp_item_count | BIGINT | 是 |  | 商品销量 | 1 |
| dp_item_count_last_day | BIGINT | 是 |  | 上一天商品销量 | 0 |
| dp_item_count_last_week | BIGINT | 是 |  | 上一周商品销量 | 0 |
| dp_item_count_last_year | BIGINT | 是 |  | 去年同期商品销量 | 1 |
| dp_pay_amount | DECIMAL(16,2) | 是 |  | 商品实收金额 | 0.00 |
| dp_pay_amount_last_day | DECIMAL(16,2) | 是 |  | 上一天商品实收金额 | 15.09 |
| dp_pay_amount_last_week | DECIMAL(16,2) | 是 |  | 上一周商品实收金额 | 0.00 |
| dp_pay_amount_last_year | DECIMAL(16,2) | 是 |  | 去年同期商品实收金额 | 4.40 |
| dp_discount_amount | DECIMAL(16,2) | 是 |  | 商品优惠金额 | 0.00 |
| dp_discount_amount_last_day | DECIMAL(16,2) | 是 |  | 上一天商品优惠金额 | 0.00 |
| dp_discount_amount_last_week | DECIMAL(16,2) | 是 |  | 上一周商品优惠金额 | 0.00 |
| dp_discount_amount_last_year | DECIMAL(16,2) | 是 |  | 去年同期商品优惠金额 | 0.00 |
| dp_return_item_count | BIGINT | 是 |  | 商品退货量 | 0 |
| dp_return_item_count_last_day | BIGINT | 是 |  | 上一天商品退货量 | 0 |
| dp_return_item_count_last_week | BIGINT | 是 |  | 上一周商品退货量 | 0 |
| dp_return_item_count_last_year | BIGINT | 是 |  | 去年同期商品退货量 | 0 |
| dp_return_total_amount | DECIMAL(16,2) | 是 |  | 商品退款金额 | 0.00 |
| dp_return_total_amount_last_day | DECIMAL(16,2) | 是 |  | 上一天商品退款金额 | 0.00 |
| dp_return_total_amount_last_week | DECIMAL(16,2) | 是 |  | 上一周商品退款金额 | 0.00 |
| dp_return_total_amount_last_year | DECIMAL(16,2) | 是 |  | 去年同期商品退款金额 | 0.00 |
| xl_total_amount | DECIMAL(16,2) | 是 |  | 小料流水金额 | 0.00 |
| xl_total_amount_last_day | DECIMAL(16,2) | 是 |  | 上一天小料流水金额 | 0.00 |
| xl_total_amount_last_week | DECIMAL(16,2) | 是 |  | 上一周小料流水金额 | 0.00 |
| xl_total_amount_last_year | DECIMAL(16,2) | 是 |  | 去年同期小料流水金额 | 0.00 |
| xl_item_count | BIGINT | 是 |  | 小料销量 | 0 |
| xl_item_count_last_day | BIGINT | 是 |  | 上一天小料销量 | 0 |
| xl_item_count_last_week | BIGINT | 是 |  | 上一周小料销量 | 0 |
| xl_item_count_last_year | BIGINT | 是 |  | 去年同期小料销量 | 0 |
| xl_pay_amount | DECIMAL(16,2) | 是 |  | 小料实收金额 | 0.00 |
| xl_pay_amount_last_day | DECIMAL(16,2) | 是 |  | 上一天小料实收金额 | 0.00 |
| xl_pay_amount_last_week | DECIMAL(16,2) | 是 |  | 上一周小料实收金额 | 0.00 |
| xl_pay_amount_last_year | DECIMAL(16,2) | 是 |  | 去年同期小料实收金额 | 0.00 |
| tc_total_amount | DECIMAL(16,2) | 是 |  | 套餐流水金额 | 0.00 |
| tc_total_amount_last_day | DECIMAL(16,2) | 是 |  | 上一天套餐流水金额 | 0.00 |
| tc_total_amount_last_week | DECIMAL(16,2) | 是 |  | 上一周套餐流水金额 | 0.00 |
| tc_total_amount_last_year | DECIMAL(16,2) | 是 |  | 去年同期套餐流水金额 | 0.00 |
| tc_item_count | BIGINT | 是 |  | 套餐销量 | 0 |
| tc_item_count_last_day | BIGINT | 是 |  | 上一天套餐销量 | 0 |
| tc_item_count_last_week | BIGINT | 是 |  | 上一周套餐销量 | 0 |
| tc_item_count_last_year | BIGINT | 是 |  | 去年同期套餐销量 | 0 |
| tc_pay_amount | DECIMAL(16,2) | 是 |  | 套餐实收金额 | 0.00 |
| tc_pay_amount_last_day | DECIMAL(16,2) | 是 |  | 上一天套餐实收金额 | 0.00 |
| tc_pay_amount_last_week | DECIMAL(16,2) | 是 |  | 上一周套餐实收金额 | 0.00 |
| tc_pay_amount_last_year | DECIMAL(16,2) | 是 |  | 去年同期套餐实收金额 | 0.00 |
| tc_discount_amount | DECIMAL(16,2) | 是 |  | 套餐优惠金额 | 0.00 |
| tc_discount_amount_last_day | DECIMAL(16,2) | 是 |  | 上一天套餐优惠金额 | 0.00 |
| tc_discount_amount_last_week | DECIMAL(16,2) | 是 |  | 上一周套餐优惠金额 | 0.00 |
| tc_discount_amount_last_year | DECIMAL(16,2) | 是 |  | 去年同期套餐优惠金额 | 0.00 |
| zb_total_amount | DECIMAL(16,2) | 是 |  | 周边流水金额 | 0.00 |
| zb_total_amount_last_day | DECIMAL(16,2) | 是 |  | 上一天周边流水金额 | 0.00 |
| zb_total_amount_last_week | DECIMAL(16,2) | 是 |  | 上一周周边流水金额 | 0.00 |
| zb_total_amount_last_year | DECIMAL(16,2) | 是 |  | 去年同期周边流水金额 | 0.00 |
| zb_item_count | BIGINT | 是 |  | 周边销量 | 0 |
| zb_item_count_last_day | BIGINT | 是 |  | 上一天周边销量 | 0 |
| zb_item_count_last_week | BIGINT | 是 |  | 上一周周边销量 | 0 |
| zb_item_count_last_year | BIGINT | 是 |  | 去年同期周边销量 | 0 |
| zb_pay_amount | DECIMAL(16,2) | 是 |  | 周边实收金额 | 0.00 |
| zb_pay_amount_last_day | DECIMAL(16,2) | 是 |  | 上一天周边实收金额 | 0.00 |
| zb_pay_amount_last_week | DECIMAL(16,2) | 是 |  | 上一周周边实收金额 | 0.00 |
| zb_pay_amount_last_year | DECIMAL(16,2) | 是 |  | 去年同期周边实收金额 | 0.00 |
| load_time | VARCHAR(64) | 是 |  | 数据更新时间 | 2024-11-20 16:27:51 |
| item_type | VARCHAR(64) | 是 |  | 商品类型（单品、套餐、小料、周边、其它） | 单品 |
| item_status | VARCHAR(64) | 是 |  | 饮品状态(在线饮品、不在线饮品) | 其它 |
| up_type | VARCHAR(64) | 是 |  | 升级类型 |  |
| food_series | VARCHAR(64) | 是 |  | 商品系列 | 其它 |
| release_date | VARCHAR(64) | 是 |  | 上新日期 | 其它 |
| dp_order_count | BIGINT | 是 |  | 商品订单量 | 0 |
| xl_order_count | BIGINT | 是 |  | 小料订单量 | 0 |
| item_name_list | VARCHAR(255) | 是 |  | 套餐下商品/小料明细 |  |
| other_total_amount | DECIMAL(16,2) | 是 |  | 其它饮品流水金额 | 0.00 |
| other_total_amount_last_day | DECIMAL(16,2) | 是 |  | 昨日其它饮品流水金额 | 0.00 |
| other_total_amount_last_week | DECIMAL(16,2) | 是 |  | 上周同期其它饮品流水金额 | 0.00 |
| other_total_amount_last_year | DECIMAL(16,2) | 是 |  | 去年同期其它饮品流水金额 | 0.00 |
| stat_shop_id | VARCHAR(64) | 是 |  | 门店统计id | TLL02082 |
| stat_shop_name | VARCHAR(255) | 是 |  | 门店统计名称 | 新疆石河子天富康城店 |
| send_whse | VARCHAR(64) | 是 |  | 仓库 | 郑州仓 |
