# JavaScript 从零开始学  
ISBN 978-7-302-37523-4  刘增杰 陈伟光 刘玉萍 张俊彬 编著  清华大学出版社  
2021.10.24 ->
## 第1章 必须了解的JavaScript知识
DOM是什么？
DOM:浏览器中的文档对象类型,不同浏览器使用JavaScript操作同一个页面中同一个对象的方法不同，会造成页面无法跨平台的错误。
DOM为了解决不同浏览器下使用JavaScript操作对象的方法不同的问题而出现的。
DOM可访问页面其他的标准组件，解决Netscape的JavaScript和Microsoft的Jscript之间的冲突，给予Web设计师和开发者一个标准的方法，可访问站点中的数据、脚本和表现层对象。
如：document.getElementById()可根据ID得到页面中的对象，在浏览器中都适用。
## 第2章 JavaScript编程基础
JavaScript执行顺序
JavaScript程序按照在HTML文件中出现的顺序逐行执行。如果需要在整个HTML文件中执行，最好将其放在HTML文件的标记中。
某些代码，如函数体内的代码，不会被执行，只有当所在的函数被其他程序调用时，该代码才被执行。

JavaScript运算符
位运算
& 与 | 或 ^ 异或 ~取补 << 左移  >> 右移
输出十进制18的二进制数 -->example1.html

逻辑运算符
&& 逻辑与
|| 逻辑或
!  逻辑非
## 第3章 程序控制结构与语句

## 第4章 函数
JavaScript中的函数

不指定名函数
function([参数1,参数2...]){
//函数体语句
}
(1)把函数直接赋值给变量
var myFun=function([参数1,参数2...]){
//函数体语句
}
(2)网页事件直接调用函数
window.onload=function([参数1,参数2...]){
//函数体语句
}

4.4常用函数
4.4.1.嵌套函数
4.4.2.递归函数
4.4.3.内置函数
语言内部事先定义好的函数
另一种为自己定义的函数
内置函数：
1.eval函数
eval(expr)
expr:字符串参数作为代码在上下文环境中执行，并返回运行的结果，否则返回undefined.
参数字符串中的变量或函数是在调用eval的上下文环境中可用。
2.isFinite(number)函数
是否为有限数值，number为必选项，为非数字、正无穷数，或负无穷数，则返回false,否则返回true.
3.isNaN(num)函数
提供的值是否保留值NaN:如果值是NaN，返回true，否则返回false.
典型应用检测parseInt和ParseFloat方法的返回值
自身比较结果不等，就是NaN，NaN是唯一自身不等的值
4.parseInt(str,[radix])和parseFloat(str,[radix])函数
str必选，radix为进制，如果radix缺省，则前缀为'0x'的字符串当作16进制；'0'的字符串当作8进制；其它为10进制。
当一个字符串不能转为数字时，返回NaN
5.Number和String函数
主要用来将对象转为数字或字符串。
Number('1234')+Number('1234')=2468
String('1234')+String('1234')=12341234
6.escape和unescape函数
escape(charstring)用于对String对象进行编码，以便在所有计算机上可读。
返回一个包含了charstring内容的字符值（Unicode格式）。除了个别如“*@”之类的符号外，其余所有空格、标点、重音符号以及其它非ASCII字符均可用"%xx"编码代替，其中xx等于表示该字符在16进制数。
unescape(charstring) 返回指定值的ASCII字符串，即所有以%xx十六进制形式编码的字符都用ASCII字符集中等价的字符代替。

## 第5章 对象与数组
### 5.1 了解对象
属性用来描述对象的状态，使用方法和事件处理对象的各种行为。
- 事件：由于对象行为的复杂性，对象的某些行为不能使用通用代码来处理，需要用户根据实际情况来编写处理该行为的代码，该代码称为事件。

JavaScript是基于对象的编程语言，主要支持以下4种对象：
+ JavaScript核心对象：包括基本数据类型相关的对象(如 String、 Boolean、 Number)、允许创建用户自定义和组合类型的对象(如 Object.,Aray)和其他能简化JavaScript操作的对象(如Math,Date, RegExp, Function)。
+ 浏览器对象:包括不属于JavaScript语言本身但被绝大多数浏览器所支持的对象,如控制览器窗口和用户交互界面的window对象、提供客户端浏览器配置信息的Navigator对象。
+ 用户自定义对象：Web应用程序开发者用于完成特定任务而创建的自定义对象,可自由设计对象的属性,方法和事件处理程序,编程灵活性较大。
+ 文本对象:由文本域构成的对象,在DOM中定义,同时赋予很多特定的处理方法,如interData, appendData()等。

5.1.2面向对象编程  
面向对象程序设计( Objest Oriented Programming, OOP)  
面向对象编程三个重要的概念。  
1.继承  
2.封装  
3.多态  

需要说明的是:定位Javascript脚本是基于对象的脚本编程语言,而不是面向对象和编程语言。  
其原因在于:JavaScript是以DOM和BOM中定义的对象模型及操作方法为基础的,但又不具备面向对象编程语言所必须具备的显著特征,如分类、继承、封装、多态、重载等,所以只能通过嵌入其他面向对象编程语言如Java生成的JavaApplet组件等来实现相应的功能。另外, Javascript还支持DOM和BOM提供的对象模型,用于根据其对象模型的层次结构来访问目标对象的属性并对对象施加相应的操作。  
在 JavaScript语言中,之所以任何类型的对象都可以赋予任意类型的数值,是因为Javascript为弱类型的脚本语言,即变量在使用前无须任何声明,在浏览器解释运行其代码时,才检查目标变量的数据类型。  
5.1.3 JavaScript的内部对象  
分两种：  
静态对象：对象名.成员  
动态对象： new 创建对象  对象实例名.成员  
| 对象名 | 静态/动态性 | 功能 |
| :----:| ----: | :----- |
| Object对象 | 动态对象 | 使用该对象可以在程序运行时为JavaScrip对象随意添加属性 |
| String对象 | 动态对象 | 用于处理或格式化文本字符串以及确定和定位字符串中的子字符串 |
| Date对象 | 动态对象 | 使用Dae对象执行各种日期和时间的操作 |
| Event对象 | 静态对象 | 用来表示 JavaScript的事件 |
| FileSystemObject对象 | 动态对象 | 主要用于实现文件操作功能 |
| Drive对象 | 动态对象 | 主要用于收集系统中的物理或逻辑驱动器资源中的内容 |
| File对象 | 静态对象 | 用于获取服务器端指定文件的相关属性  |
| Folder对象 | 静态对象 | 用于获取服务器端指定文件夹的相关属性 |


### 5.2 对象访问语句  
5.2.1 for···in
```javascript
var myarray = new Array()
myarray[0]="星期一"
myarray[1]="星期二"
myarray[2]="星期三"
for(var i in myarray)
{
    document.write(myarry[i] + "<br/>")
}
```
5.2.2 with语句  
在with语句块中，凡是JavaScript不识别的属性和方法都和该语句块指定的对象有关。  
在存取对象属性和方法时就不用重复指定参考对象了。
```
with object{
    statements
}
```
```javascript
var date_time = new Dtate();
alert(date_time.getFullYear()+"年");
with(date_time){
    alert(getFullYear()+"年");
}
```
### 5.3 JavaScript中的数组



