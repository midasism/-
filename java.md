
## 《Java核心技术 卷1》笔记

[TOC]

### API文档

#### 1.java . lang . string 1.0

![](https://img-blog.csdnimg.cn/2019050100400048.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzU0OTE0OA==,size_16,color_FFFFFF,t_70)![](https://img-blog.csdnimg.cn/20190501004152821.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzU0OTE0OA==,size_16,color_FFFFFF,t_70)![](https://img-blog.csdnimg.cn/20190501004241516.png)

#### 2.java.lang.StringBuilder 5.0
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190902003301239.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzU0OTE0OA==,size_16,color_FFFFFF,t_70)
#### 3.java.util.Scanner 5.0 
![在这里插入图片描述](https://img-blog.csdnimg.cn/2019090200314756.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzU0OTE0OA==,size_16,color_FFFFFF,t_70)![在这里插入图片描述](https://img-blog.csdnimg.cn/20190902003208755.png)
#### 4.java.Iang.System 1.0 
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190902003127721.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzU0OTE0OA==,size_16,color_FFFFFF,t_70)
#### 5.java.io.Console 6 
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190902003113765.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzU0OTE0OA==,size_16,color_FFFFFF,t_70)
#### 6.java.io.PrintWriter 1.1 
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190902002532683.png)
#### 7. java.nio.file.Paths 7 
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190902002519939.png)
#### 8. java.math.BigInteger 1.1
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190902002505946.png)
#### 9.java.math.BigDecimal 1.1
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190902002448496.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzU0OTE0OA==,size_16,color_FFFFFF,t_70)
#### 10.java.util.Arrays 1.2
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190902002240877.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzU0OTE0OA==,size_16,color_FFFFFF,t_70)![在这里插入图片描述](https://img-blog.csdnimg.cn/20190902002302379.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzU0OTE0OA==,size_16,color_FFFFFF,t_70)
#### 11. java.time.LocalDate 8
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190903004940675.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzU0OTE0OA==,size_16,color_FFFFFF,t_70)![在这里插入图片描述](https://img-blog.csdnimg.cn/20190903005004259.png)


### 第三章：Java的基本程序设计结构

### 3.1

2. 类名规则：必须以字母开头，后面可以是字母和数字的任意组合；长度基本上没有限制；不能使用java保留字
3. 类命名规范：大写字母开头。若由多个单词组成，则每个单词首字母需要大写（驼峰命名法）
4. 源代码的文件名必须与公共类的名字相同
5. 如果main方法正常退出，那么退出代码为0。如果需要在程序终止时返回其它的代码，可以调用System.exit

### 3.2 注释

1. / /
2. /* */：长篇注释
3. /** */：文档注释，可自动生成文档

### 3.3 数据类型

#### 3.3.1 整型

Java整型

| 类型  | 储存要求 | 取值范围                                             |
| ----- | -------- | ---------------------------------------------------- |
| byte  | 1字节    | -128~127                                             |
| short | 2字节    | -32768~32767                                         |
| int   | 4字节    | -2147483648~2147483647                               |
| long  | 8字节    | -9 223 372 036 854 775 808~9 223 372 036 854 775 807 |

1. Java的整型范围固定不变，与运行的机器无关
2. byte和short类型主要用于特定场合，例如底层的文件处理或者需要控制储存空间的大数组
3. 长整型long有后缀 L 或 l
4. 十六进制：前缀0x或0X 八进制：前缀0 二进制：0b或0B（例如0b1001=9）
5. 可以为数字字面量加下划线(如1_000_000)，编译器会去除下划线

#### 3.3.2 浮点型

| 类型   | 储存要求 | 取值范围                                           |
| ------ | -------- | -------------------------------------------------- |
| float  | 4字节    | 大约+-3.402 823 47E+38F(有效位数：6~7）            |
| double | 8字节    | 大约+-1.797 693 134 862 315 70E+308(有效位数：15） |

1. float后缀：F/f
2. double后缀可加可不加：D/d
3. 正无穷大：常量Double.POSITIVE_INFINITY
4. 负无穷大：常量Double.NEGATIVE_INFINITY
5. NaN：Double.NaN 注：若检查特定值是否等于Double.NaN, 用 Double.isNaN 方法
6. 浮点运算会出现舍入误差，例如2.0-1.1=0.8999999999，而不是0.9

#### 3.3.3 char类型

```
                                 **特殊字符的转义序列**
```

| 转义序列 | 名称   | Unicode值 |
| -------- | ------ | --------- |
| \b       | 退格   | \u0008    |
| \t       | 制表   | \u0009    |
| \n       | 换行   | \u000a    |
| \r       | 回车   | \u0009    |
| \"       | 双引号 | \u0022    |
| \'       | 单引号 | \u0027    |
| \\\      | 反斜杠 | \u005c    |

char类型的字面值用单引号括起来

#### 3.3.4 Unicode和char类型

1. 码点：与一个编码表中的某个字符对应的代码值
2. 在Unicode中，码点用十六进制，加上前缀U+
3. 码点可分成17个代码级别
4. 第一个级别成为基本的多语言级别，U+10000到U+10FFFF
5. 基本的多语言级别：每个字符16位，称为代码单元
6. 辅助字符：采用一对连续的代码单元
7. 建议不在程序中使用char类型

#### 3.3.5 boolean类型

1. 两个值：false true
2. 整型和布尔值不能相互转化

### 3.4 变量

1. 检查哪些Unicode字符属于Java中的“字母”：用Character类的 isJavaIdentifierStart（检查字符是否可作为标识符的第一个字符） 和 isJavaIdentifierPart（检查字符是否可作为标识符的一部分，而不是开头） 方法
2. $ 是合法的Java字符，但不要在代码中使用


#### 3.4.2 常量

1. 用关键字 final 指示常量
2. 习惯上常量使用大写
3. 类常量：希望某个常量可以在一个类的多个方法中使用，使用关键字 static final
4. 常变量定义位于main方法的外部

### 3.5 运算符

* 使用strictfp 关键字标记的方法、类必须使用严格的浮点计算来生成可再生的结果

#### 3.5.1 数学函数与常量

**Math类：**

![4张图搞懂floorMod](https://imgconvert.csdnimg.cn/aHR0cHM6Ly9zMS41MWN0by5jb20vaW1hZ2VzL2Jsb2cvMjAxOTA0LzAxL2ZhNjcyNjU2MWUzOTQyN2NjYTRmOGIxMDk5NTViMGE1LmpwZw?x-oss-process=image/format,png)![4张图搞懂floorMod](https://imgconvert.csdnimg.cn/aHR0cHM6Ly9zMS41MWN0by5jb20vaW1hZ2VzL2Jsb2cvMjAxOTA0LzAxLzJlYjZkMzJiZDExMDBhZDU1NTliOGFjNGExNGI3MTZhLmpwZw?x-oss-process=image/format,png)

1. 平方根：sqrt（） double类型
2. 幂运算：pow（x，a）x的a次方 double类型
3. 整数取模：floorMod（除数，被除数）
4. 三角函数：sin、cos、tan、atan、atan2
5. 指数函数：exp、log、log10
6. π的近似值：PI
7. 自然常数的近似值：E

* 注：导入Math包后，使用函数不用加Math前缀 import static java.lang.Math.*;
* StrictMath类与Math类：Math类很多方法通过调用StrictMath类来实现；Math类使用计算机浮点单元的例程，性能更好；StrictMath类能保证计算精度
* StrictMath类算法实现：[http://www.netlib.org/fdlibm/index.html](http://www.netlib.org/fdlibm/index.html)

#### 3.5.2 数值类型的转化

#### ![](https://img-blog.csdnimg.cn/20190424124804517.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzU0OTE0OA==,size_16,color_FFFFFF,t_70)
* 实心箭头：无信息丢失的转换
* 虚箭头：可能有精度损失的转换
* 两个不同类型数值运算时，同化优先级：double > float > long > int

#### 3.5.3 强制类型转换

Math.round（）仍需使用（int）：因为round返回结果为long类型

1. 对浮点数舍入运算（四舍五入），得到最接近的整数：Math.round（）
2. 不要在boolean类型与任何数值类型直接强制转换，除非使用条件表达式 b ？1 : 0

#### 3.5.4 结合赋值和运算符

* 如果运算符得到一个值，其类型与左侧操作数类型不同时，以操作数类型优先，发生转换：
* int x=0；x+=3.5 等价于 (int)(x+3.5)

#### 3.5.6 关系和boolean运算符

| 操作符 | 描述                                                         |
| ------ | ------------------------------------------------------------ |
| &&     | 称为逻辑与运算符。当且仅当两个操作数都为真，条件才为真。     |
| \|\|   | 逻辑或运算符。只要任意一个操作数为真，条件为真               |
| ！     | 称为逻辑非运算符。用来反转操作数的逻辑状态。如果条件为true，则逻辑非运算符将得到false。 |

如果条件为true，表达式为第一个表达式的值，否则为第二个表达式的值 例：x<y?x:y 返回x和y中较小的那个

1. && 和 || 为短路运算符：如果第一个操作数能确定表达式的值，就不再计算第二个操作数

2. 三元操作符：condition ？expression1 ：expression2 如果条件为true，值等于第一个表达式的值，否则为第二个 

   例：x < y ? x : y 返回x、y中较小的一个

#### 3.5.7 位运算符

| 操作符 | 描述                                                         | 例子 **A:60 B:13**            |
| ------ | ------------------------------------------------------------ | ----------------------------- |
| ＆     | 如果相对应位都是1，则结果为1，否则为0                        | （A＆B），得到12，即0000 1100 |
| \|     | 如果相对应位都是0，则结果为0，否则为1                        | （A \| B）,得到61，即 111101  |
| ^      | 如果相对应位值相同，则结果为0，否则为1                       | （A ^ B）得到49，即 0011 0001 |
| 〜     | 按位取反运算符翻转操作数的每一位，即0变成1，1变成0。         | （〜A）得到-61，即1100 0011   |
| <<     | 按位左移运算符。左操作数按位左移右操作数指定的位数。         | A << 2得到240，即 1111 0000   |
| >>     | 按位右移运算符。左操作数按位右移右操作数指定的位数。         | A >> 2得到15即 1111           |
| >>>    | 按位右移补零操作符。左操作数的值按右操作数指定的位数右移，移动得到的空位以零填充。 | A>>>2得到15即0000 1111        |

* 移位运算符的右操作数需要对32取模；若左操作数为long类型，则右操作数对64取模 1<<35=1<<3

#### 3.5.8 运算符级别（从高到低）

#### 

| 类别     | 操作符                               | 关联性   |
| -------- | ------------------------------------ | -------- |
| 后缀     | () [] . (点操作符)                   | 左到右   |
| 一元     | + - ！〜 ++ --                       | 从右到左 |
| 乘性     | * / ％                               | 左到右   |
| 加性     | + -                                  | 左到右   |
| 移位     | >> >>> <<                            | 左到右   |
| 关系     | >> = << = instanceof                 | 左到右   |
| 相等     | == !=                                | 左到右   |
| 按位与   | ＆                                   | 左到右   |
| 按位异或 | ^                                    | 左到右   |
| 按位或   |                                      |          |
| 逻辑与   | &&                                   | 左到右   |
| 逻辑或   |                                      |          |
| 条件     | ？：                                 | 从右到左 |
| 赋值     | = + = - = * = / =％= >> = <<= ＆= ^= | =        |
| 逗号     | ，                                   | 左到右   |

* 一元减号用于转变数据的符号
* 唯一的作用仅仅是将较小类型的操作数提升为int



### 3.6 字符串

* 字符串：Unicode字符序列

#### 3.6.1 子串

* String**.**substring（a，b）：从一个较大的字符串提取出一个子串 子串长度：b-a 注：第二个参数不包括本身 （0,2）=0,1

#### 3.6.2 拼接

1. 使用 + 进行拼接
2. 如果需要把多个字符串放在一起，用一个定界符分隔，使用静态join方法：（a , b） 第一个参数为定界符 例：String all = String.join("/", "S", "M", "L" ,"XL") all="S/M/L/XL"

#### 3.6.4 检测字符串是否相等

注：str1、str2可以是字符串变量，也可以是字符串字面量（“hello”）

1. str1.equals(str2)：相等返回true，不等返回false
2. str1.equalsIgnoreCase（str2）：检测时不区分大小写
3. str1.compareTo(str2)：两者相等返回0，不相等返回1

* 一定不要用 = 检测字符串是否相等，= 只能确定两个字符串是否在同一位置

#### 3.6.5 空串与Null串

1. 空串""：长度为0的字符串。有串长度（0），内容（空）
2. String对象值为null：表示目前没有任何对象与该变量关联

#### 3.6.6 码点与代码单元

1. java字符串由char值序列组成
2. char数据类型是一个采用UTF-16编码表示Unicode码点的代码单元
3. 大部分常用的Unicode字符用一个代码单元表示，辅助字符需要一对代码单元表示
4. length方法返回采用UTF-16编码表示的给定字符串所需要的代码单元数量
5. str.charAt（n）：返回位置n的代码单元，n介于0~str.length（）-1
6. 遍历一个字符串，并且依次查看每一个码点：使用codePoints方法，生成一个int值的“流”，每个int值对应一个码点。转化为一个数组，再完成遍历 int[] codePoints=new codePoints().toArray(); 反之，要把一个码点数组转换为一个字符串，使用构造函数 String str=new String（codePoints，0，codePoints.length）

#### 3.6.8 联机API文档

网址：[https://docs.oracle.com/en/java/javase/12/docs/api/index.html](https://docs.oracle.com/en/java/javase/12/docs/api/index.html)

#### 3.6.9 构建字符串（StringBuilder）

* 构建空的字符串构建器：StringBuilder builder = new StringBuilder（）
  

### 3.7 输入输出

#### 3.7.1 读取输入

* Scanner类：Scanner in = new Scanner（System.in）
* 方法详见[API文档](#3.java.util.Scanner 5.0)
* Scanner类定义在java.util包。当使用的类不是定义在基本java.lang包，需要用import导入
* 如果要使输入不可见，例如读取密码，用Console类 [API文档](#5.java.io.Console 6 )

#### 3.7.2 格式化输出

* java沿用C语言的printf方法

* 每一个以 ％字符开始的格式说明符都用相应的参数替换。 格式说明符尾部的转换符将指示被
  格式化的数值类型 

![在这里插入图片描述](https://img-blog.csdnimg.cn/20190902001903633.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzU0OTE0OA==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190902001932491.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzU0OTE0OA==,size_16,color_FFFFFF,t_70)

* 可以使用 s 转换符格式化任意的对象,， 对于任意实现了 Formattable 接口的对象都将调用 formatTo 方法； 否则将调用 toString 方法， 它可以将对象转换为字符串

* Date类格式化时间已过时，应该使用java.time包的方法

![在这里插入图片描述](https://img-blog.csdnimg.cn/20190902001957955.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzU0OTE0OA==,size_16,color_FFFFFF,t_70)

![在这里插入图片描述](https://img-blog.csdnimg.cn/20190902002013597.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzU0OTE0OA==,size_16,color_FFFFFF,t_70)

* 格式说明符语法图（许多格式化规则是本地环境特有的 ）
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190902002030210.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzU0OTE0OA==,size_16,color_FFFFFF,t_70)

#### 3.7.3 文件输入与输出

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

### 3.8 控制流程

#### 3.8.1 块作用域

* 块（即复合语句）：有一对大括号括起来的若干条简单的java语句
* 块确定变量的作用域
* 块能嵌套 不能在嵌套的两个块中声明同名的变量（在C++中可以，内层变量覆盖外层变量）

#### 3.8.2 条件语句

* else子句与最邻近的if构成一组	if() if() ……;else sign=-1;  else与第二个 if 配对

#### 3.8.3 循环

1. while循环语句首先检测循环条件，若不符合，一次都不执行

* 如果希望循环体至少执行一次，用do/while 语句，先执行，再检测条件：
  * do  statement  while  （condition）；


#### 3.8.5 多重选择：switch语句

* switch语句将从与选项值匹配的case标签处开始执行直到遇到break语句，或者执行到switch语句的结束处
* 如果没有相匹配的case标签，而有 dafault 子句，则执行dafault子句

警告：如果case分支语句末尾没有break语句，就会接着执行下一个语句

* 如果想使用这种“直通式”行为，可以标注： @SuppressWarnings（“fallthrough”）
* case标签可以是：
  * 类型为char、byte、short、int的常量表达式
  * 枚举常量
  * 从java SE 7开始，case还可以是字符串字面量

#### 3.8.6 中断控制流程语句：break continue

* break continue都可以带标签，可以跳到指定的循环（只出不进）
  * 标签写在流程语句的前面，例如：
    * read_data：
      * while（***）
      * break read_data；

### 3.9 大数值

* 如果基本的整数和浮点数精度不能满足，可以使用java.math包中的两个类：BigInteger、BigDecimal
* 这两个类可以处理包含任意长度数字序列的数值
* BigInteger实现任意精度的整数运算
* BigDecimal实现浮点数运算


### 3.10 数组

* 一种数据结构，用来储存同一类型值的集合
* 声明形式：int[] a（推荐） 或者 int  a[]
* 数组长度不要求是常量：
  * new int [n]会创建一个长度为n的数组
* 创建数组：
  * 数字数组初始化为0
  * boolean数组初始化为false
  * 对象数组初始化为特殊值null 表示这些元素还没存放任何对象
* 创建数组后，就不能再改变数组大小

#### 3.10.1 for each循环

* 格式：for( variable : collection )  statement

  例： for( int element : a)  System.out.println(element)  打印数组a的每一个元素

* collection 表达式：数组或一个实现了Iterable接口的类对象

* 打印数组所有的值的技巧：使用Arrays的toString方法

  例：System.out.println( Arrays.toString ( arr ) )；

#### 3.10.2 数组初始化及匿名数组

* java允许数组长度为0：new elementType[0]

#### 3.10.3 数组拷贝

* int[] b = a； ：相当于两个变量同时引用同一个数组

* 将原数组的值拷贝到新数组：Arrays类的copyOf方法（第2个参数是新数组的长度，若大于原数组长度，则多余项初始化为默认值，小于则只拷贝前面的数据元素）

  type[]  newArray = Arrays.copyOf( oldArray , length );

* java中的[ ]运算符被预定义为检查数组边界

#### 3.10.4 命令行参数

* 在命令行中运行java程序时，后面可额外添加参数，参数依次被赋值到main方法接受的字符串数组args[]

#### 3.10.5 数组排序

* Arrays类的sort方法：使用了优化的快速排序算法（该算法对于大多数数据集合都是效率高的）

#### 3.10.6 多维数组

* 快速打印二维数组：Arrays类的deepToString（）
* 二维数组包含的一维数组长度可以不相等



### 第四章 对象和类

### 4.1 概述

#### 4.1.1 类的特性

* 封装：将数据和行为组合在一个包中，并对对象的使用者隐藏了数据的实现方式
  * 实例域：对象中的数据		方法：操作数据的过程
* 继承：通过扩展一个类来建立另外一个新的类
  * 扩展后的新类具有父类的全部属性和方法

#### 4.1.4 类常见关系



1. 依赖（uses-a）：一个类的方法可以操纵另一个类的对象
   * 在程序设计中，应尽可能把相互依赖的类减至最少，即降低程序耦合度
2. 聚合（has-a）
3. 继承
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190902001751881.png)

### 4.2 使用预定义类

#### 4.2.1 对象和对象变量

* 一个对象变量并不是包含一个对象，而是引用一个对象
* 局部变量不会自动地初始化为null，而必须通过调用 new 或将它们设置为 null 来初始化
* Date birthday;//java  等价于  Date* birthday;//C++

#### 4.2.2 Java类库的LocalDate类
* 构造LocalDate对象：使用静态工厂方法代替构造器
* plusDays方法：生成新的对象，原来对象的日期不会增加
* 详见API

#### 4.2.3 更改器方法和访问器方法

* 访问器方法：只访问对象、不修改对象的方法
* C++：带有const后缀的方法是访问器方法

#### 4.3.4 构造器

* java对象都是在堆里构造的

#### 4.3.5 隐式参数和显式参数

* 隐式参数
  * 方法调用的目标或接受者
  * this可表示隐式参数
* 显示参数：列在方法声明中的

#### 4.3.9 final

* 被final修饰的基本数据类型的变量，不可修改（常量）
* 被final修饰的引用类型，初始化后则不可再引用新的对象，但自身对象不受任何影响



### 4.4 静态域与静态方法

* static ：属于类但不属于类对象的变量与方法
#### 4.4.1 静态域
* 静态域：static修饰的域，被该类的所有对象共用

#### 4.4.2 静态常量
* 常用的静态常量：Math.PI , System.out
* System的setOut方法，可以将System.out设置为不同的流（setOut方法是本地方法，不是用java实现的，可以绕过java的存取控制机制）

#### 4.4.3 静态方法
* 静态方法不能访问实例域，只能访问静态域
* 静态方法可以省略static关键字，但需要通过对象调用，因为静态方法本身与对象无关，这样做会产生混淆，不建议省略static关键字
* 两种情况使用静态方法：
	* 方法不需要访问对象状态，所需参数都是由显式参数提供
	* 方法只需要访问类的静态域

#### 4.4.4 静态工厂方法
* 不通过 new，而是用一个静态方法来对外提供自身实例的方法
详见 [java的静态方法](https://blog.csdn.net/weixin_43549148/article/details/100528668)
相比构造器的优势：
* 有名字，不用重载构造器
* 不用每次被调用时都创建对象
* 可以有多个参数相同但名称不用的工厂方法
* 可以减少对外暴露的属性
* 可以返回原返回类型的子类

### 4.5 方法参数
* 按值调用：接收的是调用者的值
* 按引用调用：接收的是调用者提供的变量地址
* Java采取的是**按值调用**（即使参数是对象，也是传入对象引用的拷贝）
* 总结：
	1. 方法不能修改基本数据类型的参数
	2. 方法可以改变对象参数的状态
	3. 方法不能让对象参数引用一个新的对象（传入的只是对象引用的拷贝）
	


### 4.6 对象构造
#### 4.6.3 无参构造器
* 如果在构造器中没有显式地给域赋予初值，域就会被自动赋为默认值（数值为0、布尔值为false、对象引用为null ）
* 如果类中提供了至少一个构造器，系统就不会自动提供无参构造器

#### 4.6.4 显式域初始化
* 当所有构造器给一个特定的实例域赋相同的值时，可以在定义该实例域的时候赋值
* 初始值不一定是常量值，也可以是一个有返回值的方法

#### 4.6.6 调用其它构造器
* 如果构造器代码有重复，可以使用this（参数）复用其它构造器

#### 4.6.7 初始化块
* 初始化数据域的方法：
	1. 构造器设置值
	2. 定义时赋值
	3. 初始化块（不常用）
* 初始化块{ }：对象实例化时先按块顺序调用所有初始化块，然后才调用构造器
* 静态的初始化块：static { }

#### 4.6.8 对象析构
* 可以为任何一个类添加finalize（）方法，将在垃圾回收器清除对象前调用
* java不是一定会执行finalize方法
* finalize（）适合释放非Java资源，如文件句柄、window字符字体
1. 对象不一定被回收
2. 垃圾回收不是析构函数
3. 垃圾回收只与内存有关
4. 垃圾回收和finalize（）都是靠不住的，只要JVM内存还没耗尽，不会浪费时间去垃圾回收
* System.runFinalizersOnExit( true )可以确保在程序结束后进行垃圾回收（被废弃：存在安全问题，当有对象仍在活动时执行，当有线程并发操作这些对象时就会出现奇怪的行为和死锁）
	* Runtime.addShutdownHook添加“关闭钩”可以代替


### 4.7 包
* 使用包的主要原因：确保类名的唯一性

#### 4.7.1 类的导入
* 使用import语句，可以导入一整个包或者单独一个类
* 注意：只能使用星号 * 导入一个包，不能 import java . * 或者 import java . * . * 导入以java为前缀的所有包

#### 4.7.2 静态导入
* import 可以导入静态方法和静态域
* 例如： import static java.lang.System.*;

#### 4.7.3 将类放入包中
* 想要把类放入包中，需要将包的名字放在源文件开头：
	package [目录结构]；
* 编译器在编译源文件时不检查目录结构。若包与目录不匹配，最终虚拟机就找不到类

#### 4.7.4 包作用域
* 标记为public的部分可以被任意类使用
* 标记为private的部分只能被定义它们的类使用
* 默认（没有指定访问修饰符）可以被同一个包的所有方法访问
* 可以通过**包密封**机制来解决将各种包混杂在一起的问题（详见第9章）


### 4.8 类路径
* 类文件可以存储到 JAR（Java归档）文件中
* 一个JAR文件，可以包含多个压缩形式的类文件和子目录，节省空间、改善性能
*  默认java虚拟机要从classpath环境变量的路径中搜索class文件去执行，对于java虚拟机来说，这不是类文件，而是类。它只有类路径，而没有文件系统路径
* **javac编译器搜索的是文件路径，和环境变量classpath无关**
* **java虚拟机搜索的是类文件，严格地说是类，搜索路径由环境变量classpath决定，且有先后顺序**
* 类路径：
1. 基目录
2. 当前目录（.）
3. JAR文件（SE 6开始，可以在JAR文件目录中指定通配符(UNIX禁止使用)
例：c:\classdir;.; c:\archieves\*
* 警告：如果设置了类路径却忘记了包含“ . ”目录，则程序仍可以通过编译，但不能运行
* 虚拟机搜寻文件，首先查看储存在jre/lib和jre/lib/ext目录下的归档文件中所存放的系统类文件

* 编译器定位文件比虚拟机复杂：
1. 如果引用一个类，而没有指出这个类所在的包，那么编译器首先查找包含这个类的包，并查询所有的import指令，确定是否包含被引用的类
2. 编译器查看源文件是否比类文件新，如果新，就自动地重新编译

#### 4.8.1 设置类路径
* 建议使用 -classpath（-cp）选项指定类路径：
java -classpath /home/user/classdir ; . ; /home/user/archives/archive.jar Myprog
* 也可以设置环境变量：（Windows）set CLASSPATH=c:\classdir ; . ; c:\archives\archive.jar
直到退出shell为止，类路径设置均有效


### 4.9 文档注释
* javadoc：由源文件生成一个HTML文件

#### 4.9.1 注释的插入
* 每个/ * * ... */ 文档注释在标记之后紧跟自由格式文本
* 自由格式文本：
	* 第一句应该是一个概要性的句子，javadoc程序自动将这些句子取出形成概要页
	* 可以使用HTML标签（不要使用<h1>或<hr>，会和文档格式起冲突）
* 注：如果在文档中有到其他文件的链接，应该把这些文件放到子目录 doc-files中（javadoc程序将从源目录拷贝这些目录及其中的文件到文档目录中）
在链接中需要使用doc-files目录

#### 4.9.2 类注释
* 类注释必须放在import语句后，类定义前

#### 4.9.3 方法注释
* @param 变量描述：
	* 对当前方法的“param”（参数）部分添加一个条目
	* 可以占据多行，并可以使用HTML标记
	* 一个方法的所有@param标记必须放在一起

* @return 描述：
	* 对当前方法添加“return”部分
	* 可以跨越多行，并可以使用HTML标记

* @throws 类描述：
	* 添加一个注释，表示这个方法有可能抛出异常

#### 4.9.5 通用注释
* 适用类文档注释
	* @author 姓名：（可以使用多个）每个标记对应一个作者
	* @version 文本：可以是对当前版本的任何描述

* 适用所有文档注释
	* @since 文本：可以是对引入特性的版本描述
	例：@since version 1.7.10
	* @deprecated 文本：对类、方法或变量添加一个不再使用的注释，文本中给出了取代的建议

* @see 引用：添加一个超链接，可以用于类或方法(可以添加多个，但必须放在一起)
	1. package.class#feature label
	* 只要提供类、方法或变量的名字，javadoc就在文档中插入一个超链接
	* 一定要使用 # 代替 . 分隔类名和方法名，或类名和变量名
	
	2. <a  href=“...”>label</a>
	3. "text"

* @link：可以在注释中的任何位置放置指向其他类或方法的超链接，以及插入一个专用的标记
	例：{@link  package.class#feature label}   规则与 @see 一样

#### 4.9.6 包注释

* 想要产生包注释，需要在每一个包目录中添加一个单独的文件，两个选择：
	1. 提供一个以package.html命名的HTML文件
	在标记<body>...</body>之间的所有文本都会被抽取出来
	2. 提供一个以package-info.java命名的Java文件
	这个文件必须包含一个初始的以/ * * 和 * / 界定的Javadoc注释，跟随在一个包语句之后（它不应该包含更多的代码或注释）

* 可以为所有的源文件提供一个概述性的注释
	这个注释被放置在一个名为overview.html的文件，这个文件位于包含所有源文件的父目录下
	
#### 4.9.7 注释的抽取
* 指令：
	1. -d<directory>:指定一个路径，用于将生成的API文档放到该目录下
	2. -windowtitle<text>:指定一个字符串，用于设置API文档的浏览器窗口标题
	3. -doctitle:<html-code>:指定一个HTML的文本，用于指定概述页面的标题
	4. -header<text>:指定浏览器左半部分包列表头标题显示

更多详见：https://blog.csdn.net/u011479200/article/details/78554836



### 第5章 继承

* super：指示编译器调用超类方法的特殊关键字（不是一个对象的引用）
* 使用super调用构造器的语句必须是子类构造器的第一条语句
* 如果子类构造器没有显式地调用超类的构造器，则自动地调用超类默认（没有参数）的构造器（若超类没有空构造器，则报错）

#### 5.1.4 继承层次

* 继承层次：由一个公共超类派生出的所有类的集合
* 继承链：在继承层次中，从某个特定的类到其祖先的路径

#### 5.1.5 多态

* 多态：同一种行为具有不同表现形式或形态
* 对象变量是多态的

#### 5.1.6 方法调用

1. 编译器查看对象的声明类型和方法名。编译器列举所有该对象类中同名的方法和其超类中访问属性为public且同名的方法（超类的私有方法不可访问）
2. 编译器查看调用方法时提供的参数类型。如果在所有同名的方法中存在一个与提供的参数类型完全匹配，就选择这个方法（重载解析）

* **动态绑定和静态绑定（方法调用机制）**：https://blog.csdn.net/weixin_43549148/article/details/100687800

* private方法、static方法、final方法和构造器：静态绑定
* 每次调用方法都要搜索，时间开销很大。所以虚拟机预先为每一个类创建了一个**方法表**，列出了所有方法的签名（方法名+参数列表）和实际调用的方法

#### 5.1.7 阻止继承：final类和方法
* final类：不允许被扩展（继承）的类
* final类中的所有方法自动成为final方法
* 用final修饰的方法，子类不能覆盖
* 如果方法很简短、被频繁调用且没有真正地被覆盖，那么即时编译器就会将这个方法**内联**处理。如果虚拟机加载了另外一个子类，而在这个子类中包含了对内联方法的覆盖，那么优化器将取消对覆盖方法的内联
* 内联：把目标方法的代码“复制”到发起调用的方法中，避免真正的方法调用，减少性能开销
详见：
1. https://blog.csdn.net/weixin_43549148/article/details/100689531
2. 《深入理解Java虚拟机（第二版）》: P352~354

#### 5.1.8 强制类型转换
* 对象进行类型转换时：
	* 只能在继承层次内进行类型转换
	* 将超类转化为子类之前，应该使用instanceof进行检查
	 instanceof关键字详解：https://blog.csdn.net/weixin_43549148/article/details/100920160

#### 5.1.9 抽象类
* 包含一个或多个抽象方法的类本身必须被声明为抽象的
* 抽象类还可以包含具体数据和具体方法
* 类即使不含抽象方法，也可以将类声明为抽象类
* 抽象类不能被实例化
* 可以定义一个抽象类的对象变量，但是它只能引用非抽象子类的对象

#### 5.1.10 受保护访问

* 任何声明为private的内容对其他类都是不可见的（子类也不能访问超类的私有域）
* 若想超类中某些方法或域允许被子类访问，可以声明为protected（不建议标记域）
* 4个访问修饰符归纳：
  * private——仅对本类可见
  * public——对所有类可见
  * protected——对本包和所有子类可见
  * 默认——对本包可见


### 5.2 Object：所有类的超类
* Object类是Java中所有类的始祖
* Java中，只有基本类型不是对象

#### 5.2.1 equal方法
* Object中的equals方法用于检测一个对象是否等于另外一个对象（是否具有相同的引用，一般没什么意义）
* 在重写equals方法时，防止比较双方可能为null的情况，应使用Objects.equals方法
如果两个参数都为null，Object.equals（a，b）返回true；如果其中一个参数为null，返回false；如果两个参数都不为null，则调用a.equals（b）
* 编写equals方法的建议：
	1. 显式参数命名为otherObject（稍后需要将它转化为一个叫other的变量）
	2. 检测this和otherObject是否引用同一个对象：
		if（this == otherObject） return true；
	3. 检测otherObject是否为null，如果为null，返回false
		if（otherObject == null） return false；
	4. 比较this和otherObject是否属于同一个类
	* 如果equals的语义在每个子类中有所改变，就是用getClass检测：
		if（getClass()  !=  otherObject . getClass())） return false；
		
	* 如果所有子类都拥有统一的语义，就使用instanceof检测：
	if（！（otherObject instanceof ClassName）） return false；

  5. 将otherObject转换为相应的类类型变量：
      ClassName other = （ClassName）otherObject；
  6. 使用 == 比较基本类型域，使用equals比较对象域。如果都匹配，返回true
  
* 数组类型的域可以使用静态的Arrays.equals检测数组元素是否相等

#### 5.2.3 hashCode方法
* 散列码：由对象导出的一个整型值
* 由于hashCode方法定义在Object类中，每个对象都有一个默认的散列码，其值为对象的存储地址
* 调用hashCode方法时，最好使用null安全的方法Objects.hashCode（如果参数为null，返回0，否则返回对参数调用hashCode的结果）
* 还可以调用包装类的静态方法hashCode来避免创建对象
* 需要组合多个散列值时，可以调用Objects.hash并提供多个参数（这个方法会对各个参数调用Objects.hashCode，并组合这些散列值）


#### 5.2.4 toString方法
* 可以通过调用getClass().getName()获得类名
* 只要对象与一个字符串通过 + 连接，就会自动地调用toString方法
* 如果想打印数组元素，可以使用Arrays.toString（多维数组使用Arrays.deepToString）


### 5.3 泛型数组列表
* ArrayList：底层是Object数组，所以具有数组的查询速度快的优点以及增删速度慢的缺点
* LinkedList：双向循环链表实现，查询效率低但是增删效率高
	* 可以使用toArray方法将数组存入List中
	* 可以用foreach遍历：
		for（Object e：arr）
			do something with e
	* 添加元素：add（）
	* 删除元素：remove（）
	* 获取个数：size（）


### 5.4 对象包装器与自动装箱
* 为了某些需求，所有的基本类型都有对应的包装类（泛型数组列表的类型参数不允许为基本类型，而应该是对应的包装类）
int-Integer   long-Long   float-Float    double-Double    short-Short   byte-Byte
char-Character    void-Void    boolean-Boolean（前六个类派生于公共的超类Number）
* 对象包装器类不可变（一旦构造了包装器，就不允许更改包装在其中的值）
* 对象包装器为final，不能定义子类

#### 自动装箱
* 自动装箱：当使用泛型数组时，如果直接使用add（）添加基本类型，会自动将基本类型转化为包装类再添加进去
list.add(3) == list.add(Integer.valueOf(3))
* 自动拆箱：将一个包装类对象赋给一个基本类型变量
int n = list.get（i）  ==   int n = list.get(i).intValue()
* 在算术表达式中也可以自动地装箱、拆箱（Integer自加：先拆箱，再装箱）
* java为了节省内存开销，将经常出现的值包装到同一个对象（比较包装器对象时，不建议使用==，而使用equals）
boolean、byte、char<=127，介于-128~127之间的short和int
* 装箱和拆箱是编译器认可的，而不是虚拟机。编译器在生成类的字节码时，插入必要的方法调用，虚拟机只是执行
* 将数字字符串转为数值：
	* java：Integer.parseInt（s） 静态方法
	* C++：s - '0'
* 如果想编写修改数值参数值的方法，需要使用 org.omg.CORBA包中定义的持有者（holder）类型，包括IntHolder、BooleanHolder等。每个持有者类型都含有一个公有域值，通过它可访问储存在里面的值
	public static void triple(IntHolder x){
		x.value=3*x.value;
	}

### 5.5 参数数量可变的方法
* 方法中的参数可为省略号… ：表明方法可接受任意数量的实参
void sum(int… nums){}   相当于传入一个数组
sum(1,2,3) / sum(1,2,3,4,5,6)

### 5.6 枚举类
* 所有的枚举类型都是Enum类的子类
* toString：返回枚举常量名
* toString的逆方法：valueOf（Class enumClass，String name）
* 静态的values：返回一个包含全部枚举值的数组
* ordinal：返回enum声明中枚举常量的位置（从0开始）

深入了解枚举：https://blog.csdn.net/javazejian/article/details/71333103


### 5.7 反射
反射可以用来：
* 在运行时分析类的能力
* 在运行时查看对象，例如编写toString方法供所有类使用
* 实现通用的数组操作代码
* 利用Method对象，很像C++中的函数指针

#### 5.7.1 Class类
* 程序运行期间，Java运行时系统始终为所有的对象维护一个被称为运行时的类型标识。虚拟机利用运行时类型信息选择相应的方法执行。
保存这些信息的类称为Class
* 获得Class类对象：
	1. Object类中的getClass（）：返回一个Class类型的实例
	2. 可以调用静态方法forName获得类名对应的Class对象
		String ClassName = “java.util.Random”；
		Class cl = Class.forName（className）；
		* 如果className不是类名或接口名，抛出checkedexception（已检查异常）
		* 使用这个方法必须提供一个异常处理器
	3. T.class代表匹配的类对象（T是任意的Java类型或者 void 关键字）
		* 一个Class对象实际上表示的是一个类型，而该类型未必是类（ int.class ）
* 最常用的Class方法是getName：返回类的名字（如果类在包中，包名也作为类名的一部分）
	警告：历史原因，getName在用于数组类型时，会返回一个奇怪的名字
* Class类实际上是泛型类（T.class = Class<T>），一般省略
* 可以使用 == 实现两个类对象的比较操作
if（ e.getClass() == T.class ）...

#### 5.7.3 利用反射分析类的能力
* java.lang.reflect包中的三个类Field、Method、Constructor分别描述域、方法和构造器
* getName：返回项目名称
* getType（Field中）：返回描述域所属类型的Class对象
* getModifiers：返回一个整型数值，用不同的位开关描述修饰符使用状况（public、static...）
用reflect包中的Modifier类的静态方法分析上述返回值：isPublic、isPrivate...
Modifier.toString：打印修饰符
* Class类中的getFields、getMethods和getConstructors：分别返回类提供的public域、方法和构造器数组（包括超类的公有成员）
* Class类的getDeclareFields、getDeclareMethods和getDeclaredConstructors：返回类中声明的全部域、方法和构造器（包括私有和受保护成员，但不包括超类的成员）