
<a href="#title1">1.什么是Redis？它主要用来什么的？</a>

<a href="#title2">2.Redis的基本数据结构类型</a>

<a href="#title3">3.Redis是单线程吗？</a>

<a href="#title4">4.Redis 单线程为什么还能这么快？</a>

<a href="#title5">5.Redis 单线程如何处理那么多的并发客户端连接？</a>

# <h2 id="title1">1.什么是Redis？它主要用来什么的？</h2>

    Redis，英文全称是Remote Dictionary Server（远程字典服务），
    是一个开源的使用ANSI C语言编写、支持网络、可基于内存亦可持久化的
    日志型、Key-Value数据库，并提供多种语言的API。

    与MySQL数据库不同的是，Redis的数据是存在内存中的。它的读写速度非
    常快，每秒可以处理超过10万次读写操作。因此redis被广泛应用于缓存，
    另外，Redis也经常用来做分布式锁。除此之外，Redis支持事务、持久化、
    LUA 脚本、LRU 驱动事件、多种集群方案。

# <h2 id="title2">2.Redis的基本数据结构类型</h2>

    Redis有以下这五种基本类型：
    
    String（字符串）
    Hash（哈希）
    List（列表）
    Set（集合）
    zset（有序集合）

# <h2 id="title3">3.Redis是单线程吗？</h2>

    Redis 的单线程主要是指 Redis 的网络 IO 和键值对读写是由一个线程来完成的，
    这也是 Redis 对外提供键值存储服务的主要流程。但 Redis 的其他功能，比如
    持久化、异步删除、集群数据同步等，其实是由额外的线程执行的。

# <h2 id="title4">4.Redis 单线程为什么还能这么快？</h2>

    因为它所有的数据都在内存中，所有的运算都是内存级别的运算，而且单线程避免了
    多线程的切换性能损耗问题。正因为 Redis 是单线程，所以要小心使用 Redis 
    指令，对于那些耗时的指令(比如keys)，一定要谨慎使用，一不小心就可能会导致 Redis 卡顿。

# <h2 id="title5">5.Redis 单线程如何处理那么多的并发客户端连接？</h2>

    Redis的IO多路复用：redis利用epoll来实现IO多路复用，将连接信息和事件放到队列中，
    依次放到文件事件分派器，事件分派器将事件分发给事件处理器。

![图片](redis1.png)


