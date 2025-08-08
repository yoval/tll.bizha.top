# 数据字典总览

本文档包含了tll_bi_dw数据库中所有核心数据表的详细说明。

## 📊 数据表列表

### 汇总层表 (ADS - Application Data Service)

| 表名 | 描述 | 数据量 | 更新时间 |
|------|------|--------|----------|
| [ads_dbs_trade_food_di](./ads_dbs_trade_food_di.md) | 食品交易汇总 | 待补充 | 实时更新 |
| [ads_dbs_trade_shop_di](./ads_dbs_trade_shop_di.md) | 门店交易汇总 | 33,076,418 条 | 实时更新 |
| [ads_dbs_trade_shop_pay_channel_di](./ads_dbs_trade_shop_pay_channel_di.md) | 门店支付渠道汇总 | 待补充 | 实时更新 |
| [ads_fin_bom_dish_cost_df](./ads_fin_bom_dish_cost_df.md) | 菜品BOM成本表 | 12,832 条 | 每日更新 |
| [ads_fin_fee_bx_detail_di](./ads_fin_fee_bx_detail_di.md) | 费用报销明细汇总 | 待补充 | 实时更新 |
| [ads_fin_finance_paid_di](./ads_fin_finance_paid_di.md) | 财务付款汇总 | 15,783 条 | 每日更新 |
| [ads_fin_shop_item_consume_di](./ads_fin_shop_item_consume_di.md) | 门店物料消耗汇总 | 18,947,835 条 | 每日更新 |
| [ads_mkt_fines_summary_df](./ads_mkt_fines_summary_df.md) | 市场罚款汇总 | 待补充 | 实时更新 |

### 明细层表 (DWD - Data Warehouse Detail)

| 表名 | 描述 | 数据量 | 更新时间 |
|------|------|--------|----------|
| [dwd_rps_dt_order_goods_di](./dwd_rps_dt_order_goods_di.md) | 订单商品明细 | 待补充 | 实时更新 |
| [dwd_rps_dt_orders_di](./dwd_rps_dt_orders_di.md) | 订单明细 | 待补充 | 实时更新 |
| [dwd_rps_tll_order_cancel_df](./dwd_rps_tll_order_cancel_df.md) | 订单取消明细 | 待补充 | 实时更新 |
| [dwd_rps_tll_order_cancel_product_df](./dwd_rps_tll_order_cancel_product_df.md) | 订单取消商品明细 | 待补充 | 实时更新 |
| [dwd_rps_tll_order_details_di](./dwd_rps_tll_order_details_di.md) | 订单详情明细 | 待补充 | 实时更新 |
| [dwd_rps_tll_order_di](./dwd_rps_tll_order_di.md) | 订单主表明细 | 47,702 条 | 实时更新 |
| [dwd_spc_report_sales_di](./dwd_spc_report_sales_di.md) | 销售报表明细 | 待补充 | 实时更新 |

### 维度层表 (DIM - Dimension)

| 表名 | 描述 | 数据量 | 更新时间 |
|------|------|--------|----------|
| [dim_oas_formmain_0145_all_df](./dim_oas_formmain_0145_all_df.md) | OA表单维度 | 待补充 | 每日更新 |
| [dim_sup_srm_goods_df](./dim_sup_srm_goods_df.md) | 商品维度 | 待补充 | 每日更新 |

### 服务层表 (DWS - Data Warehouse Service)

| 表名 | 描述 | 数据量 | 更新时间 |
|------|------|--------|----------|
| [dws_trd_mtpos_order_pay_channel_details_di](./dws_trd_mtpos_order_pay_channel_details_di.md) | 美团POS订单支付渠道详情 | 待补充 | 实时更新 |

### Flink实时流表

| 表名 | 描述 | 数据量 | 更新时间 |
|------|------|--------|----------|
| [flink_rps_all_new_tll_order_details_now_day_df](./flink_rps_all_new_tll_order_details_now_day_df.md) | 实时订单详情 | 待补充 | 实时更新 |
| [flink_rps_all_new_tll_order_now_day_df](./flink_rps_all_new_tll_order_now_day_df.md) | 实时订单主表 | 待补充 | 实时更新 |
| [flink_rps_tll_presale_order_details_df](./flink_rps_tll_presale_order_details_df.md) | 预售订单详情 | 待补充 | 实时更新 |
| [flink_rps_tll_presale_order_df](./flink_rps_tll_presale_order_df.md) | 预售订单主表 | 待补充 | 实时更新 |

### 补充数据表

| 表名 | 描述 | 数据量 | 更新时间 |
|------|------|--------|----------|
| [imp_online_new_channel_supplement](./imp_online_new_channel_supplement.md) | 线上渠道补充数据 | 待补充 | 每日更新 |

## 🔍 使用指南

### 表命名规则
- **ads_** : 应用数据服务层，面向业务的汇总数据
- **dwd_** : 明细数据层，保存最细粒度的业务数据
- **dim_** : 维度数据层，保存业务维度信息
- **dws_** : 服务数据层，面向分析的汇总数据
- **flink_** : 实时流计算表

### 字段类型说明
- **BIGINT** : 长整型，通常用于存储时间、数量等
- **DECIMAL(p,s)** : 精确小数，用于存储金额等需要精确计算的数据
- **VARCHAR(n)** : 可变长度字符串，n为最大长度
- **INT** : 整型
- **DATE** : 日期类型

### 常用查询模板

#### 1. 查询某日数据
```sql
SELECT * FROM 表名 
WHERE business_date = 20240101;
```

#### 2. 查询最新数据
```sql
SELECT * FROM 表名 
ORDER BY business_date DESC 
LIMIT 10;
```

#### 3. 查询数据量
```sql
SELECT COUNT(*) FROM 表名;
```

#### 4. 查询某时间段数据
```sql
SELECT * FROM 表名 
WHERE business_date BETWEEN 20240101 AND 20240131;
```

### 注意事项

1. **时间格式**：所有时间字段均为BIGINT类型，格式为YYYYMMDD
2. **分区字段**：大部分表都有pt分区字段，表示数据分区
3. **字符大小写**：字符类型字段查询时需注意大小写敏感问题
4. **数据更新频率**：
   - 实时表：分钟级更新
   - 日汇总表：每日凌晨更新
   - 维度表：每日更新

## 🚀 快速开始

1. **查看表结构**：点击表名链接查看详细字段说明
2. **了解业务含义**：查看每个字段的业务描述和取值说明
3. **参考查询示例**：每个表都提供了常用查询SQL示例
4. **注意数据质量**：查看每个表的注意事项和最佳实践