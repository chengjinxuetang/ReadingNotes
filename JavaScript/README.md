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


| Array对象 | 动态对象 | 使用Array对象定义数组操作 |

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
JavaScript中的数组元素允许属于不同的数据类型。
5.3.2创建访问数组
```javascript
myArray = new Array();
myArray = new Array([size])
myArray = new Array([element0[,element1[,...[,elementN]]]]);

```

5.3.3
不需要知道数组个数的情况下输出数组元素 for···in
```javascript
for(key in myArray)
```
5.3.4 Array对象的常用属于和方法
1.常用属于
(1). length
```javascript
my_array.length
```
(2). prototype
所有Javascript对象所共有的属性，定义新的属性和方法添加到Array对象中
```javascript
Array.prototype.methodName = functionName
```
1.常用方法
连接方法concat、分隔方法join、追加方法push、倒转方法reverse、切片方法slice等
(1). concat
```javascript
var array3 = array1.concat(array2)
```
(2). join
```javascript
var arrayString = array.join(separator)
```
(3). push
```javascript
array.push([data1[,data2[,...[datan]]]])
```
(4). reverse
数组元素反序排列
```javascript
array.reverse()
```
(5). slice  切片(部分)
该方法将提取数组中的一个片段或子字符串，并将其作为新数组返回，而不修改原始数组。返回的数组包括start元素到end元素(但不包括该元素)的所有元素
```javascript
my_array.slice([start[,end]])
```
(6). sort
按Unicode编码进行排序,默认按升序排列，也可以指定对比函数进行排序，对比函数格式
comparefunction(arg1,arg2)。
返回为负,arg2排在arg1的后面；返回为0，视为相等；返回为正，arg2排在arg1的前面。
```javascript
sort([cmpfun(arg1,arg2)])
```
(7). splice  
指定索引和数据个数，删除或替换数组中的部分数据，该方法的返回值为被删除或替换掉的数据。
```javascript
array.splice([start,count[,data1[data2,[,...[,datan]]]])
```
没有指定data参数则指定的数据被删除，指定了则被替换。

### 5.4 详解常用的数组对象方法
5.4.1 连接其它数组到当前数组
arrayObject.concat(array1,array2,.....,arrayN)
5.4.2 将数组元素连接为字符串
arrayObject.join(separator)
5.4.3 移除数组中最后一个元素
arrayObject.pop()
如果数组为空，pop不改变数组，并返回undefined值，否则返回移除的元素的值。
5.4.4 将指定的数值添加到数组中
arrayObject.push(newelement1,newelement2,....,newelementN)
5.4.5 反序排列数组中的元素
arrayObject.reverse()
不会创建新数组，会改变原来的数组。
5.4.6 删除数组中第一个元素
arrayObject.shift()
删除数组中第一个元素,并返回第一个元素的值。不会创建新数组，直接修改原来的数组。
5.4.7 获取数组中的一部分数据
arrayObject.slice(start,end)
5.4.8 对数组中的元素进行排序
arrayObject.sort(sortby)
5.4.9 将数组转成字符串
arrayObject.toString()
元素之间用逗号分隔。
5.4.10 将数组转换成本地字符串
arrayObject.toLocaleString()
5.4.11 在数组开头插入数据，并返回该数组
arrayObject.unshift(newelement1,newelement2,....,newelementN)

### 5.5 创建和使用自定义对象
Java作为基于对象的编程语言，其对象实例通过构造函数来创建。   
每一个构造函数包括一个对象原型，定义了每个对象包含的属性和方法。  
两种方法创建自定义对象：  
1.通过定义对象的构造函数的方法  
2.通过对象直接初始化的方法  
#### 5.5.1 通过定义对象的构造函数的方法 
通过定义对象的构造函数,然后使用new操作符来生成该对象的实例  
```
source/5.26.html
```
也可以写成内部函数
```javascript
function Student(iName,iAddress,iGrade,iScore)
{
   this.name=iName;
   this.address=iAddress;
   this.grade=iGrade;
   this.Score=iScore;
   this.information=function()
   {
        var msg="";
        msg="学生信息：\n"
        msg+="\n学生姓名 : "+this.name+" \n";
        msg+="家庭地址 : "+this.address +"\n";
        msg+="班级 : "+this.grade +" \n";
        msg+="分数 : "+this.Score
        window.alert(msg);
   };
}
```
#### 5.5.2 通过对象直接初始化的方法
该方法无须生成此对象的实例  
```javascript
//直接初始化对象
var ZJDX = {name:"test1", address:"test2",grade:"401",score:"99",infomation:showInfomation};
function showInfomation()
   {
        var msg="";
        msg="学生信息：\n"
        msg+="\n学生姓名 : "+this.name+" \n";
        msg+="家庭地址 : "+this.address +"\n";
        msg+="班级 : "+this.grade +" \n";
        msg+="分数 : "+this.Score
        window.alert(msg);
   };
```
这种代码紧凑，编程效率高，但要生成若干个对象的实例，就必须为每个实例重复相同的代码结构，而只是参数不同而已，代码的重用性比较差。  

