## 函数
####  定义函数
>如何定义一个函数呢？看看下面的格式：
```
    function  函数名( )
{
    函数体;
}
```

  function定义函数的关键字，“函数名”你为函数取的名字，“函数体”替换为完成特定功能的代码。
  我们完成对两个数求和并显示结果的功能。并给函数起个有意义的名字：“add2”，代码如下：
```html
<script type="text/javascript">
  function add2(){
    sum = 3 + 2;
    alert(sum);
  }
  ​add2();
</script>
```

#### 调用函数
函数调用
函数定义好后，是不能自动执行的，需要调用它,直接在需要的位置写函数名。
```html
<!--第一种情况:在<script>标签内调用。-->
  <script type="text/javascript">
    function add2()
    {
         sum = 1 + 1;
         alert(sum);
    }
  add2();//调用函数，直接写函数名。
</SCRIPT>

<!--第二种情况:在HTML文件中调用，如通过点击按钮后调用定义好的函数。-->

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
注意:鼠标事件会在后面讲解。

#### 有参数的函数
上节中add2()函数不能实现任意指定两数相加。其实，定义函数还可以如下格式：
```
function 函数名(参数1,参数2)
{
     函数代码
}
```
>注意:参数可以多个，根据需要增减参数个数。参数之间用(逗号，）隔开。
按照这个格式，函数实现任意两个数的和应该写成：
```
function add2(x,y)
{
   sum = x + y;
   document.write(sum);
}
```
x和y则是函数的两个参数，调用函数的时候，我们可通过这两个参数把两个实际的加数传递给函数了。
例如，add2(3，4)会求3+4的和，add2(60,20)则会求出60和20的和。

####返回值的函数
思考:上一节函数中，通过"document.write"把结果输出来，如果想对函数的结果进行处理怎么办呢？
我们只要把"document.write(sum)"这行改成如下代码：
```
function add2(x,y)
{
   sum = x + y;
   return sum; //返回函数值,return后面的值叫做返回值。
}
```
还可以通过变量存储调用函数的返回值，代码如下:
```
result = add2(3,4);//语句执行后,result变量中的值为7。
```
注意:函数中参数和返回值不只是数字，还可以是字符串等其它类型。 