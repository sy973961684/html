# html

## HTML 叫做超文本标记语言

HTML 文档是由无数个标记（标签、tag）组成
由标签和内容组成的称为元素（element）
一般的说法: head 元素、`<head>`标签, img 元素、`<img>`标签
html、head、meta、title、body、img、div、ul、ol、li、br、input 都是组成 HTML 文档的元素

超文本（Hyper Text）？
页面内可以包含图片、链接、甚至音乐、视频等非文字元素

## 常用元素

- 区块: div
- 区分: span
- 文本: p、h1~h6、em、dt、dd、
- 表格: table、tbody、thead、tr、td、th、tfoot、caption
- 表单: from、input、label、textarea、select
- 链接: a
- 图片: img
- 文档: html、head、title、body、meta
- 列表: ul、ol、li、dl、dt、dd、footer、nav
- 其他: br、hr、iframe
- 结构: header、section、a、strong、pre、address、q、blockquote、cite、code

## 元素的属性

- 每一个元素都可以拥有自己的属性,属性可以增强元素的功能
- 书写格式是: <起始标签 属性名="属性值">
- 属性名都是小写,而且是无序的
- 属性值可以使用双引号或单引号,也可以省略引号,建议统一使用双引号
- 有一些属是公共的,每一个元素都可以设置,比如 class、id、title 属性
- 有写属性是元素特有的,不是每一个元素都可以设置,比如 meta 元素的 charset 属性、img 元素的 alt 属性等

## 1.1 html 元素

- html 元素是 HTML 文档的根元素,一个文档中只能有一个,其他所有元素都是它的后代元素
- W3C 标准建议为 html 元素增加一个 lang 属性,作用是帮助语音合成工具确定要使用的发音,帮助翻译工具确定要使用的翻译规则
- lang="en"告诉浏览器: 这个 HTML 文档的语言是英文,所有 Chrome 浏览器的有翻译提示
- lang="zh"表示这个 HTML 文档的语言是中文
- h 元素有助于网站的 SEO(Search Engine Optimization)优化,可以促进关键词排名
- div 元素一般作为其他元素的父容器,把其他元素包住,代表一个整体
- div 元素把网页分割为多个独立的部分
- 尝试给网站添加这个样式试试`div { outline: 2px solid red !important}`
- 一般情况下,英文字体只适用于英文,中文字体同时适用于英文和中文
- 所以,如果希望中英文分别使用不同的字体,应该先将英文字体写在前面,中文字体写在后面
- line-height 用于设置文本的最小高度
- 行高可以先简单的理解为一行文字所占据的高度
- 行高的严格定义: 两行文字基线(baseline)之间的间距
- 基线: 与小写字母 x 最底部对齐的线
- height 是指元素整体的高度,line-height 元素中每一行文字所占据的高度
- font
- :nth-last-child(1) 代表倒数第 1 个子元素
- :nth-last-child(-n+2) 代表最后 2 个子元素
- :first-child = nth-child(1)
- :last-child = nth-last-child(1)
- :first-of-type = nth-of-type(1)
- :last-of-type = nth-last-of-type(1)
- :only-child 是父元素中唯一的子元素
- :only-of-type 是父元素中唯一的这种类型的子元素
- :root 根元素 就是 HTML 元素
- :not()的格式是:not(x)
- :x 是一个简单的选择器
- :not(x) 表示除 x 以外的元素
- 元素选择器 通用选择器 属性选择器 类选择器 id 选择器 伪类(除否定伪类)
- 常用的伪元素
- :first-line ::first-line
- :first-letter ::first-letter
- :before ::before
- :after ::after

## day03 内容概述

## 一. 伪类和伪元素

### 1.1 伪类

