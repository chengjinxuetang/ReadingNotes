# JavaScript 从零开始学  
ISBN 978-7-302-37523-4  刘增杰 陈伟光 刘玉萍 张俊彬 编著  清华大学出版社
2021.10.24 ->
DOM是什么？
DOM:浏览器中的文档对象类型,不同浏览器使用JavaScript操作同一个页面中同一个对象的方法不同，会造成页面无法跨平台的错误。
DOM为了解决不同浏览器下使用JavaScript操作对象的方法不同的问题而出现的。
DOM可访问页面其他的标准组件，解决Netscape的JavaScript和Microsoft的Jscript之间的冲突，给予Web设计师和开发者一个标准的方法，可访问站点中的数据、脚本和表现层对象。
如：document.getElementById()可根据ID得到页面中的对象，在浏览器中都适用。

JavaScript执行顺序
JavaScript程序按照在HTML文件中出现的顺序逐行执行。如果需要在整个HTML文件中执行，最好将其放在HTML文件的<head>...</head>标记中。
某些代码，如函数体内的代码，不会被执行，只有当所在的函数被其他程序调用时，该代码才被执行。

JavaScript运算符
位运算
& 与 | 或 ^ 异或 ~取补 << 左移  >> 右移
输出十进制18的二进制数 -->example1.html

逻辑运算符
&& 逻辑与
|| 逻辑或
!  逻辑非

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



