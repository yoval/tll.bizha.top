# 正则表达式

---

- REGEXEXTRACT

从文本中提取符合正则模式的子字符串。

```excel
=REGEXEXTRACT(text, pattern, [return_mode], [case_sensitivity])
```

例：提取AB之间的内容。

```python
import re
text = "开头A这是要提取的内容B结尾"
pattern = r'(?<=A).*?(?=B)'  # 模式定义
matches = re.findall(pattern, text, re.DOTALL)  # re.DOTALL允许匹配换行符
print(matches)  # 输出: ['这是要提取的内容']
```

- REGEXREPLACE

按正则模式替换文本

```excel
=REGEXREPLACE(text, pattern, replacement, [occurrence], [match_mode])
```

*replacement：替换后的文本，可用 $1、$2 引用捕获组。*

*occurrence（可选）：指定替换第几次匹配（默认全部替换）。*