#### 5.5.3 修改和删除对象实例的属性
```javascript
//直接初始化对象
var ZJDX = {name:"test1", address:"test2",grade:"401",score:"99",infomation:showInfomation};
function showInfomation()
   {
        var msg="";
        msg="学生信息：\n"
        msg+="\n学生姓名 : "+this.name+" \n";
        msg+="家庭地址 : "+this.address +"\n";
        msg+="班级 : "+this.grade +" \n";
        msg+="分数 : "+this.Score+" \n";
        //修改score属性
        this.Score = 88;
        //删除对象实例的address属性
        delete this.address;
        window.alert(msg);
   };
```

#### 5.5.4 通过原型为对象添加新属性和新方法
JavaScript中对象的prototype属性，是用来返回对象类型原型引用的。使用prototype属性提供对象类的一组基本功能，并且对象的新实例会“继承”赋予该对象原型的操作。所有JavaScript内部对象都有只读的prototype属性。可以向其原型中动态添加功能（属性和方法），但该对象不能被赋予不同的原型。然而，用户定义的对象可以被赋予新的原型。   
给已经存在的对象添加新属性和新方法。  
```
source/5.27.html
```
原型里添加了方法，为什么每一个对象实例有这个方法，第二个对象实例没有这个方法，所有对象的prototype不都指向同一个原型吗?  TODO:

#### 5.5.5 自定义对象的嵌套
```
source/5.28.html
```
```javascript
var StudentData={
    age:"26",
    Tel:"181000000",
    teacher:"张老师"
}
var ZJDX = {
    name:"test1", 
    address:"test2",
    grade:"401",
    score:"99",
    //嵌套对象StudentData
    data:StudentData,
    infomation:showInfomation
};

```
#### 5.5.6 内存的分配和释放
JavaScript是基于对象的编程语言，而不是面向对象的编程语言，因此缺少指针的概念。面向对象的编程语言在动态分配和释放内存方面起着非常重要的作用，那么JavaScript中的内存如何管理呢？在创建对象的同时，浏览器自动为创建的对象分配内存空间，JavaScript将新对象的引用传递给调用的构造函数；而在对象清除时其占据的内存将被自动回收，其实整个过程都是浏览器的功能，JavaScript只是创建该对象。
浏览器中的这种内存管理机制称为“内存回收”，它动态分析程序中的每个占据内存空间的数据（变量、对象等）。如果该数据对于程序标记为不可再用时，浏览器调用内部函数将其占据的内存空间释放，实现内存的动态管理。在自定义的对象使用过后，可以通过给其赋空值的方法来标记对象占据的空间是否可以释放，如“ZJDX=null;”。浏览器将根据此标记动态释放其占据的内存，否则将保存该对象直至当前程序再次使用它为止。  

### 5.6 动态改变下拉菜单内容 
5.29.html

## 第6章 日期与字符串对象

### 6.1 日期对象
#### 6.1.1 创建日期对象
方法一  
//以当前时间创建一个日期对象  
var myDate1=new Date();  
方法二  
日期对象 = New Date(日期字符)  
将一个字符串转换成日期对象，这个字符串可以是只包含日期的字符串，也可以是即包含日期又包含时间的字符串。
JavaScript对日期格式有要求，通常使用的格式有如下两种：  
+ 日期字符串可以表示为："月 日,年 小时:分钟:秒钟"，其中月份必须使用英文单词，而其它部分可以使用数字表示，日和年之间一定要有逗号(,)。  
+ 日期字符串可以表示为："年/月/日 小时:分钟:秒钟"，所有部分要求使用数字，年份要求使用4位，月份用0~11的整数，代表1月~12月。

方法三  
var myDate4=new Date(2011,10,19,16,16,16);  
通过指定年、月、日、时、分、秒创建日期对象，时、分、秒都可以省略。  月份用0~11的整数，代表1月~12月。  

方法四  
使用毫秒来创建日期对象。可以把1970年1月1日0时0分0秒0毫秒看成一个基数，而给定的参数代表距离这个基数的毫秒数。如果把指定参数毫秒为3000，则该日期对象中的日期为1970年1月1日0时0分3秒0毫秒。  
6.1.html

#### 6.1.2 Date对象属性
只包含两个属性，分别是 constructor 和 prototype,因为这两个属性在每个内部对象中都有。

