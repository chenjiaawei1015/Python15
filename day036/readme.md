# HTML

## web相关名称

- w3c：万维网联盟组织，用来制定web标准的机构（组织）
- web标准：制作网页遵循的规范
- web准备规范的分类：结构标准、表现标准、行为标准
- 结构：html。表示：css。行为：Javascript
- 总结
  - 结构标准：相当于人的骨架。html就是用来制作网页的
  - 表现标准： 相当于人的衣服。css就是对网页进行美化的
  - 行为标准： 相当于人的动作。JS就是让网页动起来，具有生命力

## HTML介绍

### 概述

- html全称HyperText Mackeup Language，翻译为超文本标记语言，它不是一种编程语言，是一种描述性的标记语言，用于描述超文本内容的显示方式。比如字体、颜色、大小等

  - 超文本：音频，视频，图片称为超文本
  - 标记 ：<英文单词或者字母>称为标记，一个HTML页面都是由各种标记组成

- **作用**：HTML是负责描述文档**语义**的语言

- **注意**：HTML语言不是一个编程语言(有编译过程)，而是一个**标记语言**(**没有编译过程**)，HTML页面直接由浏览器解析执行

- HTML是负责描述文档语义的语言,在html中，除了**语义**，其他什么都没有


### 规范

- HTML是一个弱势语言
- HTML不区分大小写
- HTML页面的后缀名是html或者htm(有一些系统不支持后缀名长度超过3个字符，比如dos系统)
- HTML的结构
  - 声明部分：主要作用是用来告诉浏览器这个页面使用的是哪个标准。是HTML5标准
  - head部分：将页面的一些额外信息告诉服务器。不会显示在页面上
  - body部分：我们所写的代码必须放在此标签內

#### 编写HTML的规范

- 所有标记元素都要正确的嵌套，不能交叉嵌套。正确写法举例：`<h1><font></font></h1>`
- 所有的标记都必须小写
- 所有的标记都必须关闭
  - 双边标记：`<span></span>`
  - 单边标记：`<br>` 转成 `<br />` `<hr>` 转成 `<hr />`，还有`<img src=“URL” />`
- 所有的属性值必须加引号。`<h1 id="head"></h1>`
- 所有的属性必须有值。```<input type="radio" checked="checked" />`

#### HTML的基本语法特征

- HTML对换行不敏感，对tab不敏感

  - HTML只在乎标签的嵌套结构，嵌套的关系。谁嵌套了谁，谁被谁嵌套了，和换行、tab无关。换不换行、tab不tab，都不影响页面的结构
  - 也就是说，HTML**不是**依靠缩进来表示嵌套的，就是看标签的包裹关系。但是，我们发现有良好的缩进，代码更易读。要求大家都正确缩进标签

- 空白折叠现象

  - HTML中所有的**文字之间**，如果有空格、换行、tab都将被折叠为一个空格显示

- 标签要严格封闭

  ```html
  <html>
    <head>
    </head>
    <body>
    </body>
  </html>
  ```

## HTML结构

- html常见的结构

  ```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <title>Document</title>
  </head>
  <body>
      
  </body>
  </html>
  ```

### 文档声明头 `<!DOCTYPE html>`

开头的这一行，就是文档声明头，DocType Declaration，简称DTD。此标签可告知浏览器文档使用哪种 HTML 或 XHTML 规范

- XHTML：Extensible Hypertext Markup Language，可扩展超文本标注语言

  *XHTML的主要目的是为了**取代HTML**，也可以理解为HTML的升级版*

  *HTML的标记书写很不规范，会造成其它的设备(ipad、手机、电视等)无法正常显示*

  *XHTML与HTML4.0的标记基本上一样*

  *XHTML是**严格的、纯净的**HTML*

- HTML5中极大的简化了DTD，也就是说HTML5中就没有XHTML了

### 头标签

head标签都放在头部分之间。这里面包含了：`<title>`、`<meta>`、`<link>`，`<style>`

- `<title>`：指定整个网页的标题，在浏览器最上方显示
- `<meta>`：提供有关页面的基本信息
- `<link>`：定义文档与外部资源的关系
- `<style>`: 定义内部样式表与网页的关系

