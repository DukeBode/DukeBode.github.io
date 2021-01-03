---
title: 汇编语言基础
date: 2018-11-10 16:15:47
tags:
- Assembly
---

<!-- more -->

# PC 硬件的基本特征


## 1、计算机存储单位

1. 位 bit(Binary digit))
    > 一个位表示 0 或 1
1. 字节
    > 一组 9 个相关的位称为字节，它代表内存储器和外部设备的一个存储单元
    - 每个字节由 8 个数据位和 1 个奇偶位组成（[奇偶校验]()）
    - 一个字节中的各位从右到左是按 0 到 7 编号的
    - 在存储器中的每个字节都有一个唯一的地址。第一个字节在最低的存储器单元中，编号为 0 ， 第二个字节编号为 1 
1. 字
    > 2 字节（16位）数据项
1. 双字
    > 4 字节（32位）数据项
1. 匹字
    > 8 字节（64位）数据项
1. 小段
    > 16字节（128位）区
1. 千字节（KB）
    > 2^10等于1024字节
1. 兆字节（MB）
    > 2^20等于1048576字节


## 2、二进制数系统

> 位的集合可以表示任何数字的值。
- 二进制数的值是由为 1 的位及其相关的位置所决定的。

位编号||11|10|9|8||7|6|5|4||3|2|1|0
-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-
位的值||1|1|1|1||1|1|1|1||1|1|1|1
位置的值||2048|1024|512|256||128|64|32|16||8|4|2|1


## 3、十六进制表示

十进制|二进制|十六进制|峘进制|huán
:-:|:-:|:-:|:-:|-
0|0000|0|零
1|0001|1|壹
2|0010|2|贰
3|0011|3|叁
4|0100|4|肆
5|0101|5|伍
6|0110|6|陆
7|0111|7|柒
8|1000|8|捌
9|1001|9|玖
10|1010|A|拾
11|1011|B|屲|wā
12|1100|C|亗|suì
13|1101|D|岌|jí
14|1110|E|岄|yuè
15|1111|F|岪|fú


## 4、PC 的组成

> PC 的主要组成部分是它的主板。它包括`处理器`、`协处理器`、`主存储器`、`接插件`以及为可选电路卡用的`扩展槽`。这些槽和接插件为下面部件提供了出入口，比如`只读存储器 ROM、随机存取存储器 RAM、硬盘、CD-ROM 设备、附加的主存储器、显示设备、键盘、鼠标、并行与串行设备、声音合成器以及高速缓冲存储器等`。处理器利用高速缓冲存储器，减少对较低速主存储器的访问。



1. 处理器

    > 处理器，也称中央处理器或 CPU ，用来完成所有的指令执行与数据处理。
    - 8088


### 段寄存器

标志|名称
--|-
CS|代码段(Code Segment)
DS|数据段(Data Segment)
SS|堆栈段(Stack Segment)
ES|附加段指针(Extra Segment)
FS|附加段指针
GS|附加段指针

### 通用寄存器

寄存器|名称|说明
-|-|-
EAX|主累加器(accumulator)寄存器
EBX|基址(base)寄存器
ECX|计数(count)寄存器
EDX|数据(data)寄存器
EDI|目的变址(Destination Index)寄存器
ESI|源变址(Source Index)寄存器
ESP|堆栈指针(Stack Pointer)寄存器
EBP|基址指针(Base Pointer)寄存器
EIP|指令指针(Instruction Pointer)寄存器|下一条指令的偏移地址


### 标志寄存器

位编号|符号|标志(Flag)|置位符号 1|复位符号 0
:-:|:-:|-|-|-
0|CF|进位(carry)标志|CY(carry)|NY(no carry)
1|1|
2|PF|奇偶校验(parity)标志|PE(parity even)|PO(parity odd)
3|0|
4|AF|辅助进位(auxiliary carry)标志|AC(auxiliary carry)|NA(no auxiliary)
5|0|
6|ZF|零(zero)标志|ZR(zero)|NZ(no zero)
7|SF|符号(sign)标志|NG(negative)|PL(plus)
8|TF|陷阱(trap)标志|
9|IF|中断允许(interrupt)标志|EI(enable interrupt)|DI(disable interrupt)
A|DF|方向(direction)标志|DN(down)|UP(up)
B|OF|溢出(overflow)标志|OV(overflow)|NV(no overflow)
C|IOPL|I/O 特权级(I/O Privilege Level)
D|IOPL|I/O 特权级(I/O Privilege Level)
E|NT|嵌套任务(Nested Task)标志
F|0|
10|RF|恢复(Resume)标志
11|VM|虚拟8086模式(Virtual 8086 Mode)
12|AC|对齐检查(Alignment Check)
13|VIF|虚拟中断(Virtual Interrupt)标志
14|VIP|虚拟中断挂起(Virtual Interrupt Pending)
15|ID|标志(Identification)标识