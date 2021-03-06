# 1. HTML基础

## 1.1. HTML简介

<!-- TOC -->

- [1. HTML基础](#1-html基础)
    - [1.1. HTML简介](#11-html简介)
        - [1.1.1. HTML是什么](#111-html是什么)
        - [1.1.2. HTML能做什么](#112-html能做什么)
        - [1.1.3. HTML书写规范](#113-html书写规范)
    - [1.2. HTML基本标签](#12-html基本标签)
        - [1.2.1. 文件标签(结构标签)](#121-文件标签结构标签)
        - [1.2.2. 排版标签](#122-排版标签)
        - [1.2.3. 块标签](#123-块标签)
        - [1.2.4. 字体标签](#124-字体标签)
        - [1.2.5. 清单标签（也称为列表标签）](#125-清单标签也称为列表标签)
        - [1.2.6. 图形标签：（自关闭标签）](#126-图形标签自关闭标签)
        - [1.2.7. 链接标签：](#127-链接标签)
        - [1.2.8. 表格标签](#128-表格标签)
    - [1.3. HTML表单标签(重点)](#13-html表单标签重点)
        - [form标签：](#form标签)
        - [input标签：](#input标签)
        - [select标签：下拉菜单](#select标签下拉菜单)
        - [textarea:文本域标签](#textarea文本域标签)
    - [1.4. HTML框架标签及其他](#14-html框架标签及其他)
        - [框架标签](#框架标签)
        - [其他标签](#其他标签)
        - [特殊字符](#特殊字符)

<!-- /TOC -->

### 1.1.1. HTML是什么

>HTML是用来描述网页的一种语言。

- (1)HTML 指的是超文本标记语言 (Hyper Text Markup Language)
- (2)HTML 不是一种编程语言，而是一种标记语言(markup language,标记语言是一套标记标签(markup tag));
- (3)HTML 使用标记标签来描述网页

- 超文本 标记 语言
  - 语言：人与计算机交互的工具
  - 超文本：
    - (1)普通文本不能实现的，超文本可以实现，能实现普通文本不能实现的功能
    - (2)包括超链接的文本
  - 标记：就是标签，不同的标签能实现不同的功能

### 1.1.2. HTML能做什么

>HTML通过标签的形式将信息展示给用户

### 1.1.3. HTML书写规范

- (1)HTML结构

```HTML
<html>
    <head>
        包括资讯信息：整个页面的属性、指导浏览器解析的标签、引入外部文件的标签
    </head>

    <body>
    我们需要展示的信息
    </body>
</html>
```

- (2)HTML标签是以尖括号包裹关键字成对出现的，有开始标签和结束标签，支持正确的嵌套
- (3)大部分标签有属性 格式：属性=“属性值”（多个属性之间用空格隔开）
- (4)空标签：功能比较单一 ，例如：<br></br> === <br/>
- (5)**HTML不区分大小写，建议使用小写**

## 1.2. HTML基本标签

### 1.2.1. 文件标签(结构标签)

<HTML><HTML>:根标签
    <head>
        <title></title>:页面的标题
    </head>
    <body></body>：内容

  >属性：text:文本的颜色 bgcolor:背景色 background:背景图片

- 颜色的三种表示方式：
  - (1)单词：red green black
  - (2)rgb三原色：reg(0,0,0)  0-255
  - (3)#000000  #ffffff  #325687   #377405

### 1.2.2. 排版标签

- (1)注释标签：<!--注释-->
- (2)换行标签：<br/>
- (3)段落标签：<p>文本文字</p>
  - 特点：段与段之间有空行
  - 属性：
    - align:对齐方式（有三个属性值：left  center   right）
- (4)水平线标签：

<hr/>

```html
<hr/>
```
  - 属性：
    - width:长度
    - size:粗度
    - color：颜色
    - align:对齐方式

- 尺寸的写法：
  - （1）像素：10px
  - （2）百分比：占据副标签的百分比，会随着副标签的大小进行变化

### 1.2.3. 块标签

1. <div></div>:行级块标签
2. <span></span>:行内块标签

```html
作用：
  （1）<div></div>：div+css布局
  （2）<span></span>：进行友好提示
```

### 1.2.4. 字体标签

- 基本文字标签：

```html
<font></font>
```

- 属性：
  - color:颜色
  - size:大小（最大值:7，最小值:1，默认值:3）
  - face:字体类型，即字体，直接写文字就可以
- 标题标签：

```html
<h1></h1>-<h6></h6>
```

> 随着数字的增大逐渐变小，字体是加粗的，内置字号 默认占据一行

### 1.2.5. 清单标签（也称为列表标签）

1. 无序列表：

```html
<ul></ul>
<li></li>:列表项
  属性：
  type：有三个值，分别为disc、 square和circle

  示例：
  <ul >
    <li>列表项</li>
    <li>列表项</li>
    <li>列表项</li>
  </ul>
```

2. 有序列表：

```html
<ol></ol>
<li></li>:列表项
    属性：
        type：1、A、a、I、i（数字、字母、罗马数字）
        start:数字，代表首项开始位置

    示例：
        <ol>
        <li>列表项</li>
        <li>列表项</li>
        <li>列表项</li>
        </ol>

        列表标签的作用：实现菜单项（可以实现横向或者纵向菜单）
        无序列表标签怎么去掉小圆点？HTML中不能直接去掉，没有这个属性值，需要在CSS中给li标签添加样式list-style:none;
```

### 1.2.6. 图形标签：（自关闭标签）

```html
<img />
```

- 属性：
  - src:图形地址
  - width:宽度
  - height:高度
  - border:边框
  - align:对齐方式，代表图片与相邻的文本的相对位置（有三个属性值：top middle bottom）
  - alt:图片的文字说明

### 1.2.7. 链接标签：

```html
<a></a>
    <!--
    属性：
    href:跳转页面地址
    name:名称，锚点
        target:
            _self(自己)
            _blank(新页面,之前的页面还有)，
    作用：
    （1）页面跳转，注意：要调到外网必须要加协议
    （2）访问锚点；回到锚点（顶部、底部、中间），在访问锚点时的书写格式：#name的值； -->
```

### 1.2.8. 表格标签

```html
<table></table>:
    属性：
    border:表格边框
    width:表格的宽度
    align:表格的对齐方式（<tr align="center">单元格里面的内容居中对齐<tr>）
    bgcolor:背景颜色
    <tr></tr>: 代表行
        <td></td>：代表单元格
            属性：
            colspan:列合并
            rowspan:行合并
        <th></th>：相等于<td>, 只是内置样式加粗居中
    <caption></caption>：表格的标题，即表头

    表格的作用：
    (1)简单的实现一个表格样式
    (2)进行页面布局

    示例：
<table>
    <tr><!--行-->
    <th>表格标头</th>
    <td>普通单元格</td>
    </tr>
</table>

<thead></thead>、<tbody></tbody>、<tfoot></tfoot>
作用：分块加载，用户体验比较好
```

## 1.3. HTML表单标签(重点)

### form标签：

```html
<form></form>
```

- 属性：
  - name:表单名称
  - action:提交的路径地址
  - method:提交方式（get和post）

    - **get和post的区别（重点）：**
      - (1)get提交将数据加在地址栏的后面，格式?name=value&name=value；post提交将数据封装在请求体中
      - ?username=zhangsan&password=123&sex=male&hobby=football&hobby=paiqiu&city=bj#
      - (2)get提交相对不安全；post提交相对安全
      - (3)get提交有大小限制，根据浏览器不同而不同；post不限制大小

- 示例：

```html
<form>
    <table>
        <!--form里面嵌套table-->
    </table>
</form>
```

### input标签：

  <input type=" "/>

```html
<input type=" "/>
```

- type属性:根据type属性实现各种不同功能的表单项；
  - text：普通的文本输入框；
  - name：username value="张三"<!--张三是默认值-->
  - password：密码输入框；特点是显示的是掩码
  - radio：单选按钮
    - name：如果想让一组单选按钮互斥，就用指定同一name属性值，需要加value属性值；
    - checked：默认被选中；
  - checkbox：复选框；
    - name：组的概念，需要加value属性值。
    - checked：默认被选中；
  - file：上传文件的控件
  - button：普通按钮，没有任何内置的功能；
  - submit：内置功能，点击会按照action地址提交
  - reset：重置，点击会清空之前填写的内容
  - image：图片按钮，功能类似与submit
    - src：加载图片
    - alt:图片的提示文字
    - **hidden**:隐藏表单，作用是在提交数据的时候，服务器需要这个数据，但是不需要用户看到。

>**注意：name属性必须要写。**

### select标签：下拉菜单

```html
(<select></select>)
```

- 属性：
  - name;表单项的名称
  - option标签：可选项（下拉菜单之间的级联）
- 属性：
  - value，表单项的值
  - selected：默认被选中

### textarea:文本域标签

- 属性：
  - cols：列数
  - rows：行数
- **注意：默认的文本值在标签体当中**

## 1.4. HTML框架标签及其他

### 框架标签

```html
    <!--
        frameset:
			属性：
				rows；按行划分
				cols：按列划分
				划分格式： rows="120,*"
		frame:
			属性：
				name：名称，方便target根据name值进行定位
				src:加载的页面地址； -->
```

### 其他标签

```html
<meta>
    <meta http-equiv="keywords" content="keyword1,keyword2,keyword3">
        <meta http-equiv="description" content="this is my page">
        <meta http-equiv="content-type" content="text/HTML; charset=UTF-8">
    <link>
    <link rel="stylesheet" type="text/css" href="./styles.css">
    <!-- href：引入css文件的地址 -->
    <script>
    <script type="text/javascript" src=""></script>
    <!-- src：js的文件地址 -->
```

### 特殊字符

- &nbsp; 空格
- &gt;   大于号
- &lt;   小于号
- &copy; 版权符号
- &reg;  注册符号

```html
- &nbsp; 空格
- &gt;   大于号
- &lt;   小于号
- &copy; 版权符号
- &reg;  注册符号
```