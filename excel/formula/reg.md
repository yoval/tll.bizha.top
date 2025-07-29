# 正则表达式

excel的正则表达式采用的是C#的正则表达式。

---

**REGEXP**​(WPS)

```excel
=REGEXP(text, pattern, [mode], [replace])
=REGEXP (原始字符串, 正则表达式, 匹配模式, 替换内容)
```
- ​模式参数​​：
    - 0：提取所有匹配（默认）,多项符合会自动溢出。
    - 1：逻辑判断（返回TRUE/FALSE）
    - 2：替换匹配内容（需第四参数指定替换值）
    - 3：​​完整提取​​（隐藏多结果，需用REDUCE展开）

A1：春蚕到死丝方尽，蜡炬成灰泪始干。

1. 提取“方”到“泪”之间的内容。

```excel
=REGEXP(A1,"(?<=方).*?(?=泪)",0)
```
![](https://images.bizha.top/202507121019324.png)


2. 是否包含数字。

```excel
=REGEXP(A1,"\d+",1)
```
![](https://images.bizha.top/202507121027029.png)

3. 将“蜡炬”替换成“秋菊”。

```excel
=REGEXP(A1,"蜡炬",2,"秋菊")
```
![](https://images.bizha.top/202507121029139.png)



**REGEXEXTRACT**(excel)

*相当于wps `REGEXP` 的 模式 0*

从文本中提取符合正则模式的子字符串。

```excel
=REGEXEXTRACT(text, pattern, [return_mode], [case_sensitivity])
```

- return_mode：
    - 0:返回第一个匹配结果（默认）
    - 1:返回所有匹配项的纵向数组
    - 2:返回首个匹配项的捕获组数组
- case_sensitivity（可选）：
    - 0:不区分大小写（默认）
    - 1:区分大小写



**REGEXREPLACE**(excel)

*相当于wps `REGEXP` 的 模式 2*

按正则模式替换文本

```excel
=REGEXREPLACE(text, pattern, replacement, [occurrence], [match_mode])
```
- 参数​​：
    - replacement：替换后的文本，可用 $1、$2 引用捕获组。
    - occurrence（可选）：指定替换第几次匹配（默认全部替换）。

**REGEXTEST**(excel)

*相当于wps `REGEXP` 的 模式 1*

```excel
= REGEXTEST(text, pattern, [match_mode])
```
