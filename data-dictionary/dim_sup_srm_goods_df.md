# dim_sup_srm_goods_df

## 表描述
OLAP

## 数据量
- 总记录数：576 条

## 字段信息

| 字段名称 | 数据类型 | 是否可空 | 默认值 | 字段描述 |
|---------|----------|----------|--------|----------|
| id | BIGINT | 是 |  | 主键ID |
| goods_name | VARCHAR(255) | 是 |  | 商品名称 |
| goods_code | VARCHAR(255) | 是 |  | 商品编码 |
| specs | VARCHAR(255) | 是 |  | 规格 |
| unit | VARCHAR(255) | 是 |  | 单位 |
| default_price | DECIMAL(10,2) | 是 |  | 默认价格 |
| status | INT | 是 |  | 状态（0：停用，1：启用） |
| area_price_status | INT | 是 |  | 区域价格状态（0：未设置，1：已设置） |
| area_sell_status | INT | 是 |  | 区域售卖状态（0：未设置，1：已设置） |
| up_down_status | INT | 是 |  | 上下架状态（0：未设置，1：已设置） |
| goods_category | VARCHAR(255) | 是 |  | 商品品类 |
| goods_classify | INT | 是 |  | 商品分类(0:常规商品，1：组合商品, 2:BOM组合商品) |
| goods_type | VARCHAR(255) | 是 |  | 商品类型（10：实物类商品，30:虚拟商品,20:服务类商品） |
| creator | VARCHAR(255) | 是 |  | 创建人 |
| updater | VARCHAR(255) | 是 |  | 修改人 |
| create_time | VARCHAR(255) | 是 |  | 创建时间 |
| modify_time | VARCHAR(255) | 是 |  | 修改时间 |
| spu_code | VARCHAR(255) | 是 |  | SPU编码 |
| spu_name | VARCHAR(555) | 是 |  | SPU名字 |
| delete_flag | INT | 是 |  | 是否删除（0：否 1：是） |
| make_goods | INT | 是 |  | 是否组装商品（0：否 1：是） |
| organization | VARCHAR(255) | 是 |  | 组织 |
| tenant_id | BIGINT | 是 |  | 租户ID |
| belong_org_id | BIGINT | 是 |  | 所属组织ID |
| tenant_org_id | BIGINT | 是 |  | 租户组织ID |
| remark | VARCHAR(255) | 是 |  | 备注 |
| create_user_id | BIGINT | 是 |  | 记录创建者ID |
| modify_user_id | BIGINT | 是 |  | 记录最后更新者ID |
| audit_data_version | INT | 是 |  | 锁版本 |
| sec_bu_id | BIGINT | 是 |  | 数据归属组织id |
| sec_user_id | BIGINT | 是 |  | 数据归属雇员id |
| sec_ou_id | BIGINT | 是 |  | 数据归属公司id |
| pid | BIGINT | 是 |  | 上级ID |
| sub_item_code | VARCHAR(255) | 是 |  | 子件商品编码 |
| product_type | VARCHAR(255) | 是 |  | 商品类型 |
| guarantee_days | VARCHAR(255) | 是 |  | 保质期时长 |
| guarantee_period_unit | VARCHAR(255) | 是 |  | 保质期单位 |

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
