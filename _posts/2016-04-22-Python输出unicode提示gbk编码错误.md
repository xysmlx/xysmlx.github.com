---
layout: post
title: Python输出unicode提示gbk编码错误
category: python
date: 2016-04-22
---

## 控制台输出unicode

设置stdout为utf-8即可解决：

```python
sys.stdout = io.TextIOWrapper(sys.stdout.buffer, encoding='utf8')
```

## 文件读写unicode

使用codecs即可解决

```python
import codecs

file_in = codecs.open(inp, "r", "utf-8")
file_out = codecs.open(outp, "w", "utf-8")
```