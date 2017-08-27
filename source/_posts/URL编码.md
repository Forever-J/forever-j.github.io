---
title: URL编码
date: 2017-08-27 20:38:59
tags: URL
categories: 基础知识
---
URL 只能使用 ASCII 字符集来通过因特网进行发送。
由于 URL 常常会包含 ASCII 集合之外的字符，URL 必须转换为有效的 ASCII 格式。
URL 编码使用 "%" 其后跟随两位的十六进制数来替换非 ASCII 字符。
URL 不能包含空格。URL 编码通常使用 + 来替换空格。

JavaScript、PHP、ASP 都提供了对字符串进行URL编码的函数。
JavaScript 中使用 encodeURI() 函数，PHP 中使用 rawurlencode() 函数，ASP 中使用 Server.URLEncode() 函数。

* [关于URL编码](http://www.ruanyifeng.com/blog/2010/02/url_encoding.html)
* [URL编码参考手册](http://www.runoob.com/tags/html-urlencode.html)