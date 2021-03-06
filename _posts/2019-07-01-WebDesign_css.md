---
layout: page
excerpt_separator: "<!--more-->"
title: 网页设计与css间的秘密
categories:
     - 网站设计
---
相信大家在进行网页设计，编写css样式的时候都会遇到一个问题，就是以下这三种选择器到底有什么区别？有时候真的是傻傻分不清，不知道什么时候用哪种选择器比较合适。
<!--more-->
#### 1、标签选择器
```markdown
<style type="text/css">
p{
    font-size:14px;
}</style>
<body>
<p>css</p>
</body>
```
#### 2、ID选择器
```markdown
<head>
<title>Document</title>
<style type="text/css">
#mytitle
{
    border:3px dashed green;
}
</style>
</head>
```
#### 3、类选择器
```markdown
<style type="text/css">
.oneclass/*定义类选择器*/{
    width:800px;
}
</style>
</head>
```

为了全面了解这三个选择器，我们可以先了解一下各个选择器的特点。

### 什么是标签选择器？  
- 特点：根据指定的标签名，在当前界面中找到所有该名称的标签，然后设置属性。  
- 格式：  
标签名{ 
 属性：值；
   }  
- 注意点： 
   1. 标签选择器选定的是当前界面中所有该名称的标签，而不能单独选定某一标签；   
   2. 标签选择器无论标签藏得多深都能找到；  
   3. 只要是HTML中的标签都可以作为标签选择器。

### ID选择器：规定用#来定义（名字自定义）
- 特点：针对某一个特定的标签来使用，只能使用一次。css中的ID选择器以”#”来定义。
- 格式
#id{ 
 属性：值；
  }
- ID的命名
1.只能有字母、数字、下划线。 
2.必须以字母开头。 
3.不能和标签同名。比如id不能叫做body、img、a。 
4.大小写严格区分，也就是说aa,和AA是两个不同的ID

### 类选择符 :规定用圆点.来定义
- 特点：针对你想要的所有标签使用。同一个标签可以使用多个类选择器。用空格隔开。
- 格式： 
.类名{  属性：值；  }
- 注意点
1.在同一个界面中class是不可重复的。
2.在编写id选择器的时候class前一定要加。
3.类名的命名规范和id命名规范是一样的。
4。类名就是专门给某个特定的标签设置样式的；

### 选择器使用原则
- 1、 准确的选到要控制的标签。  
- 2、 使用最合理优先级的选择器 。
- 3、 HTML和CSS代码尽量简洁美观。

那为何我们有时候选择器都设置准确了，可相关的样式却总是出不来呢？

### 样式设置不生效的三大原因 

a.设置的样式被其他样式叠加               
- 设置的样式优先级没有其他样式优先级高
             
b.样式属性名写错               
- unknow property name  （浏览器错误提示）              
- Invalid property value（浏览器错误提示）  
           
c.样式表中选择器标识符写错                
- 样式表中选择器之间不能有其他字符, 如果有，该字符将向下与相邻的选择器构成新的选择器，导致选不中。
- 检查方法：在谷歌浏览器的控制台中，选中该标签，查看styles里面的选择器，查看那个选择器不存在，那么是该选择器标识符写法出错。

如果大家看了这篇文章还不是很了解的话，那不妨来多看一些比较生动的介绍[比较生动的介绍](https://www.zhihu.com/question/20081418)
本文参考文章：[CSS标签选择器](https://blog.csdn.net/u010636314/article/details/74276626)