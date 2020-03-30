---
layout: page
excerpt_separator: "<!--more-->"
title: 给你的jeklly添点料
categories:
     - study_note
---
### 如何更改theme
- 如何更改一个jeklly的theme呢？其实不一定要去下载模板，在这里就有一个小方法和大家分享一下。就以我们这次的期末项目为例。打开_sass/basically-basic/themes文件夹就可以发现有好几个以“.scss”结尾的文件。这些就是这个项目里自带的一些主题模板。
<!--more-->

![输入图片说明](https://gitee.com/limiaohuang/Mywebsite/raw/gh-pages/assets/images/%E6%95%99%E7%A8%8B2.PNG)

接下来再打开_data/theme.yml。修改skin后的主题名称就大功造成啦。

![输入图片说明](https://gitee.com/limiaohuang/Mywebsite/raw/gh-pages/assets/images/%E6%95%99%E7%A8%8B1.PNG)

### DIY一个自己想要的主题配色
- 可能有些同学不喜欢这些自带的theme。但没关系，我们也可以自己DIY一个。接下来的步骤就跟上面的相反啦。首先，打开_data/theme.yml，看看自己的skin是哪种主题。然后再打开_sass/basically-basic/themes去修改相应的scss文件。

![输入图片说明](https://gitee.com/limiaohuang/Mywebsite/raw/gh-pages/assets/images/%E6%95%99%E7%A8%8B3.PNG)

- 这样就可以创造自己喜欢的theme啦。是不是很简单呢？