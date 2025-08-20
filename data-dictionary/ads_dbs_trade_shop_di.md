# ads_dbs_trade_shop_di

## 表描述
OLAP

## 数据量
- 总记录数：33,763,549 条

## 字段信息

| 字段名称 | 数据类型 | 是否可空 | 默认值 | 字段描述 | 示例 |
|---------|----------|----------|--------|----------|------|
| business_date | BIGINT | 是 |  | 日期 | 20230106 |
| oper_center_name | VARCHAR(255) | 是 |  | 营运中心 | 全部 |
| prov_id | VARCHAR(255) | 是 |  | 省份编码 | 650000 |
| prov_name | VARCHAR(255) | 是 |  | 省份名称 | 新疆维吾尔自治区 |
| city_id | VARCHAR(255) | 是 |  | 城市编码 | 其它 |
| city_name | VARCHAR(255) | 是 |  | 城市名称 | 其它 |
| city_level | VARCHAR(255) | 是 |  | 城市等级 | 其它 |
| district_id | VARCHAR(255) | 是 |  | 区县编码 | 659002 |
| district_name | VARCHAR(255) | 是 |  | 区县名称 | 阿拉尔市 |
| busi_area_type | VARCHAR(255) | 是 |  | 商圈 | 普通沿街商铺店 |
| bussiness_type | VARCHAR(255) | 是 |  | 业务类型 | 堂食 |
| anal_type | VARCHAR(255) | 是 |  | 分析类型:到家、到店 | 到店 |
| platform | VARCHAR(255) | 是 |  | 平台:到家：美团、饿了么、其它 到店：POS、小程序、其它 | pos |
| stat_shop_id | VARCHAR(255) | 是 |  | 门店统计id | TLL04998 |
| stat_shop_name | VARCHAR(255) | 是 |  | 门店统计名称 | 胡杨河商业街店 |
| total_amount | DECIMAL(16,2) | 是 |  | 流水金额 | 290.00 |
| total_amount_last_day | DECIMAL(16,2) | 是 |  | 上一天流水金额 | 238.50 |
| total_amount_last_week | DECIMAL(16,2) | 是 |  | 上一周流水金额 | 0.00 |
| total_amount_last_year | DECIMAL(16,2) | 是 |  | 去年同期流水金额 | 0.00 |
| pay_amount | DECIMAL(16,2) | 是 |  | 实收金额 | 14.38 |
| pay_amount_last_day | DECIMAL(16,2) | 是 |  | 上一天实收金额 | 0.00 |
| pay_amount_last_week | DECIMAL(16,2) | 是 |  | 上一周实收金额 | 19.78 |
| pay_amount_last_year | DECIMAL(16,2) | 是 |  | 去年同期实收金额 | 0.00 |
| order_count | BIGINT | 是 |  | 订单量 | 15 |
| order_count_last_day | BIGINT | 是 |  | 上一天订单量 | 0 |
| order_count_last_week | BIGINT | 是 |  | 上一周订单量 | 1 |
| order_count_last_year | BIGINT | 是 |  | 去年同期订单量 | 0 |
| is_trd_shop | BIGINT | 是 |  | 是否交易门店 | 1 |
| is_trd_shop_last_day | BIGINT | 是 |  | 上一天是否交易门店 | 1 |
| is_trd_shop_last_week | BIGINT | 是 |  | 上一周是否交易门店 | 1 |
| is_trd_shop_last_year | BIGINT | 是 |  | 去年同期是否交易门店 | 0 |
| discount_amount | DECIMAL(16,2) | 是 |  | 优惠金额 | 7.14 |
| discount_amount_last_day | DECIMAL(16,2) | 是 |  | 上一天优惠金额 | 0.00 |
| discount_amount_last_week | DECIMAL(16,2) | 是 |  | 上一周优惠金额 | 0.00 |
| discount_amount_last_year | DECIMAL(16,2) | 是 |  | 去年同期优惠金额 | 0.00 |
| dp_item_count | BIGINT | 是 |  | 商品销量 | 3 |
| dp_item_count_last_day | BIGINT | 是 |  | 上一天商品销量 | 20 |
| dp_item_count_last_week | BIGINT | 是 |  | 上一周商品销量 | 2 |
| dp_item_count_last_year | BIGINT | 是 |  | 去年同期商品销量 | 0 |
| dp_total_amount | DECIMAL(16,2) | 是 |  | 商品流水金额 | 12.74 |
| dp_total_amount_last_day | DECIMAL(16,2) | 是 |  | 上一天商品流水金额 | 0.00 |
| dp_total_amount_last_week | DECIMAL(16,2) | 是 |  | 上一周商品流水金额 | 317.00 |
| dp_total_amount_last_year | DECIMAL(16,2) | 是 |  | 去年同期商品流水金额 | 0.00 |
| return_order_count | BIGINT | 是 |  | 退款订单量 | 0 |
| return_order_count_last_day | BIGINT | 是 |  | 上一天退款订单量 | 1 |
| return_order_count_last_week | BIGINT | 是 |  | 上一周退款订单量 | 0 |
| return_order_count_last_year | BIGINT | 是 |  | 去年同期退款订单量 | 0 |
| return_total_amount | DECIMAL(16,2) | 是 |  | 退款金额 | 0.00 |
| return_total_amount_last_day | DECIMAL(16,2) | 是 |  | 上一天退款金额 | 0.00 |
| return_total_amount_last_week | DECIMAL(16,2) | 是 |  | 上一周退款金额 | 0.00 |
| return_total_amount_last_year | DECIMAL(16,2) | 是 |  | 去年同期退款金额 | 0.00 |
| load_time | VARCHAR(255) | 是 |  | 数据更新时间 | 2024-11-20 16:15:39 |
| is_dj_sold_shop | BIGINT | 是 |  | 是否有外卖业绩门店 | 1 |
| is_dj_sold_shop_last_day | BIGINT | 是 |  | 上一天是否有外卖业绩门店 | 1 |
| is_dj_sold_shop_last_week | BIGINT | 是 |  | 上一周是否有外卖业绩门店 | 0 |
| is_dj_sold_shop_last_year | BIGINT | 是 |  | 去年同期是否有外卖业绩门店 | 0 |
| is_wechat_community | VARCHAR(100) | 是 |  | 是否微信社群用户 |  |
| is_sign | VARCHAR(100) | 是 |  | 是否签约 |  |
| franchisee_type | VARCHAR(255) | 是 |  | 加盟商类型：直营、加盟 | 加盟店 |
| is_doubt_shop | BIGINT | 是 |  | 是否存疑门店 | 0 |
| up_1_order_count | BIGINT | 是 |  | 2杯及以上订单量 | 11 |
| up_1_order_count_last_day | BIGINT | 是 |  | 上一天2杯及以上订单量 | 9 |
| up_1_order_count_last_week | BIGINT | 是 |  | 上周同期2杯及以上订单量 | 0 |
| up_1_order_count_last_year | BIGINT | 是 |  | 去年同期2杯及以上订单量 | 0 |
| time_name | VARCHAR(255) | 是 |  | 时段 | 午餐 |
| channel_name | VARCHAR(255) | 是 |  | 渠道 | pos |
| report_amount | DECIMAL(16,2) | 是 |  | 报货金额 |  |
| report_amount_last_day | DECIMAL(16,2) | 是 |  | 上一天报货金额 |  |
| report_amount_last_week | DECIMAL(16,2) | 是 |  | 上周同期报货金额 |  |
| report_amount_last_year | DECIMAL(16,2) | 是 |  | 去年同期报货金额 |  |

## 使用说明

### 常用查询示例

```sql
-- 查询最新数据
SELECT * FROM ads_dbs_trade_shop_di 
ORDER BY business_date DESC 
LIMIT 10;

-- 查询数据总量
SELECT COUNT(*) FROM ads_dbs_trade_shop_di;

-- 查询某日数据
SELECT * FROM ads_dbs_trade_shop_di 
WHERE business_date = 20240101;
```

### 注意事项
- 时间字段通常为bigint类型，格式为YYYYMMDD
- 金额字段单位为分，需要除以100转换为元
- 字符类型字段需要注意大小写敏感问题
