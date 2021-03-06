## 一、flex布局是什么
    Flex是Flexible Box的缩写，意为"弹性布局"，用来为盒状模型提供最大的灵活性。

- 任何一个容器都可以指定为Flex布局。
    ```css
    .box{
      display: flex;
    }
    ```
- 行内元素也可以使用Flex布局。
    ```css
    .box{
      display: inline-flex;
    }
    ```
- Webkit内核的浏览器，必须加上`-webkit`前缀。
    ```css
    .box{
      display: -webkit-flex; /* Safari */
      display: flex;
    }
    ```
## 二、基本概念
    采用Flex布局的元素，称为Flex容器（flex container），简称"容器"。
    它的所有子元素自动成为容器成员，称为Flex项目（flex item），简称"项目"。
    容器默认存在两根轴：水平的主轴、垂直的交叉轴。
    项目默认沿主轴排列。
## 三、容器的属性
#### flex-direction

- `flex-direction:row` （默认值）
    - 左 → 右
    - 主轴为水平方向，起点在左端
- `flex-direction:row-reverse`
    - 右 → 左
    - 主轴为水平方向，起点在右端
- `flex-direction:column`
    - 上 → 下
    - 主轴为垂直方向，起点在上沿
- `flex-direction:column-reverse`
    - 下 → 上
    - 主轴为垂直方向，起点在下沿

#### flex-wrap
决定项目换行方式
- `nowrap`
    - 不换行（默认值）
- `wrap`
    - 换行，第一行在上方
- `wrap-reverse`
    - 换行，第一行在下方

#### flex-flow
是`flex-direction`属性和`flex-wrap`属性的简写形式

```css
flex-flow:row nowrap; /*默认*/
```

#### justify-content
定义项目在主轴上的对齐方式
- `flex-start`（默认值）
    - 与主轴起点对齐
- `flex-end`
    - 与主轴终点对齐
- `center`
    - 与主轴中点对齐
- `space-between`
    - 两端对齐，项目之间的间隔都相等。
- `space-around`
    - 每个项目两侧的间隔相等。所以，项目之间的间隔比项目与边框的间隔大一倍。

#### align-items
定义项目在交叉轴上如何对齐
- `flex-start`
    - 交叉轴的起点对齐。
- `flex-end`
    - 交叉轴的终点对齐。    
- `center`
    - 交叉轴的中点对齐。
- `baseline`
    - 项目的第一行文字的基线对齐。
- `stretch`（默认值）
    - 如果项目未设置高度或设为auto，将占满整个容器的高度。

#### align-content
定义了多根轴线的对齐方式。如果项目只有一根轴线，该属性不起作用。
- `flex-start`
    - 与交叉轴的起点对齐
- `flex-end`
    - 与交叉轴的终点对齐。
- `center`
    - 与交叉轴的中点对齐。
- `space-between`
    - 与交叉轴两端对齐，轴线之间的间隔平均分布。
- `space-around`
    - 每根轴线两侧的间隔都相等。所以，轴线之间的间隔比轴线与边框的间隔大一倍。
- `stretch`（默认值）
    - 轴线占满整个交叉轴。

## 四、项目的属性
#### order
定义项目的排列顺序。值为整数，数值越小，排列越靠前，默认为0。

#### flex-grow
定义项目的放大比例（放大倍数），默认为0，即如果存在剩余空间，也不放大。</br>
如果所有项目的flex-grow属性都为1，则它们将等分剩余空间（如果有的话）。如果一个项目的flex-grow属性为2，其他项目都为1，则前者占据的剩余空间将比其他项多一倍。

#### flex-shrink
定义了项目的缩小比例，默认为1，即如果空间不足，该项目将缩小。</br>\
如果所有项目的flex-shrink属性都为1，当空间不足时，都将等比例缩小。如果一个项目的flex-shrink属性为0，其他项目都为1，则空间不足时，前者不缩小。</br>
负值无效

#### flex-basis
定义在分配多余空间之前，项目占据的主轴空间（main size）。浏览器根据这个属性，计算主轴是否有多余空间。它的默认值为auto，即项目的本来大小。</br>
它可以设为跟width或height属性一样的值（比如350px），则项目将占据固定空间。
#### flex
是flex-grow, flex-shrink 和 flex-basis的简写

- `flex:0 1 auto;`（默认值）
- `flex:1 0;`
- `flex:1`
- `flex:auto;` 1 1 auto
- `flex:none;` 0 0 auto

#### align-self
允许单个项目有与其他项目不一样的对齐方式，可覆盖align-items属性。属性值除了auto， 和align-items属性的值相同

-  `auto`（默认值）
    - 表示继承父元素的align-items属性，如果没有父元素，则等同于stretch。
- `flex-start`
    - 与交叉轴的起点对齐。
- `flex-end`
    - 与交叉轴的终点对齐。    
- `center`
    - 与交叉轴的中点对齐。
- `baseline`
    - 与项目的第一行文字的基线对齐。
- `stretch`（默认值）
    - 如果项目未设置高度或设为auto，将占满整个容器的高度。
