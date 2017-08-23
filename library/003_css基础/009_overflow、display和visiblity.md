# overflow、display和visibility

## overflow属性

```css
overflow:hidden;  /* 将超出的内容隐藏 */
overflow:visible; /* 全部显示内容 */
overflow:scroll;  /* 始终出现滚动条 */
overflow:auto;    /* 自动调整，超出时才出现滚动条 */
overflow-x:hidden;/* 只对横向超出的内容进行设置 */
overflow-y:hidden;/* 只对纵向超出的内容进行设置 */
```

## display属性
```css
/* 让元素隐藏起来并且不占用页面空间 */
display:none;
/* 将任何元素转为块元素 */
display:block;
/* 将任何元素转为行元素 */
display:inline;
/* 将任何元素转为行内块元素 */
display:inline-block;
```

【兼容性】在IE6中当行内元素转换为块元素时，高度会比原有的高度大，所以要设置overflow:hidden,来做兼容。

## visibility属性
主要是控制元素的隐藏和显示状态,想当于opacity的0和1状态。【隐藏状态下浏览器认为该元素存在，但是不显示出来，所有隐藏的元素还会占据原有的位置】
```css
/* 显示状态 */
visibility:visible;

/* 隐藏状态 */
visibility:hidden;

/* 隐藏表格的一行或一列 */
visibility:collapse;

```
