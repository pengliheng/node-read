# node单线程与事件循环
 ## node单线程
 ### 什么是线程和进程
 #### 概念
 - 线程是CPU独立运行和独立调度的基本单位；
 - 进程是资源分配的基本单位；
两者的联系：进程和线程都是操作系统所运行的程序运行的基本单元。
区别：
 - 进程具有独立的空间地址，一个进程崩溃后，在保护模式下不会对其它进程产生影响。
 - 线程只是一个进程的不同执行路径，线程有自己的堆栈和局部变量，但线程之间没有单独的地址空间，一个线程死掉就等于整个进程死掉。

#### 总结
  node如果是单线程，那么一个nodeApp即是一个单线程进程，线程是进程的子集，一个进程必须含有一个或多个线程
### node单线程
 node单线程即是它主线程是线程,这个线程是用来js的解析和加载用的，而其他线程如处理请求的线程，处理IO的线程,加密解密的线程
