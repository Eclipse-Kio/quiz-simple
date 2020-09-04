# CSS 的使用

如果你最近不常写 CSS，那么写上简单的文字说明也行，  
如果你常写 CSS，那么附上简单的 Demo 代码更好。

Demo 代码可以新建一个或多个文件（不限），  
例如新建一个 `writing-style.css`，并在其中完成。

`说明：本人使用的css预处理语言较少，此处不太了解`

## Q1

下面是 PostCSS 编译后生成的代码，如果你来写源码，你会怎么写。
（实现方式不限，比如可以用 CSS in JS、Vue style 等方式）

```css
.container {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-pack: justify;
  -ms-flex-pack: justify;
  justify-content: space-between;
  -webkit-box-align: stretch;
  -ms-flex-align: stretch;
  align-items: stretch;
}
.container > div:nth-child(1) {
  -webkit-box-flex: 1;
  -ms-flex-positive: 1;
  flex-grow: 1;
}
```

## Q2

你用过哪些 CSS 的方法论和工具  
简单描述即可，例如：

> - PostCSS + autoprefixer 用来编译 CSS 代码，提高部分 CSS 的浏览器兼容性。
>
> - BEM 是用来处理 class 命名的，有一个三段式命名规则，形如 ↓：
>
> ```css
> .form--theme-xmas {
> }
> ```

答：

1. 可以定义一些标准的工具类，类似Bootstrap及Tailwind的理念，.mb .mp等
2. 生产环境中可以使用uglifycss对css文件进行压缩，去除不必要的空格及换行后减少传输带宽，提升用户体验。
3. 可复用组件的css定义应该写入单独的文件，便于管理
4. 尽量避免!important的使用，这样会使得CSS优先级算法失效
