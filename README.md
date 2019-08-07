[toc]
## 前端面试题汇总
---
### 个人背景
![image](./src/img/logo.png)

![image](C:/Users/JackLin/Desktop/
15093777.jpg)
说起自己的前端之路，就想起大一时候一位同学找我帮忙的事情，那时候的我虽然选择了计算机专业，但其实并不清楚以后甚至当时是要干嘛的。但是我的一位同学他以为我是计算机专业的就叫我帮他做一个很简单的个人网页，然后我就硬着头皮帮他做了，从此就走上了不归路。。。
然后大一就参加了计算机学院一个工作室的面试，很遗憾在最后一轮考核中被刷了，虽然花了两个多月的时间没能进去工作室，但还是收获颇多，这也自己第一次系统地去学习前端知识，也为自己在大二第一个学期找到学习奠定了基础。

大二第一学期我收到了人生第一份offer，然后进入一家游戏公司开发H5小游戏，基本上大二都在实现。然后大三自己又想回到学校待一年，然后就进入了现在的小A创客教育团队，然后开发了我们团队的官网。

---
### 大厂建议
其实在大公司里面，做前端开发重要的东西并不是你能够做得多好看，而是你做的那些东西里面安全性好不好，性能高不高。因为一旦重要信息泄露了，那就会导致很多无法想象的事情，所以需要注重安全性。
一下几个方面都是重点
> JS基础  
计算机网络  
性能优化  
开发技巧  
移动端知识  
安全性问题

---
### 一、HTML试题
#### HTML5有哪些新特性、移除了哪些元素？
Html5新增了 27 个元素，废弃了 16 个元素，根据现有的标准规范，把 HTML5 的元素按优先级定义为结构性属性、级块性元素、行内语义性元素和交互性元素 4 大类。

结构性元素主要负责web上下文结构的定义

section：在 web 页面应用中，该元素也可以用于区域的章节描述。

header：页面主体上的头部， header 元素往往在一对 body 元素中。

footer：页面的底部（页脚），通常会标出网站的相关信息。

nav：专门用于菜单导航、链接导航的元素，是 navigator 的缩写。

article：用于表现一篇文章的主体内容，一般为文字集中显示的区域。

级块性元素主要完成web页面区域的划分，确保内容的有效分割。

aside：用于表达注记、贴士、侧栏、摘要、插入的引用等作为补充主体的内容。

figure：是对多个元素进行组合并展示的元素，通常与 ficaption 联合使用。

code：表示一段代码块。

dialog：用于表达人与人之间的对话，该元素包含 dt 和 dd 这两个组合元素， dt 用于表示说话者，而 dd 用来表示说话内容。

行内语义性元素主要完成web页面具体内容的引用和描述，是丰富内容展示的基础。

meter：表示特定范围内的数值，可用于工资、数量、百分比等。

time：表示时间值。

progress：用来表示进度条，可通过对其 max 、 min 、 step 等属性进行控制，完成对进度的表示和监事。

video：视频元素，用于支持和实现视频文件的直接播放，支持缓冲预载和多种视频媒体格式。

audio：音频元素，用于支持和实现音频文件的直接播放，支持缓冲预载和多种音频媒体格式。

交互性元素主要用于功能性的内容表达，会有一定的内容和数据的关联，是各种事件的基础。

details：用来表示一段具体的内容，但是内容默认可能不显示，通过某种手段（如单击）与 legend 交互才会显示出来。

datagrid：用来控制客户端数据与显示，可以由动态脚本及时更新。

menu：主要用于交互菜单（曾被废弃又被重新启用的元素）。

command：用来处理命令按钮。

#### 表单提交中Get和Post方式的区别？
(1)、 get 是从服务器上获取数据， post 是向服务器传送数据。  
(2)、 get 是把参数数据队列加到提交表单的 ACTION 属性所指的 URL 中，值和表单内各个字段一一对应，在 URL 中可以看到。 post 是通过 HTTP post 机制，将表单内各个字段与其内容放置在 HTML HEADER 内一起传送到 ACTION 属性所指的 URL 地址 , 用户看不到这个过程。  
(3)、对于 get 方式，服务器端用 Request.QueryString 获取变量的值，对于 post 方式，服务器端用 Request.Form 获取提交的数据。  
(4)、 get 传送的数据量较小，因此相对简单且速度快，不能大于 2KB 。 post 传送的数据量较大，一般被默认为不受限制。但理论上， IIS4 中最大量为 80KB ， IIS5 中为 100KB 。  
(5)、 get 安全性低， post 安全性较高。

---
### 二、CSS试题
#### 请举例集中清除浮动的方法？
1. 父级div定义 height   
原理：父级div手动定义height，就解决了父级div无法自动获取到高度的问题。   
优点：简单、代码少、容易掌握   
缺点：只适合高度固定的布局，要给出精确的高度，如果高度和父级div不一样时，会产生问题   
建议：不推荐使用，只建议高度固定的布局时使用 

2. 结尾处加空div标签 clear:both   
原理：添加一个空div，利用css提高的clear:both清除浮动，让父级div能自动获取到高度   
优点：简单、代码少、浏览器支持好、不容易出现怪问题   
缺点：不少初学者不理解原理；如果页面浮动布局多，就要增加很多空div，让人感觉很不好   
建议：不推荐使用，但此方法是以前主要使用的一种清除浮动方法    

3. 父级div定义 伪类:after 和 zoom 
原理：IE8以上和非IE浏览器才支持:after，原理和方法2有点类似，zoom(IE转有属性)可解决ie6,ie7浮动问题   
优点：浏览器支持好、不容易出现怪问题（目前：大型网站都有使用，如：腾迅，网易，新浪等等）   
缺点：代码多、不少初学者不理解原理，要两句代码结合使用才能让主流浏览器都支持。   
建议：推荐使用，建议定义公共类，以减少CSS代码。  

