# dim_sup_srm_goods_df

## 表描述
OLAP

## 数据量
- 总记录数：582 条

## 字段信息

| 字段名称 | 数据类型 | 是否可空 | 默认值 | 字段描述 | 示例 |
|---------|----------|----------|--------|----------|------|
| id | BIGINT | 是 |  | 主键ID | 860561445274852353 |
| goods_name | VARCHAR(255) | 是 |  | 商品名称 | 焦糖QQ粉-10kg*2包/件 |
| goods_code | VARCHAR(255) | 是 |  | 商品编码 | 030001006 |
| specs | VARCHAR(255) | 是 |  | 规格 | 3kg*8包/件 |
| unit | VARCHAR(255) | 是 |  | 单位 | BAG |
| default_price | DECIMAL(10,2) | 是 |  | 默认价格 | 710.00 |
| status | INT | 是 |  | 状态（0：停用，1：启用） | 1 |
| area_price_status | INT | 是 |  | 区域价格状态（0：未设置，1：已设置） | 0 |
| area_sell_status | INT | 是 |  | 区域售卖状态（0：未设置，1：已设置） | 0 |
| up_down_status | INT | 是 |  | 上下架状态（0：未设置，1：已设置） | 1 |
| goods_category | VARCHAR(255) | 是 |  | 商品品类 | 402 |
| goods_classify | INT | 是 |  | 商品分类(0:常规商品，1：组合商品, 2:BOM组合商品) | 0 |
| goods_type | VARCHAR(255) | 是 |  | 商品类型（10：实物类商品，30:虚拟商品,20:服务类商品） | 10 |
| creator | VARCHAR(255) | 是 |  | 创建人 | 杜爱静 |
| updater | VARCHAR(255) | 是 |  | 修改人 | 毕为为 |
| create_time | VARCHAR(255) | 是 |  | 创建时间 | 2024-08-29 14:56:55 |
| modify_time | VARCHAR(255) | 是 |  | 修改时间 | 2024-12-08 16:29:52 |
| spu_code | VARCHAR(255) | 是 |  | SPU编码 | 020000013 |
| spu_name | VARCHAR(555) | 是 |  | SPU名字 | 花涧幽兰(茉莉)-50g*100包/箱 |
| delete_flag | INT | 是 |  | 是否删除（0：否 1：是） | 0 |
| make_goods | INT | 是 |  | 是否组装商品（0：否 1：是） | 0 |
| organization | VARCHAR(255) | 是 |  | 组织 | 1000 |
| tenant_id | BIGINT | 是 |  | 租户ID | 854339203348044495 |
| belong_org_id | BIGINT | 是 |  | 所属组织ID | 857617200679225855 |
| tenant_org_id | BIGINT | 是 |  | 租户组织ID |  |
| remark | VARCHAR(255) | 是 |  | 备注 |  |
| create_user_id | BIGINT | 是 |  | 记录创建者ID | 0 |
| modify_user_id | BIGINT | 是 |  | 记录最后更新者ID | 860479005101395717 |
| audit_data_version | INT | 是 |  | 锁版本 |  |
| sec_bu_id | BIGINT | 是 |  | 数据归属组织id |  |
| sec_user_id | BIGINT | 是 |  | 数据归属雇员id |  |
| sec_ou_id | BIGINT | 是 |  | 数据归属公司id |  |
| pid | BIGINT | 是 |  | 上级ID |  |
| sub_item_code | VARCHAR(255) | 是 |  | 子件商品编码 | 120001151,120000106,120000069,120000031 |
| product_type | VARCHAR(255) | 是 |  | 商品类型 | PT |
| guarantee_days | VARCHAR(255) | 是 |  | 保质期时长 | 9999 |
| guarantee_period_unit | VARCHAR(255) | 是 |  | 保质期单位 | DAY |

## 使用说明

### 常用查询示例

```sql
-- 查询最新数据
SELECT * FROM dim_sup_srm_goods_df 
ORDER BY business_date DESC 
LIMIT 10;

-- 查询数据总量
SELECT COUNT(*) FROM dim_sup_srm_goods_df;

-- 查询某日数据
SELECT * FROM dim_sup_srm_goods_df 
WHERE business_date = 20240101;
```

### 注意事项
- 时间字段通常为bigint类型，格式为YYYYMMDD
- 金额字段单位为分，需要除以100转换为元
- 字符类型字段需要注意大小写敏感问题
