# ProducerConsumerSimulation
Linux下模擬生產者與消費者問題

## 題目要求
### 1.	实验目的
 熟悉 Linux 操作系统进程通信的系统调用
### 2.	实验内容
实现生产者和消费者问题。  
创建两个生产者进程和两个消费者进程：  
生产者进程 a 需要生成 10000 个整数，每次都将自己的进程号（用 getpid()函数获得）和生成的整数放入共享内存中（共享内存大小为 64Byte）。  
生产者 b 每次从 26 个英文字母中选一个，并将自己的进程号和选中的字母放入共享内存中，直到 26 个字母全部都选中。  
消费者进程 c 负责从共享内存中读取数据生产者进程 a 的数据并且将这些数据写入文件 a.out。  
消费者进程 d 从共享内存读取进程 b 的数据后写入 b.out 中。  
## 實驗環境
Ubuntu 14.04
gcc version 4.8.4
 
## 實驗結果
![](https://raw.githubusercontent.com/Jaxx9527/ProducerConsumerSimulation/refs/heads/main/image.png)  
在本次实验中使用到了共享数据结构、信号量初始化、P/V  操作、生产者和消费者逻辑，以及进程间通信资源的创建与清理等操作。  
熟悉了 Linux 下进程间通信系统调用，包括 shmget、shmat、shmdt、shmctl 等共享内存函数，以及 semget、semop、 semctl  等信号量函数。  
同时也让我对多生产者多消费者问题有了更深入的掌握。