4. 父级div定义 overflow:hidden   
原理：必须定义width或zoom:1，同时不能定义height，使用overflow:hidden时，浏览器会自动检查浮动区域的高度   
优点：简单、代码少、浏览器支持好   
缺点：不能和position配合使用，因为超出的尺寸的会被隐藏。   
建议：只推荐没有使用position或对overflow:hidden理解比较深的朋友使用。

5. 父级div定义 overflow:auto   
原理：必须定义width或zoom:1，同时不能定义height，使用overflow:auto时，浏览器会自动检查浮动区域的高度   
优点：简单、代码少、浏览器支持好   
缺点：内部宽高超过父级div时，会出现滚动条。   
建议：不推荐使用，如果你需要出现滚动条或者确保你的代码不会出现滚动条就使用吧。

#### 谈谈你对CSS中的单位的认识？ 
a、特殊值0可以省略单位。例如：margin:0px可以写成margin:0   
b、一些属性可能允许有负长度值，或者有一定的范围限制。如果不支持负长度值，那应该变换到能够被支持的最近的一个长度值。   
c、长度单位包括：相对单位和绝对单位。   
相对长度单位有： em, ex, ch, rem, vw, vh, vmax, vmin   
绝对长度单位有： cm, mm, q, in, pt, pc, px  
绝对长度单位：1in = 2.54cm = 25.4 mm = 72pt = 6pc = 96px  

#### 盒子模型是什么？有几种模型？各有什么特点？
- 把所有的网页元素都看成一个个盒子，它具有content、padding、border以及margin四个属性，这就是盒子模型。盒子模型有标准盒子模型和怪异盒子模型
- 标准盒子模型：width = content.width
- 怪异盒子模型：width = content.width + padding-left + padding-right + border-left + border-right

#### li和li之间为什么出现空白间隙？如何消除
- 原因：以为浏览器默认行为会把`inline`元素间的空白字符（包括空格、换行和tab）渲染成一个空格
- 消除方法
```
    // 方法一：把所有的li写成一行，不要出现空白字符；缺点：代码看起来有点乱
    <ul>
        <li class="part1"></li><li class="part2"></li><li class="part3"></li><li class="part4"></li>
    </ul>
    // 方法二：给ul内的字符尺寸设置为0;缺点：导致里面所有字符都看不到
    .wrap ul {font-size:0px};
    // 方法三：
    .wrap ul{letter-spacing: -4px;}
    .wrap ul li{letter-spacing: normal;}
```

#### 如何给位置宽高的元素设置水平垂直居中？
- 方法一
```
    .parent1 {
        display:table-cell;
        vertical-align:middle;
        text-align:center
    }
    .parent1 .child {
        vertical-align: middle;
    }
```
- 方法二：子元素绝对定位，距离顶部50%，距离底部50%；然后使用css3 transform：translate(-50%; -50%)
```
    .parent2 {
        position: relative;
    }
    .child {
        position:absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%)
    }
```
- 方法三：使用flex布局
```
    .parent3 {
        display: flex;
        justify-content: center; // 水平居中
        align-items: center; // 垂直居中
    }
```

#### 谈谈你对box-sizing的认识？
设置或检索对象的盒模型组成模式  

a、box-sizing:content-box（默认样式）： padding和border不被包含在定义的width和height之内。对象的实际宽度等于设置的width值和border、padding之和，即 ( Element width = width + border + padding，但占有页面位置还要加上margin ) 此属性表现为**标准模式**下的盒模型。   

b、box-sizing:border-box： padding和border被包含在定义的width和height之内。对象的实际宽度就等于设置的width值，即使定义有border和padding也不会改变对象的实际宽度，即 ( Element width = width ) 此属性表现为**怪异模式**下的盒模型。

#### 谈谈你对BFC和IFC的理解?
1. 什么是BFC与IFC  
- BFC（Block Formatting Context）即“块级格式化上下文”， IFC（Inline Formatting Context）即行内格式化上下文。常规流（也称标准流、普通流）是一个文档在被显示时最常见的布局形态。一个框在常规流中必须属于一个格式化上下文，你可以把BFC想象成一个大箱子，箱子外边的元素将不与箱子内的元素产生作用。

- BFC是W3C CSS 2.1 规范中的一个概念，它决定了元素如何对其内容进行定位，以及与其他元素的关系和相互作用。当涉及到可视化布局的时候，Block Formatting Context提供了一个环境，HTML元素在这个环境中按照一定规则进行布局。一个环境中的元素不会影响到其它环境中的布局。比如浮动元素会形成BFC，浮动元素内部子元素的主要受该浮动元素影响，两个浮动元素之间是互不影响的。也可以说BFC就是一个作用范围。

- 在普通流中的 Box(框) 属于一种 formatting context(格式化上下文) ，类型可以是 block ，或者是 inline ，但不能同时属于这两者。并且， Block boxes(块框) 在 block formatting context(块格式化上下文) 里格式化， Inline boxes(块内框) 则在 Inline Formatting Context(行内格式化上下文) 里格式化。

2. 如何产生BFC  
当一个HTML元素满足下面条件的任何一点，都可以产生Block Formatting Context：
- float的值不为none
- overflow的值不为visible
- display的值为table-cell, table-caption, inline-block中的任何一个
- position的值不为relative和static

CSS3触发BFC方式则可以简单描述为：在元素定位非static，relative的情况下触发，float也是一种定位方式。