- target:目标转换
- 元素状态伪类: disabled/enable/checked(input)

  - 动态伪类:

    - link
    - visited:a
    - focus:a 和 input
    - hover 其他元素
    - active 其他元素

  - 结构伪类

    - nth-child
    - 数字
    - n -> 2n -> -n+5
    - p:nth-child(3)
    - nth-last-child
    - 从后往前数
    - nth-of-type
    - 相同类型
    - 如果类型不同,忽略
    - nth-last-of-type
    - 从后向前数
    - first-child
    - last-child
    - first-of-type
    - last-of-type
    - only-child
    - empty
    - root

  - 否定伪类

    - 特殊场景下用否定伪类
    - class 不香吗?

### 1.2 伪元素

- first-line
- first-letter
- before
- after
- 建议:使用两个冒号

### 1.3 Emmet 语法

- `html5和!`
- `>和+`
- `*和^和()`
- `属性id/class/普通`
- `内容{}`
- `$`
- `隐式标签 div ul>.item table>.row>.content`
- `css emmet语法`

## day04 内容概述

## 一. CSS 特性

### 1.1 继承

- CSS 中有些属性是可继承的,何为属性的继承?

  - 一个元素中如果没有设置某属性的值,就会跟随父元素的值
  - 比如 color font-size 等属性都是可以继承的
  - 哪些属性可以继承,多去查官网
  - 不能继承的属性,一般可以使用 inherit 值来强制继承
  - 浏览器的开发者工具也会标识出哪些样式是继承过来的(inherited for div)
  - 注意点
    - CSS 属性值继承的是计算值,并不是当初编写属性时的指定值(字面值)

- CSS 允许多个相同名字的 CSS 属性层叠在同一个元素上

  - 层叠后的结果是: 只有一个 CSS 属性会生效
  - 浏览器的开发者工具非常清晰地显示了哪个 CSS 会生效\
  - 哪个 CSS 属性会生效,取决于 CSS 属性所处环境的优先级高低
  - 按照经验,为了方便比较 CSS 属性的优先级,可以给 CSS 属性所处的环境定义一个权重
    - `!important:1000`
    - `内联样式:1000`
    - `id选择器:100`
    - `类选择器、属性选择器、伪类:10`
    - `元素选择器、伪元素:1`
    - `通配符:0`
  - 比较优先级的严谨方法
    - 从权重最大的开始比较每一种权值的数量多少,数量多的则优先级高,即可比较结束
    - 如果数量相同,比较下一个较小的权值,以此类推
    - 如果所有的权值比较完毕后,发现数量都相同,就采取"就近原则"

- CSS 属性使用经验
  - 为何有时候编写的 CSS 属性不好使,有可能是因为:
    - 选择器的优先级太低
    - 选择器没选中对应的元素
    - CSS 属性的使用形式不对
    - 元素不支持此 CSS 属性,比如 span 默认是不支持 width 和 height 的
    - 浏览器不支持此 CSS 属性,比如旧版本的浏览器不支持 CSS3 的某些特性
    - 被同类型的 CSS 属性覆盖,比如 font 覆盖 font-size
  - 建议
    - 充分利用浏览器的开发者工具进行调试(增加、修改样式)、查错

## 二. HTML-列表元素

### 1.1 列表

- 有序列表
  - ol(ordered list),直接子元素只能是 li
  - li(list item),列表中的每一项
- 无序列表
  - ul(unordered list),直接子元素只能是 li
  - li(list item),列表中的每一项
- 定义列表
  - dl( definition list),定义列表,直接子元素只能是 dt、dd
  - dt( definition term),列表中每一项的项目名
  - dd( definition description),列表中每一项的具体描述,是对 dt 的描述、解释、补充
- dt、dd 常见的组合
  - 事务的名称、事务的描述
  - 问题、答案
  - 类别名、归属于这类的各种事务
- 列表相关的常见 CSS 属性有 4 个
  - list-style-type: 设置 li 元素前面标记的样式(none|disc|circle|square|decimal|lower-roman|upper-roman|lower-alpha|upper-alpha)
  - list-style-image: 设置某张图片为 li 元素前面的标记,会覆盖 list-style-type 的设置
  - list-style-position: 设置 li 元素前面标记的位置,可以取 outsize、inside2 个值
  - list-style: 是 list-style-type、list-style-image、list-style-position 的缩写属性
  - list-style: outside url("images/dot.png")
  - 他们都可以继承,所以设置给 ol、ul 元素,默认也会应用到 li 元素
  - 一般最常用的还是设置为 none,去掉 li 元素前面的默认标记 list-style:none;

