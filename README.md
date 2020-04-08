# 前端开发工程师面试题——HTML部分
　1、Doctype作用? 严格模式与混杂模式如何区分？它们有何意义?


　　（1）、 声明位于文档中的最前面，处于 标签之前。告知浏览器的解析器，用什么文档类型 规范来解析这个文档。 


　　（2）、严格模式的排版和 JS 运作模式是  以该浏览器支持的最高标准运行。


　　（3）、在混杂模式中，页面以宽松的向后兼容的方式显示。模拟老式浏览器的行为以防止站点无法工作。


　　（4）、DOCTYPE不存在或格式不正确会导致文档以混杂模式呈现。


　　2、行内元素有哪些？块级元素有哪些？ 


　　（1）CSS规范规定，每个元素都有display属性，确定该元素的类型，每个元素都有默认的display值，  比如div默认display属性值为“block”，成为“块级”元素；  span默认display属性值为“inline”，是“行内”元素。  


　　（2）行内元素有：a b span img input select strong（强调的语气）  块级元素有：div ul ol li dl dt dd h1 h2 h3 h4…p  

　　3、link 和@import 的区别是？


　　（1）link属于XHTML标签，而@import是CSS提供的;


　　（2）页面被加载的时，link会同时被加载，而@import引用的CSS会等到页面被加载完再加载;


　　（3）import只在IE5以上才能识别，而link是XHTML标签，无兼容问题;


　　（4）link方式的样式的权重 高于@import的权重. 


　　4、浏览器的内核分别是什么?




　　IE浏览器的内核Trident、Mozilla的Gecko、Chrome的Blink（WebKit的分支）、Opera内核原为Presto，现为Blink；




　　5、HTML5有哪些新特性？如何处理HTML5新标签的浏览器兼容问题？如何区分 HTML 和 HTML5？




　　HTML5 现在已经不是 SGML 的子集，主要是关于图像，位置，存储，多任务等功能的增加。
　
　　绘画 canvas    用于媒介回放的 video 和 audio 元素   本地离线存储 localStorage 长期存储数据，浏览器关闭后数据不丢失；  sessionStorage 的数据在浏览器关闭后自动删除  语意化更好的内容元素，比如 article、footer、header、nav、section   表单控件，calendar、date、time、email、url、search    新的技术webworker, websockt, Geolocation



　　6、对语义化如何理解？


　　用正确的标签做正确的事情！


　　HTML语义化就是让页面的内容结构化，便于对浏览器、搜索引擎解析；在没有样式CCS情况下也以一种文档格式显示，并且是容易阅读的。搜索引擎的爬虫依赖于标记来确定上下文和各个关键字的权重，利于 SEO。使阅读源代码的人对网站更容易将网站分块，便于阅读维护理解。


　　7、HTML5的离线储存有几种方式？


　　localStorage长期存储数据，浏览器关闭后数据不丢失；sessionStorage  数据在浏览器关闭后自动删除。



　　8、iframe有那些缺点？


　　iframe会阻塞主页面的Onload事件；


　　iframe和主页面共享连接池，而浏览器对相同域的连接有限制，所以会影响页面的并行加载。使用iframe之前需要考虑这两个缺点。如果需要使用iframe，最好是通过javascript动态给iframe添加src属性值，这样可以可以绕开以上两个问题。


　　9、请描述一下 cookies，sessionStorage 和 localStorage 的区别？


cookie在浏览器和服务器间来回传递。 sessionStorage和localStorage不会sessionStorage和localStorage的存储空间更大；sessionStorage和localStorage有更多丰富易用的接口；sessionStorage和localStorage各自独立的存储空间；




最新前端开发工程师面试题——CSS部分
1、CSS 选择符有哪些？哪些属性可以继承？优先级算法如何计算？ CSS3新增伪类有那些？


　　1.id选择器（ # myid）    　　　　2.类选择器（.myclassname）    


　　3.标签选择器（div, h1, p）  　 　4.相邻选择器（h1 + p）    


　　5.子选择器（ul < li）    　　　  　6.后代选择器（li a）    


　　7.通配符选择器（ * ）    　　　　8.属性选择器（a[rel = "external"]）    