#### 6.1.3 日期对象的常用方法
日期对象的方法主要分为三大组：setXxx、getXxx和toXxx。setXxx这些方法用于设置时间和日期值；getXxx这些方法用于获取时间和日期值；toXxx主要是将日期转换成指定格式。
6.1.3.日期对象.jpg
上面将日期转化为字符串的方法，要么就是将日期对象中的日期转换成字符串，要么就是将日期对象中的时间转换成字符串，要么就是将日期中的日期和时间一起转换成字符串。  
并且，这些方法转换成的字符串格式无法控制，例如，将日期转换成2010年6月10日的格式，以上方法就无法做到。  
从JavaScript 1.6开始添加了一个toLocalFormat()方法，该方法可以有选择地将日期对象中的某个或某些部分转换成字符串，也可以指定转换的字符串格式。toLocalFormat()方法的语法如下所示。  
日期对象.toLocaleFormat(formatString)    
参数formatString为要转换的日期字符，这些字符及含义如下图所示：
6.1.3.format String字符含义.png  
实例： 6.2.html  

### 6.2 详解日期对象的常用方法
#### 6.2.1 返回当前日期和时间
```javascript
document.write(Date())
```
#### 6.2.2 以不同的格式显示当前日期
ch06\6.4.html  

#### 6.2.3 返回日期所对应的周次
dateObject.getDay()  
返回值是0(周日)-6(周六)之间的一个整数  
ch06\6.5.html  

#### 6.2.4 显示当前时间
getHours()、getMinutes()、getSeconds()返回的值是一个两位的数字。不过返回值不总是两位的，如果该值小于10，则仅返回一位数字。  
ch06\6.6.html  

#### 6.2.5 返回距1970年1月1日午夜的时间差
getTime()返回Date对象距离1970年1月1日午夜(GMT时间)之间的毫秒数。  
ch06\6.7.html  

#### 6.2.6 以不同的格式来显示UTC日期
getUTCDate() 返回一个月(UTC)中的某一天(1~31中的一个值)             ***1为一个月的第1天  
getUTCMonth() 返回一个月份的数字0(一月)~11(十二月)之间的一个整数。  ***0为1月  
getUTCFullYear() 返回年份的4位数字，不是两位数的缩写。  
ch06\6.8.html  

#### 6.2.7 根据世界时返回日期对应的周次
getUTCDay() 返回表示星期里的一个数字。  0(周日)-6(周六)  
ch06\6.9.html  

#### 6.2.8 以不同的格式来显示UTC时间
getUTCHours()、getUTCMinutes()、getUTCSeconds()返回的值是一个两位的数字。不过返回值不总是两位的，如果该值小于10，则仅返回一位数字。   
ch06\6.10.html  

#### 6.2.9 设置日期对象中的年份、月份与日期值
setFullYear(year,month,day)  4位  0~11  1~31    
setMonth(month,day)  
setDate(day)  
ch06\6.11.html  

#### 6.2.10 设置日期对象中的小时、分钟与秒钟值
setHours(hour,min,sec,millisec)  
setMinutes(min,sec,millisec)  
setSeconds(sec,millisec)  
ch06\6.12.html  

#### 6.2.11 以UTC日期对Date对象进行设置
setUTCDate(day)  
ch06\6.13.html  

#### 6.2.12 返回当地时间与UTC时间的差值
使用getTimezoneOffset()方法可返回格林威治时间和本地时间之间的时差，以分钟为单位。  
dateObject.getTimezoneOffset()  
返回值为本地时间与GMT时间或UTC时间之间的时间差，以分钟为单位。  
返回值不是以小时计，因某些国家所占用的时区甚至不到一个小时的间隔。  
由于使用夏令时的惯例，该方法的返回值不是一个常量。  
ch06\6.14.html  
本地时间超前了 -8个小时。  

#### 6.2.13 将Date对象中的日期转化为字符串格式
toString()  
ch06\6.15.html  

#### 6.2.14 返回一个以UTC时间表示的日期字符串
toUTCString()  
ch06\6.16.html  

#### 6.2.15 将日期对象转化为本地日期
toLocaleString()  
ch06\6.17.html  

#### 6.2.16 日期间的运算
1. 日期对象与整数年、月或日相加  
date.setDate(date.getDate()+value);  //增加天  
date.setMonth(date.getMonth()+value); //增加月  
date.setFullYear(date.getFullYear()+value); //增加年
2. 日期相减  
两个日期对象相减，相减之后将会返回这两个日期之间的毫秒数。  
ch06\6.18.html  

