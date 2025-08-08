# ads_fin_finance_paid_di

## 表描述
**业务层级**: ADS层 - 财务付款汇总表  
**数据用途**: OLAP分析  
**数据量**: 15,783条记录  
**更新频率**: 每日更新  

## 表结构说明
该表存储财务系统的付款记录，包含付款单据的基本信息、支付金额、供应商信息、费用类型等关键字段。用于财务分析和供应商付款统计。

## 字段详情

| 字段名称 | 数据类型 | 是否可空 | 默认值 | 字段说明 |
|---------|----------|----------|--------|----------|
| pt | varchar | 是 | NULL | 天分区 |
| biz_no | varchar | 是 | NULL | 业务系统单号 |
| receipt_no | varchar | 是 | NULL | 财务中心单号 |
| total_paid_amt | decimal | 是 | NULL | 总支付金额 |
| create_time | varchar | 是 | NULL | 创建时间 |
| complete_time | varchar | 是 | NULL | 支付完成时间 |
| update_time | varchar | 是 | NULL | 支付更新时间 |
| receipt_type | varchar | 是 | NULL | 单据类型 |
| cost_type | varchar | 是 | NULL | 费用类型 |
| currency | varchar | 是 | NULL | 原币种 |
| settlement_method | varchar | 是 | NULL | 结算方式 |
| account_in_company_code | varchar | 是 | NULL | 入账公司代码 |
| account_in_company | varchar | 是 | NULL | 入账公司代码名称 |
| payment_reason | varchar | 是 | NULL | 支付原因 |
| payee_account_name | varchar | 是 | NULL | 收款人名称 |
| payee_account_no | varchar | 是 | NULL | 收款人账号 |
| pay_amt | decimal | 是 | NULL | 支付金额 |
| supplier_code | varchar | 是 | NULL | 供应商编码 |
| supplier_name | varchar | 是 | NULL | 供应商名称 |
| operator | varchar | 是 | NULL | 制单人 |
| apply_dept | varchar | 是 | NULL | 申请部门 |
| cost_center_code | varchar | 是 | NULL | 成本中心代码 |
| cost_center_name | varchar | 是 | NULL | 成本中心名称 |
| submit_user_id | varchar | 是 | NULL | 提交用户ID |

## 业务说明

### 关键字段解释
- **biz_no**: 业务系统生成的原始单号，用于追溯业务来源
- **receipt_no**: 财务中心生成的唯一单号，财务核算的主要标识
- **total_paid_amt**: 该笔付款的总金额，包含所有明细
- **pay_amt**: 实际支付金额，可能与总金额不同（分批支付情况）
- **settlement_method**: 支付方式，如银行转账、现金、支票等
- **cost_type**: 费用类型分类，如货款、运费、服务费等

### 单据类型说明
- **付款单**: 常规的对外付款
- **报销单**: 员工费用报销付款
- **预付款**: 预付供应商款项
- **退款单**: 供应商退款或客户退款

### 使用场景
1. **财务付款分析**: 统计各时间段付款金额
2. **供应商付款追踪**: 按供应商统计付款情况
3. **费用类型分析**: 分析各类费用的支付情况
4. **现金流管理**: 监控公司现金流出情况
5. **对账核对**: 与供应商对账付款记录

## 常用查询示例

### 1. 查询某日付款总额
```sql
SELECT 
    pt,
    COUNT(*) as payment_count,
    SUM(pay_amt) as total_payment,
    AVG(pay_amt) as avg_payment
FROM ads_fin_finance_paid_di
WHERE pt = '20241201'
GROUP BY pt;
```

### 2. 查询某供应商的付款记录
```sql
SELECT 
    receipt_no,
    biz_no,
    pay_amt,
    complete_time,
    cost_type,
    payment_reason
FROM ads_fin_finance_paid_di
WHERE supplier_code = 'SUP001'
ORDER BY complete_time DESC;
```

### 3. 统计某时间段内各费用类型的付款金额
```sql
SELECT 
    cost_type,
    COUNT(*) as payment_count,
    SUM(pay_amt) as total_amount,
    AVG(pay_amt) as avg_amount
FROM ads_fin_finance_paid_di
WHERE pt BETWEEN '20241201' AND '20241231'
GROUP BY cost_type
ORDER BY total_amount DESC;
```

### 4. 查询各供应商的累计付款金额
```sql
SELECT 
    supplier_code,
    supplier_name,
    COUNT(*) as payment_times,
    SUM(pay_amt) as total_paid
FROM ads_fin_finance_paid_di
WHERE pt >= '20241201'
GROUP BY supplier_code, supplier_name
HAVING total_paid > 10000
ORDER BY total_paid DESC;
```

### 5. 按支付方式统计付款情况
```sql
SELECT 
    settlement_method,
    COUNT(*) as payment_count,
    SUM(pay_amt) as total_amount,
    ROUND(SUM(pay_amt) * 100.0 / SUM(SUM(pay_amt)) OVER(), 2) as percentage
FROM ads_fin_finance_paid_di
WHERE pt = '20241201'
GROUP BY settlement_method
ORDER BY total_amount DESC;
```

## 注意事项

1. **时间格式**: 所有时间字段均为字符串格式，格式为`YYYY-MM-DD HH:MM:SS`
2. **金额单位**: 所有金额字段单位均为**分**
3. **分区字段**: 使用`pt`字段作为时间分区，格式为`YYYYMMDD`
4. **关联关系**: 
   - 可通过`supplier_code`关联到供应商维度表
   - 可通过`biz_no`关联到业务系统原始单据
5. **数据范围**: 仅包含已完成的付款记录，未完成的付款不会出现在此表中
6. **币种说明**: `currency`字段存储原币种，如涉及外币需要关注汇率问题

## 数据质量检查

### 1. 检查异常金额
```sql
SELECT * FROM ads_fin_finance_paid_di
WHERE pay_amt <= 0 OR pay_amt IS NULL;
```

### 2. 检查缺失供应商信息
```sql
SELECT * FROM ads_fin_finance_paid_di
WHERE supplier_code IS NULL OR supplier_name IS NULL;
```

### 3. 检查时间异常
```sql
SELECT * FROM ads_fin_finance_paid_di
WHERE complete_time < create_time;
```