# HTML&CSS

```markdown
配合[前端面试300题](https://zhuanlan.zhihu.com/p/28911400) 使用更佳
```

> ## Q1：布局类问题

- 7、基本的两列自适应布局

----

### flex布局

1. flex布局子元素的float、clear、vertical-align失效
2. flex容器（flex container）&flex项目（flex item）
3. flex container的属性
    - flex-direction: row | row-reverse | column | column-reverse;主轴方向
    - flex-wrap: nowrap | wrap | wrap-reverse;如果一条轴线排不下，如何换行
    - flex-flow: <flex-direction> || <flex-wrap>;flex-direction属性和flex-wrap属性的简写形式
    - justify-content: flex-start | flex-end | center | space-between | space-around;主轴上对齐方式
    - align-items:  flex-start | flex-end | center | baseline | stretch;交叉轴上对齐方式
    - align-content:  flex-start | flex-end | center | space-between | space-around | stretch;多根轴线的对齐方式
4. flex item的属性
    - order: <integer>; order属性定义项目的排列顺序。数值越小，排列越靠前，默认为0。
    - flex-grow: <number>; flex-grow属性定义项目的放大比例，默认为0，即如果存在剩余空间，也不放大。**按比例分时，此项属性很有用**
    - flex-shrink：<number>; flex-shrink属性定义了项目的缩小比例，默认为1，即如果空间不足，该项目将缩小。
    - flex-basis: flex-basis: <length> | auto; flex-basis属性定义了在分配多余空间之前，项目占据的主轴空间（main size）。
    - flex: none | [ <'flex-grow'> <'flex-shrink'>? || <'flex-basis'> ]; flex属性是flex-grow, flex-shrink 和 flex-basis的简写，默认值为0 1 auto。
    - align-self: auto | flex-start | flex-end | center | baseline | stretch; align-self属性允许单个项目有与其他项目不一样的对齐方式，可覆盖align-items属性。

### grid布局

1. grid容器（grid container） & grid项目（grid item）
2. **grid-auto-flow**: row/column;网格默认流方向是row，可以通过grid-auto-flow属性把网格流的方向改变成column
3. grid-template-rows: 60px 40px; grid-template-rows设置行高
4. grid-template-columns: 40px 50px 60px; grid-template-columns设置列宽
5. grid-column-gap: 创建列与列之间的间距
6. grid-row-gap: 创建行与行之间的间距
7. grid中单位fr; “fr”单位允许您将轨道大小设置为网格容器自由空间的一部分。

- 54、实现一个布局：左边固定宽度为200，右边自适应，而且滚动条要自动选择只出现最高的那个
- 92、做一个两栏布局，左边fixed width，右边responsive，用纸笔手写
- 101、css 布局，左边定宽右边自适应
- 120、Css实现三列布局
- 122、Css实现两个自适应等宽元素中间空10个像素
- 169、绝对定位与相对定位的区别
- 173、如何让各种情况下的div居中(绝对定位的div,垂直居中,水平居中)？

### 水平、垂直居中

1. 垂直居中
    1. 利用绝对定位，top: 50%;，然后margin-top偏移为 -height/2 px
    2. 采用绝对定位，top/bottom/left/right均为0；再加margin:auto;
    3. table布局
    4. flex布局：align-items/justify-content均设为center
    5. transform属性: 相对定位 + top:50%;left:50%; + translate(-50%, -50%);

2. 水平居中
    1. 利用绝对定位，left: 50%;，然后margin-left偏移 -width/2 px
    2. 采用绝对定位，top/bottom/left/right均为0；再加margin:auto;
    3. table布局
    4. flex布局：align-items/justify-content均设为center
    5. transform属性: 相对定位 + top:50%;left:50%; + translate(-50%, -50%);

- 252、实现布局：左边一张图片，右边一段文字（不是环绕）
- 261、使用flex布局实现三等分，左右两个元素分别贴到左边和右边，垂直居中

> CSS类
- 21、使用css实现一个三角形
- 70、做过css动画吗
- 118、Css实现动画效果
- 119、Animation还有哪些其他属性
- 121、Css实现保持长宽比1:1
- 138、为什么要用translate3d？  **translate3d 方法可以让浏览器开启GPU硬件加速模式**
- 159、rem是什么？em是什么？如果上一层就是根root了，em和rem等价么？
- 165、怎么在页面里放置一个很简单的图标，不能用img和background-img？
- 174、display有哪些值？说明他们的作用
- 175、css定义的权重
- 242、position有哪些值,说下各自的作用
- 257、margin坍塌？水平方向会不会坍塌？
- 258、伪类和伪元素区别

> 浮动和清除浮动
- 125、浮动的原理以及如何清除浮动
- 205、清除浮动有哪几种方式,分别说说

> 盒模型
- 55、画出盒子模型，要使谷歌浏览器的盒子模型显示得跟IE浏览器一致（让谷歌跟ie一致，不是ie跟谷歌一致），该怎么做？
- 78、盒子模型
- 83、知不知道CSS Box-model？
- 100、css 盒模型
- 108、css:两个块状元素上下的margin-top和margin-bottom会重叠。啥原因？怎么解决？

### CSS盒模型

#### 标准模型&IE模型：区别在于计算width/height的方法不同

#### 标准模型（box-sizing:content-box） IE模型（box-sizing:border-box）

#### JS获取盒模型宽&高

- ```dom.style.width/height```（内联样式）
- ```dom.currentStyle.width/height```（仅IE支持）
- ```window.getComputedStyle(dom).width/height```
- ```dom.getBoundingClientRect().width/height```

#### BFC 块级格式化作用域

> [CSS之BFC详解](http://www.html-js.com/article/1866)

- BFC可以解决边距重叠问题
- BFC不会与浮动元素重叠
- BFC用于清除浮动（计算BFC高度时，浮动元素也会参与计算）

> HTML类
- 126、Html的语义化

> 性能类
- 63、link和@import引入CSS的区别？
- 198、前端优化你知道哪些
- 238、link和@import有什么区别？
- 245、移动端性能优化
- 250、repaint和reflow区别
- 288、浏览器如何实现图片缓存

> 新特性
- 74、css3 html5新特性

> 兼容性
- 64、刚才说有些浏览器不兼容@import，具体指哪些浏览器？
- 77、兼容性

> 综合类
- 89、输入URL后发生了什么？
- 217、让你设计一个前端css框架你怎么做
- 247、点透问题
- 287、页面加载过程