### 6.3 字符串对象
可以将字符串直接看成字符串对象，不需要任何转换。字符串操作时，不会改变字符串中的内容。  
#### 6.3.1 创建字符串变量
1. 直接声明字符串变量  
[var] 字符串变量=字符串  
var myString="This is a sample";  
2. 使用new关键字来创建字符串对象  
[var] 字符串对象=new String(字符串)
var myString=new String("This is a sample");  
#### 6.3.2 字符串对象的常用属性
Constructor  字串对象的函数模型  
length  字串长度  
prototype  添加字串对象的属性  
测试字符串长度时，空格也占一个字符。一个汉字占一个字符位，即一个汉字长度为1。  
ch06\6.19.html  

#### 6.3.3 字符串对象的常用方法
ch06\String内置方法.jpg

### 6.4 详解字符串对象的常用方法
#### 6.4.1 设置字符串字体属性
stringObject.big()  
stringObject.bold();  
cho6\6.20.html  
上标  下标  
#### 6.4.2 以闪烁方式显示字符串
stringObject.blink();  
cho6\6.21.html  

#### 6.4.3 转换字符串的大小写
与toUpperCase()不同的是，toLocalUpperCase()方法按照本地方式把字符串转换为大写（小写）。只有几种语言(如土耳其语)具有地方特有的大小写映射，所有该方法的返回值通常与toUppderCase()一样。  
cho6\6.22.html  

#### 6.4.4 连接字符串
stringObject.concat(stringX, stringX,...,stringX)  
返回连接后的字符串，stringObject本身并没有被更改。  
stringObject.concat()与Array.concat()很相似，不过，使用“+”运算符更简便一些。  
cho6\6.23.html

#### 6.4.5 比较两个字符串的大小
stringObject.localCompare(target)
stringObject 小于 target  -> 小于0的数  
stringObject 大于 target  -> 大于0的数  
stringObject 等于 target  -> 等于0  
cho6\6.24.html

#### 6.4.6 分割字符串
stringObject.split(separator,howmany)  
separator为必选项，为字符串或正则表达式，从该参数指定的地方分割stringObject.  
howmany为可选项，指定返回数组的最大长度。如果设置了该参数，返回的子串不会多于这个参数指定的数组。如果没有设置这个参数，整个字符串都会被分隔，不考虑它的长度。  
cho6\6.25.html

#### 6.4.7 从字符串中提取字符串
stringObject.substring(start,stop)  
start为必选项，一个非负的整数，规定要提取的子串的第一个字符在stringObject中的位置.  
stop为可选项，是一个非负的整数，比要提取的子串的最后一个字符在stringObject中的位置多1.如果省略该参数，那么返回的子串会一直到字符串的结尾。
cho6\6.26.html

### 6.5 实战演练1--制作网页随机验证码
cho6\6.27.html  ??

### 6.6 实战演练2--制作动态时钟
cho6\6.28.html  ??

### 6.7 疑难解惑
1.产生指定范围内的随机整数  
(1) 产生0~n之间的随机数：Math.floor(Math.random()*(n+1))  
(2) 产生n1~n2之间的随机数:Math.floor(Math.random()*(n2-n1))+n1  
2.如何格式化alert弹出容器的内容？  
借助转义字符格式化： "\n" 按指定位置换行  
                   "\t" 有制表位间隔  


## 第7章 数值与数学对象

### 7.1 Number对象
#### 7.1.1 创建Number对象
numObj = new Number(value)  
ch07\7.1.html  

#### 7.1.2 Number对象的属性
| 属性 | 说明 |
| :----:| :----- |
| constructor | 返回对创建此对象的Number函数的引用
| MAX_VALUE | 可表示的最大数 近似值1.7976931348623157*10<sup>308</sup>  ch07\7.2.html |
| MIN_VALUE | 可表示的最小数 接近0，但不是负数 近似值 5*10<sup>-324</sup> ch07\7.3.html |
| NaN | 非数字值 使用isNaN()判断是不是NaN值 ch07\7.4.html |
| NEGATIVE_INFINITY | 负无穷大，溢出时返回该值  ch07\7.5.html |
| POSTIVE_INFINITY | 正无穷大，溢出时返回该值 ch07\7.6.html |
| prototype | 使您有能力向对象添加属性和方法  |

#### 7.1.3 Number对象的方法
 | 方法 | 说明 |
| :----:| :----- |
| toString | 把数字转为字符串，使用指定的基数
| toLocalString | 把数字转为字符串，使用本地数字格式顺序 |
| toFixed | 把数字转为字符串，结果的小数点后有指定位数的数字 |
| toExponential | 对对象的值转换为指数计数法 |
| toPrecision | 把数字格式化为指定的长度 |
| valueOf | 返回一个Number对象的基本数字值 |

