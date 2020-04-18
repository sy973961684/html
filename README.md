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

### 1.1 html 元素

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
- :first-line ::first-line
- :first-letter ::first-letter
- :before ::before
- :after ::after

### CSS 属性  选择器

- `https://www.bilibili.com/video/BV16j411f7p5?p=40`
