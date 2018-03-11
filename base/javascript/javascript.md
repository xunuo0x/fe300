# JavaScript

```markdown
配合[前端面试300题](https://zhuanlan.zhihu.com/p/28911400) 使用更佳
```

> ## Q1：Ajax/Jsonp

1、手写jsonp的实现
22、用promise手写ajax
43、手写一个原生ajax
44、手写一个promise版的ajax
45、手写实现一个promise
84、如何做一个AJAX Request？
93、讲一下AJAX Request
106、ajax，原生ajax的四个过程

### 原生Ajax

    - 创建XMLHttpRequest对象
    - 连接到服务器 xhr.open()
    - 发送请求 xhr.send()
    - 接收返回值，监听onReadyStateChange事件

128、Jsonp的原理。怎么去读取一个script里面的数据？

### jsonp（Json Padding）

    - 动态添加script标签，因为script标签没有跨域限制
    - 客户端注册callback，将callback函数名作为参数传至服务器
    - 注册全局函数，服务器返回结果执行此全局函数
    - 执行后，删除标签，同时将全局函数置为null


192、ajax的过程以及 readyState几个状态的含义
228、你所了解的跨域的方法都说说看你了解的？

> ## Q2：算法类

2、手写链表倒数第K个查找
10、解释平衡二叉树，以及在数据结构中的应用（红黑树）
11、快排的时间复杂度和空间复杂度
14、手写一个递归函数
19、关于平衡二叉树
27、手写第一次面试没有写出来的链表问题，要求用es6写
33、手写一个简单遍历算法
40、手写归并排序
42、实现两个数组的排序合并
105、继承的两种方法
109、js：写一个递归。就是每隔5秒调用一个自身，一共100次
214、你学过算法没,说说你都了解些什么
215、说下选择排序,冒泡排序的实现思路
286、算法题：数组去重，去除重复两次以上的元素，代码题：嵌套的ul-li结构，根据input中输入的内容，去除相应的li节点，且如果某个嵌套的ul下面的li都被移除，则该ul的父li节点也要被移除

> ## Q3：原型链

4、原型链的解释
90、new operator实际上做了什么？
91、面向对象的属性有哪些？
104、原型链
208、使用 new操作符时具体是干了些什么

> ## Q4：JavaScript基础

6、基本的数据类型
38、手写一个js的深克隆
82、如何用Native JavaScript来读写Cookie？
127、原生js添加class怎么添加，如果本身已经有class了，会不会覆盖，怎么保留？
231、一来给了张纸要求写js自定义事件
255、setTimeout和setInterval区别，如何互相实现？
285、Object.defineProperty

> ## Q5：数组操作

79、Array的unshift() method的作用是什么？如何连接两个Array？如何在Array里移除一个元素？
132、数组去除一个函数。用arr.splice。又问splice返回了什么？应该返回的是去除的元素。

> ## Q6：闭包

5、对闭包的理解，实现一个暴露内部变量，而且外部可以访问修改的函数
80、用纸笔写一个Closure，任意形式和内容
107、闭包，简单说一个闭包的应用，然后闭包的主要作用是什么
243、写个从几个li中取下标的闭包代码

> ## Q7：DOM类

102、冒泡和捕获，事件流哪三个阶段？
103、实现事件代理
117、事件代理js实现
183、w3c事件与IE事件的区别

> ## Q8：正则表达式

167、怎么去除字符串前后的空格
166、正则表达式判断url
手机号

> ## Q9：this

225、js中this的作用
226、js中上下文是什么
227、js有哪些函数能改变上下文
233、call与apply的区别

> ## Q10：ES6

178、ES6里头的箭头函数的this对象与其他的有啥区别

> ## Q11：Cookie、Session一类

65、介绍一下cookie,localstorage,sessionstorage,session
116、Cookie 是否会被覆盖，localStorage是否会被覆盖

    - cookie会被覆盖；
    - localStorage类似于sessionStorage；区别在于生命周期不同