### 7.2 详解Number对象常用的方法
#### 7.2.1 把Number对象转换为字符串
NumberObject.toString(radix)  
radix可选参数，使用2~36之间的整数。默认10  
ch07\7.7.html  

#### 7.2.2 把Number对象转换为本地格式字符串
NumberObject.toLocaleString()  
ch07\7.8.html  

#### 7.2.3 四舍五入时指定小数位数
NumberObject.toFixed(num)  
num必选项，规定小数的位数，是0~20之间的值，包括0和20.  
ch07\7.9.html  

#### 7.2.4 返回以指数记数法表示的数字
NumberObject.toExponential(num)  
num必选项，规定指数计数法中的小数的位数，在0~20之间.  
ch07\7.10.html  

#### 7.2.5 以指数记数法指定小数位
NumberObject.toPrecision(num)  
num必选项，规定必须被转换为指数计数法的最小位数，在1~21之间（且包含1和21）. 如果省略，则调用toString()，不是把数字转换成10进制的值。  
ch07\7.10.html  

### 7.3 Math对象
Math对象提供了大量的数学常量和数学函数。在使用Math对象时，不能使用关键字new来创建对象实例，而直接使用"对象名.成员"的格式来访问其属性和方法。  

#### 7.3.1 创建Math对象
Math.[{proterty|method}]

#### 7.3.2 Math对象的属性
| 属性 | 说明 |
| :----:| :----- |
| E | 返回算术常量e，即自然对数的底数(约等于2.718)
| LN2 | 返回2的自然对数(约等于0.639) |
| LN10 | 返回10的自然对数(约等于2.302) |
| LOG2E | 返回以2为底的e的对数(约等于1.414) |
| LOG10E | 返回以10为底的e的对数(约等于0.434) |
| PI | 返回圆周率(约等于3.14159) |
| SQRT1_2 | 返回2的平方根的倒数 (约等于0.707) |
| SQRT2 | 返回2的平方根 (约等于1.414) |

ch07\7.12.html  

#### 7.3.3 Math对象的方法
 | 方法 | 说明 |
| :----:| :----- |
| abs(x) | 返回数的绝对值
| acos(x) | 返回数的反余弦值 |
| asin(x) | 返回数的反正弦值 |
| atan(x) | 以介于-PI/2与PI/2弧度之间的数值来返回x的反正切值 |
| atan2(x) | 返回从x轴到点(x,y)的角度(介于-PI/2与PI/2弧度之间) |
| ceil(x) | 对数进行上舍入 |
| floor(x) | 对数进行下舍入  |
| cos(x) | 返回数的余弦 |
| exp(x) | 返回e的指数  |
| log(x) | 返回数的自然对数(底为e)  |
| max(x,y) | 返回x和y中的最高值  |
| min(x,y) | 返回x和y中的最低值  |
| pow(x,y) | 返回x的y次幂  |
| random() | 返回0~1之间的随机数  |
| round(x) | 把数四舍五入为最接近的整数  |
| sin(x) | 返回数的正弦  |
| sqrt(x) | 返回数的平方根  |
| tan(x) | 返回角的正切  |
| toSource() | 返回该对象的源代码 |
| valueOf() | 返回Math对象的原始值  |


### 7.4 详解Math对象常用的方法
#### 7.4.1 返回数的绝对值
Math.abs(x)
x必选项，必须为一个数值。  
ch07\7.13.html  

#### 7.4.2 返回数的正弦值、正切值和余弦值
1. Math.sin(x)
x必选项，是一个以弧度表示的角。将角度乘以0.017453293(2PI/360) 即可转换为弧度。  
ch07\7.14.html  

2. Math.cos(x)
x必选项，必须为一个数值。    
ch07\7.15.html  

3. Math.tan(x)
x必选项，是一个以弧度表示的角。将角度乘以0.017453293(2PI/360) 即可转换为弧度。  
ch07\7.16.html  

#### 7.4.3 返回数的反正弦值、正切值和余弦值
1. Math.asin(x)
x必选项，必须是一个数值，该值介于-1.0~1.0之间。  
超过-1.0~1.0返回NaN,x为1，返回PI/2。  
ch07\7.17.html  

2. Math.atan(x)
x必选项，需要计算反正切值的数值。  
ch07\7.18.html  

3. Math.acos(x)
x必选项，必须为一个数值，该值介于-1.0~1.0之间。  
超过-1.0~1.0返回NaN,x为1，返回0。  
ch07\7.19.html  

#### 7.4.4 返回两个或多个参数中的最大值或最小值
Math.max(x...)  
Math.min(x...)   
ch07\7.20.html  

#### 7.4.5 计算指定数值的平方根
Math.sqrt(x)  
x必选，且必须大于等于0的数。如果x小于0，返回NaN。  
ch07\7.21.html  

