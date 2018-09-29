# 单例模式

------

## 什么是单例模式

     单例模式定义：保证一个类仅有一个实例，并提供一个访问它的全局访问点。
## 单例模式使用场景

    单例模式是一种常用的设计模式，有些对象我们往往只需要一个，如：全局缓存，windows对象，部分弹框中的需求。

## 实例分析

     登录弹窗。在网页上有个登录按钮，当点击登录按钮的时候，会弹出一个登录窗口，很显然这种登录窗口是唯一的，不可能出现两个登录窗口的情况。
     
### 解决方案1：

     在页面加载完成的时候便创建好这个 div 浮窗，这个浮窗一开始肯定是隐藏状态的，当用户点击登录按钮的时候，它才开始显示。这种方式在于不需要登录的人来说，明显
     会创造多余的dom节点。
```<html>
    <body>
        <button id="loginBtn">登录</button>
        <div class="login model" id="loginModel" >
          我是登录窗口
        </div>
        </body>
        <script>
            document.getElementById( 'loginBtn' ).onclick = function(){
            var  loginLayer=document.getElementById('loginModel');
            loginLayer.style.display = 'block';
           };
        </script>
      <body>
    </html>
