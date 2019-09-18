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

   在删除链表结点时， 需要先将结点指向空，然后在free结点，而不是直接free该结点，因为删除的意思是让节点不再链接到链表中，但如果让前驱结点指向需要删除结点之后就直接free该结点的话只是没有了该结点堆内存的使用权，但结点内未指向空的指针可能还是指向链表中，
   所以真正的删除结点是让前驱结点指向需要删除结点之后将要删除结点的next指针指向NULL，若后续需要用到该结点则可以先不free，若后续不需要用到则可直接free。

   ————————————————
   版权声明：本文为CSDN博主「DiuDiuZ」的原创文章，遵循 CC 4.0 BY-SA 版权协议，转载请附上原文出处链接及本声明。
   原文链接：https://blog.csdn.net/weixin_43443402/article/details/97367960



4. 