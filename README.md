# Sword_offer
> 《剑指offer》题目练习及笔记
>
> 没到面试题包含：
>
> 1. 官方答案程序：大写字母开头
> 2. 自己编写程序：小写字母开头
> 3. notes.m：记录的笔记、易错点

[TOC]

## 面试题 1：

- 参考网页 [面试题1：复制运算符 - JudgeGong - CSDN博客](https://blog.csdn.net/qq_30483585/article/details/79414675)
- 字符串指针初始化时赋值无错无警告 用这个 `char test[] = "hello";`
- 注意 cout  的使用

```c++
cout << test << endl; //输出的是 hello
cout << *test << endl; //输出的是 h
```

- 异常安全性原则（Exception Safety）：

  指程序运行有问题，但不会破坏已有的数据。

##面试题3

- 注意 break 不能连着写，因为执行第一个 break 时，第二个就不执行了。

- 思路：搜索：多想着二分法 $log(n)$ 

## 面试题4

- 注意 `vector<cector<int> >` 有个空格，不然报错。
- 声明不能写在 if 和 else 里面。

- 思路:既然有顺序，那就依然想着从中间搜索。二分法思想。

## 面试题5

- \0 和 空格不一样，空格是一个字符，ASCII 码是32；\0 是空字符，代表字符串的结束，ASCII 码是0。
- 连续输入两个 vector，在两个中间要加

```c++
cin.clear();
cin.get();
```

- vector 注意 size 和 capacity，test.cpp 帮助理解。
- 动态数组没有长度，静态数组长度求法：`sizeof(nums)/sizeof(nums[0])`
  但是初始化时必须有长度：`int* nums = new int[10]; delete[] nums;`，test.cpp 帮助理解。

## 面试题6

- List 的尾部添加和删除某一个，都必须传入 ListNode**
- struct 具有默认的构造函数，`ListNode* a=new ListNode();`，`ListNode* b=new listNode;`，a 调用了默认构造函数，而 b 没有，a 中的成员具有初始值，但是 b 没有，b 必须在后面给值。

## 面试题7

- 树本身就是递归构建的，因此很多操作可以使用递归进行
- 递归--循环
- 三种遍历的 6 种实现方法

##面试题 8

- 也不是所有树都用递归做方便，画出树找规律
- 一个函数尽量不要写多个 return

## 面试题9

两个栈实现队列的加一个，减一个

- 队列：双通口单操作
- 栈：单通口双操作
- 队列尾部加一个 -》 栈尾部操作 -》 stack1
- 队列头部减一个 -》 栈头部操作 -》 stack2
- 要点：stack1 与 stack2 相反，一个倒序，一个正序
- 因此，可以想象 stack1 与 stack2 连接起来行成队列

### 思考题

- 要把栈的压入和弹出分开解决

## 面试题10

- 写结构的构造函数时，记得要给默认值，否则无法初始化一个没有初值的结构对象.
- 结构可以赋值，说明有默认的拷贝构造函数.





