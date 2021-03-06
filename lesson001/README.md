# 第一章

## 简单介绍些概念（你可能要用到的工具）

### terminal（控制台）

说到**控制台**，这里将会出现两个：

* 一个是**命令行工具 - terminal**；
* 另外一个是下面将要提到的浏览器**调试工具 - console**。

当前所说的 **控制台（terminal）** 主要用来执行命令，最近几章会涉及到的命令基本都是 git 相关
的。也可能会出现简单的文件操作命令，例如 `mkdir playground` 这种。

> 你要执行的操作都会放到引用块中，就像当前行这样的。
>
> 按照里面所述内容操作即可。
>
> 命令一般会 `looks like this` <- 长这样。

*控制台中执行的每行命令后面都要记得敲 `Enter` 键哦。*

### git（版本控制工具）

git 是新且优于上一代版本控制工具 svn 的、目前普及度更高且更好用的版本控制工具。这个学习项目
所在的 [GitHub](https://github.com) 是最大的 git 资源站。

#### 下面介绍几个简单的 git 命令：

* `git clone {url}` 将项目克隆到本地
* `git status` 查看当前项目状态
  * 执行改命令前需要先进入项目目录，本项目的目录（可能）是 `~/playground/geek-10101`
* `git pull` 从远程代码仓库拉取（更新）新的代码
  * 本项目会不定期更新，你可以在[项目页](https://github.com/geekpark/geek-10101)点击
  `watch` 按钮，当项目更新时将收到提醒，在本地项目目录下执行该命令即可得到最新的内容。

*目前你所要了解的 git 命令就这么多，后期将会有更详细的功能更强大的介绍，慢慢来。*

### 文本编辑器

学习是需要过程的，为了保持学习兴趣，我们将从 **html** 和 **javascript** 开始，因为这是最
快速能见到效果，能够实时享受编程快感的途径。

javascript 是解释型语言（其他还有编译型和编译解释型等等，先不做介绍），不需要编译就可以执 行
（依赖浏览器），因此我们只需要一个文本编辑器就够了。

* Windows 下可以使用 [notepad++](https://notepad-plus-plus.org/)
* Mac 和 Linux 下建议使用 [Atom](https://atom.io/)

这两个是目前对应平台下比较先进好用的编辑器，基本零配置，装上就能用。

### 浏览器

我们近期要学习的东西（html，css，javascript）都是运行于客户端的（即浏览器），所以，除了
编辑器我们还需要个浏览器。

全平台推荐使用 Chrome，其次，Mac 下可以使用 Safari，Windows 下可以使用 firefox 或 360
浏览器。

后面我们都以 Chrome 为例做讲解，几个浏览器的快捷键和界面都是相近的。

#### 浏览器中的控制台（console）

现代浏览器越来越智能，越来越强大，但对于日益复杂的前端开发来说**调试**仍然是场噩梦，幸好目前
流行的浏览器大多提供了**开发者工具**，以便前端调试他们的代码。

上面提到的几款现代浏览器打开开发者工具的快捷键都是相同的 `command + alt + i`，Windows 下
可以试试直接按 `F12`。

开发者工具样子看起来不太一样，但基本都是标签页形式的，我们要用到的几项也都有，包括：

* Elements 或者叫做 Inspector（Firefox）
  * 这个工具是用来查看 html 文档元素的，这里你可以看到折叠的当前页面的 dom 树
* Network
  * 这里可以看到一个网页（站）的所有网络请求，短期几节课内还用不到
* Console
  * 即控制台，这里会显示 js 的信息、警告或错误，也可以直接运行 js 代码，在拥有编辑器之前你
  可以尝试现在这里执行下面的 Hello World 程序。

*开发者工具的功能非常强大，其它部分在适当的时候做介绍。*

## 如何开始

如果你已经运行了首页 `README` 中提到的命令，那么这个项目应该已经存在于你本地机器上了，很可能是
这个路径 `~/playground/geek-10101`，或者：

* Windows 下修改 `~` 为某个盘符，类似 `D:/playground`
* Linux 下绝对路径类似 `/home/{user}/playground`
* Max 下绝对路径类似 `/Users/{User}/playground`

每一章的课程目录下都会有一个 `README.md` 文件，用来说明当前课程和涉及到的一些知识点，其他
文件都是 demo 文件，内附说明注释，不同的文件注释格式是不同的：

#### html 的注释：

```html
<!-- 这是 html 文件中的注释格式 -->
<strong>这里是 html 代码</strong>
<p>
html 代码中也可能包含内嵌 css 或 js 代码
相应注释格式参考下面的例子
</p>
<!--
可能是单行
也可能是多行
-->
```

#### javascript 的注释：

```javascript
// 这种是 javascript 中的单行注释
var demo = '这里是 js 代码';

/*
也可能是多行的
就像这样
*/

debug(demo); // 调用 debug 方法

/**
 * @param       str     输出文本
 * @description 这是个文档注释，用来说明一个方法的用途，可以用来生成文档（了解一下就好）
 */
function debug(str) {
    console.log(str);
}
```

#### css（级联样式表）的注释：

```css
/* 样式表中的注释 */
.geekpark {
    margin: 7px auto;
}
/*
除了 README 文件之外，
注释中也会加入一些指引，
你大多情况下都可以随意编辑 demo 文件，
保存后刷新浏览器就能看到结果。
*/
```

## 按照传统，写个 Hello World 程序

> 在你浏览器的控制台中尝试执行如下代码
>
> 注意每输入一行后敲 `Enter` 键
>
> 注释行不用输入

```javascript
// 弹出一个对话框
alert('Welcome to geekpark.net');
// 定义一个名为 email 的字符串变量
var email = 'hr@geekpark.net';
// 在控制台输出这个变量
console.log('E-mail:', email);
// 花式字符串变数组
email.split(/[@\.]/);
/*
上一行得到的结果：
["hr", "geekpark", "net"]
*/
```

这一章暂时就到这里，后面将会做一些好玩实用的东西，敬请期待～
