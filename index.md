## Welcome to ABS 中文家园

ABS是我们自己的事情，此时宣传就是为自己宣传，此时做事就是为自己做事。
    只要我们团结齐心，勇往直前，ABS定能王者归来！！！

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>实现多页签切换效果</title>
    <script src="jquery-1.11.3.js"></script>
    <style>
        * {margin: 0; padding: 0;}
        #tab li {float: left;list-style: none;width: 72px;height: 40px;line-height: 40px;cursor: pointer;text-align: center;color: #fff;font-weight: bold;}
        #container {position: relative;}
        #content1, #content2, #content3,#content4,#content5 {width: 300px;height: 100px;padding: 30px;position: absolute;top: 40px;left: 0;}
        #tab1, #content1 {background-color: #ffcc00;}
        #tab2, #content2 {background-color: #ff00cc;}
        #tab3, #content3 {background-color: #90EE90;}
        #tab4, #content4 {background-color: #FFC0CB;}
         #tab5, #content5 {background-color: #FF5500;}
        .foreground {z-index: 1;}
    </style>
</head>
<body>
    <h2>实现多标签页效果</h2>
    <ul id="tab">
        <li id="tab1" value="1">全部</li>
        <li id="tab2" value="2">待付款</li>
        <li id="tab3" value="3">待发货</li>
        <li id="tab4" value="4">已发货</li>
        <li id="tab5" value="5">已完成</li>
    </ul>
    <div id="container">
        <!--<div id="content1" class="foreground">-->
        <!--强调：使用style.设置的属性，默认格式都是:
            "属性: 值;"-->
        <div id="content1" style="z-index: 1;">
            111111111111111111111111
        </div>
        <div id="content2">
           222222222222222222222222222
        </div>
        <div id="content3">
           3333333333333333333333333
        </div>
        <div id="content4">
           444444444444444444444444
        </div>
        <div id="content5">
           555555555555555555555555
        </div>
    </div>

    <script>
    // 1. 为li元素绑定click事件
    $("#tab>li").click(function(){
        $("#content"+$(this).val()).attr("style","z-index: 1;").siblings("div").removeAttr("style");
    });
    </script>
</body>
</html>
