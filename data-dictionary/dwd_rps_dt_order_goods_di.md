# dwd_rps_dt_order_goods_di

## 表描述
OLAP

## 数据量
- 总记录数：7,789,204 条

## 字段信息

| 字段名称 | 数据类型 | 是否可空 | 默认值 | 字段描述 |
|---------|----------|----------|--------|----------|
| id | INT | 是 |  | 自增ID |
| order_id | INT | 是 |  | 订单ID |
| order_no | VARCHAR(255) | 是 |  | 订单编码 |
| sortId | INT | 是 |  | 序号 |
| article_id | INT | 是 |  | 文章ID |
| goods_no | VARCHAR(255) | 是 |  | 商品货号 |
| goods_title | VARCHAR(255) | 是 |  | 商品标题 |
| goods_price | DECIMAL(14,3) | 是 |  | 商品价格 |
| real_price | DECIMAL(14,3) | 是 |  | 实际标题 |
| quantity | DECIMAL(14,2) | 是 |  | 数量 |
| taxAmount | DECIMAL(14,3) | 是 |  | 实际金额 |
| point | INT | 是 |  | 积分 |
| discount | INT | 是 |  | 折扣金额 |
| derate | DECIMAL(14,2) | 是 |  | 利率 |
| fabh | VARCHAR(255) | 是 |  | fabh |
| cxbs | VARCHAR(255) | 是 |  | cxbs |
| decaribe | VARCHAR(255) | 是 |  | 描述 |
| entid | VARCHAR(255) | 是 |  | 企业代码 |
| IsCriticism | VARCHAR(255) | 是 |  | 是否评论 |
| PromScenario | VARCHAR(255) | 是 |  | PromScenario |
| Status | INT | 是 |  | 状态 |
| ReturnNum | DECIMAL(14,2) | 是 |  | 退货数量 |
| PiHao | VARCHAR(255) | 是 |  | PiHao |
| timestamps | VARCHAR(255) | 是 |  | 创建时间 |
| erp_orderno | VARCHAR(255) | 是 |  | U8C订单编号 |
| erp_orderno_return | VARCHAR(255) | 是 |  | U8C退单编号 |
| storcode | VARCHAR(255) | 是 |  | 仓库编码 |
| storname | VARCHAR(255) | 是 |  | 仓库名称 |
| updatetime | VARCHAR(255) | 是 |  | 审核时间 |
| data_source | INT | 是 |  | 数据源类型 |
| pt | VARCHAR(255) | 是 |  | 天分区 |

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
