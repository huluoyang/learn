---
title: Introduction to the Debugging Challenges
block: Debugging
superBlock: JavaScript Algorithms and Data Structures
---
## Introduction to the Debugging Challenges

对程序员来说，调试是一种非常有用并且必不可少到技能。在测试阶段，通过调试检查代码是否按预期执行。调试就是找 bug 然后修复 bug 的过程。你花时间写了一段漂亮的代码，感觉良好很难看出有错误。 代码中的错误通常有三种情形：1）语法错误导致程序停止运行，2）代码无法执行或具有意外行为导致运行时错误，以及 3）代码有语义（逻辑）错误，没有实现原来的意图。

主流的代码编辑器（还有你的经验）可以帮你发现语法错误。语义和运行时错误会难找一点。这些错误可能会导致程序崩溃，死循环，或者输出错误的结果。调试就是去理解代码为什么会出现这样的错误。

语法错误的示例 - 通常会被代码编辑器检测到：

```
funtion willNotWork( {
  console.log("Yuck");
}
// "function" 关键字拼写错误而且在最后缺少括号
```

以下是运行时错误的示例 - 通常在程序执行时检测到：

```
function loopy() {
  while(true) {
    console.log("Hello, world!");
  }
}
// 调用 loopy 函数会进入一个死循环，这可能会导致浏览器崩溃。
```

语义错误的示例 - 通常在测试代码输出结果时被检测到：

```
function calcAreaOfRect(w, h) {
  return w + h; // 应该是 w * h
}
let myRectArea = calcAreaOfRect(2, 3);
// 语法和执行过程都没错，但是结果是错的。
```

调试本身总是令人沮丧的，但它有助于让你学会一种逐步检查代码的方法。这意味着你要去检查中间值和变量类型，看看它们是否是你所期望的。在这过程中，运用排除法，你很快就能找到问题的所在。

举个例子：你可以直接从整段代码的中间开始检查代码中的值，将检查的区间先排除一半，如果出现了 bug 说明代码前半部分存在错误，反之，说明代码后半部分存在错误。

本节将介绍一些有用的工具来查找 bug，以及常见的使用情形。 好消息是，调试并不难，只需花一点时间练习就能掌握。


