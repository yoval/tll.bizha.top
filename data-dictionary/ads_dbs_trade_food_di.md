# ads_dbs_trade_food_di

## 表描述
OLAP

## 数据量
- 总记录数：1,029,642,953 条

## 字段信息

| 字段名称 | 数据类型 | 是否可空 | 默认值 | 字段描述 |
|---------|----------|----------|--------|----------|
| business_date | BIGINT | 是 |  | 日期 |
| oper_center_name | VARCHAR(255) | 是 |  | 营运中心 |
| prov_id | VARCHAR(64) | 是 |  | 省份编码 |
| prov_name | VARCHAR(255) | 是 |  | 省份名称 |
| city_id | VARCHAR(64) | 是 |  | 城市编码 |
| city_name | VARCHAR(255) | 是 |  | 城市名称 |
| city_level | VARCHAR(64) | 是 |  | 城市等级 |
| district_id | VARCHAR(64) | 是 |  | 区县编码 |
| district_name | VARCHAR(255) | 是 |  | 区县名称 |
| busi_area_type | VARCHAR(64) | 是 |  | 商圈 |
| bussiness_type | VARCHAR(64) | 是 |  | 业务类型 |
| channel_name | VARCHAR(255) | 是 |  | 订单渠道 |
| anal_type | VARCHAR(64) | 是 |  | 分析类型(到家、到店) |
| platform | VARCHAR(64) | 是 |  | 平台(到家：美团、饿了么、其它 到店：POS、小程序、其它) |
| cust_type | VARCHAR(64) | 是 |  | 用户类型 |
| time_name | VARCHAR(255) | 是 |  | 时段 |
| food_category_name | VARCHAR(255) | 是 |  | 商品分类 |
| food_oneid | VARCHAR(64) | 是 |  | 商品oneid |
| item_name | VARCHAR(500) | 是 |  | 商品名称 |
| new_flag | VARCHAR(64) | 是 |  | 是否新品 |
| cup_type | VARCHAR(64) | 是 |  | 杯型 |
| ice_type | VARCHAR(64) | 是 |  | 温度 |
| sugar_type | VARCHAR(64) | 是 |  | 甜度 |
| dp_total_amount | DECIMAL(16,2) | 是 |  | 商品流水金额 |
| dp_total_amount_last_day | DECIMAL(16,2) | 是 |  | 上一天商品流水金额 |
| dp_total_amount_last_week | DECIMAL(16,2) | 是 |  | 上一周商品流水金额 |
| dp_total_amount_last_year | DECIMAL(16,2) | 是 |  | 去年同期商品流水金额 |
| dp_item_count | BIGINT | 是 |  | 商品销量 |
| dp_item_count_last_day | BIGINT | 是 |  | 上一天商品销量 |
| dp_item_count_last_week | BIGINT | 是 |  | 上一周商品销量 |
| dp_item_count_last_year | BIGINT | 是 |  | 去年同期商品销量 |
| dp_pay_amount | DECIMAL(16,2) | 是 |  | 商品实收金额 |
| dp_pay_amount_last_day | DECIMAL(16,2) | 是 |  | 上一天商品实收金额 |
| dp_pay_amount_last_week | DECIMAL(16,2) | 是 |  | 上一周商品实收金额 |
| dp_pay_amount_last_year | DECIMAL(16,2) | 是 |  | 去年同期商品实收金额 |
| dp_discount_amount | DECIMAL(16,2) | 是 |  | 商品优惠金额 |
| dp_discount_amount_last_day | DECIMAL(16,2) | 是 |  | 上一天商品优惠金额 |
| dp_discount_amount_last_week | DECIMAL(16,2) | 是 |  | 上一周商品优惠金额 |
| dp_discount_amount_last_year | DECIMAL(16,2) | 是 |  | 去年同期商品优惠金额 |
| dp_return_item_count | BIGINT | 是 |  | 商品退货量 |
| dp_return_item_count_last_day | BIGINT | 是 |  | 上一天商品退货量 |
| dp_return_item_count_last_week | BIGINT | 是 |  | 上一周商品退货量 |
| dp_return_item_count_last_year | BIGINT | 是 |  | 去年同期商品退货量 |
| dp_return_total_amount | DECIMAL(16,2) | 是 |  | 商品退款金额 |
| dp_return_total_amount_last_day | DECIMAL(16,2) | 是 |  | 上一天商品退款金额 |
| dp_return_total_amount_last_week | DECIMAL(16,2) | 是 |  | 上一周商品退款金额 |
| dp_return_total_amount_last_year | DECIMAL(16,2) | 是 |  | 去年同期商品退款金额 |
| xl_total_amount | DECIMAL(16,2) | 是 |  | 小料流水金额 |
| xl_total_amount_last_day | DECIMAL(16,2) | 是 |  | 上一天小料流水金额 |
| xl_total_amount_last_week | DECIMAL(16,2) | 是 |  | 上一周小料流水金额 |
| xl_total_amount_last_year | DECIMAL(16,2) | 是 |  | 去年同期小料流水金额 |
| xl_item_count | BIGINT | 是 |  | 小料销量 |
| xl_item_count_last_day | BIGINT | 是 |  | 上一天小料销量 |
| xl_item_count_last_week | BIGINT | 是 |  | 上一周小料销量 |
| xl_item_count_last_year | BIGINT | 是 |  | 去年同期小料销量 |
| xl_pay_amount | DECIMAL(16,2) | 是 |  | 小料实收金额 |
| xl_pay_amount_last_day | DECIMAL(16,2) | 是 |  | 上一天小料实收金额 |
| xl_pay_amount_last_week | DECIMAL(16,2) | 是 |  | 上一周小料实收金额 |
| xl_pay_amount_last_year | DECIMAL(16,2) | 是 |  | 去年同期小料实收金额 |
| tc_total_amount | DECIMAL(16,2) | 是 |  | 套餐流水金额 |
| tc_total_amount_last_day | DECIMAL(16,2) | 是 |  | 上一天套餐流水金额 |
| tc_total_amount_last_week | DECIMAL(16,2) | 是 |  | 上一周套餐流水金额 |
| tc_total_amount_last_year | DECIMAL(16,2) | 是 |  | 去年同期套餐流水金额 |
| tc_item_count | BIGINT | 是 |  | 套餐销量 |
| tc_item_count_last_day | BIGINT | 是 |  | 上一天套餐销量 |
| tc_item_count_last_week | BIGINT | 是 |  | 上一周套餐销量 |
| tc_item_count_last_year | BIGINT | 是 |  | 去年同期套餐销量 |
| tc_pay_amount | DECIMAL(16,2) | 是 |  | 套餐实收金额 |
| tc_pay_amount_last_day | DECIMAL(16,2) | 是 |  | 上一天套餐实收金额 |
| tc_pay_amount_last_week | DECIMAL(16,2) | 是 |  | 上一周套餐实收金额 |
| tc_pay_amount_last_year | DECIMAL(16,2) | 是 |  | 去年同期套餐实收金额 |
| tc_discount_amount | DECIMAL(16,2) | 是 |  | 套餐优惠金额 |
| tc_discount_amount_last_day | DECIMAL(16,2) | 是 |  | 上一天套餐优惠金额 |
| tc_discount_amount_last_week | DECIMAL(16,2) | 是 |  | 上一周套餐优惠金额 |
| tc_discount_amount_last_year | DECIMAL(16,2) | 是 |  | 去年同期套餐优惠金额 |
| zb_total_amount | DECIMAL(16,2) | 是 |  | 周边流水金额 |
| zb_total_amount_last_day | DECIMAL(16,2) | 是 |  | 上一天周边流水金额 |
| zb_total_amount_last_week | DECIMAL(16,2) | 是 |  | 上一周周边流水金额 |
| zb_total_amount_last_year | DECIMAL(16,2) | 是 |  | 去年同期周边流水金额 |
| zb_item_count | BIGINT | 是 |  | 周边销量 |
| zb_item_count_last_day | BIGINT | 是 |  | 上一天周边销量 |
| zb_item_count_last_week | BIGINT | 是 |  | 上一周周边销量 |
| zb_item_count_last_year | BIGINT | 是 |  | 去年同期周边销量 |
| zb_pay_amount | DECIMAL(16,2) | 是 |  | 周边实收金额 |
| zb_pay_amount_last_day | DECIMAL(16,2) | 是 |  | 上一天周边实收金额 |
| zb_pay_amount_last_week | DECIMAL(16,2) | 是 |  | 上一周周边实收金额 |
| zb_pay_amount_last_year | DECIMAL(16,2) | 是 |  | 去年同期周边实收金额 |
| load_time | VARCHAR(64) | 是 |  | 数据更新时间 |
| item_type | VARCHAR(64) | 是 |  | 商品类型（单品、套餐、小料、周边、其它） |
| item_status | VARCHAR(64) | 是 |  | 饮品状态(在线饮品、不在线饮品) |
| up_type | VARCHAR(64) | 是 |  | 升级类型 |
| food_series | VARCHAR(64) | 是 |  | 商品系列 |
| release_date | VARCHAR(64) | 是 |  | 上新日期 |
| dp_order_count | BIGINT | 是 |  | 商品订单量 |
| xl_order_count | BIGINT | 是 |  | 小料订单量 |
| item_name_list | VARCHAR(255) | 是 |  | 套餐下商品/小料明细 |
| other_total_amount | DECIMAL(16,2) | 是 |  | 其它饮品流水金额 |
| other_total_amount_last_day | DECIMAL(16,2) | 是 |  | 昨日其它饮品流水金额 |
| other_total_amount_last_week | DECIMAL(16,2) | 是 |  | 上周同期其它饮品流水金额 |
| other_total_amount_last_year | DECIMAL(16,2) | 是 |  | 去年同期其它饮品流水金额 |
| stat_shop_id | VARCHAR(64) | 是 |  | 门店统计id |
| stat_shop_name | VARCHAR(255) | 是 |  | 门店统计名称 |
| send_whse | VARCHAR(64) | 是 |  | 仓库 |

## 使用说明

### 常用查询示例

```sql
-- 查询最新数据
SELECT * FROM ads_dbs_trade_food_di 
ORDER BY business_date DESC 
LIMIT 10;

-- 查询数据总量
SELECT COUNT(*) FROM ads_dbs_trade_food_di;

-- 查询某日数据
SELECT * FROM ads_dbs_trade_food_di 
WHERE business_date = 20240101;
```

### 注意事项
- 时间字段通常为bigint类型，格式为YYYYMMDD
- 金额字段单位为分，需要除以100转换为元
- 字符类型字段需要注意大小写敏感问题
