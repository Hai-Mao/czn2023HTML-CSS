# czn2023HTML-CSS
# 632107060224 曹主能 HTML&CSS总结 
# HTML语言总结
## 什么是HTML
HTML（Hypertext Markup Language）是一种用于创建Web页面的标准标记语言。它使用标记标签来描述页面的结构和内容，如段落、标题、链接、图像等。
## HTML的文档结构


HTML文档由三部分组成：文档声明、文档头和文档主体。
文档声明告诉Web浏览器这是一个HTML文档，通常使用以下代码：
```html
<!DOCTYPE html>
```
文档头包含有关文档的信息，如文档的标题、字符集和样式表等。它通常包含在`<head>`标签中：
```html
<head>
  <title>页面标题</title>
  <meta charset="UTF-8">
</head>
```
文档主体包含页面的主要内容，如文本、图像和链接等。它通常包含在`<body>`标签中：
```html
<body>
  页面内容
</body>
```

结合起来差不多是这样的
下面的代码是一个很简单很基本HTML文档

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>这一个页面的标题</title>
</head>
<body>
    <h1>这是一个标题</h1>
    <p>这是一个段落</p>
    <!--这是一个注释-->
</body>
</html>
```


## 常用的标签
### 标题
标题标签用于定义页面的标题。一般情况下，网页的标题会显示在浏览器的窗口标题栏中，也会作为搜索引擎的重要标识。
```html
<h1>一级标题</h1>
<h2>二级标题</h2>
<h3>三级标题</h3>
```
### 超链接
超链接标签用于在文档中创建链接。它可用于链接到其他页面、文件、电子邮件地址或下载文件等。
```html
<a href="链接地址">链接文本</a>
```
### 图片
图片标签用于在文档中插入图像。它需要指定图像的路径和尺寸。
```html
<img src="图片路径" alt="替代文本" width="宽度" height="高度">
```
### 表格
表格标签用于创建表格。它需要定义表格的行、列和单元格。
```html
<table>
  <tr>
    <th>表头1</th>
    <th>表头2</th>
  </tr>
  <tr>
    <td>行1列1</td>
    <td>行1列2</td>
  </tr>
  <tr>
    <td>行2列1</td>
    <td>行2列2</td>
  </tr>
</table>
```
### 列表
列表标签用于创建有序或无序列表。
```html
<ul>
  <li>无序列表项1</li>
  <li>无序列表项2</li>
</ul>
<ol>
  <li>有序列表项1</li>
  <li>有序列表项2</li>
</ol>
```
### 表单
表单标签用于创建表单，如登录表单、搜索表单等。
```html
<form action="提交地址" method="提交方式">
  <label for="username">用户名：</label>
  <input type="text" id="username" name="username"><br>
  <label for="password">密码：</label>
  <input type="password" id="password" name="password"><br>
  <input type="submit" value="提交">
</form>
```

## 综合
下面一段代码是使用了html语言制作的一个网页（因为没有设置格式那些所以很丑）

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>自己瞎写的html</title>
</head>
<body>
    <h1 id="title">h1标题</h1>
    <p>p段落</p>
    <p><a href="#pv">跳转到图片和视频</a></p>
    <p><a href="#pa">跳转到超链接</a></p>
    <p><a href="#table">跳转到表格</a></p>

    <hr>
    <h2 id="pv">图片和视频</h2>
    <p><img src="./html练习文件/image.jpg" alt="可爱捏" width="505" height="512"></p>

    <p>
    <video width="960" height="540" controls autoplay>
        <source src="./html练习文件/video.mp4" type="video/mp4">
    </video>
    </p>

    <hr>
    <h2 id="pa">超链接</h2>

    <p><a href="#title">返回顶部</a></p>
    <p><a href="https://www.bing.com/" target="_blank">跳转至外部网站必应Bing</a></p>

    <p>下面这张图片也是一个链接</p>
    <p>
        <a href="https://www.pixiv.net/artworks/108352784" target="_blank">
        <img src="./html练习文件/image_a.png" alt="一个图片链接" width="708" height="502"></a>
    </p>

    <hr>
    <h2 id="table">表格</h2>
    <table>
        <tr>
          <th>Firstname</th>
          <th>Lastname</th>
          <th>Age</th>
        </tr>
        <tr>
          <td>Jill</td>
          <td>Smith</td>
          <td>50</td>
        </tr>
        <tr>
          <td>Eve</td>
          <td>Jackson</td>
          <td>94</td>
        </tr>
    </table>


</body>
</html>
```