### meta标签

元素可提供有关页面的原信息（mata-information）,针对搜索引擎和更新频度的描述和关键词

- http-equiv属性

  它用来向浏览器传达一些有用的信息，帮助浏览器正确地显示网页内容，与之对应的属性值为content，content中的内容其实就是各个参数的变量值

  ```html
  <!--重定向 2秒后跳转到对应的网址，注意分号-->
  <meta http-equiv="refresh" content="2;URL=http://www.luffycity.com">
  <!--指定文档的内容类型和编码类型 -->
  <meta http-equiv="Content-Type" content="text/html;charset=utf-8" />
  <!--告诉IE浏览器以最高级模式渲染当前网页-->
  <meta http-equiv="x-ua-compatible" content="IE=edge">
  ```

- name属性

  主要用于页面的关键字和描述，是写给搜索引擎看的，关键字可以有多个用 ‘,’号隔开，与之对应的属性值为content，content中的内容主要是便于搜索引擎机器人查找信息和分类信息用的

  ```html
  <!-- 这些关键词，就是告诉搜索引擎，这个网页是干嘛的，能够提高搜索命中率。让别人能够找到你，搜索到 -->
  <meta name="Keywords" content="网易,邮箱,游戏,新闻,体育,娱乐,女性,亚运,论坛,短信" />
  ```

  *只要设置Description页面描述，那么百度搜索结果，就能够显示这些语句，这个技术叫做**SEO**（search engine optimization，搜索引擎优化）*

  ```python
  <meta name="Description" content="网易是中国领先的互联网技术公司，为用户提供免费邮箱、游戏、搜索引擎服务，开设新闻、娱乐、体育等30多个内容频道，及博客、视频、论坛等互动交流，网聚人的力量。" />
  ```

  网页支持移动端，移动设备优先

  ```html
  <meta name=viewport content="width=device-width, initial-scale=1">
  ```

### title标签

主要用来告诉用户和搜索引擎这个网页的主要内容是什么，搜索引擎可以通过网页标题，迅速的判断出当前网页的主题

## body中的标签

### 字体标签

字体标签包含：`h1~h6、<u>、<b>、<strong><em>、<sup>、<sub>`

#### h1 - h6

- 标题使用`<h1>`至`<h6>`标签进行定义。`<h1>`定义最大的标题，`<h6>`定义最小的标题。具有align属性，属性值可以是：left、center、right

#### b

- 粗体

#### u

- 下划线

#### i

- 斜体

#### sup sub

- `上标<sup> 下标<sub>`

#### 特殊字符

- `&nbsp;`：空格 （non-breaking spacing，不断打空格）
- `&lt;`：小于号（less than）
- `&gt;`：大于号（greater than）
- `&amp;`：符号`&`
- `&quot;`：双引号
- `&apos;`：单引号
- `&copy;`：版权`©`
- `&trade;`：商标`™`

### 排版标签

#### p

- 段落：是英文paragraph的缩写
- 属性: 对齐方式 align='值' , 值可以为 left, center, right
- **p标签是一个文本级标签，p标签中不能包含容器标签**。其他的一律不能放

#### 文本级标签与容器级标签

- 文本级标签：p、span、a、b、i、u、em。文本标签里只能放文字、图片、表单元素
- 容器级标签：div、h系列、li、dt、dd。容器级标签里可以放任何东西

#### html标签的分类

- 行内标签 (常用的例如 span strong em i del a)

  特点:

  - 在一行内显示
  - 不能设置宽高

- 行内块标签 (常用的例如 img input)

  特点:

  - 在一行内显示
  - 可以设置宽高

- 块级标签 (常用的例如 div p h1~h6)

  特点:

  - 独占一行
  - 可以设置宽高

#### div span

- div和span是非常重要的标签，div的语义是division“分割”； span的语义就是span“范围、跨度”。CSS课程中你将知道，这两个东西，都是最最重要的“盒子”
- `<span>和<div>唯一的区别在于：<span>是不换行的，而<div>是换行的`
- div标签是一个**容器级**标签，里面什么都能放，甚至可以放div自己
- span也是表达“小区域、小跨度”的标签，但是是一个**文本级**的标签
- span里面只能放置文字、图片、表单元素。 span里面不能放p、h、ul、dl、ol、div

