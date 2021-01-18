---
title: SVG笔记
layout: tags
permalink: /tags/SVG笔记/
taxonomy: SVG笔记
---

分类《SVG笔记》下的文章：
---
layout: page
title: 会运动的线条你见过吗？
excerpt_separator: "<!--more-->"
categories:
     - SVG笔记1
tags:
     - Line
---

### 如何制作svg动态效果？
#### 1. 假如你有一个svg图形
![line](http://www.webhek.com/wordpress/wp-content/uploads/2014/02/svg-shape.png)
#### 2. 这个图形必须要有一个线条(stroke)属性
![stroke](http://www.webhek.com/wordpress/wp-content/uploads/2014/02/svg-path-604x266.png)
#### 3. 线条可以是虚线
##### 我们可以用Illustrator制作，也可以用编程实现。我们用CSS来设置这些路径的样式(假定我们这里是inline SVG，或通过一个<object>)，把它们变成虚线形式。

```
<svg ...>    <path class="path" stroke="#000000" ... >  </svg>
.path {
  stroke-dasharray: 20;
}
```
##### 这是让虚线里的每个小线段长度为20px。
![虚线](http://www.webhek.com/wordpress/wp-content/uploads/2014/02/dashed-shape.png)
#### 4. 可以让虚线小段的长度变得更长….
```
.path {
  stroke-dasharray: 100;
}
```
![变长](http://www.webhek.com/wordpress/wp-content/uploads/2014/02/long-dashes.png)
#### 5. 我们还可以给我们的线条设置”offset”偏移量，这样会导致虚线里的小线段的位置发生移动。
##### 当我们动态设置图形中线条的“offset”值时，可以看到这个效果：
![offest](http://www.webhek.com/wordpress/wp-content/uploads/2014/02/animate-stroke.gif)
#### 以下是教程：
```
.path {
  stroke-dasharray: 100;
  animation: dash 5s linear;
}

@keyframes dash {
  to {
    stroke-dashoffset: 1000;
  }
}
```