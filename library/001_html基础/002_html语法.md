# html语法
## 概念
1. 标签 `<font>hello</font>`
  - 标记元素用<>括起来，带/表示结束
  - 大多数标记符必须成对出现
  - 结束标记必须以`/`结束
  - 标签不能交叉嵌套
  - 标签名必须小写，先写的后结束

2. 属性 `<font color='red' size="20"> 这是字体标签 </font>`
  - 必须放在开始标签里面，属性可以为标签提供更多样化的特性。  

3. 元素
  - 开始和结束标签以及他们之间的内容称为元素

4. 注释标记（提示说明文字、临时停用部分代码）
5. 网页主体结构
```html
<html lang="en">
    <head>
    <!--对html文件进行诠释、定义、描述，不会显示在文档中（当前网页的信息，如网页名称、版本信息）-->
    </head>
    <body>
    <!--显示在文档中，是html主体部分，对页面进行排版编辑-->
    </body>
</html>
```
6. 头元素中的标签
```html
<head>
    <meta name="keywords" content="关键词1,关键词2"/>
    <meta name="description" content="本篇网页的概述，一段话，对网
    站的进一步描述"/>
    <meta name="author" content="网页作者的资料"
    <meta name='robots' content=none/>
    <!--  
    "all" 本页以及本页面的所有链接都可被查询
    "none" 表示不给检索
    "index" 本文件将被检索 -->
    <meta http-equiv="Content-Type" content="text/html; charset=utf-8"> 　
    <!-- 网页常用编码方式为utf-8 -->
    <title>标题</title>
</head>    
```
7. 文档声明

    `<!DOCTYPE>`
  - 它为浏览器提供一项信息（声明）, 即 HTML 是用什么版本编写的。通过版本信息，浏览器正确地显示出 HTML 页面。
8. 编码格式
  -  utf-8

      是一种针对Unicode的可变长度字符编码，也是一种前缀码，又称万国码。

  -  gb-2312

      它是计算机可以识别的编码，适用于汉字处理、汉字通信等系统之间的信息交换。

  -  gbk

      gb2312的扩展版本

## meta标签详解
#### viewport
```html
<!--
调整移动端视口
 -->
<meta name="viewport" content="width=device-width,initial-scale=1,maximum-scale=1,minimum-scale=1,user-scalable=no">
```

| content  | value | 说明 |
| :----: |:----:| :----:|
| width | 600/device-width |控制viewport的大小，可以指定一个值，如600， 或者特殊的值，如device-width为设备的宽度（单位是缩放为100%的CSS的像素） |
| height | -  |   和width相对应，指定高度 |
| initial-scale | 1 | 初始缩放比例页面第一次加载时的缩放比例 |
| maximum-scale | 1 | 允许用户缩放到的最大比例，范围从0到10.0 |
| minimum-scale | 1 | 允许用户缩放到的最小比例，范围从0到10.0 |
| user-scalable | yes/no </br> true/false | 用户是否可以手动缩放 |

#### format-detection
```html
<!--
format-detection翻译成中文的意思是 "格式检测"
顾名思义，它是用来检测html里的一些格式的
 -->
<meta name="format-detection" content="telephone=no,email=no,adress=no">
```

| content  | value | 说明 |
| :----: |:----:| :----:|
| telephone | yes/no | 是否开启把数字转化为拨号链接，默认是开启|
| email | yes/no | 是否开启把文字默认为邮箱地址，默认是开启|
| adress | yes/no | 是否开启开启了点击地址直接跳转至地图的功能，默认是开启|

#### apple-mobile-web-app-capable
```html
<!--
删除默认的苹果工具栏和菜单栏
content有两个值"yes"和"no"
当我们需要显示工具栏和菜单栏时，这个行meta就不用加了，默认就是显示
 -->
<meta name="apple-mobile-web-app-capable" content="yes">
```

#### apple-mobile-web-app-status-bar-style
```html
<!--
控制状态栏显示样式
 -->
<meta name="apple-mobile-web-app-status-bar-style" content="black">
```
| content | 说明 |
| :----:| :----:|
| black | 状态栏背景为黑色 |
| black-translucent | 状态栏背景为灰色 |
