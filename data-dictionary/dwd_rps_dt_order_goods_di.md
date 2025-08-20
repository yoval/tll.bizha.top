# dwd_rps_dt_order_goods_di

## 表描述
OLAP

## 数据量
- 总记录数：7,789,204 条

## 字段信息

| 字段名称 | 数据类型 | 是否可空 | 默认值 | 字段描述 | 示例 |
|---------|----------|----------|--------|----------|------|
| id | INT | 是 |  | 自增ID | 3 |
| order_id | INT | 是 |  | 订单ID | 100019 |
| order_no | VARCHAR(255) | 是 |  | 订单编码 | XCD00000000009 |
| sortId | INT | 是 |  | 序号 | 1 |
| article_id | INT | 是 |  | 文章ID | 100710 |
| goods_no | VARCHAR(255) | 是 |  | 商品货号 | 120001047 |
| goods_title | VARCHAR(255) | 是 |  | 商品标题 | 端午限定杯套 |
| goods_price | DECIMAL(14,3) | 是 |  | 商品价格 | 85.000 |
| real_price | DECIMAL(14,3) | 是 |  | 实际标题 | 85.000 |
| quantity | DECIMAL(14,2) | 是 |  | 数量 | 1.00 |
| taxAmount | DECIMAL(14,3) | 是 |  | 实际金额 | 0.100 |
| point | INT | 是 |  | 积分 | 0 |
| discount | INT | 是 |  | 折扣金额 | 100 |
| derate | DECIMAL(14,2) | 是 |  | 利率 | 0.00 |
| fabh | VARCHAR(255) | 是 |  | fabh |  |
| cxbs | VARCHAR(255) | 是 |  | cxbs |  |
| decaribe | VARCHAR(255) | 是 |  | 描述 |  |
| entid | VARCHAR(255) | 是 |  | 企业代码 | E26FMM0XNYQ |
| IsCriticism | VARCHAR(255) | 是 |  | 是否评论 | N  |
| PromScenario | VARCHAR(255) | 是 |  | PromScenario |       |
| Status | INT | 是 |  | 状态 | 0 |
| ReturnNum | DECIMAL(14,2) | 是 |  | 退货数量 | 0.00 |
| PiHao | VARCHAR(255) | 是 |  | PiHao | 包邮 |
| timestamps | VARCHAR(255) | 是 |  | 创建时间 | 2023-06-14 17:23:11 |
| erp_orderno | VARCHAR(255) | 是 |  | U8C订单编号 | SO2107010001 |
| erp_orderno_return | VARCHAR(255) | 是 |  | U8C退单编号 | SO24010500102 |
| storcode | VARCHAR(255) | 是 |  | 仓库编码 | 1001F8100000000001IZ |
| storname | VARCHAR(255) | 是 |  | 仓库名称 | 蚌埠快递仓（原天津仓） |
| updatetime | VARCHAR(255) | 是 |  | 审核时间 | 2023-06-15 13:30:16 |
| data_source | INT | 是 |  | 数据源类型 | 2 |
| pt | VARCHAR(255) | 是 |  | 天分区 | 20230614 |

## 使用说明

### 常用查询示例

```sql
-- 查询最新数据
SELECT * FROM dwd_rps_dt_order_goods_di 
ORDER BY business_date DESC 
LIMIT 10;

-- 查询数据总量
SELECT COUNT(*) FROM dwd_rps_dt_order_goods_di;

-- 查询某日数据
SELECT * FROM dwd_rps_dt_order_goods_di 
WHERE business_date = 20240101;
```

### 注意事项
- 时间字段通常为bigint类型，格式为YYYYMMDD
- 金额字段单位为分，需要除以100转换为元
- 字符类型字段需要注意大小写敏感问题
