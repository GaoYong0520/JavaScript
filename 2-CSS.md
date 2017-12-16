# 1. HTML基础

# 2. CSS

<!-- TOC -->

- [1. HTML基础](#1-html基础)
- [2. CSS](#2-css)
    - [2.1. CSS的简介](#21-css的简介)
        - [2.1.1. 什么是CSS](#211-什么是css)
        - [2.1.2. CSS的作用](#212-css的作用)
        - [2.1.3. CSS的引入方式和书写规范](#213-css的引入方式和书写规范)
    - [2.2. CSS选择器](#22-css选择器)
        - [2.2.1. 基本选择器](#221-基本选择器)
        - [2.2.2. 属性选择器](#222-属性选择器)
        - [2.2.3. 伪元素选择器](#223-伪元素选择器)
        - [2.2.4. 层级选择器](#224-层级选择器)
    - [2.3. CSS属性](#23-css属性)
    - [2.4. CSS盒子模型](#24-css盒子模型)

<!-- /TOC -->

## 2.1. CSS的简介

### 2.1.1. 什么是CSS

1. 层叠样式表，CSS是对html进行样式修饰语言
1. 层叠：就是层层覆盖叠加，如果不同的CSS样式对同一html标签进行修饰，样式有冲突的部分应用优先级高的，不冲突的部分共同作用
1. 样式表：就是CSS属性样式的集合

### 2.1.2. CSS的作用

- (1)修饰html的 使其html样式更加好看
- (2)提高样式代码的复用性
- (3)html的内容与样式相分离 便于后期维护

### 2.1.3. CSS的引入方式和书写规范

- (1)内嵌样式
  >内嵌样式是把CSS的代码嵌入到html标签中

```html
<div style="color:red;font-size:100px;">你好啊 小朋友</div>
```

- 语法：
  - (1)使用style属性将样式嵌入到html标签中
  - (2)属性的写法：属性：属性值
  - (3)多个属性之间使用分号;隔开

- (2)内部样式
  - 在head标签中使用style标签进行CSS的引入

```html
<style type="text/CSS">
  div{color:red;font-size: 100px;}
</style>
```

- 语法：
  - (1)使用style标签进行CSS的引入
  - (2)属性的写法：属性：属性值
  - (3)多个属性之间使用分号;隔开

```html
<style type="text/CSS">
```

  >属性：type：告知浏览器使用CSS解析器去解析


- (3)外部样式
  >将CSS样式抽取成一个单独CSS文件 谁去使用谁就引用

```html
<link rel="stylesheet" type="text/CSS" href="demo1.CSS"/>
```

- 语法：
  - (1)创建CSS文件 将CSS属性写在CSS文件中
  - (2)在head中使用link标签进行引入
  - (3)属性的写法：属性：属性值
  - (4)多个属性之间使用分号;隔开

***
```html
<link rel="stylesheet" type="text/CSS" href="CSS文件地址"/>
```

- rel:代表要引入的文件与html的关系
- type：告知浏览器使用CSS解析器去解析
- href：CSS文件地址

***

- (4)@import方式

```html
<style type="text/CSS">
    @import url("CSS地址");
</style>
```

> link与@import方式的区别：
- link所有浏览器都支持 import部分低版本IE不支持
- import方式是等待html加载完毕之后在加载
- import方式不支持js的动态修改


## 2.2. CSS选择器

### 2.2.1. 基本选择器

1. 标签选择器

>语法：html标签名{CSS属性}

```html
示例：
<span>hello CSS!!!</span>
    <style type="text/CSS">
    span{color:red;font-size:100px; }
</style>
```
2. id选择器(id唯一性)
>语法：#id的值{CSS属性}

```html
<!-- 示例： -->
<div id="div1">hello CSS1!!!</div>
  <div id="div2">hello CSS2!!!</div>
    <style type="text/CSS">
      #div1{background-color: red;}
      #div2{background-color: pink;}
    </style>
```

3. class选择器

>语法：.class的值{CSS属性}

```html
<!-- 示例： -->
<div class="style1">div1</div>
<div class="style1">div2</div>
<div class="style2">div3</div>
<style type="text/CSS">
  .style1{background-color: red}
  .style2{background-color: pink}
</style>
```

><font size=6>**选择器的优先级：id>class>元素(标签)**</font>

### 2.2.2. 属性选择器

>语法：基本选择器[属性=‘属性值’]{CSS属性}

```html
示例：
<form action="">
    name:<input type="text" /><br/>
    pass:<input type="password" /><br/>
</form>
<style type="text/CSS">
    input[type='text']{background-color: yellow}
    input[type='password']{background-color: pink}
</style>
```

### 2.2.3. 伪元素选择器

- a标签的伪元素选择器

>语法：<br>

1. 静止状态:a:link{CSS属性}<br>
2. 悬浮状态:a:hover{CSS属性}<br>
3. 触发状态	a:active{CSS属性}<br>
4. 完成状态	a:visited{CSS属性}

```html
<!-- 示例： -->
<a href="#">点击我吧</a>
    <style type="text/CSS">
        a:link{color:blue}
        a:hover{color:red}
        a:active{color:yellow}
        a:visited{color:green}
    </style>
```

### 2.2.4. 层级选择器

>语法：父级选择器 子级选择器 .....

```html
<!-- 示例： -->
<div id="d1">
    <div class="dd1">
        <span>span1-1</span>
    </div>
    <div class="dd2">
        <span>span1-2</span>
    </div>
</div>
<div id="d2">
    <div class="dd1">
        <span>span1-1</span>
    </div>
    <div class="dd2">
        <span>span1-2</span>
    </div>
</div>

<style type="text/CSS">
    #d1 .dd2 span{color:red}
</style>
```

## 2.3. CSS属性

1. 文字属性
- font-size:大小
- font-family:字体类型
2. 文本属性
- color:颜色
- text-decoration:下划线
- 属性值：none underline
- text-align:对齐方式
  - 属性值：left  center  right

```html
<div>hello CSS!!!</div>
<a href="#">click me!!!</a>
<style type="text/CSS">
    div{color:red;text-decoration: underline;text-align: right } a{text-decoration: none;}
</style>
```

3. 背景属性
- background-color:背景颜色
- background-image:背景图片
  - 属性值：url("图片地址");
  - background-repeat:平铺方式
    - 属性值：默认横向纵向平铺
    - repeat:横向纵向平铺
    - no-repeat:不平铺
    - repeat-y：纵向
    - repeat-x：横向

```css
body{
    background-color: black;
    background-image: url("images/dog.gif");
    background-repeat: repeat-y;
}
```'

4. 列表属性
- list-style-type:列表项前的小标志
  - 属性值：太多了
- list-style-image:列表项前的小图片
  - 属性值：url("图片地址");

```html
<ul>
    <li>黑马程序员</li>
    <li>黑马程序员</li>
    <li>黑马程序员</li>
    <li>黑马程序员</li>
</ul>
<style type="text/CSS">
    ul{list-style-type: decimal-leading-zero;}
    ul{list-style-image: url("images/forward.gif");}
</style>
```

5. 尺寸属性
- width:宽度
- height:高度

```html
<div id="d1">div1</div>
<div id="d2">div2</div>
<style type="text/CSS">
    #d1{background-color: red;width: 200px;height: 200px;}
    #d2{background-color: pink;width: 200px;height: 200px;}
</style>
```

6. 显示属性
- display:
  - 属性值：none:隐藏
  - block:块级显示
  - inline：行级显示

```html
    <form action="">
        name:<input id="name" type="text" /><span id="span">对不起 输入不符合要求</span>
        <br> pass:
        <input id="pass" type="password" />
        <br>
        <input id="btn" type="button" value="button" />
    </form>
    <style type="text/CSS">
        span{color:red;display: none}
    </style>
    <script type="text/javascript">
        document.getElementById("btn").onclick = function () {
        document.getElementById("span").style.display = "inline";
        };
    </script>
```

7. 浮动属性
- float:
  - 属性值：left  right
  - clear:清除浮动 left right both
  - <font color="red">**缺点：**</font>
    - (1)影响相邻元素不能正常显示
    - (2)影响父元素不能正常显示

## 2.4. CSS盒子模型

- border:
  - border-width:边框的宽度
  - border-color:边框的颜色
  - border-style:边框的线型

  - border-top:上边框
  - border-bottom:下边框
  - border-left:左边框
  - border-right:右边框

- padding:
  - 代表内边框与内部元素之间的距离
  - padding:10px;代表上下左右都是10px
  - padding:1px 2px 3px 4px;上右下左
  - padding:1px 2px;上下/左右
  - padding:1px 2px 3px;
  - padding-top:单独设置
- margin:
  - 代表边外框与其他元素之间的距离
  - margin:10px;代表上下左右都是10px
  - margin:1px 2px 3px 4px;上右下左
  - margin:1px 2px;上下/左右
  - margin:1px 2px 3px;
  - margin-top:单独设置

***