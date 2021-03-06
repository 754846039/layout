## html概述

### 一、 常用名词解释
##### 前端
- 前端主要是对人机交互的界面设计利用代码进行实现，提高用户体验、优化网站性能
- 作为页面的实现者，不仅要熟练掌握实现网页的各种技能，还要懂交互设计和一些后台技术。这样我们在工作中就可以和UI设计师、后台开发人员进行无缝沟通，大大提高工作效率。
- 前端就是视觉表现和后台开发的桥梁，是贯穿在整个产品开发过程的纽带，起到承上启下的作用。

##### World Wide web (万维网)

WWW 是环球信息网的缩写，中文名为万维网、环球网，简称web；web本意是蜘蛛网和网的意思。现广泛译作网络、互联网等技术领域。表现为三种形式，即超文本（hypertext）、超媒体（hypermedia）、超文本传输协议（HTTP）等。
- 超文本：是用超链接的方法，将各种不同空间的文字信息组织在一起的网状文本。
- 超媒体：由超文本衍生而来的；超链接能将若干文本组合起来形成超文本.同样道理,超链接也可将若干不同媒体、多媒体或流媒体文件链接起来,组合成为超媒体.
- 超文本传输协议（HTTP）：是互联网上应用最为广泛的一种网络协议。所有的WWW文件都必须遵守这个标准。HTTP是一个客户端和服务器端请求和应答的标准（TCP）。

##### 网站

网站 是构成web的基础，所谓网站(Website)，就是指在国际网路（万维网）上，根据一定的规则，使用HTML等工具制作的用于展示特定内容的相关网页的集合。


##### 网页
网页 是网站中的一「页」，是构成网站的基础，是承载各种网站应用的平台。通俗的说，网站就是由网页组成的。通常是HTML格式（文件扩展名为.html或.htm或.asp或.aspx或.php或.jsp等）要通过浏览器来阅读。

##### 构成网页的元素

图片和文字是构成一个网页的最基本元素。文字是一个网页的内容，图片负责网页的美观。当然除此之外，网页中的内容还包括音频、视频、动画等。

##### 互联网产业分类
1. 行业基础性服务（日常应用包括新闻、百度、邮箱）
2. 商务应用（天猫、京东、智联、支付宝）
3. 交流娱乐（微博、各类网游、即时通讯工具、视频网站）
4. 互联网媒体（网络电视）


### 二、制作网站的流程
1. UI设计
2. 前端
    1. 页面布局美化（html+css）
    2. 创建动态HTML页面（利用js使网站变得动感，有魅力，吸引更多的浏览者）
3. 后台
    1. 后台程序建设（php、asp、jsp、.net）
    2. 数据库建设（mysql）
    3. 选择服务器   


### 三、HTML详解
#### 1. html是什么
html是一种规范，一种标准，通过标记符号来标记要显示的内容，由浏览器解析执行的一种==超文本标记语言==。它包括文字处理、画面安排、图片显示。

【注意】浏览器按顺序阅读html文件，通过html中的标记符来解析并显示其标记的内容，对书写错误的标记并不会指出，而且不会中断解析过程，我们只能通过显示效果来判断出错原因及出错部位。
#### 2. html发展历程
![image](amWiki/images/html_develop.jpg)
##### html  （超文本标记语言）
用一些标记符号来标记网页中要显示的内容。初始阶段我们用的是html4.01版本，该版本语法结构比较松散，要求不是很严格，标签不闭合，大小写不注意，引号运用不严格。

##### xhtml  （可扩展标记语言）
他是更严谨更纯净的HTML版本，相比html语言更加的严格。可以使我们的代码更规范，更整洁，更有效率。

##### html5
html最新版本，需要注意浏览器兼容问题

##### w3c  （万维网联盟）
World Wide Web Consortium（W3C），又称W3C理事会。1994年10月在麻省理工学院计算机科学实验室成立,建立者是万维网的发明者蒂姆·伯纳斯-李。W3C为解决 Web 应用中不同平台、技术和开发者带来的不兼容问题，保障 Web 信息的顺利和完整流通，万维网联盟制定了一系列标准并督促 Web 应用开发者和内容提供者遵循这些标准。

#### 3. html特性
- 扩展名：`.html`或`.htm`
- html是一种描述性语言，简单易学
- 可以使用任意文本编辑器来创建html