# CSS语言总结
## 什么是CSS
CSS（Cascading Style Sheets）是一种用于描述网页样式和布局的语言。它通过定义样式来控制页面中的元素的外观，如字体、颜色、大小、对齐、边框等。
## CSS的基本语法
CSS由选择器、属性和值组成，如下所示：
```css
选择器 {
  属性1: 值1;
  属性2: 值2;
  ...
}
```
其中，选择器指定要应用样式的元素，属性指定要更改的属性，值指定要为属性设置的值。
## 外部样式、内部样式和内联样式的区别
- 外部样式：将样式放在一个独立的.css文件中，使用`<link>`标签将其链接到HTML文档中。
- 内部样式：将样式放在`<style>`标签中，通常放在HTML文档的头部。
- 内联样式：直接将样式应用于HTML元素中，使用`style`属性。
外部样式的优点是可以集中管理样式，同时可以被多个页面共用。内部样式和内联样式的优点是可以直接作用于某个元素，方便快捷。
## 颜色、尺寸和对齐
CSS支持设置颜色、尺寸和对齐等样式。
```css
color: red; /* 设置文字颜色 */
font-size: 16px; /* 设置文字大小 */
text-align: center; /* 设置文字对齐方式 */
```
## 盒子模型
CSS中的每个HTML元素都被视为一个盒子，包括内容、内边距、边框和外边距。
```css
.box {
  width: 200px; /* 设置盒子宽度 */
  height: 100px; /* 设置盒子高度 */
  padding: 10px; /* 设置内边距 */
  border: 1px solid black; /* 设置边框 */
  margin: 10px; /* 设置外边距 */
}
```
## 边框和边距
边框和边距是盒子模型中的两个重要概念。
```css
border: 1px solid black; /* 设置边框 */
padding: 10px; /* 设置内边距 */
margin: 10px; /* 设置外边距 */
```
边框是包围元素的线条，可以设置边框的宽度、样式和颜色。边距指元素与周围元素之间的空间。
## 定位
CSS可以使元素在页面上的位置发生变化，包括相对定位、绝对定位和固定定位、静态定位。
```css
.relative {
  position: relative; /* 设置相对定位 */
  top: 10px; /* 向上移动10像素 */
  left: 10px; /* 向左移动10像素 */
}
.absolute {
  position: absolute; /* 设置绝对定位 */
  top: 100px; /* 距离顶部100像素 */
  left: 100px; /* 距离左侧100像素 */
}
.fixed {
  position: fixed; /* 设置固定定位 */
  top: 0; /* 固定在顶部 */
  right: 0; /* 固定在右侧 */
}
.static {
  position: static;/*设置静态定位（默认的，可以不用设置的）*/
}
```
## 组合选择器
CSS可以使用多个选择器组合在一起来选择元素，如类选择器、ID选择器、后代选择器和子选择器等。
```css
.header h1 {
  color: red; /* 选择.class为header下的h1元素 */
}
#nav li {
  color: blue; /* 选择id为nav下的li元素 */
}
```
## 伪类和伪元素
伪类和伪元素是CSS中的两种特殊选择器，它们可以选择元素的某个状态或部分内容。
```css
a:hover {
  color: red; /* 鼠标悬停时改变链接颜色 */
}
p:first-letter {
  font-size: 24px; /* 选择第一个字母并设置字体大小 */
}
```

这些就是CSS基本的总结了（上面写的html文档我就没用CSS装饰了）
