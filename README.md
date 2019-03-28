# 3d旋转相册
    效果如下：
![](3d.gif)    
    
    html+css代码
```angular2
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>3d旋转相册</title>
</head>
<body>
<style>
    body{
        background: #111;
    }
    .whole{
        /*perspective 属性定义 3D 元素距视图的距离*/
        perspective: 5000px;
        /*使被转换的子元素保留其 3D 转换：该属性必须与 transform 属性一同使用*/
        transform-style: preserve-3d;
        /*transform 属性向元素应用 2D 或 3D 转换。该属性允许我们对元素进行旋转、缩放、移动或倾斜。*/
        transform: rotateX(-20deg);
        -webkit-transform: rotateX(-20deg);
        -moz-transform: rotateX(-20deg);
    }
    .pic_box{
        position: relative;
        width:150px;
        height:200px;
        border:1px solid red;
        margin:140px auto 0;
        /*使被转换的子元素保留其 3D 转换：该属性必须与 transform 属性一同使用*/
        transform-style:preserve-3d;
        -webkit-animation:rotate1 10s linear infinite;
        -moz-animation:rotate1 10s linear infinite;
        /*animation: name duration timing-function delay iteration-count direction;*/
        animation:rotateAnimations 10s linear infinite;
        -webkit-animation:rotateAnimations 10s linear infinite;
        -moz-animation:rotateAnimations 10s linear infinite;
    }
    img{
        width: 150px;
        height: 250px;
        position: absolute;
        top:0;
        left:0;
        /*box-reflect：none | <direction> <offset>? <mask-box-image>?*/
        /*详情：https://www.html.cn/book/css/properties/only-webkit/box-reflect.htm*/
        -webkit-box-reflect:below 20px -webkit-linear-gradient(top,rgba(250,250,250,0),rgba(250,250,250,0) 30%,rgba(250,250,250,0.5));
    }
    img:nth-child(1){
        transform: rotateY(0deg) translateZ(300px);
        -webkit-transform: rotateY(0deg) translateZ(300px);
        -moz-transform: rotateY(0deg) translateZ(300px);
    }
    img:nth-child(2){
        transform: rotateY(36deg) translateZ(300px);
        -webkit-transform: rotateY(36deg) translateZ(300px);
        -moz-transform: rotateY(36deg) translateZ(300px);
    }
    img:nth-child(3){
        transform: rotateY(72deg) translateZ(300px);
        -webkit-transform: rotateY(72deg) translateZ(300px);
        -moz-transform: rotateY(72deg) translateZ(300px);
    }
    img:nth-child(4){
        transform: rotateY(108deg) translateZ(300px);
        -webkit-transform: rotateY(108deg) translateZ(300px);
        -moz-transform: rotateY(108deg) translateZ(300px);
    }
    img:nth-child(5){
        transform: rotateY(144deg) translateZ(300px);
        -webkit-transform: rotateY(144deg) translateZ(300px);
        -moz-transform: rotateY(144deg) translateZ(300px);
    }
    img:nth-child(6){
        transform: rotateY(180deg) translateZ(300px);
        -webkit-transform: rotateY(180deg) translateZ(300px);
        -moz-transform: rotateY(180deg) translateZ(300px);
    }
    img:nth-child(7){
        transform: rotateY(216deg) translateZ(300px);
        -webkit-transform: rotateY(216deg) translateZ(300px);
        -moz-transform: rotateY(216deg) translateZ(300px);
    }
    img:nth-child(8){
        transform: rotateY(252deg) translateZ(300px);
        -webkit-transform: rotateY(252deg) translateZ(300px);
        -moz-transform: rotateY(252deg) translateZ(300px);
    }
    img:nth-child(9){
        transform: rotateY(288deg) translateZ(300px);
        -webkit-transform: rotateY(288deg) translateZ(300px);
        -moz-transform: rotateY(288deg) translateZ(300px);
    }
    img:nth-child(10){
        transform: rotateY(324deg) translateZ(300px);
        -webkit-transform: rotateY(324deg) translateZ(300px);
        -moz-transform: rotateY(324deg) translateZ(300px);
    }
    @keyframes rotateAnimations {
        0% {
            transform: rotateY(0deg);
            -webkit-transform: rotateY(0deg);
            -moz-transform: rotateY(0deg);
        }
        100% {
            transform: rotateY(360deg);
            -webkit-transform: rotateY(360deg);
            -moz-transform: rotateY(360deg);
        }
    }
</style>
<div class="whole">
    <div class="pic_box">
        <img src="img/1.jpg" alt="">
        <img src="img/2.jpg" alt="">
        <img src="img/3.jpg" alt="">
        <img src="img/4.jpg" alt="">
        <img src="img/5.jpg" alt="">
        <img src="img/6.jpg" alt="">
        <img src="img/7.jpg" alt="">
        <img src="img/8.jpg" alt="">
        <img src="img/9.jpg" alt="">
        <img src="img/10.jpg" alt="">
    </div>
</div>
</body>
</html>
```    
