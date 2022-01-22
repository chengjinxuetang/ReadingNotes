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
原型里添加了方法，为什么每一个对象实例有这个方法，第二个对象实例没有这个方法，所有对象的prototype不都指向同一个原型吗？  TODO:

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

