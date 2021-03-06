# learn_Html_Css_JavaScript


01. Html
    - 常见元素
        - header内部元素
            01. mata
            02. title
            03. style
            04. link
            05. script
            06. base
        - body内部元素
            01. div/section/article/aside/header/footer
            0
            04. table/thead/tbody/tr/th/td
            05. ul/li,ol/li,dl/dt/dd
            06. a
            07. form/input/select/textarea/button/label
            08. img
    - 版本
        01. HTML4/4.01(SGML)
        02. XHTML
        03. HTML5
            - 部分新增区块标签
                01. section (区域)
                02. article (区域)
                03. aside   (不重要的内容)
                04. nav     (导航)
                05. header  (头)
                06. footer  (尾)
            - 表单增强
                01. 日期, 时间, 搜索
                02. 表单验证
                03. placeholder, 自动聚焦(autofocus)

    - 元素分类
        01. 按默认样式分类
            - 块级元素
            - 行内元素
            - 行内块级元素
        02. 按内容分类
    - 元素嵌套关系
        01. 块级元素包含行内元素
        02. 块级元素不一定能包含块级元素
        03. 行内一般不能包含块级元素
            - a 元素可以用来包含块级元素
    - 元素默认样式和定制化
        01. 标签自带一些样式, 就是标签的默认样式
        02. 可是使用Css Reset 来清楚css的默认样式
        03. Normalize.css 的使用
    - 面试真题解答
        01. doctype的意义是什么?
            - 让浏览器以标准的模式渲染, 避免各浏览器的兼容性问题

        02. HTML, XHTML, HTML5 的关系
            - HTML  属于 SGML
            - XHTML 属于 XML, 是 HTML进行XML严格化的结果
            - HTML5 不属于 SGML 或 XML, 比XHTML宽松

        03. HTML5有什么变化?
            - 新的语义化元素
            - 表单增强
            - **新的API(离线, 音视频, 图形, 实时通信, 本地存储, 设备能力)**
            - 分类和嵌套变更
            - a元素被允许包裹块级元素

        04. em和i有什么区别?
            - em是语义化的标签, 表强调
            - i是纯样式标签, 表示斜体

        05. 语义化的意义是什么?
            - 开发者容易理解
            - 极其容易理解结构(搜索, 读屏软件)
            - 有助于 SEO

        06. 哪些元素可以自闭合
            - 表单元素 input
            - 图片 img
            - br,hr
            - meta, link

        07. HTML 和 DOM 的关系
            - HTML 是 '死' 的
            - DOM 是有 HTML 解析而来的, 是活的
            - JS 可以用来维护 DOM

        08. property 和 attribute 的区别
            - attribute 是 '死' 的
            - property 是 attribute 解析之后出来的

        09. form的作用有哪些
            - 直接提交表单
            - 使用 submit/reset 按钮
            - 便于浏览器保存表单
            - 第三方库可以整体提取值
            - 第三方库可以进行表单验证

    - [html的机构大纲算法工具](https://github.com/h5o/h5o.github.io)

02. Css(层叠样式表)
    01. [选择器](./01.Css基础/01.选择器优先级测试.html)
        - 用于匹配HTML元素
        - 分类和权重
        - 解析方式和性能
        - 值得关注的选择器
    ```
        选择器:{
          属性:值;
          属性:值;
        }
        浏览器解析选择器的时候, 是从右往左解析, 加快浏览器提高对css的解析速度
        01. 选择器的分类:
            01. 元素选择器 a{}
            02. 伪元素选择器 ::before{}
            03. 类选择器 .link{}
            04. 伪类选择器 :hover{}
            05. 属性选择器 [type=radio]{}
            06. ID选择器 #id{}
            07. 组合选择则器 [type=radio]+label{}
            08. 否定选择器 :not(.link){}
            09. 通用选择器 *{}

        02. 选择器的权重
            01. ID选择器 #id{}  +100
            02. 类, 属性, 伪类   +10
            03. 元素, 伪元素     +1
            04. 其他选择器       +0
            05. !important 优先级最高
            06. 行内样式 优先级高
            07. 相同权重, 后写的生效
    ```
    02. 非布局样式
        01. 字体, 字重, 颜色, 大小, 行高
            01. [字体](./01.Css基础/02.自定义字体.html)
                - 字体族 font-family:'Microsoft Yahei',serif(衬线字体族),font-family:monospace(等宽字体族);
                - 多字体fallback
                - 网络字体, 自定义字体
                - iconfont
            02. [行高](./01.Css基础/03.行高.html)
                - 行高的构成
                - 行高相关的现象和方案
                - 行高的调整
        02. 背景, 边框
            01. 背景
                - [背景颜色](./01.Css基础/04.背景颜色.html)
                - [渐变背景色](./01.Css基础/05.渐变背景色.html)
                - [多背景叠加](./01.Css基础/06.多背景叠加.html)
                - [背景图片和属性(雪碧图)](./01.Css基础/07.背景图片和属性(雪碧图).html)
                - base64和性能优化(一般用于小图标)
                    - 减少http请求
                    - 增加了文件的大小
                    - 增大了解码的开销
                - 多分辨率适配
            02. [边框](./01.Css基础/08.边框.html)
                - 边框的属性: 线型, 大小, 颜色
                - 边框背景图
                - 边框衔接(三角形)
        03. 滚动, 换行
            01. [滚动](./01.Css基础/09.滚动.html)
                - 滚动的行为和滚动条
        04. 粗体, 斜体, 下划线
    03. Css Hack
        01. Hack即不合法但是生效的写法
        02. 主要用于区分不同浏览器
        03. 缺点: 难理解, 难维护, 易失效
        04. 代替方案
            - 特性检测
            - 针对性加class

    04. Css布局
        01. float + margin
            - 元素浮动
            - 脱离文档流,但是不会脱离文本流
            - 使用float属性,该元素会形成一个'块'
            - 若父级高度没有其他高度将其撑开, 那么就会产生父级高度塌陷
        02. inline - block
            - 像文本一样排block元素
            - 需要处理间隙-将父元素的字体设置为0, 可以处理
        03. flex
            - 弹性盒子
            - 使用之后, 子盒子自动并列
            - 指定宽度即可
        04. grid
        - 盒模型
            01. content  => width + height
            02. padding
            03. border
            04. margin 距离周围元素的距离
            05. 盒子占用空间: content + border + padding
        05. 响应式的布局和设计
            - 在不同的设备上正常使用
            - 一般主要处理屏幕大小问题
            - 主要方法:
                01. 隐藏 + 折行 + 自适应空间
                02. rem/ viewport/ media query
    05. Css预处理器-less
        - 嵌套
        - 变量 @fontSize:12px, 变量需要带单位的就带上单位, 运算的时候也要带单位
            - 通常是公共同一个值的时候使用变量, 在后期变更的时候, 易于修改
        - mixin .fontSize(@color){}
            - 通常在css层面就完成了复用, 不需要到html里面再去引用这个类
        -
    99. Css面试题
        - css样式(选择器)的优先级?
        - 雪碧图的作用?
        - 自定义字体的使用场景?
        - base64的使用?
        - 伪元素和伪类的区别?
        - 如何美化checkbox?
        - 实现两栏(三栏)布局的方法?
        - position:relative/absolute/fixed有什么区别?
        - display:inline-block的间隙怎么处理?
        - 如何清除浮动, 为什么清除浮动?
        - 如何适配移动端的页面?



03. JavaScript
    01. typeof 运算符
        - 注意: **只能用来区分值类型,但是除了函数**
        - typeof undefined => undefined
        - typeof 'abc' => string
        - typeof 123 => number
        - typeof true => boolean
        - typeof {} => object
        - typeof [] => object
        - typeof null => object
        - typeof console.log => function
    02. 变量计算-强制类型转换
        - 字符串的拼接
            - let a = 10 + 20 => 30
            - let a = 10 + '20' => 1020
        - == 运算符
            - 100 == '100' => true
            - 0 == '' => true
            - null == undefined => true
        - if语句
            - if(true){}
            - if(100){}
            - if(''){}
        - 逻辑运算
            - 10&&0 => 0
            - '' || 'abc' => 'abc'
    03. instanceof
        - 用于判断**引用类型**属于哪个**构造函数**的方法
    04. 函数
        - 函数表达式 let fun = function(){}
        - 函数声明   function fun(){} => 函数声明提升

    99. JavaScript面试题
        - JS中使用typeof能得到的哪些类型?(变量类型)
        - 何时使用===何时使用==?(强制类型转换)
        - window.onload 和 DOMContentLoaded 的区别?(浏览器的渲染过程)
        - 用JS创建10个< a > 标签, 点击的时候弹出对应的序号(作用域)
        - 简书如何实现一个 **模块加载器**, 实现类似 require.js 的基本功能.(JS模块化)
        - 实现数组的随机排序.(JS的基础算法)
        - JS中有哪些内置函数
        - 如何准确判断一个变量是数组类型
        - 写一个原型链继承的例子
        - 描述new一个对象的过程
        - zepto(或其他框架) 源码中如何使用原型链
        - 说一下变量提升的理解
        - 说明this集中不同的使用场景
        - 如何理解作用域
        - 实际开发中闭包的应用
