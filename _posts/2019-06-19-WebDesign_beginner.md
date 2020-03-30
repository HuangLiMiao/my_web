---
layout: page
excerpt_separator: "<!--more-->"
title: 小白的网页制作之道
categories:
     - web_design
---
### 什么是响应式web设计？
- 响应式web设计简单来说，就是随着视口（viewport）及设备（device）的不同呈不同的样式（style）。
<!--more-->
### 为何需要将网页设计为响应式？
- 对于多数网站来说，为每种新设备及分辨率创建其独立的版本根本就是不切实际的；结果就是，我们将会赢得使用某些设备的用户群，而失去那些使用其他设备的用户。所以为了避免这种情况的发生。响应式Web设计(Responsive Web design)的理念被提出。

### 响应式 Web 设计工作原理
- 应用 CSS3 的媒体查询(Media Queries)，创建一个包含适应各种设备尺寸样式的CSS。一旦页面在特定的设备上加载，此时，会先检测设备的视口大小，然后加载特定于设备的样式。即为不同的媒体类型设定专有的样式表。

#### 何为媒体查询？
- @media 可以针对不同的屏幕尺寸设置不同的样式，特别是如果需要设置设计响应式的页面时候，@media 是非常有用的。 重置浏览器大小的过程中，页面也会根据浏览器的宽度和高度重新渲染页面。

#### 如何引入media？
- 常用的引入方法主要要两种
#### link方法引入

```markdown
<link rel="stylesheet" type="text/css" href="styleB.css"  media="screen and (min-width: 600px) and (max-width: 800px)">
```

#### @media引入

```markdown
@media screen and (min-width: 600px) and (max-width: 800px){      选择器{          属性：属性值；      }  }
```