# 1.对象的创建流程

![图片](../img/J5.png)


32位对象头

![图片](../img/J7.png)
64位对象头

![图片](../img/J8.png)

# 2.JVM内存模型

![图片](../img/J6.png)

    🚀 堆（Heap）：线程共享。所有的对象实例以及数组都要在堆上分配。回收器主要管理的对象

    🚀 方法区（Method Area）：线程共享。存储类信息、常量、静态变量、即时编译器编译后的代码, 
        JDK1.8之后改为元数据区

    🚀 方法栈（JVM Stack）：线程私有。存储局部变量表、操作栈、动态链接、方法出口，对象指针

    🚀 本地方法栈（Native Method Stack）：线程私有。为虚拟机使用到的Native 方法服务。
        如Java使用c或者c++编写的接口服务时，代码在此区运行

    🚀 程序计数器（Program Counter Register）：线程私有。有些文章也翻译成PC寄存器（PC Register），
        同一个东西。它可以看作是当前线程所执行的字节码的行号指示器。指向下一条要执行的指令。











