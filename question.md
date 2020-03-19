### 编程问题

1. IDEA注释中文字体错误
    解决方法：打开IDEA安装目录/jre32/lib，找到 fontconfig.properties.src，
    把开头为allfonts.chinese的语句值全部修改成需要的字体，例如 Microsoft YaHei
    allfonts.chinese-ms936=Microsoft YaHei ...

  

2. c实现链表  get（）方法

   ```
   //bug版本
   ElemType get(LinkedList *L, int index) {
       if (length == 0 || index < 0 || index >= length) return -1;
       LinkedList *prev = L;
       for (int i = 0; i < index; i++) {
           prev = prev->next;
       }
       return prev->data;
   }
   ```

   ```
   //正确版本
   ElemType get(LinkedList *L, int index) {
       if (length == 0 || index < 0 || index >= length) return -1;
       LinkedList *cur = L->next;
       for (int i = 0; i < index-1; i++) {
           cur = cur->next;
       }
       return cur->data;
   }
   ```

   背景：测试时，发现当index为0的时候，获取不到正确的元素

   debug心路历程：逐行观察代码，第3行的判断条件确定了链表不为空，第4行新建了一个和L指向相同地址的指针prev，prev指向头节点，当index为0时，第5行的for循环不执行，导致第8行返回的是头节点的数据域，而头节点本身并不储存数据（但数据域被初始化为0），所以导致了方法的错误输出

   改正：把指向头节点的指针改为指向链表第一个储存元素的节点，遍历至index处，返回数据域即可



3. C++：在删除链表节点时，需要先将该节点指向null，再去delete它

   在删除链表结点时， 需要先将结点指向空，然后在free结点，而不是直接free该结点，因为删除的意思是让节点不再链接到链表中，但如果让前驱结点指向需要删除结点之后就直接free该结点的话只是没有了该结点堆内存的使用权，但结点内未指向空的指针可能还是指向链表中，所以真正的删除结点是让前驱结点指向需要删除结点之后，将要删除结点的next指针指向NULL，若后续需要用到该结点则可以先不free，若后续不需要用到则可直接free。
   
4. 从控制台输入字符时，使用cin.get（）获取输入



5. 
* Clion进行文件读写时，不能使用相对路径，只能绝对路径

* Dev C++可以使用相对路径

  

6.c++ 如何让函数返回数组
	当函数里想返回的数组直接使用[]创建时，不能直接return的首地址（数组名/数组指针），因为函数中的变量为局部变量，在函数调用结束的时候会被回收，所以return的东西不是我们想要的数组首地址
	解决方法：创建数组时，使用new手动开辟内存空间，这块区域不会自动被回收



7. idea隐藏小技巧：复制光标

   按住鼠标中键，拖动光标，可以复制出多个光标，达到同时输入的效果



8. C++ max() 、min() 函数

   建议使用宏来实现，使函数具有重载功能（泛型）

   #define max（（a）>（b）?（a）：（b））

   #define min（（a）<（b）?（a）：（b））



9. Clion 控制台中文输出乱码
   1. setting---Editor---File Encodings
   2. ![image-20191214162903736](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20191214162903736.png)





10. C++ ：string转化为数字

    stoi(str): int

    stol(str): long

    stof(str): float

    stod(str): double