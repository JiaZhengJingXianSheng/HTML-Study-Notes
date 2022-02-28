# HTML-Study-Notes
# HTML 超文本标记语言

- [HTML 超文本标记语言](#html--------)
  * [网页基本信息](#------)
    + [注释](#--)
    + [DOCTYPE](#doctype)
    + [基本格式](#----)
  * [网页基本标签](#------)
    + [图像标签](#----)
    + [链接标签](#----)
    + [锚链接](#---)
    + [功能性链接](#-----)
    + [列表](#--)
    + [表格](#--)
    + [媒体](#--)
  * [页面结构分析](#------)
  * [iframe内联框架](#iframe----)
  * [表单语法](#----)
    + [文本框和单选框](#-------)
      - [表单元素格式](#------)
      - [文本输入框](#-----)
    + [列表框和文本域](#-------)
    + [搜索框滑块和简单验证](#----------)
    + [表单初级验证](#------)

<small><i><a href='http://ecotrust-canada.github.io/markdown-toc/'>Table of contents generated with markdown-toc</a></i></small>

## 网页基本信息

### 注释

> <!-- -->

### DOCTYPE

> 告诉浏览器使用什么规范
>
> 例如：
>
> ```html
> <!DOCTYPE html>
> ```

### 基本格式

```html
<!DOCTYPE html>
<html lang="en">

<!-- head 标签表示网页头部 -->
<head>
    <!-- meta 一般用来做SEO -->
    <meta charset="UTF-8">
    <!-- title 标签代表网页标题 -->
    <title>Title</title>
</head>

<!-- body 标签代表网页主体 -->
<body>

</body>
</html>
```

---

## 网页基本标签

```html
<!-- 标题标签 -->
<h1>一级标签</h1>
<h2>二级标签</h2>
<h3>三级标签</h3>
<h4>四级标签</h4>

<!-- 段落标签 -->
<p>两只老虎，两只老虎，</p>
<p>跑得快，跑得快，</p>
<p>一只没有眼睛，</p>
<p>一只没有尾巴，</p>
<p>真奇怪！真奇怪！</p>

<!-- 水平线标签 -->
<hr>

<!-- 换行标签 -->
两只老虎，两只老虎，<br>
跑得快，跑得快，<br>
一只没有眼睛，<br>
一只没有尾巴，<br>
真奇怪！真奇怪！<br>

<!-- 粗体， 斜体-->
<h1>字体样式标签</h1>
粗体 ： <strong>I Love U </strong>
斜体 ： <em>I Love U </em>
<br>

<!-- 特殊符号 -->.
<!-- 用转义字符 -->
空&nbsp;&nbsp;&nbsp;&nbsp;格
```

### 图像标签

```html
<img src="path" alt="text" title="text" width="x" height="y">
<!-- src 路径， alt 图像的代替文字， title 鼠标悬停提示文字， width 图像宽度， height 图像高度 -->
```

### 链接标签

```html
<a href="path" target="目标窗口位置">链接文本或图像</a>
<!-- href 链接路径， target 链接在哪个窗口打开 常用值： _self _blank -->

<!--
    a 标签
    href: 必填，表示要跳转到哪个页面
    target: 表示窗口在哪里打开
-->

<a href="1.我的第一个网页.html" target="_blank">点击我跳转到页面一</a>
<a href="https://www.baidu.com">点击我跳转到百度</a>
```

### 锚链接

```html
<!-- 使用name 作为标记 -->
<a name="top">顶部</a>
<!-- 锚链接
    1. 需要一个标记
    2. 跳转到标记
-->
<p>
    <a href="1.我的第一个网页.html">
        <img src="../resources/image/3.jpg" alt="头像" title="悬停文字" height="300" width="300">
    </a>
</p>
<p>
    <a href="1.我的第一个网页.html">
        <img src="../resources/image/3.jpg" alt="头像" title="悬停文字" height="300" width="300">
    </a>
</p>
<a href="#top">回到顶部</a>
```

### 功能性链接

```html
<!-- 功能性链接
    邮件链接： mailto
    QQ链接：  
-->
<a href="mailto:the_unique_guy@outlook.com">点击联系我</a>
```

### 列表

```html
<!-- 有序列表 -->
<!-- order list -->
<ol>
    <li>Java</li>
    <li>Python</li>
    <li>C</li>
    <li>C++</li>
</ol>
<hr>

<!-- 无序列表 -->
<ul>
    <li>Java</li>
    <li>Python</li>
    <li>C</li>
    <li>C++</li>
</ul>
<hr>

<!-- 自定义列表
    dl: 标签
    dt: 列表名称
    dd: 列表内容
-->
<dl>
    <dt>学科</dt>

    <dd>Java</dd>
    <dd>Python</dd>
    <dd>Linux</dd>
    <dd>C++</dd>
</dl>
```

### 表格

```html
<!-- 表格 table
    行 tr
    列 td
-->

<table border="1px">
    <tr>
    <!-- colspan 跨列 -->
        <td colspan="4">1-1</td>
    </tr>
    <tr>
    <!-- rowspan 跨行 -->
        <td rowspan="2">2-1</td>
        <td>2-2</td>
        <td>2-3</td>
        <td>2-4</td>
    </tr>
    <tr>
        <!-- rowspan 跨行 -->
        <td>3-1</td>
        <td>3-2</td>
        <td>3-3</td>
    </tr>
</table>
```

### 媒体

```html
<!-- 音频和视频
    src: 资源路径
    controls: 控制条
    autoplay: 自动播放
    
    注： chrome默认禁用自动播放
-->
<video src="../resources/video/神奇女侠.mp4" controls autoplay></video>

<audio src="../resources/audio/孙燕姿-我怀念的.mp3" controls autoplay></audio>
```

---

## 页面结构分析

>header: 	标题头部区域的内容（用于页面或页面中的一块区域）
>
>footer: 	  标记脚部区域的内容（用于页面或页面中的一块区域）
>
>section: 	Web页面中的一块独立区域
>
>article: 	  独立的文章内容
>
>aside: 	    相关内容或应用
>
>nav: 		   导航类辅助内容

```html
<header><h2>网页头部</h2></header>

<section><h2>网页主体</h2></section>

<footer><h2>网页脚部</h2></footer>
```

## iframe内联框架

```html
<!--
<iframe src="path" name="mainFrame"></iframe>
	src: 引用地址页面
	name: 框架标识名
	width: 宽度
	height: 高度
-->
<iframe src="https://www.bilibili.com" width="1000" height="800"></iframe>

<!-- 跳转链接也可以定位到iframe打开 -->
<iframe src="" frameborder="0" name="hello" width="500" height="400"></iframe>
<a href="http://www.quarkhacker.top" target="hello">点击跳转</a>
```

## 表单语法

```html
<!-- 表单参数
    hidden: 隐藏域
    readonly: 只读
    disabled: 禁用
-->
```

```html
<!-- 表单form
    action: 表单提交的位置，可以是网站，也可以是一个请求处理地址
    method: post、 get 提交方式
    get 方式提交我们可以在url中看到我们提交的信息，不安全，但高效
    post 方式提交比较安全，可以传输大文件
-->
<form action="1.我的第一个网页.html" method="post">
    <!-- 文本输入框： input type="text" -->
    <p>名字：<input type="text" name="userName"></p>
    <!-- 密码框： input type="password" -->
    <p>密码：<input type="password" name="pwd"></p>
    <p>
        <input type="submit">
        <input type="reset">
    </p>
</form>
```

### 文本框和单选框

#### 表单元素格式

> type:  指定元素的类型，text, password, checkbox, radio, submit, reset, file, hidden, image 和 button, 默认为text
>
> name:  指定表单元素的名称
>
> value:  元素的初始值，type 为 radio 时必须指定一个值
>
> size:  指定表单元素的初始宽度 （一般用 CSS 修改）
>
> maxlength:  type 为 text 或 password 时，输入的最大字符数
>
> checked:  type 为  radio 或 checkbox 时，指定按钮是否是被选中

```html
<!-- 文本输入框： input type="text"
     value="帅"      默认初始值
     maxlength="8"   最长能写几个字符
     size="30"       文本框长度
 -->
```

#### 文本输入框

> ```html
> <!-- 文本输入框： input type="text"
>   value="帅"      默认初始值
>   maxlength="8"   最长能写几个字符
>   size="30"       文本框长度
> -->
> 
> <!-- 密码框： input type="password" -->
> 
> <!-- 单选框标签
> 	input type="radio"
>  value: 单选框的值
> 	name: 表示组
> -->
> 
> <!-- 多选框
>  input type="checkbox"
> -->
> 
> <!-- 按钮
> 	普通按钮： input type="button"
> 	图片按钮： input type="image" src=""
> 	提交按钮： input type="submit"
> 	重置按钮： input type="reset"
> -->
> ```

### 列表框和文本域

```html
<!-- 下拉框，列表框 -->
<p>下拉框
    <select name="列表名称" id="">
        <option value="China">中国</option>
        <option value="USA">美国</option>
        <option value="Switzerland" selected>瑞士</option>
        <option value="India">印度</option>
    </select>
</p>
```

```html
<!-- 文本域
    textarea name="textarea" cols="10" rows="3"
-->
<p>反馈
    <textarea name="textarea" cols="10" rows="3">
        文本内容
    </textarea>
</p>
```

```html
<!-- 文件域
    input type="file"
-->
<p>
    <input type="file" name="files">
    <input type="button" value="上传" name="upload">
</p>
```

### 搜索框滑块和简单验证

```html
<!-- 邮件验证 -->
<p>邮箱:
    <input type="email" name="email">
</p>
<!-- url验证 -->
<p>URL:
    <input type="url" name="url">
</p>
<!-- 数字验证 -->
<p>数字:
    <input type="number" name="number" max="100" min="0" step="10">
</p>
<!-- 滑块
    input type="range"
-->
<p>音量:
    <input type="range" name="volume" min="10" max="100" step="2">
</p>
<!-- 搜索框 -->
<p>搜索:
    <input type="search" name="search">
</p>
```

```html
<!-- 增强鼠标可用性 -->
<p>
    <label for="mark">你点我试试</label>
    <input type="text" id = mark>
</p>
```

### 表单初级验证

```html
<!-- 表单参数
    hidden: 隐藏域
    readonly: 只读
    disabled: 禁用
    placeholder: 提示信息，用在文本框
    required: 非空判断，用在文本框
    pattern: 正则表达式
-->
```
