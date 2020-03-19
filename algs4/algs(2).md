[TOC]

### 1.2 数据抽象

* 数据类型：一组值和一组对这些值的操作的集合
* 抽象数据类型（ADT）不同之处：将数据和函数的实现关联，并将数据的表示方式隐藏起来
* Java所有数据类型都会继承 toString（）方法来返回用String表示的值，Java会在用 + 运算符将任意数据类型的值和String值连接时调用该方法，但该方法的默认实现并不实用（会返回用字符串表示的该数据类型值的内存地址）
* 对象是能够承载数据类型的值的实体
* 对象三大特性：
	1.状态：数据类型中的值
	2.标识：内存中的位置
	3.行为：数据类型的操作 
* 创建对象：new关键字
	1. 为新对象分配内存空间
	2. 调用构造函数初始化对象中的值
	3. 返回该对象的一个引用

* 变量关联的是指向对象的引用而并非值本身

* 引用类型的赋值会创建该引用的副本，本质还是引用，两个变量引用同一个对象

* 基本数据类型为不可变对象，如果作为方法的参数，传进去的只是值的拷贝（按值传递），影响不到本身的值

#### API和类库
* Point2D：P46    Interval1D/2D：P47
* 标准类库+本书自定义类库：P46

#### 字符串：String
* String : P49
* String对象的初始化：字符串字面量或者构造函数
* 连接：+运算符或者concat()方法

#### 典型的字符串处理
* 字符串切割：split（）  （参数\s+"：一个或多个制表符、空格、换行符或回车）
* 判断字符串是否为回文
```
    public static boolean isPalindrome(String s) {
        int N = s.length();
        for (int i = 0; i < N / 2; i++) {
            if (s.charAt(i) != s.charAt(N - 1 - i))
                return false;
        }
        return true;
    }
```

* 检查一个字符串数组中的元素是否已按照字母表顺序排序
```
    public boolean isSorted(String[] a) {
        for (int i = 1; i < a.length; i++) {
            if (a[i - 1].compareTo(a[i]) > 0)
                return false;
        }
        return true;
    }
```



* toString的默认实现会返回一个对象内存地址的字符串

#### equal（）模板

1. 如果该对象的引用和参数对象的引用相同，返回 true
2. 如果参数为空（null），返回false（还可以避免在下面的代码使用空引用）
3. 如果两个对象的类不同，返回false（getClass（）获取类，==判断）
4. 将参数对象的类型从Object转化为使用equal（）方法的对象的类型
5. 如果任意实例变量的值不同，返回false
代码：
```
    public boolean equals(Object x) {
        if (this == x) return true;
        if (x == null) return false;
        if (this.getClass() == x.getClass()) return false;
        ...
    }
```

#### 答疑

* java中易错、重要的的知识点，查漏补缺
* 详见P69~P71