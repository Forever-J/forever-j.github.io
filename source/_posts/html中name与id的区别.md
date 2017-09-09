---
title: html中name与id的区别
date: 2017-08-28 18:52:40
tags: html
categories: 前端
---
name 属性用于在 JavaScript 中对元素进行引用，或者在表单提交之后，对表单数据进行引用。

html的name和id可以类比身份证的姓名和身份证编号
编号id具有唯一性，一个id只出现一次。
名称name具备可重复性，可以多次出现。
在css中两者都具备识别html元素的作用，name用点号.表示，id用井号#
一般name用于通用多次出现元素的样式定义，id用于唯一性元素样式定义。
在表单当中，由于有些控件具备多元素特性，例如radio checkbox等，使用id不便于表单数据的提交，此外浏览器会根据name来设定发送到服务器的request，因此在表单当中，用name来提交数据。
当然，在实际的html中，也完全可以不用id，用单独的class也可以起到代替id的作用。但是在js中，是无法通过class直接后去html元素的， 定义id便于相关操作。

* [html中name与id的区别](https://wenku.baidu.com/view/a3fcdc976bec0975f465e2c4.html)
* [HTML name、id、class 的区别](http://www.cnblogs.com/polk6/archive/2013/05/28/3101571.html)