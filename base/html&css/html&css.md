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
        - 利用绝对定位，top: 50%;，然后margin-top偏移为 -height/2 px
        - 采用绝对定位，top/bottom/left/right均为0；再加margin:auto;
        - table布局
        - flex布局：align-items/justify-content均设为center
        - transform属性: 相对定位 + top:50%;left:50%; + translate(-50%, -50%);
    2. 水平居中
        - 利用绝对定位，left: 50%;，然后margin-left偏移 -width/2 px
        - 采用绝对定位，top/bottom/left/right均为0；再加margin:auto;
        - table布局
        - flex布局：align-items/justify-content均设为center
        - transform属性: 相对定位 + top:50%;left:50%; + translate(-50%, -50%);

- 252、实现布局：左边一张图片，右边一段文字（不是环绕）
- 261、使用flex布局实现三等分，左右两个元素分别贴到左边和右边，垂直居中

> CSS类
- 21、使用css实现一个三角形

### css实现三角形

```css
.triangle-up {
      width: 0;
      height: 0;
      border-bottom: 20px solid #EEB422;
      border-left: 20px solid transparent;
      border-right: 20px solid transparent;
    }
```

- 70、做过css动画吗
- 118、Css实现动画效果
- 119、Animation还有哪些其他属性
- 121、Css实现保持长宽比1:1
- 138、为什么要用translate3d？  **translate3d 方法可以让浏览器开启GPU硬件加速模式**
- 159、rem是什么？em是什么？如果上一层就是根root了，em和rem等价么？

### rem 和 em

    - em和rem都是相对的字体单位
    - em的值是不固定的，会继承父级元素的字体大小
    - rem是相对root em；只修改根元素就成比例地调整所有字体大小

- 165、怎么在页面里放置一个很简单的图标，不能用img和background-img？
- 174、display有哪些值？说明他们的作用

### display的属性

    - none 此元素不会被显示并且不占用空间
    - block 此元素显示为块级元素，此元素前后会带有换行符
    - inline 默认，此元素会被显示为内联元素，元素前后没有换行符
    - inline-block 行内块元素，前后无换行符
    - inherit 规定应该从父类元素继承display属性的
    - list-item 不设置宽度时，宽度撑满一行，支持宽高

- 175、css定义的权重

### CSS权重

    > 通用选择器（*） < 元素(类型)选择器 < 类选择器 < 属性选择器 < 伪类 < ID 选择器 <内联样式

    - 元素，伪元素：+1
    - 类，伪类，属性：+10
    - ID：+100
    - 内联样式：+1000
    - !important：∞

- 242、position有哪些值,说下各自的作用

### position的属性

    - static
    - relative
    - absolute
    - fixed
    - sticky 粘性定位

```css
{
    <!-- 距离页面顶部大于20px，表现为 position:relative; -->
    <!-- 距离页面顶部小于20px，表现为 position:fixed; -->
    <!-- 运用 position:sticky; 实现导航栏固定，也是最常见的用法 -->
    position: -webkit-sticky;
    position: sticky;
    top: 20px;
}
```

- 257、margin坍塌？水平方向会不会坍塌？ **margin坍塌就是编剧重叠；水平方向margin永远不会重叠**
- 258、伪类和伪元素区别

### 伪元素和伪类的区别

    - 伪类用于当已有元素处于的某个状态时，为其添加对应的样式，这个状态是根据用户行为而动态变化的。
    - 伪元素用于创建一些不在文档树中的元素，并为其添加样式。比如说，我们可以通过:before来在一个元素前增加一些文本，并为这些文本添加样式。虽然用户可以看到这些文本，但是这些文本实际上不在文档树中。

> 浮动和清除浮动
- 125、浮动的原理以及如何清除浮动

### 浮动的原理

    > 浮动元素脱离文档流，不占据空间。浮动元素碰到包含它的边框或者浮动元素的边框停留。

### 清除浮动

#### 清除浮动的原因

    - 父元素的高度无法被撑开，影响与父元素同级的元素与浮动元素同级的非浮动元素（内联元素）会跟随其后
    - 若非第一个元素浮动，则该元素之前的元素也需要浮动，否则会影响页面显示的结构

#### 清除浮动的方式

    - 父级创建BFC清除浮动
    - 使用:after伪元素清除浮动
    - 使用:after :brfore 双伪元素清除浮动
    - 浮动元素下添加额外标签清除浮动

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

    - dom.style.width/height（内联样式）
    - dom.currentStyle.width/height（仅IE支持）
    - window.getComputedStyle(dom).width/height
    - dom.getBoundingClientRect().width/height