## 三. HTML-表格元素

- table 表格
  - border: 边框的高度
  - cellpadding: 单元格内部的间距
  - cellspacing: 单元格之间的间距
  - width: 表格的宽度
  - align: 表格的水平对齐方式 left|center|right
- tr(table row): 表格中的行
  - valign: 单元格的垂直对齐方式 top|middle|bottom|baseline
  - align: 单元格的水平对齐方式 left|center|right
- td(table description): 行中的单元格
  - valign: 单元格的垂直对齐方式 top|middle|bottom|baseline
  - align: 单元格的水平对齐方式 left|center|right
  - width: 单元格的宽度
  - height: 单元格的高度
  - rowspan: 单元格可横跨的行数
  - colspan: 单元格可横跨的列数
- tbody 表格的主体
- caption: 表格的标题
- thead: 表格的头部
- tfoot: 表格的页脚
- th: 表格的表头单元格

## 单词

- inherited: 继承
- vertical: 垂直的
- horizontal: 水平的

## day05 内容概述

## 一.表单元素

- form 表单
  - 一般情况下,其他表单相关元素都是它的后代元素
- input

  - 单行文本输入框、单选框、复选框、按钮等元素
  - type: input 的类型
  - text: 文本输入框(明文输入)
  - password: 文本输入框(密文输入)
  - radio: 单选框
  - checkbox: 复选框
  - button: 按钮
  - reset: 重置
  - submit: 提交表单数据给服务器
  - file: 文件上传
  - 常用的属性
    - maxlength: 允许输入的最大字数
    - placeholder: 占位字符
    - readonly: 只读
    - disabled: 禁用
    - checked: 默认被选中,只有当 type 为 radio 和 checkbox 时可用
    - autofocus: 当页面加载时,自动聚焦
    - name: 名字,在提交数据给服务器时,用于区分数据类型
    - value: 取值,发送给服务器
    - form: 设置所属的 from 元素(填写 form 元素的 id),一旦设置了此属性,input 元素即使不在 from 元素内部,它的数据也可以提交给服务器
  - 布尔属性(boolean attributes)
    - 布尔属性可以没有属性值,写上属性名就代表使用这个属性
    - 常见的不二属性有 disabled checked readonly multiple autofocus selected
    - 如果要给布尔属性设值,值就是属性名本身

- textarea
  - 多行文本框
- select、option
  - 下拉选择框
- button
  - 按钮
- label
  - 表单元素的话题
- fieldset
  - 表单元素组
- legend

  - fieldset 的标题

- 表单提交

  - 1 传统方式
    - 将所有的 input 包裹到一个 form 中
    - form 设置 action(服务器的地址)
    - input/button 类型是 submit
    - 点击 submit,自动将所有的数据提交给服务器
    - 弊端 1: 会进行页面的跳转,意味着服务器必须将一个页面写好,并且返回给前端,前段直接展示这个页面
    - 服务端提前将页面写好: 服务端渲染
    - 弊端 2: 不方便进行表单数据的验证
  - 2 前后端分离
    - 通过 JavaScript 获取到所有的表单内容
    - 通过正则表达式进行表单的验证
    - 发送 ajax 请求,将数据发送给服务器
    - 验证成功后,服务器会返回结果,需要前端解析这个结果,并且决定显示什么内容(前端渲染和前端路由)
  - 3 get
    - 在请求 URL 后面以?的形式跟上发给服务器的参数,多个参数之间用&隔开
    - 由于浏览器和服务器对 URL 长度有限制,因此在 URL 后面附带的参数是有限制的,通常不超过 1KB
  - 4 post
    - 发送给服务器的参数全部放在请求体中
    - 理论上,post 传递的数据量没有限制(具体还得看服务器的处理能力)
  - 5 enctype
    - 固定了向服务器发送表单数据之前如何对数据进行编码
    - 取值有 3 种
      - application/x-www-form-urlencoded: 默认的编码方式
      - multipart/form-data: 文件上传时必须为这个值,并且 method 必须是 post
      - text/plain: 普通文本传输
  - 6 accept-charset
    - 规定表单提交时使用的字符编码(默认值 UNKNOWN,和文档相同的编码)