　　9.伪类选择器（a: hover, li: nth - child）


　　可继承的样式： font-size font-family color, UL LI DL DD DT;


　　不可继承的样式：border padding margin width height ;


　　优先级就近原则，同权重情况下样式定义最近者为准;


　　载入样式以最后载入的定位为准;


　　优先级为:
　　!important >  id > class > tag     important 比 内联优先级高



　　2、CSS3新增伪类举例：
　　p:first-of-type 选择属于其父元素的首个元素的每个元素。


　　p:last-of-type  选择属于其父元素的最后元素的每个元素。
　　p:only-of-type  选择属于其父元素唯一的元素的每个元素。
　　p:only-child    选择属于其父元素的唯一子元素的每个元素。
　　p:nth-child(2)  选择属于其父元素的第二个子元素的每个元素。
　　:enabled  :disabled 控制表单控件的禁用态。
　　:checked单选框或复选框被选中。


　　3、如何居中div？如何居中一个浮动元素？


　　给div设置一个宽度，然后添加margin:0 auto属性

　　div{    width:200px;    margin:0 auto; }  



　　居中一个浮动元素


　　确定容器的宽高 宽500 高 300 的层  设置层的外边距 .div {   Width:500px ; height:300px;//高度可以不设  Margin: -150px 0 0 -250px;  position:relative;相对定位  background-color:pink;//方便看效果  left:50%;  top:50%;} 


　　列出display的值，说明他们的作用。position的值， relative和absolute定位原点是？


　　1.block 象块类型元素一样显示。  none 缺省值。象行内元素类型一样显示。  inline-block 象行内元素一样显示，但其内容象块类型元素一样显示。  list-item 象块类型元素一样显示，并添加样式列表标记。  


　　2. absolute　生成绝对定位的元素，相对于 static 定位以外的第一个父元素进行定位。


　　fixed （老IE不支持）        生成绝对定位的元素，相对于浏览器窗口进行定位。   


　　relative 　生成相对定位的元素，相对于其正常位置进行定位。   


　　static  默认值。没有定位，元素出现在正常的流中  *（忽略 top, bottom, left, right z-index 声明）。


　　inherit 规定从父元素继承 position 属性的值。
4、为什么要初始化CSS样式？

　　因为浏览器的兼容问题，不同浏览器对有些标签的默认值是不同的，如果没对CSS初始化往往会出现浏览器之间的页面显示差异。当然，初始化样式会对SEO有一定的影响，但鱼和熊掌不可兼得，但力求影响最小的情况下初始化。最简单的初始化方法就是： * {padding: 0; margin: 0;} （不建议）淘宝的样式初始化： body, h1, h2, h3, h4, h5, h6, hr, p, blockquote, dl, dt, dd, ul, ol, li, pre, form, fieldset, legend, button, input, textarea, th, td { margin:0; padding:0; }body, button, input, select, textarea { font:12px/1.5tahoma, arial, /5b8b/4f53; }h1, h2, h3, h4, h5, h6{ font-size:100%; }address, cite, dfn, em, var { font-style:normal; }code, kbd, pre, samp { font-family:couriernew, courier, monospace; }small{ font-size:12px; }ul, ol { list-style:none; }a { text-decoration:none; }a:hover { text-decoration:underline; }sup { vertical-align:text-top; }sub{ vertical-align:text-bottom; }legend { color:#000; }fieldset, img { border:0; }button, input, select, textarea { font-size:100%; }table { border-collapse:collapse; border-spacing:0; } 


　　5、absolute的containing block计算方式跟正常流有什么不同？


　　6、position跟display、margin collapse、overflow、float这些特性相互叠加后会怎么样？


　　7、对BFC规范的理解？


　　（W3C CSS 2.1 规范中的一个概念,它决定了元素如何对其内容进行定位,以及与其他元素的关 系和相互作用。）


　　8、css定义的权重



　　以下是权重的规则：标签的权重为1，class的权重为10，id的权重为100，以下例子是演示各种定义的权重值：/*权重为1*/div{}/*权重为10*/.class1{}/*权重为100*/#id1{}/*权重为100+1=101*/#id1 div{}/*权重为10+1=11*/.class1 div{}/*权重为10+10+1=21*/.class1 .class2 div{} 如果权重相同，则最后定义的样式会起作用，但是应该避免这种情况出现


　　9、解释下浮动和它的工作原理？清除浮动的技巧


　　10、用过媒体查询，针对移动端的布局吗？


　　11、使用 CSS 预处理器吗？喜欢那个？


　　12、CSS3有哪些新特性？


　　CSS3实现圆角（border-radius:8px），阴影（box-shadow:10px），  对文字加特效（text-shadow、），线性渐变（gradient），旋转（transform）  transform:rotate(9deg) scale(0.85,0.90) translate(0px,-30px) skew(-9deg,0deg);//旋转,缩放,定位,倾斜  增加了更多的CSS选择器  多背景 rgba 


　　13、经常遇到的CSS的兼容性有哪些？原因，解决方法是什么？

　　14、介绍一下CSS的盒子模型？


　　（1）有两种， IE 盒子模型、标准 W3C 盒子模型；IE的content部分包含了 border 和 pading;


　　（2）盒模型： 内容(content)、填充(padding)、边界(margin)、 边框(border).

1.对WEB标准以及W3C的理解与认识？


　　标签闭合、标签小写、不乱嵌套、提高搜索机器人搜索几率、使用外链css和js脚本、结构行为表现的分离、文件下载与页面速度更快、内容能被更多的用户所访问、内容能被更广泛的设备所访问、更少的代码和组件，容易维护、改版方便，不需要变动页面内容、提供打印版本而不需要复制内容、提高网站易用性;


　　2.XHTML和HTML有什么区别？


　　HTML是一种基本的WEB网页设计语言，XHTML是一个基于XML的置标语言
　　最主要的不同：
　　XHTML 元素必须被正确地嵌套。
　　XHTML 元素必须被关闭。
　　标签名必须用小写字母。
　　XHTML 文档必须拥有根元素。

　　3.Doctype? 严格模式与混杂模式-如何触发这两种模式，区分它们有何意义?
　　用于声明文档使用那种规范(HTML/XHTML)一般为 严格 过度 基于框架的html文档

　　加入XMl声明可触发，解析方式更改为IE5.5 拥有IE5.5的bug


　　4.行内元素有哪些?块级元素有哪些?CSS的盒模型?


　　块级元素：div p h1 h2 h3 h4 form ul
　　行内元素: a b br i span input select

　　Css盒模型:内容，border ,margin，padding


　　5.CSS引入的方式有哪些? link和@import的区别是?


　　内联 内嵌 外链 导入
　　区别 ：同时加载
　　前者无兼容性，后者CSS2.1以下浏览器不支持

　　Link 支持使用javascript改变样式，后者不可


　　6.CSS选择符有哪些?哪些属性可以继承?优先级算法如何计算?内联和important哪个优先级高?


　　标签选择符 类选择符 id选择符
　　继承不如指定 Id>class>标签选择

　　后者优先级高


　　7.前端页面有哪三层构成，分别是什么?作用是什么?


　　结构层 HTML 表示层 CSS 行为层 js


　　8.CSS的基本语句构成是?


　　选择器{属性1:值1;属性2:值2;……}


　　9.你做的页面在哪些流览器测试过?这些浏览器的内核分别是什么?


　　Ie(Ie内核) 火狐(Gecko) 谷歌(webkit) opear(Presto)


　　10.写出几种IE6 BUG的解决方法


　　1.双边距BUG float引起的 使用display
　　2.3像素问题 使用float引起的 使用dislpay:inline -3px
　　3.超链接hover 点击后失效 使用正确的书写顺序 link visited hover active
　　4.Ie z-index问题 给父级添加position:relative
　　5.Png 透明 使用js代码 改
　　6.Min-height 最小高度 !Important 解决’
　　7.select 在ie6下遮盖 使用iframe嵌套
　　8.为什么没有办法定义1px左右的宽度容器(IE6默认的行高造成的，使用over:hidden,zoom:0.08 line-height:1px)

　　9.ie 6 不支持!important


　　11.img标签上title与alt属性的区别是什么?


　　Alt 当图片不显示是 用文字代表。

　　Title 为该属性提供信息


　　12.描述css reset的作用和用途。


　　Reset重置浏览器的css默认属性 浏览器的品种不同，样式不同，然后重置，让他们统一


　　13.解释css sprites，如何使用。


　　Css 精灵 把一堆小的图片整合到一张大的图片上，减轻服务器对图片的请求数量


　　14.浏览器标准模式和怪异模式之间的区别是什么?


　　盒子模型 渲染模式的不同

　　使用 window.top.document.compatMode 可显示为什么模式


　　15.你如何对网站的文件和资源进行优化?期待的解决方案包括：


　　文件合并
　　文件最小化/文件压缩
　　使用CDN托管

　　缓存的使用


　　16.什么是语义化的HTML?


　　直观的认识标签 对于搜索引擎的抓取有好处


　　17.清除浮动的几种方式，各自的优缺点


　　1.使用空标签清除浮动 clear:both(理论上能清楚任何标签，增加无意义的标签)
　　2.使用overflow:auto(空标签元素清除浮动而不得不增加无意代码的弊端,,使用zoom:1用于兼容IE)

　　3.是用afert伪元素清除浮动(用于非IE浏览器)


　　18.css hack
　　
　　_marging \\IE 6
　　+margin \\IE 7
　　Marging:0 auto \9 所有Ie

　　Margin \0 \\IE 8


　　Javascript部分

　　1.javascript的typeof返回哪些数据类型

　　Object number function boolean underfind


　　2.例举3种强制类型转换和2种隐式类型转换?

　　强制（parseInt,parseFloat,number）

　　隐式（== – ===）


　　3.split() join() 的区别

　　前者是切割成数组的形式，后者是将数组转换成字符串


　　4.数组方法pop() push() unshift() shift()

　　Push()尾部添加 pop()尾部删除

　　Unshift()头部添加 shift()头部删除


　　5.事件绑定和普通事件有什么区别


　　6.IE和DOM事件流的区别

　　1.执行顺序不一样、

　　2.参数不一样

　　3.事件加不加on

　　4.this指向问题


　　7.IE和标准下有哪些兼容性的写法

　　Var ev = ev || window.event


　　document.documentElement.clientWidth || document.body.clientWidth


　　Var target = ev.srcElement||ev.target


　　8.ajax请求的时候get 和post方式的区别


　　一个在url后面 一个放在虚拟载体里面


　　有大小限制


　　安全问题


　　应用不同 一个是论坛等只需要请求的，一个是类似修改密码的


　　9.call和apply的区别


　　Object.call(this,obj1,obj2,obj3)


　　Object.apply(this,arguments)


　　10.ajax请求时，如何解释json数据


　　使用eval parse 鉴于安全性考虑 使用parse更靠谱


　　11.b继承a的方法


　　12.JavaScript this指针、闭包、作用域


　　13.事件委托是什么


　　让利用事件冒泡的原理，让自己的所触发的事件，让他的父元素代替执行！


　　14.闭包是什么，有什么特性，对页面有什么影响


　　闭包就是能够读取其他函数内部变量的函数。



　　15.如何阻止事件冒泡和默认事件


　　canceBubble return false


　　16.添加 删除 替换 插入到某个接点的方法


　　obj.appendChidl()


　　obj.innersetBefore


　　obj.replaceChild


　　obj.removeChild



　　17.解释jsonp的原理，以及为什么不是真正的ajax


　　动态创建script标签，回调函数


　　Ajax是页面无刷新请求数据操作


　　18.javascript的本地对象，内置对象和宿主对象


　　本地对象为array obj regexp等可以new实例化


　　内置对象为gload Math 等不可以实例化的


　　宿主为浏览器自带的document,window 等


　　19.document load 和document ready的区别


　　Document.onload 是在结构和样式加载完才执行js


　　Document.ready原生种没有这个方法，jquery中有 $().ready(function)


　　20.”==”和“===”的不同


　　前者会自动转换类型


　　后者不会


　　21.javascript的同源策略


　　一段脚本只能读取来自于同一来源的窗口和文档的属性，这里的同一来源指的是主机名、协议和端口号的组合


　　22.编写一个数组去重的方法


　　function oSort(arr)
　　{
　　var result ={};
　　var newArr=[];
　　for(var i=0;i<arr.length;i++)
　　{
　　if(!result[arr])
　　{
　　newArr.push(arr)
　　result[arr]=1
　　}
　　}
　　return newArr
　　}
</arr.length;i++)
1.自我评价一下HTML/CSS/JS的掌握情况


　　2.简述HTML经常使用的标签和作用。


　　Div/a/p/span/li/ul/ol/table/tr/td


　　3.你认为最常遇到的兼容Bug有哪些?有哪些问题是你认为解决起来最麻烦的?

　　IE6 PNG


　　IE6 Fixed

　　4.块级元素和行内元素都有哪些? 行内元素有哪些特点?


　　5.介绍所知道的CSS hack技巧(如：_， *， +， \9， !important 之类)


　　6.CSS定位方式有哪些?position属性的值有哪些?他们之间的区别是什么?


　　在CSS中关于定位的内容是：position:relative | absolute | static | fixed


　　•    static 没有特别的设定，遵循基本的定位规定，不能通过z-index进行层次分级。


　　•    relative 不脱离文档流，参考自身静态位置通过 top,bottom,left,right 定位，并且可以通过z-index进行层次分级。


　　•    absolute 脱离文档流，通过 top,bottom,left,right 定位。选53D6其最近的父级定位元素，当父级 position 为 static 时，absolute元素将以body坐标原点进行定位，可以通过z-index进行层次分级。


　　•    fixed 固定定位，这里他所固定的对像是可视窗口而并非是body或是父级元素。可通过z-index进行层次分级。


　　7.函数的几种定义方法？


　　function a(){},


　　var a = function(){}


　　8.对象的定义方法？


　　a = new Object(), a = {}


　　9.类的定义方法（prototype）（继承）


　　Var a = function(){}


　　a.prototype = {}


　　new a();


　　10.this 关键字的指向


　　obj.foo() == obj        //方法调用模式,this指向obj


　　foo() == window;         //函数调用模式,this指向window


　　new obj.foo() == obj    //构造器调用模式, this指向新建立对象


　　foo.call(obj) == obj;//APPLY调用模式,this指向obj


　　11.什么是闭包，及其作用是什么？


　　12.事件绑定的几种方法，事件冒泡？


　　13.Ajax/json/json0070？


　　14.异步ajax的优缺点都有什么？


　　优点：


　　•    相对于同步ajax：不会造成UI卡死，用户体验好。


　　•    相对于刷新页面，省流量


　　缺点：


　　•    后退按钮无效；


　　•    多个请求同时触发时，由于回调时间不确定，会造成混乱，避免这种混乱需要复杂的判断机制。


　　•    搜索引擎不友好


　　•    数据安全


　　15.常用JS框架都有什么？是否使用过jQuery，以及jQuery的优点是什么？


　　16.JS用了多久，介绍一下自己做过的JS项目？


　　17.开发调试工具和方法都有什么（编辑器、浏览器）


　　18.类、函数、对象（代码表达）


　　19.闭包（setTimeout）（产生两个首尾相连的计时器）（使用for循环产生10个计时器）||


　　20.Jquery Mobile 相关


　　21.HTML5/CSS3的掌握情况


　　22.是否听说过和理解webapp？


　　23.个人擅长的语言，优缺点都是什么？


　　24.介绍一下曾经参与过的项目经验，合作开发、独立开发


　　25.编程的重要知识？


　　26.开发过程中遇到困难，如何解决？


　　27.有没有个人/开源项目



　　28.前端开发（HTML/CSS/）

最新前端开发工程师面试题——JavaScript部分
　　1、eval是做什么的？
　　它的功能是把对应的字符串解析成JS代码并运行；应该避免使用eval，不安全，非常耗性能（2次，一次解析成js语句，一次执行）。
　　2、Node.js的适用场景？
　　高并发、聊天、实时消息推送
　　3、介绍js的基本数据类型。
　　number,string,boolean,object,undefined
　　4、Javascript如何实现继承？
　　通过原型和构造器


　5、如何创建一个对象? （画出此对象的内存图）


　　function Person(name, age) {    this.name = name;    this.age = age;    this.sing = function() { alert(this.name) }   } 
　
　6、谈谈This对象的理解。

　　this是js的一个关键字，随着函数使用场合不同，this的值会发生变化。但是有一个总原则，那就是this指的是调用函数的那个对象。this一般情况下：是全局对象Global。 作为方法调用，那么this就是指这个对象 


　7、事件是什么？IE与火狐的事件机制有什么区别？ 如何阻止冒泡？
　　（1） 我们在网页中的某个操作（有的操作对应多个事件）。例如：当我们点击一个按钮就会产生一个事件。是可以被 JavaScript 侦测到的行为。   
　　（2） 事件处理机制：IE是事件冒泡、火狐是 事件捕获； 
　　（3） ev.stopPropagation();


　8、什么是闭包（closure），为什么要用它？
　　执行say667()后,say667()闭包内部变量会存在,而闭包内部函数的内部变量不会存在.使得Javascript的垃圾回收机制GC不会收回say667()所占用的资源，因为say667()的内部函数的执行需要依赖say667()中的变量。这是对闭包作用的非常直白的描述.  function say667() {    // Local variable that ends up within closure    var num = 666;    var sayAlert = function() { alert(num); }    num++;    return sayAlert;} var sayAlert = say667(); sayAlert()//执行结果应该弹出的667  

　　9、如何判断一个对象是否属于某个类？
　　使用instanceof （待完善）   if(a instanceof Person){       alert('yes');   }


　　10、Javascript中，有一个函数，执行时对象查找时，永远不会去查找原型，这个函数是？
　　hasOwnProperty


　　11、对JSON 的了解？
　　JSON(JavaScript Object Notation) 是一种轻量级的数据交换格式。它是基于JavaScript的一个子集。数据格式简单, 易于读写, 占用带宽小{'age':'12', 'name':'back'}



		2016年Web前端面试题目汇总
以下是收集一些面试中经常会遇到的经典面试题以及自己面试过程中无法解决的问题，通过对知识的整理以及经验的总结，重新巩固自身的前端基础知识，如有错误或更好的答案，欢迎指正。:）

HTML/CSS部分

1、什么是盒子模型？

在网页中，一个元素占有空间的大小由几个部分构成，其中包括元素的内容（content），元素的内边距（padding），元素的边框（border），元素的外边距（margin）四个部分。这四个部分占有的空间中，有的部分可以显示相应的内容，而有的部分只用来分隔相邻的区域或区域。4个部分一起构成了css中元素的盒模型。

2、行内元素有哪些？块级元素有哪些？ 空(void)元素有那些？

行内元素：a、b、span、img、input、strong、select、label、em、button、textarea
块级元素：div、ul、li、dl、dt、dd、p、h1-h6、blockquote
空元素：即系没有内容的HTML元素，例如：br、meta、hr、link、input、img

3、CSS实现垂直水平居中

一道经典的问题，实现方法有很多种，以下是其中一种实现：
HTML结构：

 <div class="wrapper">
    <div class="content"></div>
 </div>

CSS：

.wrapper{position:relative;}
    .content{
        background-color:#6699FF;
        width:200px;
        height:200px;
        position: absolute;        //父元素需要相对定位
        top: 50%;
        left: 50%;
        margin-top:-100px ;   //二分之一的height，width
        margin-left: -100px;
    }

4、简述一下src与href的区别

href 是指向网络资源所在位置，建立和当前元素（锚点）或当前文档（链接）之间的链接，用于超链接。

src是指向外部资源的位置，指向的内容将会嵌入到文档中当前标签所在位置；在请求src资源时会将其指向的资源下载并应用到文档内，例如js脚本，img图片和frame等元素。当浏览器解析到该元素时，会暂停其他资源的下载和处理，直到将该资源加载、编译、执行完毕，图片和框架等元素也如此，类似于将所指向资源嵌入当前标签内。这也是为什么将js脚本放在底部而不是头部。

5、什么是CSS Hack?

一般来说是针对不同的浏览器写不同的CSS,就是 CSS Hack。
IE浏览器Hack一般又分为三种，条件Hack、属性级Hack、选择符Hack（详细参考CSS文档：css文档）。例如：

// 1、条件Hack
   <!--[if IE]>
      <style>
            .test{color:red;}
      </style>
   <![endif]-->
   // 2、属性Hack
    .test{
    color:#0909; /* For IE8+ */
    *color:#f00;  /* For IE7 and earlier */
    _color:#ff0;  /* For IE6 and earlier */
    }
   // 3、选择符Hack
    * html .test{color:#090;}       /* For IE6 and earlier */
    * + html .test{color:#ff0;}     /* For IE7 */

6、简述同步和异步的区别

同步是阻塞模式，异步是非阻塞模式。
同步就是指一个进程在执行某个请求的时候，若该请求需要一段时间才能返回信息，那么这个进程将会一直等待下去，直到收到返回信息才继续执行下去；
异步是指进程不需要一直等下去，而是继续执行下面的操作，不管其他进程的状态。当有消息返回时系统会通知进程进行处理，这样可以提高执行的效率。

7、px和em的区别

px和em都是长度单位，区别是，px的值是固定的，指定是多少就是多少，计算比较容易。em得值不是固定的，并且em会继承父级元素的字体大小。
浏览器的默认字体高都是16px。所以未经调整的浏览器都符合: 1em=16px。那么12px=0.75em, 10px=0.625em

8、什么叫优雅降级和渐进增强？

渐进增强 progressive enhancement：
针对低版本浏览器进行构建页面，保证最基本的功能，然后再针对高级浏览器进行效果、交互等改进和追加功能达到更好的用户体验。

优雅降级 graceful degradation：
一开始就构建完整的功能，然后再针对低版本浏览器进行兼容。

区别：

a. 优雅降级是从复杂的现状开始，并试图减少用户体验的供给

b. 渐进增强则是从一个非常基础的，能够起作用的版本开始，并不断扩充，以适应未来环境的需要

c. 降级（功能衰减）意味着往回看；而渐进增强则意味着朝前看，同时保证其根基处于安全地带

9、浏览器的内核分别是什么?

IE: trident内核
Firefox：gecko内核
Safari：webkit内核
Opera：以前是presto内核，Opera现已改用Google Chrome的Blink内核
Chrome：Blink(基于webkit，Google与Opera Software共同开发)

JavaScript部分

1、怎样添加、移除、移动、复制、创建和查找节点？

1）创建新节点

createDocumentFragment() //创建一个DOM片段
createElement() //创建一个具体的元素
createTextNode() //创建一个文本节点

2）添加、移除、替换、插入

appendChild() //添加
removeChild() //移除
replaceChild() //替换
insertBefore() //插入

3）查找

getElementsByTagName() //通过标签名称
getElementsByName() //通过元素的Name属性的值
getElementById() //通过元素Id，唯一性

2、实现一个函数clone，可以对JavaScript中的5种主要的数据类型（包括Number、String、Object、Array、Boolean）进行值复制。

  /**
 * 对象克隆
 * 支持基本数据类型及对象
 * 递归方法
 */
function clone(obj) {
    var o;
    switch (typeof obj) {
        case "undefined":
            break;
        case "string":
            o = obj + "";
            break;
        case "number":
            o = obj - 0;
            break;
        case "boolean":
            o = obj;
            break;
        case "object": // object 分为两种情况 对象（Object）或数组（Array）
            if (obj === null) {
                o = null;
            } else {
                if (Object.prototype.toString.call(obj).slice(8, -1) === "Array") {
                    o = [];
                    for (var i = 0; i  obj.length; i++) {
                        o.push(clone(obj[i]));
                    }
                } else {
                    o = {};
                    for (var k in obj) {
                        o[k] = clone(obj[k]);
                    }
                }
            }
            break;
        default:
            o = obj;
            break;
    }
    return o;
}

3、如何消除一个数组里面重复的元素？

// 方法一：
var arr1 =[1,2,2,2,3,3,3,4,5,6],
    arr2 = [];
for(var i = 0,len = arr1.length; i< len; i++){
    if(arr2.indexOf(arr1[i]) < 0){
        arr2.push(arr1[i]);
    }
}
document.write(arr2); // 1,2,3,4,5,6

4、想实现一个对页面某个节点的拖曳？如何做？（使用原生JS）。

5、在Javascript中什么是伪数组？如何将伪数组转化为标准数组？

伪数组（类数组）：无法直接调用数组方法或期望length属性有什么特殊的行为，但仍可以对真正数组遍历方法来遍历它们。典型的是函数的argument参数，还有像调用getElementsByTagName,document.childNodes之类的,它们都返回NodeList对象都属于伪数组。可以使用Array.prototype.slice.call(fakeArray)将数组转化为真正的Array对象。

function log(){
      var args = Array.prototype.slice.call(arguments);  
//为了使用unshift数组方法，将argument转化为真正的数组
      args.unshift('(app)');
 
      console.log.apply(console, args);
};

6、Javascript中callee和caller的作用？

caller是返回一个对函数的引用，该函数调用了当前函数；

callee是返回正在被执行的function函数，也就是所指定的function对象的正文。

7、请描述一下cookies，sessionStorage和localStorage的区别

sessionStorage用于本地存储一个会话（session）中的数据，这些数据只有在同一个会话中的页面才能访问并且当会话结束后数据也随之销毁。因此sessionStorage不是一种持久化的本地存储，仅仅是会话级别的存储。而localStorage用于持久化的本地存储，除非主动删除数据，否则数据是永远不会过期的。

web storage和cookie的区别

Web Storage的概念和cookie相似，区别是它是为了更大容量存储设计的。Cookie的大小是受限的，并且每次你请求一个新的页面的时候Cookie都会被发送过去，这样无形中浪费了带宽，另外cookie还需要指定作用域，不可以跨域调用。
除此之外，Web Storage拥有setItem,getItem,removeItem,clear等方法，不像cookie需要前端开发者自己封装setCookie，getCookie。但是Cookie也是不可以或缺的：Cookie的作用是与服务器进行交互，作为HTTP规范的一部分而存在 ，而Web Storage仅仅是为了在本地“存储”数据而生。

8、手写数组快速排序

关于快排算法的详细说明，可以参考阮一峰老师的文章快速排序
“快速排序”的思想很简单，整个排序过程只需要三步：
（1）在数据集之中，选择一个元素作为”基准”（pivot）。
（2）所有小于”基准”的元素，都移到”基准”的左边；所有大于”基准”的元素，都移到”基准”的右边。
（3）对”基准”左边和右边的两个子集，不断重复第一步和第二步，直到所有子集只剩下一个元素为止。

9、统计字符串”aaaabbbccccddfgh”中字母个数或统计最多字母数。

var str = "aaaabbbccccddfgh";
var obj  = {};
for(var i=0;istr.length;i++){
    var v = str.charAt(i);
    if(obj[v] & obj[v].value == v){
        obj[v].count = ++ obj[v].count;
    }else{
        obj[v] = {};
        obj[v].count = 1;
        obj[v].value = v;
    }
}
for(key in obj){
    document.write(obj[key].value +'='+obj[key].count+' '); // a=4  b=3  c=4  d=2  f=1  g=1  h=1 
}

10、写一个function，清除字符串前后的空格。（兼容所有浏览器）

function trim(str) {
    if (str & typeof str === "string") {
        return str.replace(/(^s*)|(s*)$/g,""); //去除前后空白符
    }
}

其他

1、一次完整的HTTP事务是怎样的一个过程？

基本流程：

a. 域名解析

b. 发起TCP的3次握手

c. 建立TCP连接后发起http请求

d. 服务器端响应http请求，浏览器得到html代码

e. 浏览器解析html代码，并请求html代码中的资源

f. 浏览器对页面进行渲染呈现给用户

2、对前端工程师这个职位你是怎么样理解的？

a. 前端是最贴近用户的程序员，前端的能力就是能让产品从 90分进化到 100 分，甚至更好

b. 参与项目，快速高质量完成实现效果图，精确到1px；

c. 与团队成员，UI设计，产品经理的沟通；

d. 做好的页面结构，页面重构和用户体验；

e. 处理hack，兼容、写出优美的代码格式；

f. 针对服务器的优化、拥抱最新前端技术。