#### BFC 块级格式化作用域

> [CSS之BFC详解](http://www.html-js.com/article/1866)

##### BFC特点

    - 内部的Box会在垂直方向，从顶部开始一个接一个地放置
    - Box垂直方向的距离由margin决定。属于同一个BFC的两个相邻Box的margin会发生叠加
    - BFC的区域不会与float box叠加
    - BFC就是页面上的一个隔离的独立容器，容器里面的子元素不会影响到外面的元素，反之亦然
    - 计算BFC的高度时，浮动元素也参与计算

##### 触发BFC

    - float 除了none以外的值
    - overflow 除了visible 以外的值（hidden，auto，scroll )
    - display (table-cell，table-caption，inline-block, flex, inline-flex)
    - position值为（absolute，fixed）
    - fieldset元素

##### BFC应用

    - BFC可以解决边距重叠问题
    - BFC不会与浮动元素重叠 => 用于布局
    - BFC用于清除浮动（计算BFC高度时，浮动元素也会参与计算）

> HTML类
- 126、Html的语义化

> 性能类
- 63、link和@import引入CSS的区别？

### link和@import引入css的区别

1. 从属关系区别：@import是 CSS 提供的语法规则，只有导入样式表的作用；link是HTML提供的标签，不仅可以加载 CSS 文件，还可以定义 RSS、rel 连接属性等
2. 加载顺序：加载页面时，link标签引入的 CSS 被同时加载；@import引入的 CSS 将在页面加载完毕后被加载
3. DOM可控性区别：可以通过 JS 操作 DOM ，插入link标签来改变样式；由于 DOM 方法是基于文档的，无法使用@import的方式插入样式。
4. 兼容性区别：@import是 CSS2.1 才有的语法，故只可在 IE5+ 才能识别；link标签作为 HTML 元素，不存在兼容性问题。

- 198、前端优化你知道哪些
- 238、link和@import有什么区别？
- 245、移动端性能优化
- 250、repaint和reflow区别

### 回流 & 重绘

> 参考[浏览器的回流与重绘 (Reflow & Repaint)](https://juejin.im/post/5a9923e9518825558251c96a?utm_medium=fe&utm_source=weixinqun)
> **结论：回流必将引起重绘，重绘不一定会引起回流**

![回流和重绘](http://newimg88.b0.upaiyun.com/newimg88/2014/08/8_1.jpg)

#### 浏览器渲染流程

    1. 浏览器会把HTML解析成DOM，把CSS解析成CSSOM，DOM和CSSOM合并就产生了Render Tree（Render Tree中不包含display:none的节点，还有head节）
    2. 有了RenderTree，我们就知道了所有节点的样式，然后计算他们在页面上的大小和位置，最后把节点绘制到页面上。
    3. 浏览器使用流式布局，对Render Tree的计算通常只需要遍历一次就可以完成，但table及其内部元素除外，他们可能需要多次计算，通常要花3倍于同等元素的时间，这也是为什么要避免使用table布局的原因之一。

#### 回流

当页面布局和几何属性改变时就需要回流，以下为回流发生的情况：

    1. 添加或者删除可见的DOM元素
    2. 元素位置改变
    3. 元素尺寸改变——边距、填充、边框、宽度和高度
    4. 内容改变——比如文本改变或者图片大小改变而引起的计算值宽度和高度改变
    5. 页面渲染初始化
    6. 浏览器窗口尺寸改变——resize事件发生时

#### 重绘

当页面中元素样式的改变并不影响它在文档流中的位置时，例如：*color*、*background-color*、*visibility*发生改变

#### 回流比重绘的代价要更高，避免的策略

##### CSS

    1. 避免使用table布局。
    2. 尽可能在DOM树的最末端改变class。
    3. 避免设置多层内联样式。
    4. 将动画效果应用到position属性为absolute或fixed的元素上。
    5. 避免使用CSS表达式（例如：calc()）。

##### JS

    1. 避免频繁操作样式，最好一次性重写style属性，或者将样式列表定义为class并一次性更改class属性。
    2. 避免频繁操作DOM，创建一个documentFragment，在它上面应用所有DOM操作，最后再把它添加到文档中。
    3. 也可以先为元素设置display: none，操作结束后再把它显示出来。因为在display属性为none的元素上进行的DOM操作不会引发回流和重绘。
    4. 避免频繁读取会引发回流/重绘的属性，如果确实需要多次使用，就用一个变量缓存起来。
    5. 对具有复杂动画的元素使用绝对定位，使它脱离文档流，否则会引起父元素及后续元素频繁回流。

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