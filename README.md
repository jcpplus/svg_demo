svg_demo
========

sample svg demo.for beginner

#### svg 教程

*SVG 指可伸缩矢量图形 (Scalable Vector Graphics)*
*SVG 用来定义用于网络的基于矢量的图形*
*SVG 使用 XML 格式定义图形*
*SVG 图像在放大或改变尺寸的情况下其图形质量不会有所损失*
*SVG 是万维网联盟的标准*
*SVG 与诸如 DOM 和 XSL 之类的 W3C 标准是一个整体*

#### svg嵌入页面
    - <embed>, <object>, <iframe> 三种方式嵌入页面，src="*.svg"
    - 我们也可以仅通过svg的空间命名，就把svg引入html页面中。

~~~~~~html
<html xmlns:svg="http://www.w3.org/2000/svg">
<body>

<p>This is an HTML paragraph</p>

<svg:svg width="300" height="100" version="1.1" >
<svg:circle cx="100" cy="50" r="40" stroke="black"
stroke-width="2" fill="red" />
</svg:svg>

</body>
</html>
~~~~~~

#### 例子

##### circle

**代码**

```xml
<?xml version="1.0" standalone="no"?>
<!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN" 
"http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd">

<svg width="100" height="100" version="1.1"
xmlns="http://www.w3.org/2000/svg">

<circle cx="100" cy="50" r="40" stroke="black"
stroke-width="2" fill="red"/>
</svg>
```

*说明*

cx和cy属性定义圆点的x和y坐标。如果省略cx和cy，则圆的中心会设置为(0, 0)


##### 矩形

**代码**

```xml
<?xml version="1.0" standalone="no"?>
<!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN" 
"http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd">

<svg width="100%" height="100%" version="1.1"
xmlns="http://www.w3.org/2000/svg">

<rect width="300" height="100"
style="fill:rgb(0,0,255);stroke-width:1;
stroke:rgb(0,0,0)"/>

</svg>
```

**解释**

    - rect 元素的 width 和 height 属性可定义矩形的高度和宽度
    - style 属性用来定义 CSS 属性
    - CSS 的 fill 属性定义矩形的填充颜色（rgb 值、颜色名或者十六进制值）
    - CSS 的 stroke-width 属性定义矩形边框的宽度
    - CSS 的 stroke 属性定义矩形边框的颜色

##### 椭圆
**代码**
```xml
<?xml version="1.0" standalone="no"?>
<!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN" 
"http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd">

<svg width="100%" height="100%" version="1.1"
xmlns="http://www.w3.org/2000/svg">

<ellipse cx="300" cy="150" rx="200" ry="80"
style="fill:rgb(200,100,50);
stroke:rgb(0,0,100);stroke-width:2"/>
</svg>
```

**解释**

    - cx定义圆心x坐标
    - cy定义圆心y坐标
    - rx定义水平（x）方向半径
    - ry定义垂直（y）方向半径

##### 线条
**代码**
```xml
<?xml version="1.0" standalone="no"?>
<!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN" 
"http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd">

<svg width="100%" height="100%" version="1.1"
xmlns="http://www.w3.org/2000/svg">

<line x1="0" y1="0" x2="300" y2="300"
style="stroke:rgb(99,99,99);stroke-width:2"/>

</svg>
```

**解释**

    - x1 属性在 x 轴定义线条的开始
    - y1 属性在 y 轴定义线条的开始
    - x2 属性在 x 轴定义线条的结束
    - y2 属性在 y 轴定义线条的结束

##### 多边形
**代码**
```xml
<?xml version="1.0" standalone="no"?>
<!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN" 
"http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd">

<svg width="100%" height="100%" version="1.1"
xmlns="http://www.w3.org/2000/svg">

<polygon points="220,100 300,210 170,250 123,234"
style="fill:#cccccc;stroke:#000000;stroke-width:1"/>
</svg>
```

**解释**

    - polygon 用于创建不少于三个边的多边形，points="x1,y1 x2,y2 x3,y3 x4,y4..."

##### 折线
**代码**
```xml
<?xml version="1.0" standalone="no"?>
<!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN" 
"http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd">

<svg width="100%" height="100%" version="1.1"
xmlns="http://www.w3.org/2000/svg">

<polyline points="0,0 0,20 20,20 20,40 40,40 40,60"
style="fill:white;stroke:red;stroke-width:2"/>

</svg>
```

**解释**

    - polyline用来创建仅包含直线的形状

##### 路径
**代码**
```xml
<?xml version="1.0" standalone="no"?>
<!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN" 
"http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd">

<svg width="100%" height="100%" version="1.1"
xmlns="http://www.w3.org/2000/svg">

<path d="M153 334
C153 334 151 334 151 334
C151 339 153 344 156 344
C164 344 171 339 171 334
C171 322 164 314 156 314
C142 314 131 322 131 334
C131 350 142 364 156 364
C175 364 191 350 191 334
C191 311 175 294 156 294
C131 294 111 311 111 334
C111 361 131 384 156 384
C186 384 211 361 211 334
C211 300 186 274 156 274"
style="fill:white;stroke:red;stroke-width:2"/>

</svg>
```

`！由于绘制路径的复杂性，因此强烈建议您使用 SVG 编辑器来创建复杂的图形。`

**解释**

    - M = moveto
    - L = lineto
    - H = horizontal lineto
    - V = vertical lineto
    - C = curveto
    - S = smooth curveto
    - Q = quadratic Belzier curve
    - T = smooth quadratic Belzier curveto
    - A = elliptical Arc
    - Z = closepath


