### 简介

Object 类自 jdk1.0 就引入了，其他所有类都继承自Object。

该类的源码比较少：一个 static 代码块 & 几个 native 方法。

* [源码]([](https://docs.oracle.com/javase/8/docs/api/java/lang/Object.html))
* UML图：

![](https://wangyt-imgs.oss-cn-beijing.aliyuncs.com/blog/java%E6%BA%90%E7%A0%81/Object/001.png)

### 知识点梳理

乍一看没啥代码，其实涉及的知识点挺多，这里简单梳理下：

**static 关键字的用法**

1. 修饰类、方法、变量
2. 静态导包
3. 静态变量在内存中的位置（需要学习jvm内存相关知识）

**jni**

全称 java native interface ，用来支持 java 和 c/c++ 交互的，做 ndk 相关的开发需要学习。

**hashCode() & equals()**

这俩方法放一起主要是因为子类覆写时，最好同时覆写两者，尽量避免只覆写其中一个，否则会出问题（比如使用HashSet存储子类对象时）。

**clone()**
 
 1. 使用场景
 2. 浅拷贝、深拷贝

**wait() & notify()**

用来支持线程间通信的，这只是线程间通信的一种方式，还有很多工具和途径实现，需要学习多线程和并发方面的知识。

**finalize()**

java 对象被 gc 回收时的一个方法，需要学习 jvm gc 相关的知识。

### 总结

该类代码虽然不多，但是涉及的知识点是很多的，这里简单做了梳理，后面可以对上面的知识点，分别进行深入学习。