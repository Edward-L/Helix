# Helix
Helix（双螺旋）
这个项目希望能够实现一个远程调试工具。最近要在Linux上对一些大型程序进行分析，发现目前主流的gdb使用起来不够智能和方便，没有在Windows下的od和mdebug之类的好用，所以想要自己实现一个更加友好，方便的调试工具。
初步的设想是，整个工具分为服务端和用户端，服务端会部署在linux上，利用gdb或者ptrace，完成调试功能。客户端可以根据平台的不同打包成不同的版本，目前主要想在windows上部署。两端通过socket连接，主要在windows下实现一个友好的界面，能够清晰的方便的进行调试。
##Todo List
1.完成客户端和服务端的基础通信
2.完成客户端的简答的界面显示
3.对gdb进行封装，基本实现od（Mdebug）上所有的功能：
 * 汇编的即时回显
 * 实现gdb自定义的脚本编程
 * 实现单步进入，单步步过，函数返回
 * 执行，重新开始，停止等功能
 * 即时查看内存，寄存器，堆栈调用等
 * etc...
