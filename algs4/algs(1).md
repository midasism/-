

[TOC]

###  1.1 基础编程模型

#### java基础知识

* 标识符：由字母、数字、下划线和 $ 组成的字符串
* 字面量：值在源代码中的表示
* 程序：由一系列声明、赋值、条件、循环、调用和返回语句组成
* 标准输入流：程序读取后消失

  

####  数组常用操作

* 矩阵相乘（方阵） a[] * b[] = c[][]
	```
		int N = a.length;
	    double[][] c = new double[N][N];
	    for (int i = 0; i < N; i++) {
	        for (int j = 0; j < N; j++) {
	            //计算行i和列j的点乘
	            for (int k = 0; k < N; k++) {
	                c[i][j] = a[i][k] * b[k][j];
	            }
	        }
	    }
	
	
	```


​	
​	
#### 典型静态方法的实现

* 判断一个数是否是素数

```
  		public static boolean isPrime(int N) {
        	if (N < 2) return false;
        	for (int i = 2; i * i < N; i++) {
            	if (N % i == 0) return false;
        	}
        	return true;
	  	}
```




* 计算平方根（牛顿迭代法）

```
	public static double sqrt(double c) {
	if (c < 0) return Double.NaN;
	double err = 1e-15;
	double t = c;
	while (Math.abs(t - c / t) > err * t) {
		t = (c / t + t) / 2.0;
	}
	return t;
	}
```




* 计算调和级数

```
  	public static double H(int N) {
        double sum = 0.0;
        for (int i = 1; i <= N; i++) {
            sum += 1.0 / i;
        }
	      return sum;
	  }
```




#### 方法的性质
* 方法的参数按值传递：方法处理的是参数的值，而非参数本身
* 方法可被重载




#### 递归

* 递归总有一个最简单的情况——方法的第一条语句总是一个包含return的条件语句
* 递归调用总是去尝试解决一个规模更小的子问题，这样递归才能收敛到最简单的情况
* 递归调用的父问题和尝试解决的子问题之间不应该有交集
	
	
	
#### 基础编程模型

* 静态方法库：定义在一个Java类中的一组静态方法
	
* 模块化编程：通过静态方法库实现
	* 好处：
	1. 程序整体代码量很大时，每次处理的模块大小仍然适中
	2. 可以共享和重用代码而无需重新实现
	3. 很容易用改进的实现替换老的实现
	4. 可以为解决编程问题建立合适的抽象模型
	5. 缩小调试范围
	
* 建议每个静态方法库都包含一个main（）函数来测试方法



#### API（应用程序编程接口）
*记录方法的用法并供他人参考的文档
* 目的：将调用和实现分离 
* Math API（节选）

| public class Math                                            |                       |
| ------------------------------------------------------------ | --------------------- |
| static double abs(double a)                                  | a的绝对值             |
| static double max(double a,double b)                         | a和b中的较大者        |
| static double min(double a,double b)                         | a和b中的较小者        |
| 注：abs()、min()、max()也定义了int、long、float的版本        |                       |
| static double sin(double theta)、cos（）、tan（）            | 正弦、余弦、正切      |
| 注：角用弧度表示，可以使用toDegrees()和toRadians()转化角度和弧度 |                       |
| 注：反函数为：asin() 、acos() 、atan()                       |                       |
| static double exp(double a)                                  | 指数函数              |
| static double log(double a )                                 | 自然对数函数（log a） |
| static double pow(double a,double b)                         | 求a的b次方            |
| static double random()                                       | [0, 1）之间的随机数   |
| static double sqrt(double a)                                 | a的平方根             |
| static double E                                              | 常数e（常数）         |
| static double PI                                             | 常数π（常数）         |

| java.util.Arrays           |                |
| -------------------------- | -------------- |
| static void sort(type[] a) | 将数组升序排序 |


* 书中的方法库API：StdRandom(随机数)、StdStats(数据分析)       P18
StdOut(输出)    P22
StdIn(输入)     P24
StdDraw(绘图)   P26~P27
	
* String和数字之间转化

  | public class Integer          |                     |
  | ----------------------------- | ------------------- |
  | static int parseInt(String s) | 将字符串s转化为整数 |
  | static String toString(int i) | 将整数i转化为字符串 |


#### 命令和参数
* java类中的静态方法main（）：有一个String数组类型的参数args[]，数组内容是输入的命令行参数
* 操作系统常用指令

| 命令 | 参数           | 作用         |
| ---- | -------------- | ------------ |
| more | 任意文本文件名 | 打印文件内容 |

* 重定向和管道
	* 将标准输出重定向到文件中：java [java文件名] > [文件名]
	* 从文件中读取数据：java [java文件名] < [文件名] 
	* 管道（将一个程序的输出重定向为另一个程序的输入）：java [输出java文件名] | java [输入java文件名]


#### 二分查找
* 正常版本：
```
    public static int rank(int key, int[] a) {
        //数组必须是有序的
        int lo = 0;
        int hi = a.length - 1;
        while (lo <= hi) {
            //被查找的键要么不存在，要么必然存在于a[lo..hi]之中
            int mid = lo + (hi - lo) / 2;
            if (key < a[mid]) hi = mid - 1;
            else if (key > a[mid]) lo = mid + 1;
            else return mid;
        }
        return -1;
    }

```

* 递归版本
```
    public static int rank(int key,int[] a, int lo,int hi){
        if(lo>hi) return -1;
        int mid=lo+(hi-lo)/2;
        if      (key<a[mid]) return rank(key,a,lo,mid-1);
        else if (key>a[mid]) return rank(key,a,mid+1,hi);
        else                 return mid;
    }
```

#### 答疑

* java中易错、重要的的知识点，查漏补缺

* 详见P31~P32

