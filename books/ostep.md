# Operator System Three Easy Pieces

- 虚拟化（virtualization）

  - 虚拟化CPU
    时间片，中断，进程状态. 如何调度?
  - 虚拟化内存
    每个进程访问自己的私有虚拟地址空间（virtual address space）
    操作系统以某种方式(快表)映射到机器的物理内存上，当然操作系统得高效管理真实的物理内存

- 并发（concurrency）
  对多线程CRUD某一个共享变量

- 持久性（persistence）
  内存快但不持久，磁盘慢但持久,如何设计让它能用，并且安全高效

## 进程的状态

- 创建
- 销毁
- 等待
- 其他控制
- 状态
  - 运行：进程正在处理器上运行，正在执行指令。
  - 就绪：进程已准备好，但不在此时运行。
  - 阻塞：进程执行了某种操作，直到其他事件时才会准备运行。

## 进程 API

- fork() 创建新进程
- exec() 替换当前进程
- wait() 等待子进程结束

## 指令受限执行

- 操作系统限制进程的指令执行，如fork()，exec()，wait() 必须陷入操作系统
- 等待时钟中断
- 上下文切换

## 进程调度

- FIFO(First In First Out)
- SJF(Shortest Job First)
- STCF(Shortest Time to completion First)
- MLFQ(Multi-Level Feedback Queue)
- 彩票调度
- 步长调度
- SQMS(Single Queue Multiprocessor Scheduling)
- MQMS(Multi-Queue Multiprocessor Scheduling)