#### br

- 换行
- `<p>标签和<br>标签的区别在于：<p>标签会在段落的前后自动插入一个空行，而<br>标签没有空行；而且<br>标签没有属性`

#### center

- center代表是一个标签，而不是一个属性值了。只要是在这个标签里面的内容，都会居于浏览器的中间

  ```html
  <center>
    <p>
      content1
    </p>
  </center>
  ```

#### pre

- 预格式化标签
- 将保留其中的所有的空白字符(空格、换行符)，原封不动的输出结果（告诉浏览器不要忽略空格和空行）

### 超链接

#### 外部链接

```html
<a href="new.html">点击进入到新网页</a>
```

#### 锚链接

- 指给超链接起一个名字，作用是**在本页面或者其他页面的的不同位置进行跳转**。比如说，在网页底部有一个向上箭头，点击箭头后回到顶部，这个就是利用到了锚链接

  ```html
  <a name='top'>顶部</a>
  此次有 1000 行代码
  <a href='#top'>回到顶部</a>
  ```

#### 邮件链接

- 效果：点击之后，会弹出outlook，作用不大

- 前提：计算机中必须安装邮件客户端，并且配置好了邮件相关信息

  ```html
  <a href='mailto:aa@qq.com'></a>
  ```

#### 特殊的链接

- 返回页面顶部的位置

  ```html
   <a href="#">跳转到顶部</a>
  ```

- js相关

  ```html
  <!-- 表示在触发<a>默认动作时，执行一段JavaScript代码 -->
  <a href="javascript:alert(1)">内容</a>
  
  <!-- 表示什么都不执行，这样点击<a>时就没有任何反应 -->
  <a href="javascript:;">内容</a>
  ```

#### 超链接的属性

- `href`：目标URL
- `title`：悬停文本
- `name`：主要用于设置一个锚点的名称
- `target`：告诉浏览器用什么方式来打开目标页面。`target`属性有以下几个值
  - `_self`：在同一个网页中显示（默认值）
  - `_blank`：**在新的窗口中打开**
  - `_parent`：在父窗口中显示
  - `_top`：在顶级窗口中显示

#### 超链接清除默认的样式

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>

    <style type="text/css">
        a {
            /* 下划线清除. */
            text-decoration: none;
        }
    </style>

</head>
<body>

<!-- javascript:void(0); 清除默认的点击动作 -->
<a href="javascript:void(0);">清除默认样式</a>

</body>
</html>
```

### 图片标签 img

- img是自封闭标签，也称为单标签
- 能够插入的图片类型是：jpg(jpeg)、gif、png、bmp
- 不能往网页中插入的图片格式是：psd、ai
- HTML页面不是直接插入图片，而是插入图片的引用地址，所以也要把图片上传到服务器上

#### 属性

- src : 图片资源
- `width`：宽度
- `height`：高度
- `title`：**提示性文本**。公有属性。也就是鼠标悬停时出现的文本
- `align`：指图片的水平对齐方式，属性值可以是：left、center、right
- `alt`：当图片显示不出来的时候，代替图片显示的内容。alt是英语 alternate “替代”的意思

一般为了是 img 具有点击操作, 一般会与 a 标签一同使用

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>

    <style type="text/css">
        a {
            /* 下划线清除. */
            text-decoration: none;
        }
    </style>

</head>
<body>

<!-- 点击图片, 跳转百度 -->
<a href="http://www.baidu.com">
    <img src="https://www.baidu.com/img/PCtm_d9c8750bed0b3c7d089fa7d55720d6cf.png" alt="百度图片">
</a>

</body>
</html>
```

#### 注意

- 文本级的标签显示在浏览器上时，不管你的图片多高，它总会底边对齐，这是一种现象，“高矮不齐，底边对齐”
- 如果要想保证图片等比例缩放，请只设置width和height中其中一个
- 如果想实现图文混排的效果，请使用align属性，取值为left或right

