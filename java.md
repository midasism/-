#                                               《Java核心技术 卷1》笔记
[TOC]

## API文档

### 1.java . lang . string 1.0

![](https://img-blog.csdnimg.cn/2019050100400048.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzU0OTE0OA==,size_16,color_FFFFFF,t_70)
![](https://img-blog.csdnimg.cn/20190501004152821.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzU0OTE0OA==,size_16,color_FFFFFF,t_70)
![](https://img-blog.csdnimg.cn/20190501004241516.png)

### 2.java.lang.StringBuilder 5.0

[回转到3.6.9](#3.6.9 构建字符串（StringBuilder）)
![1556702449884](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1556702449884.png)



### 3.java.util.Scanner 5.0 

  [回转到3.7.1](#3.7.1 读取输入)
![](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1556704389521.png)
![1556720702077](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1556720702077.png)



### 4.java.Iang.System 1.0 

![](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1556704463094.png)



### 5.java.io.Console 6 

![](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1556704502915.png)

### 6.java.io.PrintWriter 1.1 

![1556720755830](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1556720755830.png)



### 7. java.nio.file.Paths 7 

![1556720794529](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1556720794529.png)



### 8. java.math.BigInteger 1.1

[回转](# 3.9 大数值)
![1556901614870](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1556901614870.png)
![1556901635256](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1556901635256.png)



### 9.java.math.BigDecimal 1.1

![1556902096371](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1556902096371.png)



### 第三章：Java的基本程序设计结构

## 3.1

1. public 访问修饰符：用于控制程序的其他部分对这段代码的访问级别
2. 类名规则：必须以字母开头，后面可以是字母和数字的任意组合；长度基本上没有限制；不能使用java保留字
3. 类命名规范：大写字母开头。若由多个单词组成，则每个单词首字母需要大写（驼峰命名法）
4. 源代码的文件名必须与公共类的名字相同
5. 如果main方法正常退出，那么退出代码为0。如果需要在程序终止时返回其它的代码，可以调用System.exit
6. System.out.println( )：打印信息，并换行 System.out.print( )：打印信息，不换行

## 3.2 注释

1. / /
2. /* */：长篇注释
3. /** */：文档注释，可自动生成文档

## 3.3 数据类型

### 3.3.1 整型

Java整型

| 类型    | 储存要求 | 取值范围                                                 |
| ----- | ---- | ---------------------------------------------------- |
| byte  | 1字节  | -128~127                                             |
| short | 2字节  | -32768~32767                                         |
| int   | 4字节  | -2147483648~2147483647                               |
| long  | 8字节  | -9 223 372 036 854 775 808~9 223 372 036 854 775 807 |

1. Java的整型范围固定不变，与运行的机器无关
2. byte和short类型主要用于特定场合，例如底层的文件处理或者需要控制储存空间的大数组
3. 长整型long有后缀 L 或 l
4. 十六进制：前缀0x或0X 八进制：前缀0 二进制：0b或0B（例如0b1001=9）
5. 可以为数字字面量加下划线(如1_000_000)，编译器会去除下划线

### 3.3.2 浮点型

                                    **浮点类型**

| 类型     | 储存要求 | 取值范围                                       |
| ------ | ---- | ------------------------------------------ |
| float  | 4字节  | 大约+-3.402 823 47E+38F(有效位数：6~7）            |
| double | 8字节  | 大约+-1.797 693 134 862 315 70E+308(有效位数：15） |

1. float后缀：F/f
2. double后缀可加可不加：D/d
3. 正无穷大：常量Double.POSITIVE_INFINITY
4. 负无穷大：常量Double.NEGATIVE_INFINITY
5. NaN：Double.NaN 注：若检查特定值是否等于Double.NaN, 用 Double.isNaN 方法
6. 浮点运算会出现舍入误差，例如2.0-1.1=0.8999999999，而不是0.9

### 3.3.3 char类型

                                     **特殊字符的转义序列**

| 转义序列 | 名称  | Unicode值 |
| ---- | --- | -------- |
| \b   | 退格  | \u0008   |
| \t   | 制表  | \u0009   |
| \n   | 换行  | \u000a   |
| \r   | 回车  | \u0009   |
| \"   | 双引号 | \u0022   |
| \'   | 单引号 | \u0027   |
| \\\  | 反斜杠 | \u005c   |

char类型的字面值用单引号括起来

### 3.3.4 Unicode和char类型

1. 码点：与一个编码表中的某个字符对应的代码值
2. 在Unicode中，码点用十六进制，加上前缀U+
3. 码点可分成17个代码级别
4. 第一个级别成为基本的多语言级别，U+10000到U+10FFFF
5. 基本的多语言级别：每个字符16位，称为代码单元
6. 辅助字符：采用一对连续的代码单元
7. 建议不在程序中使用char类型

### 3.3.5 boolean类型

1. 两个值：false true
2. 整型和布尔值不能相互转化

## 3.4 变量

1. 检查哪些Unicode字符属于Java中的“字母”：用Character类的 isJavaIdentifierStart 和 isJavaIdentifierPart 方法
2. $ 是合法的Java字符，但不要在代码中使用

### 3.4.1 变量初始化

1. 变量使用前必须初始化
2. 变量的声明尽可能地靠近第一次使用的地方（良好的程序编写风格）

### 3.4.2 常量

1. 用关键字 final 指示常量
2. 习惯上常量使用大写
3. 类常量：希望某个常量可以在一个类的多个方法中使用，使用关键字 static final
4. 常变量定义位于main方法的外部

## 3.5 运算符

## 使用strictfp 关键字标记的方法、类必须使用严格的浮点计算来生成可再生的结果

### 3.5.1 数学函数与常量

**Math类：**

![4张图搞懂floorMod](https://s1.51cto.com/images/blog/201904/01/fa6726561e39427cca4f8b109955b0a5.jpg?x-oss-process=image/watermark,size_16,text_QDUxQ1RP5Y2a5a6i,color_FFFFFF,t_100,g_se,x_10,y_10,shadow_90,type_ZmFuZ3poZW5naGVpdGk=)![](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw== "点击并拖拽以移动")​![4张图搞懂floorMod](https://s1.51cto.com/images/blog/201904/01/2eb6d32bd1100ad5559b8ac4a14b716a.jpg?x-oss-process=image/watermark,size_16,text_QDUxQ1RP5Y2a5a6i,color_FFFFFF,t_100,g_se,x_10,y_10,shadow_90,type_ZmFuZ3poZW5naGVpdGk=)![](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw== "点击并拖拽以移动")​

1. 平方根：sqrt（） double类型
2. 幂运算：pow（x，a）x的a次方 double类型
3. 整数取模：floorMod（除数，被除数）
4. 三角函数：sin、cos、tan、atan、atan2
5. 指数函数：exp、log、log10
6. π的近似值：PI
7. 自然常数的近似值：E
- 注：导入Math包后，使用函数不用加Math前缀 import static java.lang.Math.*;

- StrictMath类与Math类：Math类很多方法通过调用StrictMath类来实现；Math类使用计算机浮点单元的例程，性能更好；StrictMath类能保证计算精度

- StrictMath类算法实现：[http://www.netlib.org/fdlibm/index.html](http://www.netlib.org/fdlibm/index.html)

### 3.5.2 数值类型的转化

### ![](https://img-blog.csdnimg.cn/20190424124804517.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzU0OTE0OA==,size_16,color_FFFFFF,t_70)![](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw== "点击并拖拽以移动")​

- 实心箭头：无信息丢失的转换
- 虚箭头：可能有精度损失的转换
- 两个不同类型数值运算时，同化优先级：double > float > long > int

### 3.5.3 强制类型转换

Math.round（）仍需使用（int）：因为round返回结果为long类型

1. 使用（）：例如，（int）4.5=4
2. 对浮点数舍入运算（四舍五入），得到最接近的整数：Math.round（）
3. 不要在boolean类型与任何数值类型直接强制转换，除非使用条件表达式 b ？1 : 0

### 3.5.4 结合赋值和运算符

- 如果运算符得到一个值，其类型与左侧操作数类型不同时，以操作数类型优先，发生转换：

- int x=0；x+=3.5 等价于 (int)(x+3.5)

### 3.5.6 关系和boolean运算符

| 操作符 | 描述                                               | 例子           |
| --- | ------------------------------------------------ | ------------ |
| &&  | 称为逻辑与运算符。当且仅当两个操作数都为真，条件才为真。                     | （A && B）为假。  |
| ||  | 称为逻辑或操作符。如果任何两个操作数任何一个为真，条件为真。                   | （A | | B）为真。 |
| ！   | 称为逻辑非运算符。用来反转操作数的逻辑状态。如果条件为true，则逻辑非运算符将得到false。 | ！（A && B）为真。 |

如果条件为true，表达式为第一个表达式的值，否则为第二个表达式的值 例：x<y?x:y 返回x和y中较小的那个

1. && 和 || 为短路运算符：如果第一个操作数能确定表达式的值，就不再计算第二个操作数
2. 三元操作符：condition ？expression1 ：expression2 如果条件为true，值等于第一个表达式的值，否则为第二个 
   
   例：x < y ? x : y 返回x、y中较小的一个

### 3.5.7 位运算符

| 操作符 | 描述                                        | 例子 **A:60 B:13**        |
| --- | ----------------------------------------- | ----------------------- |
| ＆   | 如果相对应位都是1，则结果为1，否则为0                      | （A＆B），得到12，即0000 1100   |
| |   | 如果相对应位都是0，则结果为0，否则为1                      | （A | B）得到61，即 0011 1101 |
| ^   | 如果相对应位值相同，则结果为0，否则为1                      | （A ^ B）得到49，即 0011 0001 |
| 〜   | 按位取反运算符翻转操作数的每一位，即0变成1，1变成0。              | （〜A）得到-61，即1100 0011    |
| <<  | 按位左移运算符。左操作数按位左移右操作数指定的位数。                | A << 2得到240，即 1111 0000 |
| >>  | 按位右移运算符。左操作数按位右移右操作数指定的位数。                | A >> 2得到15即 1111        |
| >>> | 按位右移补零操作符。左操作数的值按右操作数指定的位数右移，移动得到的空位以零填充。 | A>>>2得到15即0000 1111     |

- 移位运算符的右操作数需要对32取模；若左操作数为long类型，则右操作数对64取模 1<<35=1<<3

### 3.5.8 运算符级别（从高到低）

### 

| 类别   | 操作符                                   | 关联性  |
| ---- | ------------------------------------- | ---- |
| 后缀   | () [] . (点操作符)                        | 左到右  |
| 一元   | + - ！〜 ++ --                          | 从右到左 |
| 乘性   | * / ％                                 | 左到右  |
| 加性   | + -                                   | 左到右  |
| 移位   | >> >>> <<                             | 左到右  |
| 关系   | >> = << = instanceof                  | 左到右  |
| 相等   | == !=                                 | 左到右  |
| 按位与  | ＆                                     | 左到右  |
| 按位异或 | ^                                     | 左到右  |
| 按位或  | |                                     | 左到右  |
| 逻辑与  | &&                                    | 左到右  |
| 逻辑或  | ||                                    | 左到右  |
| 条件   | ？：                                    | 从右到左 |
| 赋值   | = + = - = * = / =％= >> = <<= ＆= ^= |= | 从右到左 |
| 逗号   | ，                                     | 左到右  |

- 一元减号用于转变数据的符号
- 唯一的作用仅仅是将较小类型的操作数提升为int



## 3.6 字符串

- 字符串：Unicode字符序列

### 3.6.1 子串

- String**.**substring（a，b）：从一个较大的字符串提取出一个子串 子串长度：b-a 注：第二个参数不包括本身 （0,2）=0,1

### 3.6.2 拼接

1. 使用 + 进行拼接
2. 如果需要把多个字符串放在一起，用一个定界符分隔，使用静态join方法：（a , b） 第一个参数为定界符 例：String all = String.join("/", "S", "M", "L" ,"XL") all="S/M/L/XL"

### 3.6.4 检测字符串是否相等

注：str1、str2可以是字符串变量，也可以是字符串字面量（“hello”）

1. str1.equals(str2)：相等返回true，不等返回false

2. str1.equalsIgnoreCase（str2）：检测时不区分大小写

3. str1.compareTo(str2)：两者相等返回0，不相等返回1
- 一定不要用 = 检测字符串是否相等，= 只能确定两个字符串是否在同一位置

### 3.6.5 空串与Null串

1. 空串""：长度为0的字符串。有串长度（0），内容（空）

2. String对象值为null：表示目前没有任何对象与该变量关联

### 3.6.6 码点与代码单元

1. java字符串由char值序列组成

2. char数据类型是一个采用UTF-16编码表示Unicode码点的代码单元

3. 大部分常用的Unicode字符用一个代码单元表示，辅助字符需要一对代码单元表示

4. length方法返回采用UTF-16编码表示的给定字符串所需要的代码单元数量

5. str.charAt（n）：返回位置n的代码单元，n介于0~str.length（）-1

6. 遍历一个字符串，并且依次查看每一个码点：使用codePoints方法，生成一个int值的“流”，每个int值对应一个码点。转化为一个数组，再完成遍历 int[] codePoints=new codePoints().toArray(); 反之，要把一个码点数组转换为一个字符串，使用构造函数 String str=new String（codePoints，0，codePoints.length）

### 3.6.8 联机API文档

网址：[https://docs.oracle.com/en/java/javase/12/docs/api/index.html](https://docs.oracle.com/en/java/javase/12/docs/api/index.html)

### 3.6.9 构建字符串（StringBuilder）

* 构建空的字符串构建器：StringBuilder builder = new StringBuilder（）

* 方法详见[API文档](#2.java.lang.StringBuilder 5.0)

  


## 3.7 输入输出

### 3.7.1 读取输入

* Scanner类：Scanner in = new Scanner（System.in）
*  方法详见[API文档](#3.java.util.Scanner 5.0)
*  Scanner类定义在java.util包。当使用的类不是定义在基本java.lang包，需要用import导入
*  如果要使输入不可见，例如读取密码，用Console类 [API文档](#5.java.io.Console 6 )

### 3.7.2 格式化输出

* java沿用C语言的printf方法

* 每一个以 ％字符开始的格式说明符都用相应的参数替换。 格式说明符尾部的转换符将指示被
  格式化的数值类型 

  ![1556706381054](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1556706381054.png)

![1556706406247](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1556706406247.png)

*  可以使用 s 转换符格式化任意的对象,， 对于任意实现了 Formattable 接口的对象都将调用 formatTo 方法； 否则将调用 toString 方法， 它可以将对象转换为字符串。 

* Date类格式化时间已过时，因使用java.time包的方法

  ![1556706644138](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1556706644138.png)

![1556706699197](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1556706699197.png)

* 格式说明符语法图（许多格式化规则是本地环境特有的 ）

  ![1556708184651](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1556708184651.png)

### 3.7.3 文件输入与输出

1. 对文件进行读取，需要用 File 对象构造一个 Scanner 对象：

​		Scanner in = new Scanner（Paths.get（“xxx.txt”），“UTF-8”）

​		字符编码如果省略，则使用机器的“默认编码”，不建议这么做

* 如果文件名包含反斜杠符号，需要在每个反斜杠前再加一个反斜杠

  * 例：“c：\\\mydirectory\\\myfile.txt”

  

2. 写入文件：构建 PrintWriter 对象，只需提供文件名，若文件不存在，创建该文件

   ​		PrintWriter out = new PrintWriter（“myfile.txt”，“UTF-8”）

3. 若用不存在的文件构造Scanner，或者用不能被创建的文件名构造PrintWriter，会发生异常。需要提前告知编译器可能出现这种异常情况，在main方法中用throws子句标记：

   ​		public static void main（String args[]）throws IOException

4. 当采用命令行方式启动程序时，可以利用shell的重定向语法将任意文件关联到System.in和System.out：

   ​		java MyProg<myfile.txt> output.txt


## 3.8 控制流程

### 3.8.1 块作用域

* 块（即复合语句）：有一对大括号括起来的若干条简单的java语句
* 块确定变量的作用域
* 块能嵌套 不能在嵌套的两个块中声明同名的变量（在C++中可以，内层变量覆盖外层变量）

### 3.8.2 条件语句

* else子句与最邻近的if构成一组	if() if() ……;else sign=-1;  else与第二个 if 配对

### 3.8.3 循环

1. while循环语句首先检测循环条件，若不符合，一次都不执行

* 如果希望循环体至少执行一次，用do/while 语句，先执行，再检测条件：
  * do  statement  while  （condition）；

2. for循环语句：
   * 如果在内部定义变量，这个变量不能在循环体外使用

### 3.8.5 多重选择：switch语句

* switch语句将从与选项值匹配的case标签处开始执行直到遇到break语句，或者执行到switch语句的结束处
* 如果没有相匹配的case标签，而有 dafault 子句，则执行dafault子句11

警告：如果case分支语句末尾没有break语句，就会接着执行下一个语句

* 如果想使用这种“直通式”行为，可以标注： @SuppressWarnings（“fallthrough”）
* case标签可以是：
  * 类型为char、byte、short、int的常量表达式
  * 枚举常量
  * 从java SE 7开始，case还可以是字符串字面量

### 3.8.6 中断控制流程语句：break continue

* break continue都可以带标签，可以跳到指定的循环（只出不进）

  * 标签写在流程语句的前面，例如：

    * read_data：
      * while（***）
      * break read_data；


## 3.9 大数值

- 如果基本的整数和浮点数精度不能满足，可以使用java.math包中的两个类：BigInteger、BigDecimal
- 这两个类可以处理包含任意长度数字序列的数值
- BigInteger实现任意精度的整数运算
  - 方法详见 [API文档](# 8. java.math.BigInteger 1.1)
- BigDecimal实现浮点数运算
  - 方法详见 [API文档](# 9.java.math.BigDecimal 1.1)



## 3.10 数组

* 一种数据结构，用来储存同一类型值的集合
* 声明形式：int[] a（推荐） 或者 int  a[]
* 数组长度不要求是常量：
  * new int [n]会创建一个长度为n的数组
* 创建数组：
  * 数字数组初始化为0
  * boolean数组初始化为false
  * 对象数组初始化为特殊值null 表示这些元素还没存放任何对象
* 创建数组后，就不能再改变数组大小

### 3.10.1 for each循环

