---
header-includes:
  - \hypersetup{colorlinks=false,
            allbordercolors={0 0 0},
            pdfborderstyle={/S/U/W 1}}

---

## *JavaScript Study Notes*

********************

### 2 JavaScript基础语法

+ 2-2 变量命名

  **变量名字可以任意取，**只不过取名字要遵循一些规则:

  1. 必须以字母、下划线或美元符号开头，后面可以跟字母、下划线、美元符号和数字。如下:

     ```javascript
     正确:           
         mysum            
         _mychar         
         $numa1          
     错误:
       6num  //开头不能用数字
       %sum //开头不能用除(_ $)外特殊符号,如(%  + /等)
       sum+num //开头中间不能使用除(_ $)外特殊符号，如(%  + /等)
     ```

  2. 变量名区分大小写，如:A与a是两个不同变量。

  3. 不允许使用JavaScript关键字和保留字做变量名。

     ![](http://img.mukewang.com/529c07c000014f5103080447.jpg)

+ 2-3 变量声明

  声明变量语法:

  ```javascript
  var 变量名;    
  ```

  var就相当于找盒子的动作，在JavaScript中是关键字（即保留字），这个关键字的作用是声明变量，并为"变量"准备位置(即内存）。

  ```javascript
  var mynum ; //声明一个变量mynum
  ```

  当然，我们可以一次找一个盒子，也可以一次找多个盒子，所以Var还可以一次声明多个变量，变量之间用","逗号隔开。

  ```javascript
  var num1,mun2 ; //声明两个变量num1和num2
  ```

  **注意:变量也可以不声明，直接使用，但为了规范，需要先声明，后使用。**

+ 2-4 变量赋值

  使用`"="`号给变量存储内容,看下面的语句:

  ```javascript
  var mynum = 5 ; //声明变量mynum并赋值。
  ```

  也可以这样写:

  ```javascript
  var mynum; //声明变量mynum
  mynum = 5 ; //给变量mynum赋值
  ```

  **注:这里 `"="`号的作用是给变量赋值，不是等于号。**

  变量是无所不能的容器，你可以把任何东西存储在变量里，如数值、字符串、布尔值等，例如：

  ```javascript
  var num1 = 123;       // 123是数值
  var num2 = "一二三";    //"一二三"是字符串
  var num3=true;    //布尔值true（真），false(假)
  ```

  其中，num1变量存储的内容是数值；num2变量存储的内容是字符串，字符串需要用一对引号`""`括起来，num3变量存储的内容是布尔值(true、false)。

+ 2-5 表达式

  表达式是指具有一定的值、用操作符把常数和变量连接起来的代数式。**一个表达式可以包含常数或变量。**

  我们先看看下面的JavaScript语句：

  ![](http://img.mukewang.com/52b9227d0001acc703000174.jpg)

  生活中“再见”表达方法很多，如:英语(goodbye）、网络语（88）、肢体语（挥挥手）等。在JavaScript表达式无处不在，所以一定要知道可以表达哪些内容，看看下面几种情况:

  ![](http://img.mukewang.com/529c21600001d02302800228.jpg)

  注意:串表达式中mychar是变量

   

  ![](http://img.mukewang.com/52b922a00001445b02920187.jpg)

  注意:数值表达式中num是变量

   

  ![](http://img.mukewang.com/529c218f000101d402980228.jpg)

  注意:布尔表达式中num是变量

+ 2-6 操作符

  操作符是用于在JavaScript中指定一定动作的符号。

  （1）操作符

  看下面这段JavaScript代码。

  ```javascript
  sum = numa + numb;
  ```

  其中的`"="`和`"+"`都是操作符。

  JavaScript中还有很多这样的操作符，例如，算术操作符(+、-、*、/等)，比较操作符(<、>、>=、<=等)，逻辑操作符(&&、||、！)。

  **注意: “=” 操作符是赋值，不是等于。**

  (2) `"+"`操作符

  算术运算符主要用来完成类似加减乘除的工作，在JavaScript中，“+”不只代表加法，还可以连接两个字符串，例如：

  ```javascript
  mystring = "Java" + "Script"; // mystring的值“JavaScript”这个字符串
  ```

+ 2-7 ++和--

  算术操作符除了(+、-、*、/)外，还有两个非常常用的操作符，自加一`“++”`；自减一`“--”`。首先来看一个例子：

  ```javascript
  mynum = 10;
  mynum++; //mynum的值变为11
  mynum--; //mynum的值又变回10
  ```

  上面的例子中，mynum++使mynum值在原基础上增加1，mynum--使mynum在原基础上减去1,其实也可以写成:

  ```javascript
  mynum = mynum + 1;//等同于mynum++
  mynum = mynum - 1;//等同于mynum--
  ```

+ 2-8 比较操作符

  在JavaScript中，这样的比较操作符有很多，这些操作符的含义如下: 

  ![](http://img.mukewang.com/532a3c150001c65802010207.jpg)

  看看下面例子:

  ```javascript
  var a = 5;//定义a变量，赋值为5
  var b = 9; //定义b变量，赋值为9
  document.write (a<b); //a小于b的值吗? 结果是真(true)
  document.write (a>=b); //a大于或等于b的值吗? 结果是假(false)
  document.write (a!=b); //a不等于b的值吗? 结果是真(true)
  document.write (a==b); //a等于b的值吗? 结果是假(false)
  ```

+ 2-9 逻辑操作符

  + `“&&”`是逻辑与操作符，只有“&&”两边值同时满足(同时为真)，整个表达式值才为真。
  + `"||"`逻辑或操作符，当两个条件中有任一个条件满足，“逻辑或”的运算结果就为“真”。
  + `"!"`是逻辑非操作符，也就是"不是"的意思,非真即假，非假即真。

+ 2-12 操作符优先级

  **操作符之间的优先级（高到低）:**

  算术操作符 → 比较操作符 → 逻辑操作符 → "="赋值符号

  如果同级的运算是按从左到右次序进行,多层括号由里向外。



### 3 数组

+ 3-1 数组

  数组是一个值的集合，每个值都有一个索引号，从0开始，每个索引都有一个相应的值，根据需要添加更多数值。

  ```html
  <script type="text/javascript">
   var myarr=new Array(); //定义数组
   myarr[0]=80; 
   myarr[1]=60;
   myarr[2]=99;
   document.write("第一个人的成绩是:"+myarr[0]);
   document.write("第二个人的成绩是:"+myarr[1]);
   document.write("第三个人的成绩是:"+myarr[2]);
  </script>
  ```

+ 3-2 创建数组

  使用数组之前首先要创建，而且需要把数组本身赋至一个变量。

  **创建数组语法：**

  ```javascript
  var myarray=new Array();
  ```

   ![](http://img.mukewang.com/52ca004b0001c81103980228.jpg)  

  我们创建数组的同时，还可以为数组指定长度，长度可任意指定。

  ```javascript
  var myarray= new Array(8); //创建数组，存储8个数据。 
  ```

  **注意：**

  1. 创建的新数组是空数组，没有值，如输出，则显示undefined。
  2. 虽然创建数组时，指定了长度，但实际上数组都是变长的，也就是说即使指定了长度为8，仍然可以将元素存储在规定长度以外。

+ 3-3 数组赋值

  + 第一种方法：

    ```javascript
    var myarray=new Array(); //创建一个新的空数组
    myarray[0]=66; //存储第1个人的成绩
    myarray[1]=80; //存储第2个人的成绩
    ```

  + 第二种方法：

    ```javascript
    var myarray = new Array(66,80,90,77,59);//创建数组同时赋值
    ```

  + 第三种方法：

    ```javascript
    var myarray = [66,80,90,77,59];//直接输入一个数组（称 “字面量数组”）
    ```

  **注意：**

  1. 数组存储的数据可以是任何类型（数字、字符、布尔值等）
  2. 数组每个值有一个索引号，从0开始。

+ 3-4 向数组增加一个新元素

  只需使用下一个未用的索引，任何时刻可以不断向数组增加新元素。

+ 3-5 使用数组元素

  要得到一个数组元素的值，只需引用数组变量并提供一个索引，如：
  **第一个人的成绩表示方法：**`myarray[0]`
  **第三个人的成绩表示方法:**  `myarray[2]`

+ 3-6 数组属性

  Length属性表示数组的长度，即数组中元素的个数。

  **语法：**

  ```javascript
  myarray.length; //获得数组myarray的长度
  ```

  **注意：**因为数组的索引总是由0开始，所以一个数组的上下限分别是：0和length-1。如数组的长度是5，数组的上下限分别是0和4。

  ```javascript
  var arr=[55,32,5,90,60,98,76,54];//包含8个数值的数组arr 
  document.write(arr.length); //显示数组长度8
  document.write(arr[7]); //显示第8个元素的值54
  ```

  同时，JavaScript数组的length属性是可变的，这一点需要特别注意。

  ```javascript
  arr.length=10; //增大数组的长度
  document.write(arr.length); //数组长度已经变为10
  ```

  数组随元素的增加，长度也会改变，如下:

  ```javascript
  var arr=[98,76,54,56,76]; // 包含5个数值的数组
  document.write(arr.length); //显示数组的长度5
  arr[15]=34;  //增加元素，使用索引为15,赋值为34
  alert(arr.length); //显示数组的长度16
  ```

+ 3-7 二维数组

  二维数组的表示:

  ```javascript
  myarray[ ][ ]
  ```

  **注意:** 二维数组的两个维度的索引值也是从0开始，两个维度的最后一个索引值为长度-1。 

  1. 二维数组的定义方法一

     ```javascript
     var myarr=new Array();  //先声明一维 
     for(var i=0;i<2;i++){   //一维长度为2
        myarr[i]=new Array();  //再声明二维 
        for(var j=0;j<3;j++){   //二维长度为3
        myarr[i][j]=i+j;   // 赋值，每个数组元素的值为i+j
        }
      }
     ```

  2. 二维数组的定义方法二

     ```javascript
     var Myarr = [[0 , 1 , 2 ],[1 , 2 , 3]]
     ```

  3. 赋值

     ```javascript
     myarr[0][1]=5; //将5的值传入到数组中，覆盖原有值。
     ```



### 4 流程控制语句

+ 4-1 if语句

  if语句是基于条件成立才执行相应代码时使用的语句。

  **语法**:

  ```javascript
  if(条件) { 
    条件成立时执行代码
  }
  ```

  **注意：if小写，大写字母（IF）会出错！**

+ 4-2 if...else语句

  if...else语句是在指定的条件成立时执行代码，在条件不成立时执行else后的代码。

  **语法**:

  ```javascript
  if(条件)
  { 条件成立时执行的代码}
  else
  {条件不成立时执行的代码}
  ```

+ 4-3 if...else嵌套语句

  要在多组语句中选择一组来执行，使用if..else嵌套语句。

  **语法**:

  ```javascript
  if(条件1)
  { 条件1成立时执行的代码}
  else  if(条件2)
  { 条件2成立时执行的代码}
  ...
  else  if(条件n)
  { 条件n成立时执行的代码}
  else
  { 条件1、2至n不成立时执行的代码}
  ```

+ 4-4 switch语句

  当有很多种选项的时候，switch比if else使用更方便。

  **语法:**

  ```javascript
  switch(表达式)
  {
  case值1:
    执行代码块 1
    break;
  case值2:
    执行代码块 2
    break;
  ...
  case值n:
    执行代码块 n
    break;
  default:
    与 case值1 、 case值2...case值n 不同时执行的代码
  }
  ```

  **语法说明:**

  Switch必须赋初始值，值与每个case值匹配。满足执行该 case 后的所有语句，并用break语句来阻止运行下一个case。如所有case值都不匹配，执行default后的语句。

  **注意：**记得在case所执行的语句后添加上一个break语句。否则就直接继续执行下面的case中的语句。

+ 4-5 for循环

  **for**语句结构：

  ```javascript
  for(初始化变量;循环条件;循环迭代)
  {     
      循环语句 
   }
  ```

+ 4-6 while循环

  **while**语句结构：

  ```javascript
  while(判断条件)
  {
      循环语句
   }
  ```

+ 4-7 do...while循环

  **while**语句结构：

  ```javascript
  while(判断条件)
  {
      循环语句
   }
  ```

+ 4-8 退出循环break

  在while、for、do...while、while循环中使用break语句退出当前循环，直接执行后面的代码。

  **格式如下：**

  ```javascript
  for(初始条件;判断条件;循环后条件值更新)
  {
    if(特殊情况)
    {break;}
    循环代码
  }
  ```

  当遇到特殊情况的时候，循环就会立即结束。

+ 4-9 继续循环continue

  continue的作用是仅仅跳过本次循环，而整个循环体继续执行。

  **语句结构：**

  ```javascript
  for(初始条件;判断条件;循环后条件值更新)
  {
    if(特殊情况)
    { continue; }
   循环代码
  }
  ```

  上面的循环中，当特殊情况发生的时候，本次循环将被跳过，而后续的循环则不会受到影响。



### 5 函数

+ 5-2 定义函数

  如何定义一个函数呢？看看下面的格式：

  ```javascript
  function  函数名( )
  {
       函数体;
  }
  ```

  function定义函数的关键字，“函数名”你为函数取的名字，“函数体”替换为完成特定功能的代码。

+ 5-3 函数调用

  函数定义好后，是不能自动执行的，需要调用它,直接在需要的位置写函数名。

  **第一种情况:在`<script>`标签内调用。**

  ```javascript
    <script type="text/javascript">
      function add2()
      {
           sum = 1 + 1;
           alert(sum);
      }
    add2();//调用函数，直接写函数名。
  </SCRIPT>
  ```

  **第二种情况:**在HTML文件中调用，如通过点击按钮后调用定义好的函数。

  ```javascript
  <html>
  <head>
  <script type="text/javascript">
     function add2()
     {
           sum = 5 + 6;
           alert(sum);
     }
  </script>
  </head>
  <body>
  <form>
  <input type="button" value="click it" onclick="add2()">  //按钮,onclick点击事件，直接写函数名
  </form>
  </body>
  </html>
  ```

+ 5-4 有参数的函数

  定义函数还可以如下格式：

  ```javascript
  function 函数名(参数1,参数2)
  {
       函数代码
  }
  ```

  **注意：**参数可以多个，根据需要增减参数个数。参数之间用(逗号，）隔开。

+ 5-5 返回值的函数

  **思考：**上一节函数中，通过"document.write"把结果输出来，如果想对函数的结果进行处理怎么办呢？

  我们只要把"document.write(sum)"这行改成如下代码：

  ```javascript
  function add2(x,y)
  {
     sum = x + y;
     return sum; //返回函数值,return后面的值叫做返回值。
  }
  ```

  还可以通过变量存储调用函数的返回值，代码如下:

  ```javascript
  result = add2(3,4);//语句执行后,result变量中的值为7。
  ```

  **注意：**函数中参数和返回值不只是数字，还可以是字符串等其它类型。



### 6 事件响应，让网页交互

+ 6-1 什么是事件？

  JavaScript 创建动态页面。事件是可以被 JavaScript 侦测到的行为。 网页中的每个元素都可以产生某些可以触发 JavaScript 函数或程序的事件。

  比如说，当用户单击按钮或者提交表单数据时，就发生一个鼠标单击（onclick）事件，需要浏览器做出处理，返回给用户一个结果。

  **主要事件表:**

  ![](http://img.mukewang.com/53e198540001b66404860353.jpg)

+ 6-2 鼠标单击事件 (onclick)

  onclick是鼠标单击事件，当在网页上单击鼠标时，就会发生该事件。同时onclick事件调用的程序块就会被执行，通常与按钮一起使用。

  比如，我们单击按钮时，触发 onclick 事件，并调用两个数和的函数add2()。代码如下：

  ```javascript
  <html>
  <head>
     <script type="text/javascript">
        function add2(){
          var numa,numb,sum;
          numa=6;
          numb=8;
          sum=numa+numb;
          document.write("两数和为:"+sum);  }
     </script>
  </head>
  <body>
     <form>
        <input name="button" type="button" value="点击提交" onclick="add2()" />
     </form>
  </body>
  </html>
  ```

  **注意:** 在网页中，如使用事件，就在该元素中设置事件属性。 

+ 6-3 鼠标经过事件 (onmouseover)

  鼠标经过事件，当鼠标移到一个对象上时，该对象就触发onmouseover事件，并执行onmouseover事件调用的程序。

  现实鼠标经过"确定"按钮时，触发onmouseover事件，调用函数info()，弹出消息框，代码如下:

  ```javascript
  <html>
  <head>
     <script type="text/javascript">
        function info(){
          comfirm("请输入姓名后，再单击确定！")
     		}
     </script>
  </head>
  <body>
     <form>
       密码：<input name="password" type="password">
        <input name="button" type="button" value="确定" onmouseover="info()" />
        <!--当鼠标经过“确定”按钮时，触发onmouseover="info()"-->
     </form>
  </body>
  </html>
  ```

  **运行结果:**

  ![](http://img.mukewang.com/53e196fd00017d8704870416.jpg)

+ 6-4 鼠标移开事件 (onmouseout)

  鼠标移开事件，当鼠标移开当前对象时，执行onmouseout调用的程序。

  当把鼠标移动到"登录"按钮上，然后再移开时，触发onmouseout事件，调用函数message()，代码如下:

  ```javascript
  <!DOCTYPE HTML>
  <html>
  <head>
  <meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
  <title>鼠标移开事件</title>
  <script type="text/javascript">
    function message(){
      alert("不要离开，只要输入密码，再单击登录，就ok了"); }
  </script>
  </head>
  <body>
  <form>
    密码：<input name="password" type="password">
    <input name="button" type="button" value="登录" onmouseover="message()" />
        <!--当移开“登录”按钮时，触发onmouseout="message()"-->
  </form>
  </body>
  </html>
  ```

  **运行结果:**

  ![](http://img.mukewang.com/53e195bf00010d1804760385.jpg)

+ 6-5 光标聚焦事件 (onfocus)

  当网页中的对象获得聚点时，执行onfocus调用的程序就会被执行。

  如下代码, 当将光标移到文本框内时，即焦点在文本框内，触发onfocus 事件，并调用函数message()。

  ```javascript
  <!DOCTYPE HTML>
  <html>
  <head>
  <meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
  <title>光标聚焦事件</title>
  <script type="text/javascript">
    function message(){
      alert("请在此输入姓名！"); }
  </script>
  </head>
  <body>
  <form>
    姓名：<input name="username" type="text" value="请输入姓名！" onfocus="message()">
    <!--当光标在文本框内（即文本框得到焦点）时，调用"message()"函数-->
  </form>
  </body>
  </html>
  ```

  **运行结果：**

  ![](http://img.mukewang.com/5312c5660001821a04300326.jpg)

+ 6-6 光标失焦事件 (onblur)

  onblur事件与onfocus是相对事件，当光标离开当前获得聚焦对象的时候，触发onblur事件，同时执行被调用的程序。

  如下代码, 网页中有用户和密码两个文本框。当前光标在用户文本框内时（即焦点在文本框），在光标离开该文本框后（即失焦时），触发onblur事件，并调用函数message()。

  ```javascript
  <!DOCTYPE HTML>
  <html>
  <head>
  <meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
  <title>光标失焦事件</title>
  <script type="text/javascript">
    function message(){
      alert("请确认已输入用户名后，再离开！"); }
  </script>
  </head>
  <body>
  <form>
    用户：<input name="username" type="text" value="请输入用户名！" onblur="message()">
    密码：<input name="password" type="text" value="请输入密码！">
  </form>
  </body>
  </html>
  ```

  **运行结果：**

  ![](http://img.mukewang.com/5312da710001968704410319.jpg)

+ 6-7 内容选中事件 (onselect)

  选中事件，当文本框或者文本域中的文字被选中时，触发onselect事件，同时调用的程序就会被执行。

  如下代码,当选中用户文本框内的文字时，触发onselect 事件，并调用函数message()。

  ```javascript
  <!DOCTYPE HTML>
  <html>
  <head>
  <meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
  <title>onselect</title>
  <script type="text/javascript">
    function message(){
      alert("你触发了选中事件！"); }
  </script>
  </head>
  <body>
  <form>
    用户：<input name="username" type="text" value="请输入用户名！" onselect="message()">
    <!--当选中用户文本框内的文字时，触发onselect事件-->
  </form>
  </body>
  </html>
  ```

  **运行结果：**

  ![img](http://img.mukewang.com/5312d7ba00013fff03950319.jpg)

+ 6-8 文本框内容改变事件 (onchange)

  通过改变文本框的内容来触发onchange事件，同时执行被调用的程序。

  如下代码,当用户将文本框内的文字改变后，弹出对话框“您改变了文本内容！”。

  ```javascript
  <!DOCTYPE HTML>
  <html>
  <head>
  <meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
  <title>onchange</title>
  <script type="text/javascript">
    function message(){
      alert("你改变了文本内容！"); }
  </script>
  </head>
  <body>
  <form>
    用户：<input name="username" type="text" value="请输入用户名！" onchange="message()">
    <!--当改变用户文本框内的文字时，触发onchange事件-->
  </form>
  </body>
  </html>
  ```

  **运行结果：**

  ![](http://img.mukewang.com/5312d5c600012c3703960319.jpg)

+ 6-9 加载事件 (onload)

  事件会在页面加载完成后，立即发生，同时执行被调用的程序。
  注意：

  1. 加载页面时，触发onload事件，事件写在<body>标签内。

  2. 此节的加载页面，可理解为打开一个新页面时。
     如下代码,当加载一个新页面时，弹出对话框“加载中，请稍等…”。

  ```javascript
  <!DOCTYPE HTML>
  <html>
  <head>
  <meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
  <title>onload</title>
  <script type="text/javascript">
    function message(){
      alert("加载中，请稍等..."); }
  </script>
  </head>
  <body onchange="message()">
  欢迎学习JavaScript。
  </body>
  </html>
  ```

  **运行结果：**

  ![img](http://img.mukewang.com/5312e3eb0001e8a103930318.jpg)

+ 6-10 卸载事件 (onunload)

  当用户退出页面时（页面关闭、页面刷新等），触发onUnload事件，同时执行被调用的程序。

  **注意：不同浏览器对onunload事件支持不同。**

  如下代码,当退出页面时，弹出对话框“您确定离开该网页吗？”。

  ```javascript
  <!DOCTYPE HTML>
  <html>
  <head>
  <meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
  <title>onload</title>
  <script type="text/javascript">
    window.onunload=onunload_message;
    function onunload_message(){
      alert("你确定离开该网页吗？"); }
  </script>
  </head>
  <body>
  欢迎学习JavaScript。
  </body>
  </html>
  ```

  **运行结果：（IE浏览器）**

  ![](http://img.mukewang.com/546470c90001583205460464.jpg)

+ 6-11 编程练习

  使用JS完成一个简单的计算器功能。实现2个输入框中输入整数后，点击第三个输入框能给出2个整数的加减乘除。

  提示：获取元素的值设置和获取方法为：例：赋值：document.getElementById(“id”）.value = 1； 取值：var = document.getElementById(“id”）.value；

  **注意:** 使用parseInt()函数可解析一个字符串,并返回一个整数。

  ```javascript
  <!DOCTYPE html>
  <html>
   <head>
    <title> 事件</title>  
    <script type="text/javascript">
     function count(){
         
      //获取第一个输入框的值
      var num1 = document.getElementById("txt1").value;
  	//获取第二个输入框的值
  	var num2 = document.getElementById("txt2").value;
  	//获取选择框的值
  	var op = document.getElementById("select").value;
  	
  	var res;
  	
  	//获取通过下拉框来选择的值来改变加减乘除的运算法则
  	switch(op) {
  	    case "+":
  	        res = parseInt(num1) + parseInt(num2);  // 不然会是两个String的整合，e.g. 4 + 5 = 45
  	        break;
  	    case "-":
  	        res = num1 - num2;
  	        break;
          case "*":
  	        res = num1 * num2;
  	        break;
  	    case "/":
  	        res = num1 / num2;
  	}
      //设置结果输入框的值 
      document.getElementById("fruit").value = res;
      
     }
    </script> 
   </head> 
   <body>
     <input type='text' id='txt1' /> 
     <select id='select'>
  		<option value='+'>+</option>
  		<option value="-">-</option>
  		<option value="*">*</option>
  		<option value="/">/</option>
     </select>
     <input type='text' id='txt2' /> 
     <input type='button' value=' = ' onclick="count()"/> <!--通过 = 按钮来调用创建的函数，得到结果--> 
     <input type='text' id='fruit' />   
   </body>
  </html>
  ```



### 7 JavaScript内置对象

+ 7-1 什么是对象

  JavaScript 中的所有事物都是对象，如:字符串、数值、数组、函数等，每个对象带有**属性**和**方法**。

  **对象的属性：**反映该对象某些特定的性质的，如：字符串的长度、图像的长宽等；

  **对象的方法：**能够在对象上执行的动作。例如，表单的“提交”(Submit)，时间的“获取”(getYear)等；

  JavaScript 提供多个内建对象，比如 String、Date、Array 等等，使用对象前先定义，如下使用数组对象：

  ```javascript
    var objectName =new Array();//使用new关键字定义对象
  或者
    var objectName =[];
  ```

  **访问对象属性的语法:**

  ```javascript
  objectName.propertyName
  ```

  如使用 Array 对象的 length 属性来获得数组的长度：

  ```javascript
  var myarray=new Array(6);//定义数组对象
  var myl=myarray.length;//访问数组长度length属性
  ```

  **以上代码执行后，myl的值将是：6**

  **访问对象的方法：**

  ```javascript
  objectName.methodName()
  ```

  如使用string 对象的 toUpperCase() 方法来将文本转换为大写：

  ```javascript
  var mystr="Hello world!";//创建一个字符串
  var request=mystr.toUpperCase(); //使用字符串对象方法
  ```

  以上代码执行后，request的值是**：HELLO WORLD!**

+ 7-2 Date 日期对象

  日期对象可以储存任意一个日期，并且可以精确到毫秒数（1/1000 秒）。

  定义一个时间对象 :

  ```
  var Udate=new Date(); 
  ```

  **注意：**使用关键字new，Date()的首字母必须大写。 

  使 Udate 成为日期对象，并且已有初始值：**当前时间(当前电脑系统时间)**。

  如果要自定义初始值，可以用以下方法：

  ```
  var d = new Date(2012, 10, 1);  //2012年10月1日
  var d = new Date('Oct 1, 2012'); //2012年10月1日
  ```

  我们最好使用下面介绍的“方法”来严格定义时间。

  **访问方法语法：**“<日期对象>.<方法>”

  Date对象中处理时间和日期的常用方法：

  ![](http://img.mukewang.com/555c650d0001ae7b04180297.jpg)

  + 返回/设置年份方法

    **`get/setFullYear() `**返回/设置年份，用四位数表示。

    ```javascript
    var mydate=new Date();//当前时间2014年3月6日
    document.write(mydate+"<br>");//输出当前时间
    document.write(mydate.getFullYear()+"<br>");//输出当前年份
    mydate.setFullYear(81); //设置年份
    document.write(mydate+"<br>"); //输出年份被设定为 0081年。
    ```

    **注意:**不同浏览器， mydate.setFullYear(81)结果不同，年份被设定为 0081或81两种情况。

    **结果:**

    ```javascript
    Thu Mar 06 2014 10:57:47 GMT+0800
    2014
    Thu Mar 06 0081 10:57:47 GMT+0800
    ```

    **注意:**

    1. 结果格式依次为：星期、月、日、年、时、分、秒、时区。(火狐浏览器)

    2. 不同浏览器，时间格式有差异。

  + 返回星期方法

    **getDay()** 返回星期，返回的是0-6的数字，0 表示星期天。如果要返回相对应“星期”，通过数组完成，代码如下:

    ```html
    <script type="text/javascript">
      var mydate=new Date();//定义日期对象
      var weekday=["星期日","星期一","星期二","星期三","星期四","星期五","星期六"];
    //定义数组对象,给每个数组项赋值
      var mynum=mydate.getDay();//返回值存储在变量mynum中
      document.write(mydate.getDay());//输出getDay()获取值
      document.write("今天是："+ weekday[mynum]);//输出星期几
    </script>
    ```

    注意：以上代码是在2014年3月7日，星期五运行。

    **结果:**

    ```javascript
    5
    今天是：星期五
    ```

  + 返回/设置时间方法

    **get/setTime()** 返回/设置时间，单位毫秒数，计算从 1970 年 1 月 1 日零时到日期对象所指的日期的毫秒数。

    如果将目前日期对象的时间推迟1小时，代码如下:

    ```html
    <script type="text/javascript">
      var mydate=new Date();
      document.write("当前时间："+mydate+"<br>");
      mydate.setTime(mydate.getTime() + 60 * 60 * 1000);
      document.write("推迟一小时时间：" + mydate);
    </script>
    ```

    **结果:**

    ```javascript
    当前时间：Thu Mar 6 11:46:27 UTC+0800 2014
    推迟一小时时间：Thu Mar 6 12:46:27 UTC+0800 2014
    ```

    **注意:**

    1. 一小时 60 分，一分 60 秒，一秒 1000 毫秒

    2. 时间推迟 1 小时,就是: “x.setTime(x.getTime() + 60 * 60 * 1000);”

+ 7-6 String 字符串对象

  定义字符串的方法就是直接赋值。比如：

  ```javascript
  var mystr = "I love JavaScript!"
  ```

  定义mystr字符串后，我们就可以访问它的属性和方法。

  **访问字符串对象的属性length:**

  stringObject.length; 返回该字符串的长度。

  ```javascript
  var mystr="Hello World!";
  var myl=mystr.length;
  ```

  以上代码执行后，myl 的值将是：12

  **访问字符串对象的方法：**

  使用 String 对象的 toUpperCase() 方法来将字符串小写字母转换为大写：

  ```javascript
  var mystr="Hello world!";
  var mynum=mystr.toUpperCase();
  ```

  以上代码执行后，mynum 的值是：HELLO WORLD!

  + 返回指定位置的字符

    charAt() 方法可返回指定位置的字符。返回的字符是长度为 1 的字符串。

    **语法:**

    ```javascript
    stringObject.charAt(index)
    ```

    **参数说明：**

    ![](http://img.mukewang.com/53251a310001cf1e03370092.jpg)

    **注意**：

    1. 字符串中第一个字符的下标是 0。最后一个字符的下标为字符串长度减一（string.length-1）。

    2. 如果参数 index 不在 0 与 string.length-1 之间，该方法将返回一个空字符串。

    **如:**在字符串 "I love JavaScript!" 中，返回位置2的字符：

    ```html
    <script type="text/javascript">
      var mystr="I love JavaScript!"
      document.write(mystr.charAt(2));
    </script>
    ```

    **注意：**一个空格也算一个字符。

    以上代码的运行结果：

    ```javascript
    l
    ```

  + 返回指定的字符串首次出现的位置

    indexOf() 方法可返回某个指定的字符串值在字符串中首次出现的位置。

    **语法**

    ```javascript
    stringObject.indexOf(substring, startpos)
    ```

    **参数说明：**

    ![](http://img.mukewang.com/53853d4200019feb04920149.jpg)
    **说明：**

    1. 该方法将从头到尾地检索字符串 stringObject，看它是否含有子串 substring。

    2. 可选参数，从stringObject的startpos位置开始查找substring，如果没有此参数将从stringObject的开始位置查找。

    3. 如果找到一个 substring，则返回 substring 的第一次出现的位置。stringObject 中的字符位置是从 0 开始的。

    **注意：**

    1. indexOf() 方法区分大小写。

    2. 如果要检索的字符串值没有出现，则该方法返回 -1。

    例如: 对 "I love JavaScript!" 字符串内进行不同的检索：

    ```html
    <script type="text/javascript">
      var str="I love JavaScript!"
      document.write(str.indexOf("I") + "<br />");
      document.write(str.indexOf("v") + "<br />");
      document.write(str.indexOf("v",8));
    </script>
    ```

    以上代码的输出：

    ```javascript
    0
    4
    9
    ```

  + 字符串分割 split()

    split() 方法将字符串分割为字符串数组，并返回此数组。

    **语法：**

    ```javascript
    stringObject.split(separator,limit)
    ```

    **参数说明:**

    ![](http://img.mukewang.com/532bee4800014c0404230108.jpg)

    **注意：**如果把空字符串 ("") 用作 separator，那么 stringObject 中的每个字符之间都会被分割。

    **我们将按照不同的方式来分割字符串：**

    使用指定符号分割字符串，代码如下:

    ```javascript
    var mystr = "www.imooc.com";
    document.write(mystr.split(".")+"<br>");
    document.write(mystr.split(".", 2)+"<br>");
    ```

    **运行结果:**

    ```javascript
    www,imooc,com
    www,imooc
    ```

    将字符串分割为字符，代码如下：

    ```javascript
    document.write(mystr.split("")+"<br>");
    document.write(mystr.split("", 5));
    ```

    运行结果:

    ```javascript
    w,w,w,.,i,m,o,o,c,.,c,o,m
    w,w,w,.,i
    ```

  + 提取字符串 substring()

    substring() 方法用于提取字符串中介于两个指定下标之间的字符。

    **语法:**

    ```javascript
    stringObject.substring(startPos,stopPos) 
    ```

    **参数说明:**

    ![](http://img.mukewang.com/532bf1bb000151af04450082.jpg)

    **注意：**

    1. 返回的内容是从 start开始(包含start位置的字符)到 stop-1 处的所有字符，其长度为 stop 减start。

    2. 如果参数 start 与 stop 相等，那么该方法返回的就是一个空串（即长度为 0 的字符串）。

    3. 如果 start 比 stop 大，那么该方法在提取子串之前会先交换这两个参数。

    使用 substring() 从字符串中提取字符串，代码如下：

    ```html
    <script type="text/javascript">
      var mystr="I love JavaScript";
      document.write(mystr.substring(7));
      document.write(mystr.substring(2,6));
    </script>
    ```

    **运行结果**:

    ```javascript
    JavaScript
    love
    ```

  + 提取指定数目的字符 substr()

    substr() 方法从字符串中提取从 startPos位置开始的指定数目的字符串。

    **语法:**

    ```javascript
    stringObject.substr(startPos,length)
    ```

    **参数说明:**

    ![](http://img.mukewang.com/532bf2e00001105305100098.jpg)

    **注意：**

    1. 如果参数startPos是负数，从字符串的尾部开始算起的位置。也就是说，-1 指字符串中最后一个字符，-2 指倒数第二个字符，以此类推。

    2. 如果startPos为负数且绝对值大于字符串长度，startPos为0。

    使用 substr() 从字符串中提取一些字符，代码如下：

    ```html
    <script type="text/javascript">
      var mystr="I love JavaScript!";
      document.write(mystr.substr(7));
      document.write(mystr.substr(2,4));
    </script>
    ```

    **运行结果：**

    ```javascript
    JavaScript!
    love
    ```

+ 7-12 Math对象

  Math对象，提供对数据的数学计算。

  使用 Math 的属性和方法，代码如下：

  ```html
  <script type="text/javascript">
    var mypi=Math.PI; 
    var myabs=Math.abs(-15);
    document.write(mypi);
    document.write(myabs);
  </script>
  ```

  **运行结果**:

  ```javascript
  3.141592653589793
  15
  ```

  **注意：**Math 对象是一个固有的对象，无需创建它，直接把 Math 作为对象使用就可以调用其所有属性和方法。这是它与Date,String对象的区别。

  Math 对象属性

  ![](http://img.mukewang.com/532fe7cf0001e7b505170269.jpg)

  Math 对象方法

  ![](http://img.mukewang.com/532fe841000174db05160622.jpg)

  + 向上取整 ceil()

    ceil() 方法可对一个数进行向上取整。

    **语法:**

    ```javascript
    Math.ceil(x)
    ```

    **参数说明:**

    ![](http://img.mukewang.com/532fe8e00001e4e605230063.jpg)

    **注意：**它返回的是大于或等于x，并且与x最接近的整数。

    我们将把 ceil() 方法运用到不同的数字上，代码如下：

    ```html
    <script type="text/javascript">
      document.write(Math.ceil(0.8) + "<br />")
      document.write(Math.ceil(6.3) + "<br />")
      document.write(Math.ceil(5) + "<br />")
      document.write(Math.ceil(3.5) + "<br />")
      document.write(Math.ceil(-5.1) + "<br />")
      document.write(Math.ceil(-5.9))
    </script>
    ```

    **运行结果：**

    ```javascript
    1
    7
    5
    4
    -5
    -5
    ```

  + 向下取整 floor()

    floor() 方法可对一个数进行向下取整。

    **语法:**

    ```javascript
    Math.floor(x)
    ```

    **参数说明：**

    ![](http://img.mukewang.com/532fe8e00001e4e605230063.jpg)

    **注意：**返回的是小于或等于x，并且与 x 最接近的整数。

    我们将在不同的数字上使用 floor() 方法，代码如下:

    ```html
    <script type="text/javascript">
      document.write(Math.floor(0.8)+ "<br>")
      document.write(Math.floor(6.3)+ "<br>")
      document.write(Math.floor(5)+ "<br>")
      document.write(Math.floor(3.5)+ "<br>")
      document.write(Math.floor(-5.1)+ "<br>")
      document.write(Math.floor(-5.9))
    </script>
    ```

    **运行结果：**

    ```javascript
    0
    6
    5
    3
    -6
    -6
    ```

  + 四舍五入 round()

    round() 方法可把一个数字四舍五入为最接近的整数。

    **语法:**

    ```javascript
    Math.round(x)
    ```

    **参数说明：**

    ![](http://img.mukewang.com/532feb70000180ab03210059.jpg)

    **注意：**

    1. 返回与 x 最接近的整数。

    2. 对于 0.5，该方法将进行上舍入。(5.5 将舍入为 6)

    3. 如果 x 与两侧整数同等接近，则结果接近 +∞方向的数字值 。(如 -5.5 将舍入为 -5; -5.52 将舍入为 -6),如下图:

    ![](http://img.mukewang.com/53fc4cc8000169a907530196.jpg)

    把不同的数舍入为最接近的整数,代码如下：

    ```html
    <script type="text/javascript">
      document.write(Math.round(1.6)+ "<br>");
      document.write(Math.round(2.5)+ "<br>");
      document.write(Math.round(0.49)+ "<br>");
      document.write(Math.round(-6.4)+ "<br>");
      document.write(Math.round(-6.6));
    </script>
    ```

    **运行结果：**

    ```javascript
    2
    3
    0
    -6
    -7
    ```

  + 随机数 random()

    random() 方法可返回介于 0 ~ 1（大于或等于 0 但小于 1 )之间的一个随机数。

    **语法：**

    ```javascript
    Math.random();
    ```

    **注意：**返回一个大于或等于 0 但小于 1 的符号为正的数字值。

    我们取得介于 0 到 1 之间的一个随机数，代码如下：

    ```html
    <script type="text/javascript">
      document.write(Math.random());
    </script>
    ```

    **运行结果：**

    ```javascript
    0.190305486195328  
    ```

    **注意**:因为是随机数，所以每次运行结果不一样，但是0 ~ 1的数值。

    获得0 ~ 10之间的随机数，代码如下:

    ```html
    <script type="text/javascript">
      document.write((Math.random())*10);
    </script>
    ```

    **运行结果：**

    ```javascript
    8.72153625893887
    ```

+ 7-17 Array 数组对象

  **数组属性：**

  length 用法：<数组对象>.length；返回：数组的长度，即数组里有多少个元素。它等于数组里最后一个元素的下标加一。

  **数组方法：**

  ![](http://img.mukewang.com/533295ab0001dead05190599.jpg)

  + 数组连接 concat()

    concat() 方法用于连接两个或多个数组。此方法返回一个新数组，不改变原来的数组。

    **语法**

    ```javascript
    arrayObject.concat(array1,array2,...,arrayN)
    ```

    **参数说明：**

    ![](http://img.mukewang.com/5332968d0001d39b05010137.jpg)

    **注意:** 该方法不会改变现有的数组，而仅仅会返回被连接数组的一个副本。

    我们创建一个数组，将把 concat() 中的参数连接到数组 myarr 中，代码如下：

    ```html
    <script type="text/javascript">
      var mya = new Array(3);
      mya[0] = "1";
      mya[1] = "2";
      mya[2] = "3";
      document.write(mya.concat(4,5)+"<br>");
      document.write(mya); 
    </script>
    ```

    **运行结果：**

    ```javascript
    1,2,3,4,5
    1,2,3
    ```

    我们创建了三个数组，然后使用 concat() 把它们连接起来，代码如下：

    ```html
    <script type="text/javascript">
      var mya1= new Array("hello!")
      var mya2= new Array("I","love");
      var mya3= new Array("JavaScript","!");
      var mya4=mya1.concat(mya2,mya3);
      document.write(mya4);
    </script>
    ```

    **运行结果：**

    ```javascript
    hello!,I,love,JavaScript,!
    ```

  + 指定分隔符连接数组元素 join()

    join()方法用于把数组中的所有元素放入一个字符串。元素是通过指定的分隔符进行分隔的。

    **语法：**

    ```javascript
    arrayObject.join(分隔符)
    ```

    **参数说明:**

    ![](http://img.mukewang.com/533297ff0001516905150059.jpg)

    注意：返回一个字符串，该字符串把数组中的各个元素串起来，用<分隔符>置于元素与元素之间。这个方法不影响数组原本的内容。 我们使用join（）方法，将数组的所有元素放入一个字符串中，代码如下：

    ```html
    <script type="text/javascript">
      var myarr = new Array(3);
      myarr[0] = "I";
      myarr[1] = "love";
      myarr[2] = "JavaScript";
      document.write(myarr.join());
    </script>
    ```

    **运行结果：**

    ```javascript
    I,love,JavaScript
    ```

    我们将使用分隔符来分隔数组中的元素，代码如下：

    ```html
    <script type="text/javascript">
      var myarr = new Array(3)
      myarr[0] = "I";
      myarr[1] = "love";
      myarr[2] = "JavaScript";
      document.write(myarr.join("."));
    </script>
    ```

    **运行结果：**

    ```javascript
    I.love.JavaScript
    ```

  + 颠倒数组元素顺序 reverse()

    reverse() 方法用于颠倒数组中元素的顺序。

    **语法：**

    ```javascript
    arrayObject.reverse()
    ```

    **注意：**该方法会改变原来的数组，而不会创建新的数组。

    定义数组myarr并赋值，然后颠倒其元素的顺序：

    ```html
    <script type="text/javascript">
      var myarr = new Array(3)
      myarr[0] = "1"
      myarr[1] = "2"
      myarr[2] = "3"
      document.write(myarr + "<br />")
      document.write(myarr.reverse())
    </script>
    ```

    **运行结果：**

    ```javascript
    1,2,3
    3,2,1
    ```

  + 选定元素 slice()

    slice() 方法可从已有的数组中返回选定的元素。

    **语法**

    ```javascript
    arrayObject.slice(start,end)
    ```

    **参数说明：**

    ![](http://img.mukewang.com/533299680001637b05160145.jpg)

    1. 返回一个新的数组，包含从 start 到 end （不包括该元素）的 arrayObject 中的元素。

    2. 该方法并不会修改数组，而是返回一个子数组。

    **注意：**

    1. 可使用负值从数组的尾部选取元素。

    2. 如果 end 未被规定，那么 slice() 方法会选取从 start 到数组结尾的所有元素。

    3. String.slice() 与 Array.slice() 相似。

    我们将创建一个新数组，然后从其中选取的元素，代码如下：

    ```html
    <script type="text/javascript">
      var myarr = new Array(1,2,3,4,5,6);
      document.write(myarr + "<br>");
      document.write(myarr.slice(2,4) + "<br>");
      document.write(myarr);
    </script>
    ```

    **运行结果：**

    ```javascript
    1,2,3,4,5,6
    3,4
    1,2,3,4,5,6
    ```

  + 数组排序 sort()

    **sort()**方法使数组中的元素按照一定的顺序排列。

    **语法:**

    ```javascript
    arrayObject.sort(方法函数)
    ```

    **参数说明：**

    ![](http://img.mukewang.com/53329a2a000127f705170060.jpg)

    1. 如果不指定<方法函数>，则按unicode码顺序排列。

    2. 如果指定<方法函数>，则按<方法函数>所指定的排序方法排序。

    ```javascript
    myArray.sort(sortMethod);
    ```

    **注意:** 该函数要比较两个值，然后返回一个用于说明这两个值的相对顺序的数字。比较函数应该具有两个参数 a 和 b，其返回值如下： 

     若返回值<=-1，则表示 A 在排序后的序列中出现在 B 之前。
     若返回值>-1 && <1，则表示 A 和 B 具有相同的排序顺序。
     若返回值>=1，则表示 A 在排序后的序列中出现在 B 之后。

    1. 使用sort()将数组进行排序，代码如下：

       ```javascript
       <script type="text/javascript">
         var myarr1 = new Array("Hello","John","love","JavaScript"); 
         var myarr2 = new Array("80","16","50","6","100","1");
         document.write(myarr1.sort()+"<br>");
         document.write(myarr2.sort());
       </script>
       ```

       **运行结果：**

       ```javascript
       Hello,JavaScript,John,love
       1,100,16,50,6,80
       ```

       **注意:上面的代码没有按照数值的大小对数字进行排序。**

    2. 如要实现这一点，就必须使用一个排序函数，代码如下：

       ```javascript
       <script type="text/javascript">
         function sortNum(a,b) {
         return a - b;
        //升序，如降序，把“a - b”该成“b - a”
       }
        var myarr = new Array("80","16","50","6","100","1");
         document.write(myarr + "<br>");
         document.write(myarr.sort(sortNum));
       </script>
       ```

       **运行结果：**

       ```javascript
       80,16,50,6,100,1
       1,6,16,50,80,100
       ```

       **注意：**sort(sortNum)中的sortNum是不带括号的。带括号的是把返回值赋值给事件，不带括号的是把函数体所在地址位置赋值给事件。再看myarr.sort(sortNum)：它的语法定义：arrayObject.sort(方法函数)，里面必须是一个函数，而不是一个返回值或者别的。



### 8 浏览器对象

### 9 DOM对象，控制HTML元素

### 10 编程挑战