### 列表标签

#### 无序列表`<ul>`，无序列表中的每一项是`<li>`

- li不能单独存在，必须包裹在ul里面；反过来说，ul的“儿子”不能是别的东西，只能有li

- ul的作用，并不是给文字增加小圆点的，而是增加无序列表的“语义”的

- 属性

  `type="属性值"`。属性值可以选： `disc`(实心原点，默认)，`square`(实心方点)，`circle`(空心圆)

- ul的儿子，只能是li。但是li是一个容器级标签，li里面什么都能放。甚至可以再放一个ul

#### 有序列表`<OL>`，里面的每一项是`<li>`

- 属性

  type="属性值"`。属性值可以是：1(阿拉伯数字，默认)、a、A、i、I。结合`start`属性表示`从几开始
  
- ol里面只能有li，li必须被ol包裹。li是容器级

#### 定义列表

- `<dl>`英文单词：definition list，没有属性。dl的子元素只能是dt和dd
  - `<dt>`：definition title 列表的标题，这个标签是必须的
  - `<dd>`：definition description 列表的列表项，如果不需要它，可以不加
- dt、dd只能在dl里面；dl里面只能有dt、dd

### 表格标签

- 一个表格`<table>`是由每行`<tr>`组成的，每行是由`<td>`组成的

- 属性

  - `border`：边框。像素为单位
  - `style="border-collapse:collapse;"`：单元格的线和表格的边框线合并
  - `width`：宽度。像素为单位
  - `height`：高度。像素为单位
  - `bordercolor`：表格的边框颜色
  - `align`：**表格**的水平对齐方式。属性值可以填：left right center。
    注意：这里不是设置表格里内容的对齐方式，如果想设置内容的对齐方式，要对单元格标签`<td>`进行设置）
  - `cellpadding`：单元格内容到边的距离，像素为单位。默认情况下，文字是紧挨着左边那条线的，即默认情况下的值为0。
    注意不是单元格内容到四条边的距离哈，而是到一条边的距离，默认是与左边那条线的距离。如果设置属性`dir="rtl"`，那就指的是内容到右边那条线的距离。
  - `cellspacing`：单元格和单元格之间的距离（外边距），像素为单位。默认情况下的值为0
  - `bgcolor="#99cc66"`：表格的背景颜色。
  - `background="路径src/..."`：背景图片。
    背景图片的优先级大于背景颜色

- tr 行

  - 属性
    - `dir`：公有属性，设置这一行单元格内容的排列方式。可以取值：`ltr`：从左到右（left to right，默认），`rtl`：从右到左（right to left）
    - `bgcolor`：设置这一行的单元格的背景色。
      注：没有background属性，即：无法设置这一行的背景图片，如果非要设置，可以用css实现。
    - `height`：一行的高度
    - `align="center"`：一行的内容水平居中显示，取值：left、center、right
    - `valign="center"`：一行的内容垂直居中，取值：top、middle、bottom

- td 单元格

  -  属性
    - `align`：内容的横向对齐方式。属性值可以填：left right center。
      如果想让每个单元格的内容都居中，这个属性太麻烦了，以后用css来解决。
    - `valign`：内容的纵向对齐方式。属性值可以填：top middle bottom
    - `width`：绝对值或者相对值(%)
    - `height`：单元格的高度
    - `bgcolor`：设置这个单元格的背景色。
    - `background`：设置这个单元格的背景图片
  
- 单元格的合并
  
  - `colspan`：横向合并。例如`colspan="2"`表示当前单元格在水平方向上要占据两个单元格的位置
  - `rowspan`：纵向合并。例如`rowspan="2"`表示当前单元格在垂直方向上
  
- th 加粗的单元格
  
  相当于 td + b
  
-  caption 表格的标题
  
- thead tbody tfoot
  
  如果写了，那么这三个部分的**代码顺序可以任意**，浏览器显示的时候还是按照thead、tbody、tfoot的顺序依次来显示内容。如果不写thead、tbody、tfoot，那么浏览器解析并显示表格内容的时候是从按照代码的从上到下的顺序来显示
  
  当表格非常大内容非常多的时候，如果用thead、tbody、tfoot标签的话，那么**数据可以边获取边显示**。如果不写，则必须等表格的内容全部从服务器获取完成才能显示出来
  
