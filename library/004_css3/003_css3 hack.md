## css3 hack
因为css3并不是所有的浏览器都支持，有些浏览器虽然支持，但是效果也不是很好，所以这些浏览器在支持这些新特性的时候，给这些属性加入自己的厂名，等到css3标准化后再将厂名去掉，比方说：对于圆角的支持。
```
.box{
    -o-border-radius: 30px;         /* opera欧朋 */
    -ms-border-radius: 30px;         /* IE9 */
　　-moz-border-radius: 30px;       /* FF火狐 */
　　-webkit-border-radius: 30px;    /* Safari苹果, Chrome谷歌 */
　　border-radius: 30px;        
}
```
