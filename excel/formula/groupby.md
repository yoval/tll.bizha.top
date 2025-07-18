# GROUPBY 

汇总，分组，聚合。

--- 

```excel
=GROUPBY(行字段, 值区域, 聚合函数, [标题], [总计], [排序], [筛选条件], [字段关系])  
```
- 必选参数​​：

    - 行字段​​：分组的依据列（如部门、地区）
    - ​值区域​​：需聚合的数值列（如销售额、数量）
    - ​聚合函数​​：SUM、AVERAGE、COUNT 等

- 可选参数​​：
    - ​标题​​（field_headers）：控制是否显示原表头（0=隐藏，3=显示）
    - ​总计​​（total_depth）：显示总计行（0=隐藏，1=显示）
    - ​排序​​（sort_order）：按数值列升序（正数）或降序（负数）
    - ​筛选条件​​（filter_array）：排除特定行（如 B1:B10<>"财务部"）。

例：

```excel
=GROUPBY(M19:M49,N19:N49,HSTACK(SUM,AVERAGE,COUNT))
```