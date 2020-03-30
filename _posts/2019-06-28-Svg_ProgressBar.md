---
layout: page
excerpt_separator: "<!--more-->"
title: 滚动吧！进度条
categories:
  - svg
tags:
  - svg
---
平时我们在等待页面的时候，总会看到一个滚动的小圆圈。想知道这是怎么设置的吗？一起来学一学吧。
<!--more-->

### 制作要点
- stroke-dasharray: 0, 570;，表示线框短划线和缺口的长度分别为 0 和 570，所以一开始整个图形都是被缺口占据，所以在视觉效果上长度为 0。然后过渡到 stroke-dasharray: 400, 400，表示线框短划线和缺口的长度分别为 570 和 570，因为整个图形的长度就是 400，所以整个进度条会被慢慢填充满。
- fill：类比 css 中的 background-color，给 svg 图形填充颜色。
- stroke-width：类比 css 中的 border-width，给 svg 图形设定边框宽度。
- stroke：类比 css 中的 border-color，给 svg 图形设定边框颜色。


#### 进度条例子
<div class="circle-load">
    <svg width="500px" height="240px" viewbox="0 0 440 440" version="1.1" xmlns="http://www.w3.org/2000/svg">
        <circle cx="110" cy="110" r="90" stroke-width="10" stroke="gainsboro" fill="none"></circle>
        <circle cx="110" cy="110" r="90" stroke-width="10" stroke="darkturquoise" fill="none" class="circle-load-svg"></circle>
    </svg>
</div>
<style type="text/css">
.circle-load {
    position: absolute;
    width: 200px;
    height: 200px;
    top: 54%;
    left: 20%;
    transform: translate(-50%, -50%);
}

.circle-load-svg {
    stroke-dasharray: 0 570;
    animation: rot 8s linear infinite;
}

@keyframes rot {
    100% {
        stroke-dasharray: 400 400;
    }
}
</style>







### 相关代码
```markdown
<div class="circle-load">
    <svg width="500px" height="240px" version="1.1" xmlns="http://www.w3.org/2000/svg">
        <circle cx="110" cy="110" r="90" stroke-width="10" stroke="gainsboro" fill="none"></circle>
        <circle cx="110" cy="110" r="90" stroke-width="10" stroke="darkturquoise" fill="none" class="circle-load-svg"></circle>
    </svg>
</div>
<style type="text/css">
.circle-load {
    position: absolute;
    width: 200px;
    height: 200px;
    top: 60%;
    left: 60%;
    transform: translate(-50%, -50%);
}

.circle-load-svg {
    stroke-dasharray: 0 570;
    animation: rot 8s linear infinite;
}

@keyframes rot {
    100% {
        stroke-dasharray: 400 400;
    }
}
</style>
```