## 二.元素类型

- 元素类型

  - 根据元素的显示类型(能不能在同一行显示),HTML 元素可以主要分为 2 大类
    - 1 块级元素(block-level elements)
      - 独占父元素一行
      - 比如 div p pre h1~h6 ul ol li dl dt dd table form article aside footer header hgroup main nav section blockquote hr 等
    - 2 行内级元素(inline-level elements)
      - 多个行内级元素可以在父元素的同一行显示
      - 比如 a img span strong code iframe label input button canvas embed object video audio 等
  - 根据元素的内容(浏览器是否会替换掉元素)类型,HTML 元素主要可以分为 2 大类
    - 1 替换元素(replaced elements)
      - 元素本身没有实际内容,浏览器根据元素的类型和属性,来决定元素的具体显示内容
      - 比如 img input iframe video embed canvas audio object 等
    - 2 非替换元素(non-replaced elements)
      - 和替换元素相反,元素本身是有实际内容的,浏览器会直接将其内容显示出来,而不需要根据元素的类型和属性来判断到底显示什么内容
      - 比如 div p pre h1~h6 ul ol li dl dt dd table form article aside footer header hgroup main nav section blockquote hr a strong span code label 等

- display 属性
  - CSS 中有个 display 属性,能修改元素的显示类型,有 4 个常用值
    - block: 让元素显示为块级元素
    - inline: 让元素显示为行内级元素
    - none: 隐藏元素
    - inline-block: 让元素同时具备行内级、块级元素的特征,对外来说,它是一个行内级元素,对内来说,它是一个块级元素
    - table: `<table>`,一个 block-level 表格
    - inline-table: `<table>`,一个 inline-table 表格
    - table-row: `<tr>`
    - table-row-group: `<tbody>`
    - table-header-group: `<thead>`
    - table-footer-group: `<tfoot>`
    - table-cell: `<td> <th>`,一个单元格
    - table-caption: `<caption>`,表格的标题
    - list-item: `<li>`

## 三.盒子模型

- 触发 BFC
  - BFC: block format context
  - 结界
- 如何触发 BFC
  - 浮动可以触发
  - 设置元素的 overflow 为非 visible
- 建议
  - margin 一般是用来设置兄弟之间的间距
  - padding 一般是用来设置父子元素之间的间距
- 上下 margin 折叠
  - 垂直方向上相邻的 2 个 margin(margin-top margin-bottom)有可能会合并为 1 个 margin,这种现象叫做 collapse(折叠)
  - 水平方向 margin 不会折叠
  - 折叠后最终值的计算规则:取比较大的值
- 如何防止 margin collapse
  - 只设置其中一个元素的 margin
- 边框先关的属性
  - 边框宽度
    - border-top-width
    - border-right-width
    - border-bottom-width
    - border-left-width
  - 边框颜色
  - 边框样式
- 行内非替换元素的注意点
  - 以下属性对行内非替换元素不起作用
    - width height margin-top margin-bottom
  - 以下属性对行内非替换元素的效果比较特殊
    - padding-top padding-bottom 上下方向的 border
- outline
  - 表示元素的外轮廊,不占用空间
  - outline-width
  - outline-style 和 border 的样式是一样的,比如 solid、dotted 等
  - outline-color