129、如果页面初始载入的时候把ajax请求返回的数据存在localStorage里面，然后每次调用的时候去localStorage里面取数，是否可行。

    - 无法保证数据的实时性；请求和实时性需要取舍

194、cookie与session的区别
222、浏览器缓存的区别

### 浏览器缓存：强缓存&协商缓存

    - 强缓存

    ![强缓存](https://camo.githubusercontent.com/ee0025892ed1350c27caa0ed5d2af441aea6ca49/687474703a2f2f6f6d75666a723562762e626b742e636c6f7564646e2e636f6d2f2545352542432542412545372542432539332545352541442539382e706e67)

    - 协商缓存

    ![协商缓存](https://camo.githubusercontent.com/109cdc67eda2ad3dbbfa0c35971d1d18559ef5ff/687474703a2f2f6f6d75666a723562762e626b742e636c6f7564646e2e636f6d2f2545352538442538462545352539352538362545372542432539332545352541442539382e706e67)

    1.看看是否命中强缓存，如果命中直接使用缓存
    2.如果没有命中强缓存，请求服务器是否命中协商缓存
    3.如果命中协商缓存，服务器返回**304**告诉浏览器使用本地缓存
    4.否则，返回最新资源

239、cookies(4K)，sessionStorage(5M) 和 localStorage(5M) 的区别

    - localStorage中存储的的数据没有过期的限制，sessionStorage在会话结束后会被清除
    - cookie由服务端生成，用于标识用户，每次都会携带在HTTP头
    - storage用于浏览器缓存，不参与和服务器的通信
    - session存在服务端，cookie存在客户端浏览器
    - 安全考虑使用session

> ## Q12：插件开发

12、手写一个jQuery插件
170、js轮播实现思路
249、原生js模板引擎

> ## Q13：框架类

13、在jquery方法和原型上面添加方法的区别和实现，以及jquery对象的实现
66、jquery绑定click的方法有几种

> ## Q14：计算机网络

9、OSI模型，HTTP,TCP,UDP分别在哪些层

![网络模型](http://markdown-1253575843.coscd.myqcloud.com/%E5%BE%AE%E4%BF%A1%E5%9B%BE%E7%89%87_20180311223850.png)

111、网络分层结构
130、304是什么意思？有没有方法不请求不经过服务器直接使用缓存
131、http请求头有哪些字段
179、tcp/udp区别
180、tcp三次握手过程
HTTPS
202、说下你知道的响应状态码
223、304与200读取缓存的区别
224、http请求头有哪些,说说看你了解哪些
267、http状态码。。。401和403区别？

> ## Q15：Node.js

37、介绍node.js，并且介绍你用它做的项目
99、nodejs的架构、优缺点、回调
237、nodejs中的文件怎么读写？

> ## Q16：前端安全类

85、Cross-domain access有没有了解？
181、xss与csrf的原理与怎么防范

> ## Q17：requireJS、commonJS、AMD

46、手写实现requireJS模块实现
49、AMD和CMD，commonJS的区别
123、requireJS的原理是什么
136、commonJS和AMD
176、requirejs实现原理
177、requirejs怎么防止重复加载
251、requirejs如何避免循环依赖？

> ## Q18：异步

133、js异步的方法（promise，generator，async）
148、js的异步加载，promise的三种状态，ES7中的async用过么

> ## Q19：数据结构

211、你学过数据结构没,说说你都了解些什么
264、数组和链表区别，分别适合什么数据结构

> ## Q20：计算机操作系统

212、你学过计算机操作系统没,说说你都了解些什么

> ## Q21：计算机组成原理

213、你学过计算机组成原理没,说说你都了解些什么

> ## Q22：设计模式

218、了解哪些设计模式说说看
219、说下你所了解的设计模式的优点
229、要是让你自己写一个js框架你会用到哪些设计模式
230、平常在项目中用到过哪些设计模式,说说看

> ## Q23：H5 API

234、h5有个api能定位你知道是哪个吗？