3. BFC的作用与特点
- 不和浮动元素重叠，清除外部浮动，阻止浮动元素覆盖
- 如果一个浮动元素后面跟着一个非浮动的元素，那么就会产生一个重叠的现象。常规流（也称标准流、普通流）是一个文档在被显示时最常见的布局形态，当float不为none时，position为absolute、fixed时元素将脱离标准流。

---
### 三、JavaScript以及其他JS库试题

#### ES6、ES5和TypeScipt 的区别
- TypeScript是Javascript的超集，也就是它包括ES5和ES6；ES5是ECMAScript的第五次修订版本，ES6是ECMAScript的第六次修订版本。
- ES6中的一些新特点
> ES6中多了变量声明let和const，let的增加是为js新增块级作用域，ES5中没有块级作用域。   
ES6中变量的结构赋值（数组赋值给数组）：var[a,b,c] = [0,1,2];  
ES6中新增了箭头函数：`=>`  
ES6中可以设置默认参数值，如`function foo(a = 5) {...}`  
ES6中不在像ES5一样使用原型链实现继承，而是引入Class这个概念。
- 

#### 说说你对闭包的理解  
- 闭包就是有权访问另一个函数作用域中的变量的函数
- 闭包的优点就是可以避免全局变量的污染
- 缺点是闭包会常驻内存，使用不当则会造成内存泄漏。

使用闭包实例
```
function createConparisonFunction(a) {
    var b;
    ...
    return function() {
        // 这里可以引用外部参数和变量如a和b
        // 同时外部函数不可以引用这里面的变量
    }
}
```
#### 说一下JS的数据类型？
ES5的基本数据类型：null、undefined、number、string、boolean。
ES5复杂数据类型：object。
ES6新增数据类型：symbol（独一无二）
#### 说一下JS事件流？
JS事件流图如下