- box-shadow

  - 设置一个或多个阴影
  - 每个阴影用`<shadow>`表示
  - 每个阴影之间用逗号隔开,从前到后叠加
  - `<shadow> = inset? && <length>{2,4} && <color>?`
  - 第一个`<length>`表示水平方向的偏移,正数往右偏移
  - 第二个`<length>`表示垂直方向的偏移,正数往下偏移
  - 第三个`<length>`表示模糊半径(blur radius)
  - 第四个`<length>`表示延伸距离
  - `<color>`表示阴影的颜色,如果没有设置,就跟随 color 属性的颜色
  - inset: 外框阴影变成内框阴影

- css Sprite
  - 是一种 CSS 图像合成技术,将各种小图片合并到一张图片上,然后利用 CSS 的背景定位来显示对应的图片部分
  - 减少网页的 http 请求数量,加快网页的响应速度,减轻服务器压力
  - 解决了图片命名的困扰,只需要针对一张集合的图片命名

## day06 内容概述

## 一.cursor

- CSS 属性
  - cursor
    - cursor 可以设置鼠标指针(光标)在元素上面时的显示样式
  - 常见的值
    - auto: 浏览器根据上下文决定指针的显示样式,比如根据文本和非文本切换指针样式
    - default: 有操作系统决定,一般就是一个小箭头
    - pointer: 小手
    - text: 一条竖线

## 二.定位

- position
  - 利用 position 可以对元素进行定位,常用取值有 4 个
    - static: 静态定位,默认值,元素按 normal flow 布局
      - left right top bottom 没有任何作用
    - relative: 相对定位,相对自己原来的位置
      - 元素按照 normal flow 布局
    - absolute: 绝对定位,相对属性是非 static 的父元素进行定位
      - 定位参照对象是最邻近的定位祖先元素
    - fixed: 固定定位,相对浏览器的视口
      - 元素脱离 normal flow

## 三.浮动

- 子绝父相

  - 在绝大多数情况下,子元素的绝对定位都是相对于父元素进行定位
  - 如果希望子元素相对于父元素进行定位,又不希望父元素脱标,常用的解决方案是:
    - 父元素设置 position: relative(让父元素称为定位元素,而且父元素不脱离标准流)
    - 子元素设置 position: absolute

- 绝对定位技巧

  - 绝对定位元素(absolutely positioned element)
  - position 值为 absolute 或者 fixed 的元素
  - 对于绝对定位的元素来说
  - 定位参照对象的宽度= left+right + margin-left + margin-right + 绝对定位元素的实际占用宽度
  - 定位参照对象的高度= top+bottom + margin-top + margin-bottom + 绝对定位元素的实际占用高度
  - 如果希望绝对定位元素的宽度和定位参照对象一样,可以给绝对定位元素设置以下属性
    - left:0 right:0 top:0 bottom:0 margin:0
  - 如果希望绝对定位元素在定位参照对象中居中显示,可以给绝对定位元素设置以下属性
    - left:0 right:0 top:0 bottom:0 margin:auto

- 定位方案

  - normal flow
  - absolute positioning: 绝对定位
  - float: 浮动

- 浮动的规则
  - 元素一旦浮动后,会脱离标准流,朝着向左或向右方向移动,直到自己的边界紧贴着包含块(一般是父元素)或其他浮动元素的边界为止
  - 浮动元素不能与行内级内容层叠,行内级内容将会被浮动元素推出
    - 比如行内级元素、inline-block、块级元素的文字内容
  - 行内级元素、inline-block 元素浮动后,其顶部将与所在行的顶部对齐
  - 如果元素是向左(右)浮动,浮动元素的左右边界不能超出包含块的左右边界
  - 浮动元素之间不能层叠
    - 如果一个元素浮动,另一个浮动元素已经在那个位置了,后浮动的元素将紧贴着前一个浮动元素(左浮找左浮,右浮找右浮)
    - 如果水平方向剩余的空间不够显示浮动元素,浮动元素将向下移动,直到有足够的空间为止
  - 浮动的元素的顶端不能超过包含块的顶端,也不能超过之前所有浮动元素的顶端
