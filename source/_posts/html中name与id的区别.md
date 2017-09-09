---
title: html中name、id、class的区别
date: 2017-08-28 18:52:40
tags: html
categories: 前端
---
name 属性用于在 JavaScript 中对元素进行引用，或者在表单提交之后，对表单数据进行引用。

html的name和id可以类比身份证的姓名和身份证编号
编号id具有唯一性，一个id只出现一次。
名称name具备可重复性，可以多次出现。
在css中两者都具备识别html元素的作用，name用点号.表示，id用井号#
一般name用于通用多次出现元素的样式定义，id用于唯一性元素样式定义。<!-- more -->
在表单当中，由于有些控件具备多元素特性，例如radio checkbox等，使用id不便于表单数据的提交，此外浏览器会根据name来设定发送到服务器的request，因此在表单当中，用name来提交数据。
当然，在实际的html中，也完全可以不用id，用单独的class也可以起到代替id的作用。但是在js中，是无法通过class直接后去html元素的， 定义id便于相关操作。

id要符合标识的要求，比如大小写敏感，最好不要包含下划线（因为不兼容CSS）。而name基本上没有什么要求，甚至可以 用数字。table、tr、td、div、p、span、h1、li等元素一般用id。与表单相关的元素也可以赋ID值,  但为这些元素赋ID值的时候引用这些元素的方法就要变一下了，具体的如下： 
赋name时引用元素的方式:  document.formName.inputName或document.frames("frameName") 
赋id时引用元素的方式:  document.all.inputID或document.all.frameID 
除去与表单相关的元素，只能赋id不能赋name，这些元素有body、li、a、table、tr、td、th、p、div、span、pre、dl、dt、dd、font、b等等
对于name和class来说意义是一样的。但是name主要是提交表单用的 ，而class是设置标签的类，用于指定元素属于何种样式的类，主要用来设置css样式的。但两种都可以用来识别css，推荐除了表单外都用class。

name的用途
    用途1: 主要是用于获取提交表单的某表单域信息， 作为可与服务器交互数据的HTML元素的服务器端的标示，比如input、select、textarea、框架元素(iframe、frame、 window的名字，用于在其他frame或window指定target ) 和button等，这些元素都与表单(框架元素作用于form的target)提交有关，浏 览器会根据name来设定发送到服务器的request， 在表单的接收页面只接收有name的元素,  所以赋ID的元素通过表单是接收不到值的。 我们可以在服务器端根据其Name通过Request.Params取得元素提交的值。在form里面，如果不指定Name，就不会发送到服务器端 。
    用途2: HTML元素Input type='radio'分组，我们知道radio button控件在同一个分组类，check操作是mutex的，同一时间只能选中一个radio，这个分组就是根据相同的Name属性来实现的。
    用途3: 建立页面中的锚点，我们知道<a href="URL">link</a>是获得一个页面超级链接，如果不用href属性，而改用Name，如：<a name="PageBottom"></a>，我们就获得了一个页面锚点。
    用途4: 作为对象的Identity，如Applet、Object、Embed等元素。比如在Applet对象实例中，我们将使用其Name来引用该对象。
    用途5: 在IMG元素和MAP元素之间关联的时候，如果要定义IMG的热点区域，需要使用其属性usemap，使usemap="#name"(被关联的MAP元素的Name)。
    用途6: 某些特定元素的属性，如attribute，meta和param。例如为Object定义参数<PARAM NAME = "appletParameter" VALUE = "value">或Meta中<META NAME = "Author" CONTENT = "Dave Raggett">。
    当然HTML元素的Name属性在页面中也可以起那么一点ID的作用，因为在DHTML对象树中，我们可 以使用document.getElementsByName来获取一个包含页面中所有指定Name元素的对象数组。Name属性还有一个问题，当我们动 态创建可包含Name属性的元素时，不能简单的使用赋值element.name = "..."来添加其Name，而必须在创建Element时，使用document.createElement('<element name = "myName"></element>')为元素添加Name属性。
* [html中name与id的区别](https://wenku.baidu.com/view/a3fcdc976bec0975f465e2c4.html)
* [HTML name、id、class 的区别](http://www.cnblogs.com/polk6/archive/2013/05/28/3101571.html)
* [id name class 区别](http://afunti.iteye.com/blog/988562)