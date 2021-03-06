
## 冯诺依曼邻居问题（递推关系）

### 代码

[冯诺依曼邻居问题（递推关系）代码](Neumann2_4_12.cpp)

### 问题说明

某算法从一个1×1的方格开始，每次都会在上次图形的周围再加上一圈方格，在第n次的时候要生成多少个方格？下图给出了n = 0，1，2是的结果。

![](http://ojlsgreog.bkt.clouddn.com/NeumannNeighborProblem.jpg)

### 功能说明

本程序使用递推关系求解。

### 代码简述

若设第n次生成的方格数是a(n)，则：

a(1) = a(0) + 4 * 1
a(2) = a(1) + 4 * 2
a(3) = a(2) + 4 * 3
...
a(n) = a(n-1) + 4 * n

则可得：

a(n) = a(n - 1) + 4 * n  

然后在代码中使用递归法，递归结束条件为n = 0，即

if (n == 0) return 1;

则可写出递归法的代码。

在程序中用Neumann2_4_12函数进行递归求解。