# 基础概念
 form（表单）是页面与服务器交互过程中最重要的信息来源。负责获取用户填写数据，并通过浏览器向服务器传送数据。
 主要由三个基本部分组成：
#### 1.  表单标签：
这里面包含了处理表单的数据所用程序的URL以及数据提交到服务器的方法，表单名等。

```
<form action="服务器程序URL（提交到给谁处理）" method=" get/post" enctype=" MIME信息" target="文档显示方式" >表单详细设置</form>
```

#### 2.表单域：
包括了文本框（text），密码框（password），隐藏域（hidden），复选框（checkbox），单选框（radio），文件上传框（file），多行文本框，下拉选择框等。

#### 3.表单按钮：
包括提交按钮（submit），复位按钮（reset），一般按钮（button）， 图片按钮（image）
 

# 输入元素
多数情况下被用到的表单是输入标签(<input>）。

输入类型是由类型属性（type）定义的。输入类型如下：
### 文本域
- 通过<input type="text">来设定
- 适用范围：当用户要在表单中输入字母、数字等内容

- 例： 
```
<form>
姓名: <input type="text" name="yourname">
电话: <input type="text" name="tele">
</form>
```
### 密码
- 通过<input type="password">来定义
- 例：
```
<form>
密码: <input type="password" name="pwd">//明文被星号或圆点替代
</form>
```
### 单选按钮
- 通过<input type="radio">来定义
- 例：

```
<form>
<input type="radio" name="grade" value="one">大一
<input type="radio" name="grade" value="two">大二
<input type="radio" name="grade" value="three">大三
<input type="radio" name="grade" value="four">大四
</form>
```
### 复选框
- 通过<input type="checkbox">来定义
- 例：

```
<form>
<input type="checkbox" name="vehicle" value="Bike">I have a bike
<input type="checkbox" name="vehicle" value="Car">I have a car
</form>
```
### 提交按钮
- 通过<input type="submit">来定义
- 当用户单击确认按钮时，表单的内容会被传送到另一个文件。表单的动作属性定义了目的文件的文件名。由动作属性定义的这个文件通常会对接收到的输入数据进行相关的处理。
- 例：

```
<form name="input" action="..." method="get">
Username:<input type="text" name="user">
<input type="submit" value="Submit">
</form>

```
### 复位按钮
- 通过<input type="reset">来定义

### 多行文本框
- 基本语法:
```
<textarea name="" col="" row="" wrap="" ></textraea>
```
### 下拉选择框
- 基本语法:
```
<select name=""><option value="" selected（表示默认选择本项显示在下拉菜单上）>XX</option></select）
```
- 例：

```
<label for="sel">下拉菜单：</label>
<select name="" id="sel">
    <option value="2" > 上海</option>
    <option value="1" selected> 广州市</option>
    <option value="3" > 深圳</option>
    <option value="4" > 北京</option>
</select>
```
## Action属性
- ==action 属性==定义在提交表单时执行的动作。
- 向服务器提交表单的通常做法是使用提交按钮。
- 通常，表单会被提交到web服务器上的网页。
- 若省略action属性，则action会被设置为当前页面。
## Method属性
- method属性规定在提交表单时所用的HTTP方法(==GET==/==POST==)
### GET使用：
- 如果表单提交是被动的（比如搜索引擎查询），并且没有敏感信息。

注意：
- 当您使用 GET 时，表单数据在页面地址栏中是可见的。
- GET 最适合少量数据的提交。浏览器会设定容量限制。
### POST使用：
- 如果表单正在更新数据，或者包含敏感信息（例如密码）。
- POST 的安全性更加，因为在页面地址栏中被提交的数据是不可见的。
## Name属性
如果要正确地被提交，每个输入字段必须设置一个 name 属性。