#### 7.4.6 数值的幂运算
返回x的y次幂  
Math.pow(x,y)  
x必选，为底数，且必须为数字。y也是必选项，是幂数，且必须是数字。  
如果结果是虚数或负数，则返回NaN。如果由于指数过大而引起浮点溢出，返回Infinity。  
ch07\7.22.html  

#### 7.4.7 计算指定数值的对数
Math.log(x)  
x为必选项，可以是任意数值或表达式。其返回值是x的自然对数。  
x必须大于0.  
ch07\7.23.html  

#### 7.4.8 取整运算
Math.round(x)  
x为必选项，且必须是数字。返回x最接近的整数。  
对于0.5，该方法将进行舍入。如 3.5取4，而-3.5取-3    
ch07\7.24.html  

#### 7.4.9 生成0~1之间的随机数
Math.random()  
返回0.0~1.0之间的随机数。  
ch07\7.25.html  

#### 7.4.10 根据指定的坐标返回一个弧度值
Math.atan2(y,x)  
返回从x轴到点(x,y)之间的角度。  
x必选项，指定点的X坐标。  
y必选项，指定点的Y坐标。  
其返回值为-PI与PI之间的值，是从X轴正向逆时针旋转到点(x,y)时经过的角度。  
ch07\7.26.html  

#### 7.4.11 返回大于或等于指定参数的最小整数
Math.ceil(x)  
对一个数进行上舍入，返回大于或等于指定参数的最小值。  
x必选项，且必须是一个数值。  
ch07\7.27.html  

#### 7.4.12 返回小于或等于指定参数的最大整数
Math.floor(x)  
对一个数进行下舍入，返回大于或等于指定参数的最大值。  
x必选项，且必须是一个数值。  
ch07\7.28.html  

#### 7.4.13 返回以e为基数的幂
Math.exp(x)  
返回e的x次幂的值。  
x必选项，可以是任意数值或表达式，被用作指数。  
其返回值为e的x次幂。e代表自然对数的底数，其值近似为2.71828.
ch07\7.29.html  

### 7.5 实战演练---使用Math对象设计程序
指定范围的随机数生成 ??  

## 第8章 文档对象模型与事件驱动
DOM(Document Object Model) 文档对象模型，主要涉及网页页面元素的层次关系。

### 8.1 文档对象模型
DOM是表示文档(HTML、XML)和访问、操作构成文档的各种元素的应用程序接口(API)。  
DOM是W3C定义的标准的文档对象模型。以树型结构表示HTML和XML文档，定义遍历这个树和检查、修改树节点的方法和属性。是一种与浏览器、平台、语言无关的接口，使用户可以访问页面及其它的标准组件。  

W3C DOM经历了如下三个阶段：  
(1)从DOM Level 1开始，DOM API包含了一些接口，用于表示XML文档中找到的所有不同类型的信息，它还包含使用这些对象所为必选项的方法和属性。  
Level 1 包括对XML 1.0和HTML的支持,每个HTML元素被表示为一个接口。它包括用于添加、编辑、移动和读取节点中包含的信息的方法等等。然而,它没有包括对XML名称空间(XML Namespace)的支持,XML名称空间提供分割文档中信息的能力。  
(2) DOM Level 2基于 DOM Level1并扩展了 DOM Level 1,添加了鼠标和用户界面事件、范围、遍历(重复执行DOM文档的方法)、XML命名空间、文本范围、检查文档层次的方法等新概念,并通过对象接口添加了对CSS的支持。
同时引入几个新模块,用以处理新的接口类型,包括以下几个方面。  
+ DOM视图:描述跟踪文档的各种视图(使用CSS样式设计文档前后)的接口
+ DOM事件;描述事件的接口
+ DOM样式表:描述处理基于CSS样式的接口
+ DOM遍历和范围:描述遍历和操作文档树的接口  
(3)当前正处于定稿阶段的 DOM Level 3包括能更好地支持创建 Document对象(以前版本将这个任务留给实现,使得创建通用应用程序很困难)、增强了名称空间的支持,以及用来处理文档加载和保存、验证、 XPath新模块:XPah是在XSL转换( XSL Transformation)以及其他XML技术中用来选择节点的手段。

#### 8.1.1 认识文档对象模型
文档对象模型定义了 Javascript可以进行操作的览器,描述了文档对象的逻辑结构及各功能部件的标准接口,主要包括如下方面
+ 核心Javascript语言参考(数据类型,运算符,基本语句,函数等)
+ 与数据类型相关的核心对象( String,Amay,Math,Dae等数据类型)
+ 浏览器对象( Window, Location, History, Navigator等),
+ 文对象( Document, Images,fom等)
Javascript使用览器对象模型(BOM)和文档对象模型(DOM)两种主要对象模型,前者提供了访问览器各个功能部件,如浏览器窗口本身、浏览历史等的操作方法:后者则提供了访问览器窗口的内容,如文档,图片等各种HTML元素以及这些元素包含的文本的操作方法.

