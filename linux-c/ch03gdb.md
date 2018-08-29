# gdb

<!-- TOC -->

- [gdb](#gdb)
    - [1、调试的基本思路](#1调试的基本思路)
    - [2、单步执行和跟踪函数调用](#2单步执行和跟踪函数调用)
    - [3、断点](#3断点)
    - [4、观察点](#4观察点)

<!-- /TOC -->

## 1、调试的基本思路

分析现象->假设错误原因->产生新的现象去验证假设

## 2、单步执行和跟踪函数调用

|命令|描述|
|-|-|
|backtrace(bt)|查看各级函数及调用|
|finish|连续运行到当前函数返回为止，然后停下来等待|
|frame(f)|选择帧栈|
|info(i) locals|查看当前帧栈局部变量的值|
|list(l)|列出源码，每次10行|
|next(n)|执行下一行语句|
|print(p)|打印表达式的值|
|quit(q)|退出gdb|
|set var|设置变量的值|
|start|开始执行程序|
|step(s)|执行下一行语句，如果有函数调用，进入函数|

## 3、断点

|命令|描述|
|-|-|
|break(b)行号 |在某一行设置断点|
|continue(c) |从当前位置开始连续运行程序|
|delete breakpoints 断点号 |删除某个断点|
|display 变量名 |跟踪某个变量，每次停下都显示它的值|
|disable breakpoint 断点号 |禁用某个断点|
|enable 断点号 |启用某个断点号|
|info(i) points |查看设置了哪些断点号|
|run(r) |从头开始连续运行程序|

## 4、观察点

|命令|描述|
|-|-|
|watch |设置观察点|
|info(i) watchpoints |查看当前设置的观察点|
|x |从某个位置开始打印，不区分哪个字节属于哪个变量|