![JS事件流](https://segmentfault.com/img/remote/1460000013591754)

JS事件流特点
> 1. 一个完整的JS事件流是从 window 开始，最后回到 window 的一个过程。
> 2. 事件流被分为三个阶段（1 ~ 5）捕获过程，（5 ~ 6）目标过程，（6 ~ 10）冒泡过程。

#### 如何阻止冒泡事件和默认事件？
冒泡事件：在一个对象上触发某类事件（比如单击onclick事件），如果此对象定义了此事件的处理程序，那么此事件就会调用这个处理程序，如果没有定义此事件处理程序或者事件返回true，那么这个事件会向这个对象的父级对象传播，从里到外，直至它被处理（父级对象所有同类事件都将被激活），或者它到达了对象层次的最顶层，即document对象（有些浏览器是window）。

默认事件：浏览器的一些默认的行为。例如：点击超链接跳转，点击右键会弹出菜单，滑动滚轮控制滚动条

```
// html
<div class="box1">
    <a href="http://www.baidu.com" target="_blank"></a>
</div>

// css 样式这里省略

// JS
/*第一种，阻止冒泡事件：在最里面一层添加 stopPropagation 方法*/
$(".box1 a").click(function(event){
    event.stopPropagation();//不会打印1，但是页面会跳转；		
    // IE兼容写法
    window.event.cancelBubble = true;
});
$(".box1").click(function(){
    console.log("1")				
});

/*第二种，阻止默认事件：使用 preventDefault 方法*/
$(".box1 a").click(function(event){           
    //阻止默认事件  
    event.preventDefault();//页面不会跳转，但是会打印出1，  
    // IE 兼容写法
    window.evetn.returnValue = true;
})；  
$(".box1").click(function(){  
    console.log("1")；                 
});  

/*第三种,阻止默认事件和冒泡事件*/
$(".box1").click(function(){  
                console.log("1")             
});                                   
$(".box1 a").click(function(event){  
    return false;  
    //页面不会跳转，也不会打印出1，等于同时调用了event.stopPropagation()和event.preventDefault()  
});  
```
#### 移动端的触摸事件
常见的触摸事件有
> 1. touchstart: 当手指触摸屏幕时候触发；
> 2. touchmove: 当手指在屏幕上滑动的时候连续触发；可以调用阻止默认事件preventDefault()阻止屏幕滚动；
> 3. touchend: 手指离开屏幕时触发；
> 4. touchcancel: 系统停止跟踪触摸时触发；

Touch 对象常见的属性
> 1. touches: 跟踪返回Touch对象的数组；
> 2. targetTouchs: 特定事件目标的Touch对象的数组；
> 3. changeTouchs: 上次触摸以来改变了的Touch对象的数组；
> 4. clientX,clientY：目标在浏览器中的位置；
> 5. pageX，pageY：目标在当前DOM中的位置；pageX = clientX + 滚动条移动距离；
> 6. screenX,screenY：目标在屏幕中的位置。

#### javascript 实现监听事件判断DOM是否加载完成
```
    //方法一：简单粗暴
    window.onload = function() {
        // my code
    }
    //方法二：添加监听事件
    function listen(callback) {
        if(window.addEventListener)
            window.addEventListner('load',     function(){
                callback();
            })
        else if(window.attachEvent) {
            windown.attachEvent('onreadystatechange', function(){
                callback();
            })
        }
    }
```

#### Ajax 实例
```
    // 创建一个XML请求
    var xmlhttp = new XMLHttpRequest();
    // 将请求发送到服务器，可以使用open()和send()方法
    xmlhttp.open("GET/POST", url, async); //url是文件在服务器中的位置，async：true（异步）或false（同步）
    
    //实例：通过XML HTTP加载XML文件
    function loadXMLDoc(url) {
        var xmlhttp = new XMLHttpRequest();
        if(xmlhttp != null) {
            xmlhttp.onreadystatechange = function() { // 没发送一次则做出一次响应
                if(xmlhttp.readyState == 4 && xmlhttp.status == 200) {
                    console.log(xmlhttp.status)
                }
            };
            // 发送到服务器
            xmlhttp.open("GET", url, true);
            xmlhttp.send(null);
        }
        
    }
```

#### 5种this绑定
1. 默认绑定：在非严格模式下this默认绑定到全局对象，二在严格模式下this绑定到undefined。
2. 隐式绑定：谁调用该对象就指向调用的对象
```js
    function foo() {
        console.log(this.a)
    }
    var obj = {
        a: 2,
        foo: foo
    }
    obj.foo(); // 2
```
3. 显示绑定：使用`call`和`apply`方法，则绑定到传入的第一个对象中，两者的区别时闯入的参数不一样；还可以使用`bind`函数，`bind`只有一个参数，且不会立刻执行。
```js
    function foo() {
        console.log(this.a);
    }
    var obj = {
        a: 2
    }
    foo.call(obj); // 2 调用foo时强制把this绑定到obj上面
```
4. new绑定：构造函数指向实列对
```
    function foo(a) {
        this.a = a;
    }
    
    var bar = new foo(2); // bar和foo(..)调用中的this进行绑定
    console.log( bar.a ); // 2
```
5. 箭头函数绑定：箭头函数绑定是根据作用域来决定this，且箭头函数的绑定无法被修改
```
    function foo() {
        // 返回一个箭头函数
        return(a) => { // this继承来自foo
            console.log(this.a)
        }
    }
    var obj1 = {
        a: 2
    };
    var obj2 = {
        a:3
    }
    var bar = foo.call(obj1); 
    foo.call(obj2); // 输出结果是2 而不是3
```
6. this绑定优先级
> new绑定 > 显示绑定 > 隐式绑定 > 默认绑定

#### call、apply以及bind的用法及区别
- call 和 apply 的共同点：它们的作用都是改变函数执行的上下文，将一个对象的方法交给另一个对象来执行，也就是改变函数体 this 的指向 ，且是立即执行。
- 区别：主要是它们传入的参数不同，call 的第一个数是对象，也就是需要绑定this 的对象，而后面可以接受任意个参数；而 apply 的第一个数和 call 相同，但只能接受两个参数，第二个参数必须是数组或类数组。
- bind方法的用途和上面两个类似，接受参数和 call 一样，只是bind 方法的返回值是函数，并且需要稍后调用，才会执行。

```
    function func(a, b, c) {
        ...
    }
    
    func.call(obj, 1, 2, 3) // func 实际接受的是1，2，3
    func.call(obj, [1,2,3]) // func 实际上接受的是[1,2,3],undefined,undefined
    
    func.apply(obj, [1,2,3]) //func 实际接受的是1，2，3
    func.apply(obj, { // 类数组
        0:1,
        1:2,
        2:3,
        length:3
    }) // func 实际接受的是1，2，3
```

#### setTimeout方法和setInterval的区别
- setTimout是隔多少时间之后触发，最少相隔时间是4ms；而setInterval 是每隔多少个时间就会触发一次，最少相隔时间是 10ms。
```
var timer = setTimeout(funciton() {
    console.log('hello!')
}, 1000);
clearTimeout(timer); // 清除计时器

var interval = setInterval(funciton() {
    console.log('hello!')
}, 1000);
clearInterval(interval);

```

#### 如何进行浅拷贝和深拷贝

#### 绑定事件的方法有哪些？
方法一：嵌入到DOM中，也就是直接绑定到对应的标签中
```
<input type="text" id="userName" name="userName" onblur="checkUsername()">
<script>
    // 验证用户名
    function checkUsername() {
        console.log("验证");
    }
</script>
```
方法二：获取元素，然后直接绑定事件
```
<input type="text" id="userName" name="userName">
<script>
document.getElementById('userName').onblur = function() {
    console.log("验证");
}
// 注意-->>错误用法
document.getElementById('userName').onblur(function() { 
    console.log("验证");
})
// 因为JS的事件里面并不支持插入参数，而且w3c文档里面支持的语法是：onblur="SomeJavaScriptCode"
</script>
```
方法三：使用事件监听
```
<input type="text" id="userName" name="userName">

<script>
/**
* 封装函数：添加事件监听
* 参数说明：type(添加事件的类型，如‘click’)；element(操作的元素)；handler(事件处理程序，即要执行的函数)
*/
function addEventHandler(type, handler, element) {
// 首先检测传入参数是否存在DOM2级方法
    if (element.addEventListener) {
        // 事件类型，需要执行的函数，是否捕捉(表示冒泡阶段被触发)
        element.addEventListener(type, handler, false);
    } else if (element.attachEvent) { // 检测是否存在IE级方法
        element.attachEvent('on' + type) // 在前面添加 'on'是为了在IE8 及更早版本中执行
    } else { // 检测是否存在DOM0 级方法
        element['on' + type] = null; // 在现在浏览器中应该不会执行到这一步，所以直接置空
    }
}
/* 验证用户信息函数 */
function judgeUserMsg() {
    console.log("验证");
}
// 调用函数监听事件
var userNameID = document.getElementById('userName');
addEventHandler('blur', judgeUserMsg, userNameID); // 注意，函数作为一个参数对象调用时不能带括号
</script>
```

##### 封装一个通用的事件侦听器函数
```
<script>
commonListener.Event = {
    // 页面加载完成后
    readyEvent : function(fn) {
        if (fn==null) {
            fn=document;
        }
        var oldonload = window.onload;
        if (typeof window.onload != 'function') {
            window.onload = fn;
        } else {
            window.onload = function() {
                oldonload();
                fn();
            };
        }
    },
    // 视能力分别使用dom0||dom2||IE方式 来绑定事件
    // 参数： 操作的元素,事件名称 ,事件处理程序(即需要调用的函数)
    addEvent : function(element, type, handler) {
        if (element.addEventListener) { // 判断是否存在 dom2级方法
            //事件类型、需要执行的函数、是否捕捉
            element.addEventListener(type, handler, false);
        } else if (element.attachEvent) { // 判断是否存在IE级处理方法
            element.attachEvent('on' + type, function() {
                handler.call(element);
            });
        } else { // 判断是存在dom0级方法，现在浏览器很少执行到这一步，所以可以直接置空
            element['on' + type] = handler;
            // 也可以写成下面
            // element['on' + type] = null;
        }
    },
    // 移除事件
    removeEvent : function(element, type, handler) {
        if (element.removeEnentListener) {
            element.removeEnentListener(type, handler, false);
        } else if (element.detachEvent) {
            element.detachEvent('on' + type, handler);
        } else {
            element['on' + type] = null;
        }
    }, 
    // 阻止事件 (主要是事件冒泡，因为IE不支持事件捕获)
    stopPropagation : function(ev) {
        if (ev.stopPropagation) {
            ev.stopPropagation();
        } else {
            ev.cancelBubble = true;
        }
    },
    // 取消事件的默认行为
    preventDefault : function(event) {
        if (event.preventDefault) {
            event.preventDefault();
        } else {
            event.returnValue = false;
        }
    },
    // 获取事件目标
    getTarget : function(event) {
        return event.target || event.srcElement;
    },
    // 获取event对象的引用，取到事件的所有信息，确保随时能使用event；
    getEvent : function(e) {
        var ev = e || window.event;
        if (!ev) {
            var c = this.getEvent.caller;
            while (c) {
                ev = c.arguments[0];
                if (ev && Event == ev.constructor) {
                    break;
                }
                c = c.caller;
            }
        }
        return ev;
    }
};
</script>
```

#### 创建对象的七种模式

##### 工厂模式
工厂模式特点：在函数内部先 `new` 一个对象出来，然后再在往这个对象里面添加属性和方法  

优缺点：工厂模式解决了创建多个类似对象的问题，但没有解决对象识别问题（即怎样知道一个对象的类型）
```
function createPerson(name, age, job) {
    
}
```
##### 构造函数模式
##### 原型模式
##### 混合构造函数和原型模式
##### 动态原型模式
##### 寄生构造函数模式
##### 稳妥构造函数模式

#### JavaScript继承的6种方法
1. 原型链继承
2. 借用构造函数继承
3. 组合继承(原型+借用构造)
4. 原型式继承
5. 寄生式继承
6. 寄生组合式继承

#### 浅拷贝和深拷贝
**学习资料：** [深拷贝的终极探索](https://juejin.im/post/5bc1ae9be51d450e8b140b0c)

**在谈论浅拷贝和深拷贝之前我们先谈论一下基本类型和引用类型**
>

- 浅拷贝：

#### Ajax的过程是怎样的？
1. 创建XMLHttpRequest对象,也就是创建一个异步调用对象
2. 创建一个新的HTTP请求,并指定该HTTP请求的方法、URL及验证信息
3. 设置响应HTTP请求状态变化的函数
4. 发送HTTP请求
5. 获取异步调用返回的数据
6. 使用JavaScript和DOM实现局部刷新

#### 线程与进程的区别？
1. 一个程序至少有一个进程，而进程至少包含一个线程。
2. 线程的划分尺度小于进程，使得多线程程序的并发性高。
3. 进程在执行过程中拥有独立的内存单元，而多个线程共享内存，从而极大地提高了程序的运行效率
4. 线程在执行过程中与进程还是有区别的。每个独立的线程有一个程序运行的入口、顺序执行序列和程序的出口。但是线程不能够独立执行，必须依存在应用程序中，由应用程序提供多个线程执行控制 
5. 从逻辑角度来看，多线程的意义在于一个应用程序中，有多个执行部分可以同时执行。但操作系统并没有将多个线程看做多个独立的应用，来实现进程的调度和管理以及资源分配。这就是进程和线程的重要区别。

#### 测试代码性能工具有哪些？
1. Profiler  
2. JSPerf（http://jsperf.com/nexttick-vs-setzerotimeout-vs-settimeout）  
3. Dromaeo  

#### JS延迟加载的几种方式？
[参考文献](https://blog.csdn.net/meijory/article/details/76389762)
1. defer和async
2. 动态创建DOM方式（创建script，插入到DOM中，加载完毕后callBack）
``` 
//这些代码应被放置在</body>标签前(接近HTML文件底部)
<script type="text/javascript">  
   function downloadJSAtOnload() {  
       varelement = document.createElement("script");  
       element.src = "defer.js";  
       document.body.appendChild(element);  
   }  
   if (window.addEventListener)  
      window.addEventListener("load",downloadJSAtOnload, false);  
   else if (window.attachEvent)  
      window.attachEvent("onload",downloadJSAtOnload);  
   else 
      window.onload =downloadJSAtOnload;  
</script> 
```
3. 按需异步载入js

#### js操作和设置cookie
由于js没有封装好像可以操作localStorage那样的方法，因此得自己写
```
// 创建cookie
function setCookie(name, value, expires, path, domain, secure) {
    var cookieText = encodeURIComponent(name) + '=' + encodeURIComponent(value);
    if (expires instanceof Date) {
        cookieText += '; expires=' + expires;
    }
    if (path) {
        cookieText += "; path=" + path     }
    if (domain) {
        cookieText += '; domain=' + domain;
    }
    if (secure) {
        cookieText += '; secure';
    }
    document.cookie = cookieText;
}
// 获取cookie
function getCookie(name) {
    var cookieName = encodeURIComponent(name) + '=';
    var cookieStart = document.cookie.indexOf(cookieName);
    var cookieValue = null;
    if (cookieStart > -1) {
        var cookieEnd = document.cookie.indexOf(';', cookieStart);
        if (cookieEnd == -1) {
            cookieEnd = document.cookie.length;
        }
        cookieValue = decodeURIComponent(document.cookie.substring(cookieStart + cookieName.length, cookieEnd));
    }
    return cookieValue;
}
// 删除cookie
function unsetCookie(name) {
    document.cookie = name + "= ; expires=" + new Date(0);
}
```


---
### 四、算法、数据结构问题
---
### 五、浏览器兼容性、缓存等问题
#### 一个页面从输入URL到页面加载显示完成，整个过程都发生了什么？
分为4个步骤
> 1. 当发送一个URL请求时，不管这个URL是Web页面的URL还是Web页面上每个资源的URL，浏览器都会开启一个线程来处理这个请求，同时在远程DNS服务器上启动一个DNS查询。这能使浏览器获得请求对应的IP地址。
> 2. 浏览器与远程Web服务器通过TCP三次握手协商来建立一个TCP/IP连接。该握手包括一个同步报文，一个同步-应答报文和一个应答报文，这三个报文在 浏览器和服务器之间传递。该握手首先由客户端尝试建立起通信，而后服务器应答并接受客户端的请求，最后由客户端发出该请求已经被接受的报文。
> 3. 一旦TCP/IP连接建立，浏览器会通过该连接向远程服务器发送HTTP的GET请求。远程服务器找到资源并使用HTTP响应返回该资源，值为200的HTTP响应状态表示一个正确的响应。
> 4. 此时，Web服务器提供资源服务，客户端开始下载资源。  
> 请求返回后，便进入了我们关注的前端模块
简单来说，浏览器会解析HTML生成DOM Tree，其次会根据CSS生成CSS Rule Tree，而javascript又可以根据DOM API操作DOM

#### 什么是跨域？如何解决跨域问题？
跨域，指的是浏览器不能执行其他网站的脚本。它是由浏览器的同源策略造成的，是浏览器施加的安全限制。

所谓同源是指，域名，协议，端口均相同，举个栗子：
```
http://www.123.com/index.html 调用 http://www.123.com/server.php （非跨域）

http://www.123.com/index.html 调用 http://www.456.com/server.php （主域名不同:123/456，跨域）

http://abc.123.com/index.html 调用 http://def.123.com/server.php （子域名不同:abc/def，跨域）

http://www.123.com:8080/index.html 调用 http://www.123.com:8081/server.php （端口不同:8080/8081，跨域）

http://www.123.com/index.html 调用 https://www.123.com/server.php （协议不同:http/https，跨域）

请注意：localhost和127.0.0.1虽然都指向本机，但也属于跨域。
```

解决跨域问题方法如下：
[参考文献](https://note.youdao.com/)
1. jsonp（jsonp 的原理是动态插入 script 标签）
```
function handleResponse(response){
    console.log('The responsed data is: '+response.data);
}
var script = document.createElement('script');
script.src = 'http://www.baidu.com/json/?callback=handleResponse';
document.body.insertBefore(script, document.body.firstChild);
```
2. document.domain + iframe
3. window.name、window.postMessage
4. 服务器上设置代理页面

#### 常见的网络协议？

#### http状态码有哪些？分别代表什么意思？
```
100 Continue  继续，一般在发送post请求时，已发送了http header之后服务端将返回此信息，表示确认，之后发送具体参数信息
200 OK   正常返回信息
201 Created  请求成功并且服务器创建了新的资源
202 Accepted  服务器已接受请求，但尚未处理
301 Moved Permanently  请求的网页已永久移动到新位置
302 Found  临时性重定向
303 See Other  临时性重定向，且总是使用 GET 请求新的 URI
304 Not Modified  自从上次请求后，请求的网页未修改过
400 Bad Request  服务器无法理解请求的格式，客户端不应当尝试再次使用相同的内容发起请求
401 Unauthorized  请求未授权
403 Forbidden  禁止访问
404 Not Found  找不到如何与 URI 相匹配的资源
500 Internal Server Error  最常见的服务器端错误
503 Service Unavailable 服务器端暂时无法处理请求（可能是过载或维护）
```

#### 说一下浏览器缓存有哪些？并说出他们的区别？
浏览器缓存主要有：cookies，sessionStorage 和 localStorage；  
sessionStorage 和 localStorage 是 HTML5 Web Storage API 提供的，可以方便的在 web 请求之间保存数据。有了本地数据，就可以避免数据在浏览器和服务器间不必要地来回传递。

sessionStorage、 localStorage 、 cookie 都是在浏览器端存储的数据，其中 sessionStorage 的概念很特别，引入了一个“浏览器窗口”的概念。 sessionStorage 是在同源的同窗口（或 tab ）中，始终存在的数据。也就是说只要这个浏览器窗口没有关闭，即使刷新页面或进入同源另一页面，数据仍然存在。关闭窗口后， sessionStorage 即被销毁。同时“独立”打开的不同窗口，即使是同一页面， sessionStorage 对象也是不同的

cookies会发送到服务器端。其余两个不会。

Microsoft 指出 Internet Explorer 8 增加 cookie 限制为每个域名 50 个，但 IE7 似乎也允许每个域名 50 个 cookie 。 Firefox 每个域名 cookie 限制为 50 个。 Opera 每个域名 cookie 限制为 30 个。 Firefox 和 Safari 允许 cookie 多达 4097 个字节，包括名（ name ）、值（ value ）和等号。 Opera 许 cookie 多达 4096 个字节，包括：名（ name ）、值（ value ）和等号。 Internet Explorer 允许 cookie 多达 4095 个字节，包括：名（ name ）、值（ value ）和等号。

区别：

- Cookie

+ 每个域名存储量比较小（各浏览器不同，大致 4K ）

+ 所有域名的存储量有限制（各浏览器不同，大致 4K ）

+ 有个数限制（各浏览器不同）

+ 会随请求发送到服务器

- LocalStorage

+ 永久存储

+ 单个域名存储量比较大（推荐 5MB ，各浏览器不同）

+ 总体数量无限制

- SessionStorage

+ 只在 Session 内有效

+ 存储量更大（推荐没有限制，但是实际上各浏览器也不同）

#### 常见的浏览器内核有哪些？
- Trident内核： IE,MaxThon,TT,The World,360, 搜狗浏览器等。 [ 又称 MSHTML]
- Gecko内核： Netscape6 及以上版本， FF,MozillaSuite/SeaMonkey 等
- Presto内核： Opera7 及以上。       [Opera 内核原为： Presto ，现为： Blink;]
- Webkit内核： Safari,Chrome 等。    [ Chrome 的： Blink （ WebKit 的分支） ]

#### 如何实现浏览器多个标签页之间的通信?
使用webSocket(浏览器缓存)、 SharedWorker ；  
也可以调用localstorage、 cookies 等本地存储方式；  
localstorage另一个浏览上下文里被添加、修改或删除时，它都会触发一个事件，
我们通过监听事件，控制它的值来进行页面信息通信；  
注意quirks： Safari 在无痕模式下设置 localstorge 值时会抛出 QuotaExceededError 的异常；

#### 常见浏览器兼容性问题与解决方案？
1. 浏览器兼容问题一：不同浏览器的标签默认的外补丁和内补丁不同   
问题症状：随便写几个标签，不加样式控制的情况下，各自的margin 和padding差异较大。  
碰到频率:100%   
解决方案：重置CSS样式，具体方法有下面几种      
a、最简单的办法：（不推荐使用）*{margin: 0;padding: 0;}。  
b、使用CSSReset可以将所有浏览器默认样式设置成一样。  
c、normalize：也许有些cssreset过于简单粗暴，有点伤及无辜，normalize是另一个选择。bootstrap已经引用该css来重置浏览器默认样式，比普通的cssreset要精细一些，保留浏览器有用的默认样式，支持包括手机浏览器在内的超多浏览器，同时对HTML5元素、排版、列表、嵌入的内容、表单和表格都进行了一般化。  
备注：这个是最常见的也是最易解决的一个浏览器兼容性问题，几乎所有的CSS文件开头都会用通配符*来设置各个标签的内外补丁是0。

2. 浏览器兼容问题二：块属性标签float后，又有横行的margin情况下，在IE6显示margin比设置的大  
问题症状:常见症状是IE6中后面的一块被顶到下一行  
碰到频率：90%（稍微复杂点的页面都会碰到，float布局最常见的浏览器兼容问题）  
解决方案：在float的标签样式控制中加入 display:inline;将其转化为行内属性
备注：我们最常用的就是div+CSS布局了，而div就是一个典型的块属性标签，横向布局的时候我们通常都是用div    float实现的，横向的间距设置如果用margin实现，这就是一个必然会碰到的兼容性问题。

3. 浏览器兼容问题三：设置较小高度标签（一般小于10px），在IE6，IE7，遨游中高度超出自己设置高度   
问题症状：IE6、7和遨游里这个标签的高度不受控制，超出自己设置的高度  
碰到频率：60%  
解决方案：给超出高度的标签设置overflow:hidden;或者设置行高line-height 小于你设置的高度。  
备注：这种情况一般出现在我们设置小圆角背景的标签里。出现这个问题的原因是IE8之前的浏览器都会给标签一个最小默认的行高的高度。即使你的标签是空的，这个标签的高度还是会达到默认的行高。

4. 浏览器兼容问题四：行内属性标签，设置display:block后采用float布局，又有横行的margin的情况，IE6间距bug   
问题症状：IE6里的间距比超过设置的间距  
碰到几率：20%  
解决方案 ： 在display:block;后面加入display:inline;display:table;  
备注：行内属性标签，为了设置宽高，我们需要设置display:block;(除了input标签比较特殊)。在用float布局并有横向的margin后，在IE6下，他就具有了块属性float后的横向margin的bug。不过因为它本身就是行内属性标签，所以我们再加上display:inline的话，它的高宽就不可设了。这时候我们还需要在display:inline后面加入display:talbe。

5. 浏览器兼容问题五：图片默认有间距   
问题症状：几个img标签放在一起的时候，有些浏览器会有默认的间距，加了问题一中提到的通配符也不起作用。  
碰到几率：20%  
解决方案：使用float属性为img布局  
备注 ： 因为img标签是行内属性标签，所以只要不超出容器宽度，img标签都会排在一行里，但是部分浏览器的img标签之间会有个间距。去掉这个间距使用float是正道。（我的一个学生使用负margin，虽然能解决，但负margin本身就是容易引起浏览器兼容问题的用法，所以我禁止他们使用）

6. 浏览器兼容问题六：标签最低高度设置min-height不兼容   
问题症状：因为min-height本身就是一个不兼容的CSS属性，所以设置min-height时不能很好的被各个浏览器兼容  
碰到几率：5%  
解决方案：如果我们要设置一个标签的最小高度200px，需要进行的设置为：{min-height:200px; height:auto !important; height:200px; overflow:visible;}
备注：在B/S系统前端开时，有很多情况下我们又这种需求。当内容小于一个值（如300px）时。容器的高度为300px；当内容高度大于这个值时，容器高度被撑高，而不是出现滚动条。这时候我们就会面临这个兼容性问题。

7. 浏览器兼容问题七：透明度的兼容CSS设置   
一般在ie中用的是filter:alpha(opacity=0);这个属性来设置div或者是块级元素的透明度，而在firefox中，一般就是直接使用opacity:0,对于兼容的，一般的做法就是在书写css样式的将2个都写上就行，就能实现兼容

#### 网页性能优化的方法有哪些？
[参考文献：雅虎十四天优化原则](https://blog.csdn.net/u010648555/article/details/50721751)
（1）、减少http请求次数：CSS Sprites,   JS、CSS源码压缩、图片大小控制合适；网页Gzip，CDN托管，data缓存 ，图片服务器。  
（2）、前端模板 JS+数据，减少由于HTML标签导致的带宽浪费，前端用变量保存AJAX请求结果，每次操作本地变量，不用请求，减少请求次数    
（3）、用innerHTML代替DOM操作，减少DOM操作次数，优化javascript性能。  
（4）、当需要设置的样式很多时设置className而不是直接操作style。  
（5）、少用全局变量、缓存DOM节点查找的结果。减少IO读取操作。  
（6）、避免使用CSS Expression（css表达式)又称Dynamic properties(动态属性)。  
（7）、图片预加载，将样式表放在顶部，将脚本放在底部 加上时间戳。

#### cookie、sessionStorage与localStorage的区别
- 数据生命周期不同：cookie一般是默认关闭浏览器即失效；sessionStorage 是页面会话期间可用；而local一般会长久存在，除非数据被清除。
- 存放数据大小不同：cookie一般很小，4K左右；而sessionStorage 和 localStorage 存储量都比较大。
- 易用性不同：cookie 需要自己封装setCookie和getCookie，而两外两个有原生的接口。
- 与服务器通信不同：cookie每次都会携带在HTTP头部发送到服务器，而另外两个则不会

---
### 六、Node.js问题
---
### 七、网络安全
#### 常见的网络攻击有哪些
1. XSS指cross-site-scripting, 跨站脚本攻击，指通过存在web安全漏洞的web网站注册的用户的浏览器内运行非法的html标签或者js而进行的攻击。用户通过在自己的浏览器上运行这些脚本就会被攻击。 
2. SQL注入，指的是针对web应用使用的数据库，通过运行非法的SQL而产生的攻击。 
3. OS命令注入攻击，指的是通过web应用，执行非法的操作系统命令达到非法攻击的目的。 
4. HTTP首部注入攻击，指攻击者通过在相应首部字段内插入换行，然后添加任意响应首部过主体的攻击。 邮件首部注入攻击，指攻击者通过向邮件首部to或subject内任意添加非法内容引起的攻击。 
5. 会话劫持，指攻击者通过某种手段拿到了用户的会话id，并非法使用此会话id伪装成用户达到攻击的目的。 
6. 还有DoS DDoS，一种让运行中的服务成停止状态的攻击。 
7. CSRF，跨站点请求伪造攻击，指的是攻击者通过设置好的陷阱，强制对已完成认证的用户进行非预期的个人信息或设定信息等某些状态更新，属于被动攻击。

#### xss 和 csrf 分别是什么漏洞？如何防范？
- XSS：跨站脚本攻击（Cross-Site Scripting），XSS是将恶意代码插入到html页面中，如输入表单等，当用户提交的时候，插入的html代码会被执行，这就是xss攻击。
- CSRF：跨站伪造请求（Cross-site Request forgery），是一种劫持受信任用户向服务器发送非预期请求的攻击方式。
- 两者的区别：XSS是发生在客户端，而CSRF是发生服务端。

**防范XSS和CSRF**  
防御XSS攻击可以通过以下两方面操作：   
1. 对用户表单输入的数据进行过滤，对javascript代码进行转义，然后再存入数据库； 
2. 在信息的展示页面，也要进行转义，防止javascript在页面上执行。  

CSRF攻击的防御可以通过以下两方面操作： 
1. 所有需要用户登录之后才能执行的操作属于重要操作，这些操作传递参数应该使用post方式，更加安全； 
2. 为防止跨站请求伪造，我们在某次请求的时候都要带上一个csrf_token参数，用于标识请求来源是否合法，csrf_token参数由系统生成，存储在SESSION中。
--------------------- 
作者：koastal 
来源：CSDN 
原文：https://blog.csdn.net/koastal/article/details/52905358 
版权声明：本文为博主原创文章，转载请附上博文链接！

#### 重定向状态码有哪些？适用那些场景？
1. 301
- 定义：永久移动。请求的资源已被永久移动到新URL，浏览器会自动定向到新的URL。
- 适用场景：一般是资源位置永久更改，如想更换域名或服务器等。
2. 302
- 定义：临时移动。与301类似，但资源只是临时被移动，客户端应继续使用原有的URL。
- 适用场景：一般是普通的重定向需求：临时跳转  
> 如访问某网页的时候未登录前先使用302重定向到登录页面，登陆成功之后再跳转到原来请求的页面。  
还有就是如用手机访问PC端的页面，302重定向到了移动端的页面等。  
像微博之类的使用短域名，用户浏览后需要重定向到真实的地址之类，如我访问一个微博的秒拍视频链接然后重定向到了实际的视频地址。

3. 303
- 定义：查看其它地址。301类似。使用GET和POST方法请求查看
- 适用场景：很少使用
4. 307
- 定义：临时重定向。与302类似。使用GET请求重定向
- 适用场景：很少用，与302类似，只不过是针对POST方法的请求不允许更改方法

---
### Vue基础