#### 8.1.2 文档对象的产生过程
在面向对象或基于对象的编程语言中,指定对象的作用越小,对象位置的假定也就越多.对客户端Javascript脚本而言,其对象一股不超过到览器本不会访间计算机硬件、操作系统等其他超出浏览器的对象.  
当载入HTML文档时,浏览器解释其代码,当到自身运行的HML元素对像对应的标记时，就按HTML文档我入的序在内存中创建这些对象,而不管Javascript脚本是否真正运行这些对象.对象创建后,浏览器为这些对象提供专供 Javascript脚本使用的可选属性、方法和处理程序。通过属性、方法和处理程序,Web开发人员就能够动态地操作HTML文档内容.  
动态改变文档背景颜色 ch08\8.1.html  



### 8.2 访问节点
在DOM中，HTML文档各个节点被视为各种类型的Node对象。每个Node对象都有自己的属性和方法，利用这些属性和方法可以遍历整个文档树。由于HTML文档的复杂性，DOM定义了nodeType来表示节点的类型。  

#### 8.2.1 节点的基本概念
表8-1 DOM定义的HTML文档节点类型  
 | 节点类型数值 | 节点类型 | 附加说明 | 实例 |
| :----:| :----- | :----- | :----- |
| 1 | 元素( Element) | HTML标记元素 | ```<h1>...<hl>```
| 2 | 属性( Attribute) | HTML标记元素的属性 | ```color="red"```
| 3 | 文本(Text) | 被HM标记括起来的文本段 | ```Hello World!```
| 8 | 注释( Comment) | HTML注释段 | ```<!--Comment>```
| 9 | 文档( Document) | HTML文档跟文本对象 | ```<html>```
| 10 | 文档类型( DocumentType) | 文档类型 | ```<!DOCTYPE HTMLPUBLIC"...">```

注：
文本节点：纯文本，不包含左右的标记  

#### 8.2.2 节点的基本操作
表8-2 DOM中的节点处理方法  
 | 操作类型 | 方法原型 | 附加说明 |
| :----:| :----- | :----- |
| 生成节点 | creatElement(tagName) | 创建由 tagName指定类型的标记 |
| 生成节点 | CreateTextNode(string) | 创建包含字符串 string的文本节点 |
| 生成节点 | createAttribute(name) | 针对节点创建由name指定的属性,不常用 |
| 生成节点 | createComment(string) | 创建由字符串 string指定的文本注释 |
| 插入的添加节点 | appendChild(newChild, targetChild)) | 添加子节点newChild到目标节点上 |
| 插入的添加节点 | insertBefore(newChild, targetChild) | 将新节点newChild插入目标节点targetChild之前 |
| 复制节点 | cloneNode(bool) | 复制节点自身,由逻辑量bool确定是否复制子节点 |
| 删除和替换节点 | removeChild(childName) | 删除由 childName指定的节点 |
| 删除和替换节点 | replaceChild(newChild, oldchild) | 用新节点 newChild替换旧节点oldChild |

1.创建节点  
ch08\8.2.html  
2.插入或添加节点  
ch08\8.3.html  
ch08\8.4.html  
3.复制节点  
ch08\8.5.html  
4.删除节点和替换节点  
ch08\8.6.html  

表8-3 处理文本节点的方法  
 | 方法 | 作用|
| :----:| :----- |
| appendData(string) |在文本节点的结尾添加一个由 string指定的字符串 |
| deleteData(offset, count) |删除从oset处开始由 count指定的字符串个数 |
| insertData(offset, string) |在offset处插入 string指定的文本 |
| replaceData(offset, count, string) |用 string指定的文本替换自oset开始的由 count指定数目的字符 |
| splitText(offset) |从 offset处将原文本节点一分为二,其中左半部分作为原节点内容,而右半部分作为新的文本节点 |
| substringData(offset, count) | 返回一个字符串,该字符串包含自 offset开始的由 count指定的数目的一组字符 |

5.修改节点  
ch08\8.7.html  




### 8.3 文档对象模型的属性和方法
表8-4 Node对象方法  
 | 方法 | 作用|
