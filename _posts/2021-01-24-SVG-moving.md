---
layout: page
title: 如何让制作一只会移动的“马”
excerpt_separator: "<!--more-->"
categories:
     - SVG笔记
tags:
     - svg
---

## 我们可以使用一些基础动画元素，实现单属性的动画过渡效果。

#### 下面这个马儿奔跑的效果就是使用的animate元素
<svg xmlns="http://www.w3.org/2000/svg" width="320" height="200">
  <title>马儿跑</title>
  <g> 
    <text font-family="microsoft yahei" font-size="120" y="160" x="160">
		马
	    <animate attributeName="x" from="160" to="60" begin="0s" dur="3s" repeatCount="indefinite"/>
	</text>
  </g>
</svg>

##### 以下是该svg动图制作的代码
```
<svg xmlns="http://www.w3.org/2000/svg" width="320" height="200">
  <title>马儿跑</title>
  <g> 
    <text font-family="microsoft yahei" font-size="120" y="160" x="160">
		马
	    <animate attributeName="x" from="160" to="60" begin="0s" dur="3s" repeatCount="indefinite"/>
	</text>
  </g>
</svg>
```

#### 我们可以使用animateTransform来变换动画效果。
<svg width="320" height="320" xmlns="http://www.w3.org/2000/svg">
  <g> 
    <text font-family="microsoft yahei" font-size="80" y="100" x="100">马</text>
    <animateTransform attributeName="transform" begin="0s" dur="3s"  type="scale" from="1" to="1.5" repeatCount="indefinite"/>
  </g>
</svg>

#### 以下是该svg动图制作的代码
```
<svg width="320" height="320" xmlns="http://www.w3.org/2000/svg">
  <g> 
    <text font-family="microsoft yahei" font-size="80" y="100" x="100">马</text>
    <animateTransform attributeName="transform" begin="0s" dur="3s"  type="scale" from="1" to="1.5" repeatCount="indefinite"/>
  </g>
</svg>
```
### 按照以上代码便可以制作简单的svg动画