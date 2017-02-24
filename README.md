# dbg3
window 3 环下的单线程调试器.

## 调试器特点
- 控制台带高亮界面(好像这点并没有多么地特)
- 提供类C的条件表达式
- 框架式编程, 各个模块相对独立,编码便捷

---

## 程序的主要模块
- 调试器框架

> 主要建立了调试循环, 调用断点管理引擎来处理异常事件

- 断点管理引擎

> 主要管理断点.
> 断点由各个断点模块提供功能.
>`BPObject`作为基类,当添加特定类型的断点时,都从这个基类中派生出子类.

- 反汇编引擎(使用其他库)
- 汇编引擎(使用其他库)
- 表达式
- 显示模块

## 常见编译错误
由于编码问题会导致一些错误, 在vs2013中,默认的文件编码是gb2312, 当我在github网页中直接修改文件时,导致文件编码变成了utf-8, 因此造成了编码的一些故障,导致在编译时无法通过, 现已修复. 
