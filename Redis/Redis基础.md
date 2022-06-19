
<a href="#title1">1.什么是Redis？它主要用来什么的？</a>

<a href="#title2">2.Redis的基本数据结构类型</a>

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

    
