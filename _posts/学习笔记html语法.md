---
layout: page
title: HTML太难了？难点一篇全搞定
excerpt_separator: "<!--more-->"
categories:
     - 学习笔记
image: assets/images/study/banner_html.jpg
---

# HTML语法大全
### 一、认识html
#### 1. html：hypertext markup language，超文本标记语言，超链接（实现页面跳转）；
+ #### html结构标准：

```
1. <!doctype html> //声明文档类型，由渲染引擎解析

2. <html>  //根标签

3. <head>  //头部标签，里面的内容是给浏览器/搜索引擎看的
4.    <title></title> //标题标签
5. </head>

6. <body>  //主体标签，给用户、浏览者看
7. </body>

8. </html>
```

+ #### html和htm是一样的；
+ #### 后缀名不能决定文件格式，只能决定文件打开方式；
+ #### html标签分类：
+ #### 单标签<!doctype html>;
+ #### 双标签`<html></html>、<body></body>、<title></title>`
+ ### 2.  html标签关系
+ #### 包含（嵌套）：`<head><title></title><head> `父子关系
+ #### 并列关系：`<head></head><body></body>` 兄弟姐妹关系

### 二、开发工具
#### Dreamweaver：历史悠久，偏设计师使用；
#### sublime：轻量级的，简单、好学，有好多好用的插件；
##### 常用快捷键：
`html:xt + tab	html`结构代码
`tab`	补全标签代码
`ctrl + shift + d`	快速复制一行
`ctrl + shift + k`	快速删除一行
`ctrl +` 鼠标左键单击	集体输入
`ctrl + h	`查找替换
`ctrl + f	`查找
`ctrl + /`	注释
`ctrl + l	`快速选中一行
`ctrl + shift + ↑（↓）	`快速上移（下移）一行

#### webstorm：很强大、很智能。

### 三、简单标签
```
单标签
注释标签：ctrl + /
换行标签：<br/>，在html5中可以省略/
水平线标签：<hr />
双标签
标题标签：<h1></h1>，取值是h1-h6，一个页面中只能有一个h1。
段落标签：<p>段落内容</p>，特点：上下自动生成空白行；<br/>换行不会生成空白行；
文本标签：<font size="16" color="red" >文本内容</font>，早期做网站时候使用；
文本格式化标签：
加粗：<strong></strong>，<b></b>,工作中建议使用strong；
倾斜：<em></em>，<i></i>,工作中建议使用em；
删除线：<del></del>,<s><s/>，工作中建议使用del；
下划线：<ins></ins>,<u></u>,工作中建议使用ins。
建议使用的都是更具语义化，可读性更强。
```

```
图片标签
<img src="" alt="" title="提示文本" width="" height=""/>
src:图片的来源，必写属性；
当鼠标放在图片上时显示title的内容；
当图片加载失败时显示alt的内容;
如果不设置图片宽高,显示图片默认大小，如果只设置其中一个，会进行等比例缩放，如果两个都设置就会按照设置的大小进行展示。
a标签(超链接)
<a href="" title="" target="">登录</a>

href存放目标页面的url，为必写属性；
鼠标放在超链接上显示title的内容；
target为页面打开的方式，默认在原页面打开_self，如果设置值为_black，就会打开一个新的页面进行展示。
锚链接

首先定义一个锚点：在标签中添加一个id属性；
超链接到锚点:<a href="#id属性名">跳转</a>
```
### 四、绝对路径和相对路径
 #### 相对路径：相对于文件自身出发
+ #### 文件(html文档)和图片在同一个目录(文件夹)，直接写文件名；
+ #### 如果图片在下一级目录里，src就为文件夹名+/+图片名称；
+ #### 如果图片在上一级目录里，scr就是 ../ + 图片名
 #### 绝对路径
+ #### 电脑上绝对路径：从电脑盘符开始，如F:\Documents\学习\前端学习\mage.png；
+ #### 互联网上绝对路径：http://... 
### 五、几种HTML结构的快速搭建
```html:xt + tab，过渡结构；
html:xs + tab，严格结构；
! + tab，html5标签结构
九、高级标签
meta标签
编码格式，在meta标签里面设置charset，英语用ascll、ansi；日文、韩文用Unicode；中文的用gbk、gbk2312；台湾big5（繁体字符）；utf-8支持180到200个国家语言，所以用utf-8基本能解析所有国家语言<meta charset="utf-8">；
关键字：给搜索引擎看，主要用于SEO，<meta name="keywords" content="阳光,帅气,有担当,进步">(逗号使用英语格式的)；
网页描述：在搜索的时候会出现的描述：<meta name="description" content="江苏是一个好地方，有山有人妹子水灵">；
网页重定向：<meta http-equiv="refresh" content="5;http://baidu.com">过5秒之后跳转到设定的页面;
告诉搜索引擎站点的作者：<meta name="author" content="姓名">（不常用）；
<meta name="robots" content="all/none/index/noindex/follow/nofollow">（不常用，了解）：
all：文件将被检索，且页面上的链接可以被查询；
none：文件将不被检索，且页面上的链接不可以被查询；
index：文件将被检索；
noindex：文件将不被检索，但页面上的链接可以被查询；
follow：页面上的链接可以被查询；
nofollow：文件将不被检索，页面上的链接可以被查询。
```
```
link标签
链接外部样式表文件<link rel="stylesheet" href="1.css">;
设置网站icon：<meta rel="icon" href="xxx.png">
```
```
表格标签
展示数据，是对网页重构（css+div）的一个有益补充 ；
属性：
边框属性：border；
表格大小会根据内容自动进行填充，也可以自己设定；
单元格之前的距离：cellspacing，默认值为2；
内容和边框的距离:cellpadding；
对齐方式：align，有三个值：left/right/center,如果给表格设为center，表格居中；如果给tr设置center，一行的内容居中；如果给td设置center，则某一列的内容居中，优先级：td > tr > table
```
### 六、标签语义化
+ ##### 标签语义化概念：根据内容的结构化（内容语义化），选择合适的标签（代码语义化）；
+ ##### 标签语义化意义：
+ ##### 网页结构合理；
+ ##### 有利于SEO和搜索引擎简历良好沟通，有了良好的结构和语义，你的网页内容自然容易被搜索引擎抓取；
+ ##### 方便其他设备解析（如屏幕阅读器、盲人阅读器、移动设备）；
+ ##### 便于团队开发和维护。
+ ##### 好的语义化的网站标准：去掉样式表文件之后，结构依然很清晰。
+ ##### 标签语义化的注意事项：

+ ##### 尽可能少的使用没有语义的标签div和span；
+ ##### 在语义不明显时，既可以使用div或者p时，尽量使用p，因为p在默认情况下有上下间距，对兼容特殊终端有利；
+ ##### 不要使用纯样式标签，如：font、b、i、s、u等，改用css样式；
+ ##### 需要强调的文本，可以包含在strong或者em标签中，strong默认样式是加粗（不要用b），em是斜体（不用i）；