| :----:| :----- |
| appendChild(newChild) |给当前节点添加一个子节点 |
| cloneNode(deep) |复制当前节点,当deep为true时,复制当前节点和其所有子节点,否则仅复制当前节点本身 |
| haschildNodes |当前节点有子节点,返回true,否则返回 false |
| InsertBefore(newNode, refNode) |把一个 newNode节点插入到 refNode节点之前 |
| removeChild(Child) |删除指定的子节点 |
| replaceChild(newChild, oldchild) | 用 newChild子节点代替 oldChild子节点 |
| selectNodes(patten) | 获得符合指定类型的所有节点 |
| selectSingleNodes(patten) | 获得符合指定类型的第一个节点 |
| TransformNode(styleSheetOBJ) | 利用指定的样式来变换当前节点及其子节点 |


### 8.4 事件处理
少数事件的名字不易理解，如blur在英文中是模糊的意思，在这里表示是一个域或者一个表单失去焦点。  
一般情况下事件名称前加前缀on为其处理器，如onclick  
也包含浏览器状态的改变，如resize和Load这样的事件。k
现代事件模型中引入Event对象，它包含其它对象使用的常量和方法的集合。当事件发生后，产生临时的Event对象实例，而且还附带当前事件的信息，如鼠标定位、事件类型等，然后将其它传递给相关的事件处理器进行处理。待事件处理完毕后，该临时对象实例所占据的内存空间被释放，浏览器等待其它事件的出现并进行处理。如果短时间内发生的事件较多，浏览器按事发生的顺序将这些事件排序，然后按排好的顺序依次执行。  

#### 8.4.1 常见的事件驱动
基于对象(object-based)有形界面下的特征是采用事件驱动(evnt-driven)。使得一切输入变简单化。通常鼠标或热键的动作称之为事件(Event)，则由鼠标或热键引发的一连串程序的动作，称之为事件驱动(Event Driver)。而对事件进行处理的程序或函数，称之为事件处理程序(Event Handler)。   
1.onClick  
2.onChange  
3.onSelect  
4.onFocus  
5.onBlur  失去焦点  
6.onLoad  
7.onUnload   
ch08\8.8.html  

#### 8.4.2 JavaScript的常用事件
1.鼠标事件  
1.1 onclick  
1.2 ondblclick  
1.3 onmouseover  
1.4 onmouseout  
1.5 onmousedown
1.6 onmouseup
1.7 onselect  

2.键盘事件  
2.1 onkeydown  
2.2 onkeypress  
2.3 onkeyup  

3.HTML事件  
指HTML文件状态改变时触发的、用户可以捕获的事件。  

4.变动事件  
由于光标位置的改变引起的状态改变。  
4.1 onblur  
4.2 onfocus  
4.3 onchange

#### 8.4.3 JavaScript处理事件的方式
1.匿名函数  
通过Function对象构造匿名函数  
ch08\8.9.html  
2.显式声明  
ch08\8.10.html  
3.手工触发  
通过其它元素的方法来触发一个事件而不用通过用户的动作来触发事件。  
ch08\8.11.html  

#### 8.4.4 使用Event对象
Event代表事件状态，如事件发生的元素，键盘状态，鼠标位置和鼠标按钮状态。一旦事件发生，就会生成Event对象。  
1.IE事件的引用   
event根目录于window.event  
2.Event对象的主要属性和方法  
2.1 type: 事件的类型 如 click  
2.2 srcElement 事件源  
2.3 button 按下的鼠标键，是一个整数，0 没有按钮 1鼠标左键 2鼠标右键 4 鼠标中间键 多个同时按下则相加，如 3代表左右键同时按下。   
2.4 clinetX/clientY: 事件发生时，鼠标的横、纵坐标，返回的是整数，它们的值相对于包容窗口的左上角生成。  
2.5 offsetX/offsetY: 鼠标指针相对源元素位置，可确定单击Image对象的哪个像素。  
2.6 altKey、ctrlKey、shiftKey: 布尔值，对应键是否按下  
2.7 keyCode: 返回keydown和keyup事件发生的时候，按键的代码以及keypress事件的Unicode字符。如event.keyCode=13代表按下Enter键。  
2.8  fromElement、toElement:前者是mouseover事件移动过的文档元素，后者是mouseout事件中鼠标移动到的文档元素。  
2.9 cancelBubble: 一个布尔属性，true将停止事件进一步上传到包容层次的元素，用于检测是否接受上层元素的事件控制。 true不被上层元素控制，false允许上层元素的事件控制。  
2.10  returnValue: 一个布尔属性，设置为false可以阻止浏览器执行默认的事件动作。相当于  
```
<a href="#" onclick="ProcessMethod(); return false;">
```
2.11 attachEvent()和detachEvent():为制定DOM对象事件类型注册多个事件处理函数的方法，它们有两个参数，第一个是事件类型，第二个是事件处理函数。在attachEvent()事件执行的时候，this关键字指向的是window对象，而不是发生事件的那个元素。  
