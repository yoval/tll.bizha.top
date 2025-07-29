# SUMMARIZE 

---

基本语法：

```dax
SUMMARIZE(
    <table>,
    <groupBy_column1>[, <groupBy_column2>]…,
    [<name>, <expression>][, [<name>, <expression>]…]
)
```

例：
```dax
EVALUATE
SUMMARIZE(

'表2',

'表2'[大类],
'表2'[小类],
"产品数量",COUNT('表2'[存货编号])
)
```

