---
title: Clean Code
tags: 后端
---

### 第二章 有意义的命名

1. 有意义的区分
2. 避免冗余
3. 使用读的出来的名称（而非自造词）

### 第三章 函数

1. 每个函数一个抽象层级
2. 函数参数应尽可能少，否则测试的参数难写。

### 第四章 注释

1. 几种可行的注释

TODO注释

```jsx
// TODO: These are not needed
// We expect this to go away when we do the checkout model
```

放大某种看起来不合理之物的重要性

```jsx
String listItemContent = match.group(3).trim();
// the trim is real important. It removes the starting
// spaves that could cause the item to be recognized
// as another list
```

警示

对意图的解释

1. 直接把代码注释掉会让别人觉得依然放在那里可能很重要。

### 第五章 格式

1. 垂直方向上的区隔：
    - 封包声明、导入声明和每个函数间都有空白行隔开。 每个空白行是一条线索，标示出新的独立概念。
    - 被调用的函数应该放在执行调用的函数下面
2. 横向格式：
    - 空格字符： 乘法因子间没有空格，因为乘法具有较高优先级。加减法用空格隔开，因为优先级低。
        - 赋值操作符周围加上空格，达到强调目的。
        - 函数调用括号中的参数一一隔开，表示参数是互相分离的。


### 第九章 单元测试