# Emmet
## 安装
在 Sublime Text 中按 `Ctrl+Shift+p` 快捷键或在菜单-工具中打开“命令面板"，输入：Install Package (安装扩展)后回车，弹出新的窗口，再输入Emmet查找“Emmet"确定安装，等到自动打开一个文档，说明安装成功。

## 语法
> 【不能有空格，会导致代码无法使用】

#### 生成 HTML 文档初始结构

|Emmet|Html|
|:---:|:---:|
|! | HTML5 结构 |
|html:5  | HTML5 结构 |
|html:xt | HTML4 过渡型 |
|html:4s | HTML4 严格型 |

##### ==【Eg】==
```html
<!-- ! -->
<!doctype html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>
<body>

</body>
</html>
```

#### 生成带有 id 、class 的 HTML 标签
CSS选择器在块级元素中默认的HTML标签为div，在内联级元素中为span，而对于HTML一些特殊的标签：ul li、table tr td，将会生成对应的内部标签。
##### ==【Eg】==
```HTML
.className
div.className
<div class="className"></div>

#idName
div#idName
<div id="className"></div>

#idName.className
div#idName.className

```

#### 生成后代（子标签）：>
##### ==【Eg】==
```HTML
div>ul>li
<div>
    <ul>
        <li></li>
    </ul>
</div>
```

#### 生成兄弟：+
##### ==【Eg】==
```HTML
div+p
<div></div>
<p></p>
```

#### 生成上级元素：^
##### ==【Eg】==


```HTML
1. 跟 ul 平级的 span 标签
div>ul>li^span
<div>
    <ul>
        <li></li>
    </ul>
    <span></span>
</div>


2. 跟 div 平级的 span 标签
div>ul>li^^span
<div>
    <ul>
        <li></li>
    </ul>
</div>
<span></span>
```

#### 重复生成多份：*
##### ==【Eg】==
```HTML
ul>li*5
<ul>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
</ul>
```

#### 生成分组：()
##### ==【Eg】==
```HTML
div>(header>ul>li*2>a)+footer>p
<div>
    <header>
        <ul>
            <li><a href=””></a></li>
            <li><a href=””></a></li>
        </ul>
    </header>
    <footer>
        <p></p>
    </footer>
</div>
```

#### 生成自定义属性：[attr=value]
##### ==【Eg】==
```HTML
a[href="http://www.baidu.com" title="百度"]
<a href="http://www.baidu.com" title="百度"></a>
```

#### 对生成内容编号：$
> 1. `$` 就表示一位数字，只出现一个的话，就从1开始。
> 2. 如果出现多个，就从0开始。如果我想生成三位数的序号，那么要写三个 `$`。
> 3. 在 `$` 后面增加 `@-` 来实现倒序排列
> 4. 使用 `@N` 指定开始的序号

##### ==【Eg】==
```HTML
ul>li.item$*2
<ul>
	<li class="item1"></li>
	<li class="item2"></li>
</ul>

ul>li.item$$$*2
<ul>
	<li class="item001"></li>
	<li class="item002"></li>
</ul>

ul>li.item$@-*2
<ul>
  <li class="item2"></li>
	<li class="item1"></li>
</ul>

ul>li.item$@3*2
<ul>
	<li class="item3"></li>
	<li class="item4"></li>
</ul>

ul>li.item$@-5*2
<ul>
  <li class="item6"></li>
	<li class="item5"></li>
</ul>
```

#### 生成文本内容：{}
##### ==【Eg】==
```HTML
a{Click me}
a>{Click me}
<a href="">Click me</a>

a{click}+b{here}
<a href="">click</a><b>here</b>

a>{click}+b{here}
<a href="">click<b>here</b></a>
```
