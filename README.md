# coroutine-library
本项目参考开源项目sylar服务器框架，专注于协程库部分的改编和简化。通过引入协程、调度器和定时器等核心模块，利用HOOK技术将Linux系统中的传统同步函数（如 sleep、read、write 等）转化为异步版本。此改造允许保持同步I/O的编程方式，同时享受异步执行的效率和响应速度提升
# 协程类
使用非对称的独立栈协程。
支持调度协程与任务协程之间的高效切换。
# 调度器
结合线程池和任务队列维护任务。
工作线程采用FIFO策略运行协程任务，并负责将epoll中就绪的文件描述符事件和超时任务加入队列。
# 定时器
利用最小堆算法管理定时器，优化超时回调函数的获取效率。
# 关键技术点
1、线程同步与互斥
2、线程池管理
3、epoll的事件驱动模型
4、Linux网络编程
5、泛型编程
6、同步与异步I/O
7、HOOK技术
