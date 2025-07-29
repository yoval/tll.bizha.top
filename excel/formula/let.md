# LET

LET 函数会向计算结果分配名称。 这样就可存储中间计算、值或定义公式中的名称。 这些名称仅可在 LET 函数范围内使用。 与编程中的变量类似， LET 是通过 Excel 的本机公式语法完成的。

---

```excel
=LET(name1, name_value1, [name2, name_value2, ...], calculation)

```

例：

```excel
=LET(
    sales, SUM(SalesRange),
    costs, SUM(CostsRange),
    profit, sales - costs,
    profit / sales
)
```