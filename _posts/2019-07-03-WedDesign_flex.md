---
layout: page
excerpt_separator: "<!--more-->"
title: 你了解flex布局吗？
categories:
     - web_design
---  

平时做项目的时候，相信你也曾和我一样，被设置flex布局所烦恼。不知道如何设置才能让几个框框排列的整齐一点。首先，我们得知道Flex是Flexible Box的缩写，意为”弹性布局”，用来为盒状模型提供最大的灵活性。任何一个容器都可以指定为Flex布局。现在就让我们一起来复习一下flex的布局设置吧。
<!--more-->
### 一、基本概念:
- Flex布局由父容器称为Flex容器（flex-container）和它直接的子元素称为flex 项目（flex-item）构成，在下文中将它们简称为“容器”和“项目”。

![输入图片说明](https://gitee.com/limiaohuang/Mywebsite/raw/gh-pages/assets/images/CSS3-Flexbox-Model.jpg)
 

- flex容器有两个参考的轴：水平的主轴（main axis）和交叉的轴（cross axis）。 
- 主轴的开始位置main start，主轴结束位置main end； 交叉轴的开始位置叫做cross start，结束位置叫做cross end。 
- 直接子元素“项目”沿主轴排列； 单个项目占据的主轴空间叫做main size，占据的交叉轴空间叫做cross size。
- flex容器：即指定了display: flex的DOM元素; flex项目：即flex容器内的下一层DOM元素。

### 二、属性总结表

![输入图片说明](https://gitee.com/limiaohuang/Mywebsite/raw/gh-pages/assets/images/%E5%B1%9E%E6%80%A7%E6%80%BB%E7%BB%93%E8%A1%A8.png)
 

### 三、容器属性详述
#### 1、flex-direction属性：属性决定主轴的方向（即项目的排列方向）。
> .box {
  flex-direction: row | row-reverse | column | column-reverse;
}

![输入图片说明](https://gitee.com/limiaohuang/Mywebsite/raw/gh-pages/assets/images/flex-direction%E5%B1%9E%E6%80%A7.png)
 
```markdown
- row（默认值）：主轴为水平方向，起点在左端。
- row-reverse：主轴为水平方向，起点在右端。
- column：主轴为垂直方向，起点在上沿。
- column-reverse：主轴为垂直方向，起点在下沿。
```

#### 2、flex-wrap属性：定义如果一条轴线排不下，如何换行。
> .box{
  flex-wrap: nowrap | wrap | wrap-reverse;
}

- nowrap：自动缩小项目，不换行
![输入图片说明](https://gitee.com/limiaohuang/Mywebsite/raw/gh-pages/assets/images/nowrap.png)

- wrap：换行，且第一行在上方
![输入图片说明](https://gitee.com/limiaohuang/Mywebsite/raw/gh-pages/assets/images/wrap.jpg)

- wrap-reverse：换行，第一行在下面
![输入图片说明](https://gitee.com/limiaohuang/Mywebsite/raw/gh-pages/assets/images/wrap-reverse.jpg)

#### 3、flex-flow:是flex-direction属性和flex-wrap属性的简写形式。
> .box {
  flex-flow: <flex-direction> <flex-wrap>;
}

#### 4、justify-content属性:定义了项目在主轴上的对齐方式。
> .box {
  justify-content: flex-start | flex-end | center | space-between | space-around;
}

![输入图片说明](https://gitee.com/limiaohuang/Mywebsite/raw/gh-pages/assets/images/justify-content%E5%B1%9E%E6%80%A7.png)

```markdown
- flex-start：左对齐
- flex-end：右对齐
- center：居中对齐
- space- between：两端对齐
- space-around：沿轴线均匀分布
```

#### 5、align-items属性：定义项目在交叉轴上如何对齐。
> .box {
  align-items: flex-start | flex-end | center | baseline | stretch;
}

![输入图片说明](https://gitee.com/limiaohuang/Mywebsite/raw/gh-pages/assets/images/align-items.png)
```markdown
- flex-start：顶端对齐
- flex-end：底部对齐
- center：竖直方向上居中对齐
- baseline：item第一行文字的底部对齐
- stretch：当item未设置高度时，item将和容器等高对齐
```

#### 6、align-content属性:定义了多根轴线的对齐方式。
- 如果项目只有一根轴线，该属性不起作用。
> .box {
  align-content: flex-start | flex-end | center | space-between | space-around | stretch;
}

![输入图片说明](https://gitee.com/limiaohuang/Mywebsite/raw/gh-pages/assets/images/align-content.png)
![输入图片说明](https://gitee.com/limiaohuang/Mywebsite/raw/gh-pages/assets/images/align-content_space.png)

```markdown
- flex-start：与交叉轴的起点对齐。
- flex-end：与交叉轴的终点对齐。
- center：与交叉轴的中点对齐。
- space-between：与交叉轴两端对齐，轴线之间的间隔平均分布。
- space-around：每根轴线两侧的间隔都相等。
- stretch（默认值）：轴线占满整个交叉轴。
```

本文参考文章：[Flex 布局语法教程](https://www.runoob.com/w3cnote/flex-grammar.html)