# 前端代码规范

[借鉴网址链接](https://guide.aotu.io)

## HTML

### 属性书写顺序

以重要程度以及修改频率进行书写

- class
- id,name
- data-\*
- src,for,type,href
- title,alt
- aria-\*,role

### 团队约定

```
    <html lang="zh-CN">
    <meta charset="UTF-8">
```

### 元素及标签闭合

- 所有具有开始标签和结束标签的元素都要写上起止标签，某些允许省略开始标签或和束标签的元素亦都要写上
- 空元素标签都不加 “/” 字符

  推荐

  ```
  <div>
      <h1>我是h1标题</h1>
      <p>我是一段文字，我有始有终，浏览器能正确解析</p>
  </div>
   <br>
  ```

  不推荐

  ```
   <div>
        <h1>我是h1标题</h1>
        <p>我是一段文字，我有始无终，浏览器亦能正确解析
    </div>
    <br/>
  ```

### HTML 代码书写

- HTML 标签名、类名、标签属性和大部分属性值统一用小写
- 不需要为 CSS、JS 指定类型属性，HTML5 中默认已包含
- 元素属性值使用双引号语法，元素属性值可以写上的都写上

### 代码缩进

- 统一使用四个空格进行代码缩进 ，可统一使用格式化工具

### 注释

- 单行注释：注释内容前后各一个空格字符，注释位于要注释代码的上面，单独占一行
- 模块注释：注释内容前后各一个空格字符，
  `<!-- S Comment Text --> 表示模块开始，<!-- E Comment Text --> 表示模块结束，模块与模块之间相隔一行`
- 嵌套模块注释: 当模块注释内再出现模块注释的时候，为了突出主要模块如下所示：

  ```
  <!-- S Comment Text A -->
  <div class="mod_a">

      <div class="mod_b">
          ...
      </div>
      <!-- /mod_b -->

      <div class="mod_c">
      	...
      </div>
      <!-- /mod_c -->

   </div>
   <!-- E Comment Text A -->
  ```

### 文件模板

- HTML5 标准模板

  ```
  <!DOCTYPE html>
  <html lang="zh-CN">
  <head>
  <meta charset="UTF-8">
  <title>HTML5标准模版</title>
  </head>
  <body>
  </body>
  </html>

  ```

- 移动端

```
<!DOCTYPE html>
 <html lang="zh-CN">
 <head>
 <meta charset="UTF-8">
 <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no, shrink-to-fit=no" >
 <meta name="format-detection" content="telephone=no" >
 <title>移动端HTML模版</title>

   <!-- S DNS预解析 -->
   <link rel="dns-prefetch" href="">
   <!-- E DNS预解析 -->

   <!-- S 线上样式页面片，开发请直接取消注释引用 -->
   <!-- #include virtual="" -->
   <!-- E 线上样式页面片 -->

   <!-- S 本地调试，根据开发模式选择调试方式，请开发删除 -->
   <link rel="stylesheet" href="css/index.css" >
   <!-- /本地调试方式 -->

   <link rel="stylesheet" href="http://srcPath/index.css" >
   <!-- /开发机调试方式 -->
   <!-- E 本地调试 -->

   </head>
   <body>

   </body>
   </html>

```

- pc 端

```
<!DOCTYPE html>
<html lang="zh-CN">
<head>
<meta charset="UTF-8">
<meta name="keywords" content="your keywords">
<meta name="description" content="your description">
<meta name="author" content="author,email address">
<meta name="robots" content="index,follow">
<meta http-equiv="X-UA-Compatible" content="IE=Edge,chrome=1">
<meta name="renderer" content="ie-stand">
<title>PC端HTML模版</title>

<!-- S DNS预解析 -->
<link rel="dns-prefetch" href="">
<!-- E DNS预解析 -->

<!-- S 线上样式页面片，开发请直接取消注释引用 -->
<!-- #include virtual="" -->
<!-- E 线上样式页面片 -->

<!-- S 本地调试，根据开发模式选择调试方式，请开发删除 -->
<link rel="stylesheet" href="css/index.css" >
<!-- /本地调试方式 -->

<link rel="stylesheet" href="http://srcPath/index.css" >
<!-- /开发机调试方式 -->
<!-- E 本地调试 -->

</head>
<body>

</body>
</html>

```

## css

### 命名

- 统一使用中横线

`.info-title{ }`

### 属性书写顺序

- 定位属性：position left top right bottom display float overflow clear z-index visibility
- 自身属性：width height padding border margin background
- 文字样式：font-family font-size font-style font-weight font-varient color
- 文本属性：text-align  vertical-align  text-wrap  text-transform text-indent  text-decoration letter-spacing  word-spacing    white-space   text-overflow
- 其它(css3 中新增属性)：content box-shadow border-radius transform……

### css 缩写

- 尽量使用缩写属性，比如：padding, maring, font 等

### 代码格式化

- 统一使用工具进行格式，比如: **pretter**

### 代码大小写

- 样式选择器，属性名，属性值关键字全部使用小写字母书写，属性字符串允许使用大小写

`.jdc{ display: block}`

### 选择器

- 尽量少用通用选择器 \*
- 不使用 ID 选择器
- 不使用无具体语义定义的标签选择器

### 代码缩进

- 统一使用四个空格进行代码缩进

### 分号

- 每个属性声明末尾统计都要加上分号

### 属性值引号

- css 属性值需要用到引号时，统一使用单引号

`.jdc { font-family: 'Hiragino Sans GB'; }`

### CSS3 浏览器私有前缀写法

- CSS3 浏览器私有前缀在前，标准前缀在后
  `.jdc { -webkit-border-radius: 10px; -moz-border-radius: 10px; -o-border-radius: 10px; -ms-border-radius: 10px; border-radius: 10px; }`

### 注释

- 单行注释

- 注释内容第一个字符和最后一个字符都是一个空格字符，单独占一行，行与行之间相隔一行

- 模块注释

- 注释内容第一个字符和最后一个字符都是一个空格字符，/_ 与 模块信息描述占一行，多个横线分隔符-与_/占一行，行与行之间相隔两行

推荐

```
/* Module A
    ---------------------------------------------------------------- */
.mod_a {}

```

不推荐

```
/* Module A ---------------------------------------------------- */
.mod_a {}
```

- 文件信息注释

```
    @charset "UTF-8";
    /**
    * @desc File Info
    * @author Author Name
    * @date 2015-10-10
    */
```

## js 规范

### 变量申明

- 在声明变量时，一个声明只能有一个变量
- 禁止使用 var 进行变量的申明
- 推荐：复杂类型统一使用**const**,基础类型使用**let**,常量使用**const**

### 对象

- 使用对象字面量创建对象
- 请使用对象方法的简写方式

  ```
  const item = {
    value: 1,
    addValue(val) {
        return item.value + val
    }
  }
  ```

- 请使用对象属性值的简写方式

  ```
    const job = 'FrontEnd'
    // bad
    const item = {
       job: job
    }

    // good
     const item = {
        job
    }
  ```

- 对象属性值的简写方式要和声明式的方式分组

  ```
    const job = 'FrontEnd'
    const department = 'JDC'
    // bad
    const item = {
        sex: 'male',
        job,
        age: 25,
        department
    }

    // good
    const item = {
        job,
        department,
        sex: 'male',
        age: 25
    }

  ```

### 数组

- 使用字面量值创建数组
- 向数组中添加元素时，请使用 push 方法
- 使用拓展运算符 ... 复制数组
- 使用数组的 map 等方法时，请使用 return 声明，如果是单一声明语句的情况，可省略 return

### 解构赋值

- 当需要使用对象的多个属性时，请使用解构赋值

  ```
  // bad
  function getFullName (user) {
    const firstName = user.firstName
    const lastName = user.lastName

    return `${firstName} ${lastName}`
  }

  // good
  function getFullName (user) {
    const { firstName, lastName } = user

    return `${firstName} ${lastName}`
  }

  // better
   function getFullName ({ firstName, lastName }) {
     return `${firstName} ${lastName}`
    }

  ```

- 当需要使用数组的多个值时，请同样使用解构赋值

  ```
    const arr = [1, 2, 3, 4]

    // bad
    const first = arr[0]
    const second = arr[1]

    // good
    const [first, second] = arr
  ```

- 函数需要回传多个值时，请使用对象的解构，而不是数组的解构

  ```
    // bad
    function doSomething () {
        return [top, right, bottom, left]
    }

    // 如果是数组解构，那么在调用时就需要考虑数据的顺序
    const [top, xx, xxx, left] = doSomething()

    // good
    function doSomething () {
      return { top, right, bottom, left }
    }

    // 此时不需要考虑数据的顺序
    const { top, left } = doSomething()

  ```

### 函数

- 构造函数首字母大写
- 请使用函数声明，而不是函数表达式
- 不要使用 arguments，可以选择使用 ...

  ```
  // bad
  function test () {
      const args = Array.prototype.slice.call(arguments)
  return args.join('')
  }

  // good
  function test (...args) {
      return args.join('')
  }

  ```

- 不要更改函数参数的值

  ```
    // bad
    function test (opts) {
      opts = opts || {}
    }

    // good
    function test (opts = {}) {
      // ...
    }
  ```

### 原型

- 使用 class,避免使用 protype

### 模块

- 使用标准的 ES6 模块语法 import 和 export
- 不要使用 import 的通配符 \*，这样可以确保你只有一个默认的 export

### 迭代器

- 不要使用 iterators

  ```
   const numbers = [1, 2, 3, 4, 5]

   // bad
   let sum = 0
   for (let num of numbers) {
      sum += num
   }

   // good
   let sum = 0
   numbers.forEach(num => sum += num)

   // better
   const sum = numbers.reduce((total, num) => total + num, 0)

  ```

### 变量命名

- 使用驼峰命名

## 命名规范

### 目录命名

- 项目文件夹：projectname
- 样式文件夹：css
- 脚本文件夹：js
- 样式类图片文件夹：img

### 图片命名

命名顺序：图片业务(可选) + (mod\_)图片功能类别(必选) + 图片模块名称(可选)

- 图片业务
  - fx\_: 飞享
  - wx\_:微信
  - jd\_:京东
- 图片功能类别

  - mode\_：是否公共，可选
  - icon:模块
  - logo:LOGO 类
  - btn:按钮
  - bg:大背景

- 图片模块名称
  - goodslist:商品列表
  - goodsinfo:商品信息

### HTML/CSS 文件命名

- 确保文件命名总是以字母开头而不是数字，且字母一律小写，以中横线连接且不带其他标点符号

```
  goods-list.html
  good-detail.html
  goods-list.css

```

### 文件夹，组件命名
- 确保文件命名总是以字母开头而不是数字，且字母一律小写，以中横线连接且不带其他标点符号