### 表单标签 form

- form 表单属性

  - `name`：表单的名称，用于JS来操作或控制表单时使用；
  - `id`：表单的名称，用于JS来操作或控制表单时使用；
  - `action`：指定表单数据的处理程序，一般是PHP，如：action=“login.php”
  - `method`：表单数据的提交方式，一般取值：get(默认)和post

- GET 请求与 POST 请求的区别

  GET方式：
  将表单数据，以"name=value"形式追加到action指定的处理程序的后面，两者间用"?"隔开，每一个表单的"name=value"间用"&"号隔开。
  特点：只适合提交少量信息，并且不太安全(不要提交敏感数据)、提交的数据类型只限于ASCII字符。

  POST方式：
  将表单数据直接发送(隐藏)到action指定的处理程序。POST发送的数据不可见。Action指定的处理程序可以获取到表单数据。
  特点：可以提交海量信息，相对来说安全一些，提交的数据格式是多样的(Word、Excel、rar、img)

#### input标签

- 属性值
  - `type="属性值"`：文本类型。属性值可以是：
    - `text`（默认）
    - `password`：密码类型
    - `radio`：单选按钮，名字相同的按钮作为一组进行单选（单选按钮，天生是不能互斥的，如果想互斥，必须要有相同的name属性。name就是“名字”。
      ）。非常像以前的收音机，按下去一个按钮，其他的就抬起来了。所以叫做radio。
    - `checkbox`：多选按钮，名字相同的按钮作为一组进行选择。
    - `checked`：将单选按钮或多选按钮默认处于选中状态。当`<input>`标签的`type="radio"`时，可以用这个属性。属性值也是checked，可以省略。
    - `hidden`：隐藏框，在表单中包含不希望用户看见的信息
    - `button`：普通按钮，结合js代码进行使用。
    - `submit`：提交按钮，传送当前表单的数据给服务器或其他程序处理。这个按钮不需要写value自动就会有“提交”文字。这个按钮真的有提交功能。点击按钮后，这个表单就会被提交到form标签的action属性中指定的那个页面中去。
    - `reset`：重置按钮，清空当前表单的内容，并设置为最初的默认值
    - `image`：图片按钮，和提交按钮的功能完全一致，只不过图片按钮可以显示图片。
    - `file`：文件选择框。
      提示：如果要限制上传文件的类型，需要配合JS来实现验证。对上传文件的安全检查：一是扩展名的检查，二是文件数据内容的检查。
  - **value="内容"**：文本框里的默认内容（已经被填好了的）
  - `size="50"`：表示文本框内可以显示**五十个字符**。一个英文或一个中文都算一个字符。
    注意**size属性值的单位不是像素哦**。
  - `readonly`：文本框只读，不能编辑。因为它的属性值也是readonly，所以属性值可以不写。
    用了这个属性之后，在google浏览器中，光标点不进去；在IE浏览器中，光标可以点进去，但是文字不能编辑。
  - `disabled`：文本框只读，不能编辑，光标点不进去。属性值可以不写

#### select 标签

- `<select>`标签里面的每一项用`<option>`表示。select就是“选择”，option“选项”  
- select 属性
  - `multiple`：可以对下拉列表中的选项进行多选。没有属性值。
  - `size="3"`：如果属性值大于1，则列表为滚动视图。默认属性值为1，即下拉视图
- option 属性
  - `selected`：预选中。没有属性值

#### textarea 多行文本输入框

- 属性
  - `value`：提交给服务器的值。
  - `rows="4"`：指定文本区域的行数。
  - `cols="20"`：指定文本区域的列数。
  - `readonly`：只读

#### label标签

- 可以与 input 标签进行绑定, label 中的 for 属性值与 input 标签的 id 值进行对应

  ```html
  <input type="radio" name="sex" id="nan" /> <label for="nan">男</label>
  <input type="radio" name="sex" id="nv"  /> <label for="nv">女</label>
  ```

  


