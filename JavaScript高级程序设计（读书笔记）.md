## JavaScript高级程序设计第四版-读书笔记

### 第一章：JavaScript是什么

#### 1.1 历史

- 1995。1.0版本；处理输入验证
- 1996。微软再IE3中出现JScript
- 1997。ECMA-262标准出现
- 1998。IOS和IEC将ECMAScript采纳为标准

#### 1.2 实现

- 核心（ECMAScript）
- 文档对象模型（DOM）
- 浏览器对象模型（BOM）

##### 1.2.1 ECMAScript

> ECMAScript是JavaScript的语言标准；

- 语法
- 类型
- 语句
- 关键字
- 保留字
- 操作符
- 全局对象

##### 1.2.2 DOM

> DOM是用于操作文档树API。W3C制定HTML的标准

- 访问和操作文档
- 视图
- 事件
- 样式
- 遍历和范围

> 其他DOM

- SVG
- MathML
- SMIL

##### 1.2.3 BOM

> DOM是用于访问和操作浏览器窗口的API。HTML5规范了部分标准

#### 

### 第二章 HTML中的JavaScript

#### 2.1 `<script>`元素

- script 元素的属性
  - async  立即开始下载脚本
  - charset  使用src属性指定的代码字符集 
  - crossorigin  配置相关请求的CORS（跨源资源共享）设置。默认不适用CORS
    - anonymous 配置文件请求不必设置凭据标志
    - use-credentials 设置凭据标志，出站请求会包含凭据
  - defer  脚本可以杨驰到文档完全被解析和显示之后再执行
  - integrity 允许对比接受到的资源和指定的加密签名以雁阵子资源完整性（SRI）。接受到资源的签名与这个属性指定的签名不匹配，则页面会报错。
  - language  废弃
  - src  包含要执行的代码的外部文件
  - type  表示代码块中脚本语言的内容类型（MIME）。
    - application/javascript
    - application/ecmascript
    - module
- 注意点
  - 行内代码和外部代码
  - `<script>`中代码自上而下解释
  - 代码中不能包含`</script>`，可以通过转义字符`\`
  - 执行JavaScript文件时会导致页面阻塞，阻塞时间=下载时间+执行时间
  - 如果在一个`<script>`包含外部和行内代码，只会执行外部代码
  - src可以使用外部域的JavaScript文件
  - script标签依次执行

##### 2.1.1 标签占位符

- 将`<script>`标签放在`<body>`元素的页面内容后面会让页面空白时间缩短

##### 2.1.2 推迟执行脚本

- defer 
- 脚本立即下载，延迟到整个页面都解析完毕之后再运行。
- DOMContentLoaded事件之前
- 只对外部脚本有效
- 最好只包含一个defer脚本。否则有可能不会按照预期顺序执行

##### 2.1.3 异步执行脚本

- async
- 只对外部脚本有效
- 立即开始下载，不会阻塞页面加载
- 在load事件之前执行
- 不应该在加载期间修改DOM

##### 2.1.4 动态加载脚本

##### 2.1.5XHTML中的变化

##### 2.1.6 废弃的语法

#### 2.2 行内代码与外部代码

#### 2.3 文档模式

#### 2.4`<noscript>`元素

#### 2.5 小结































