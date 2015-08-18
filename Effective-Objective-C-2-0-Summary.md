title: "Effective Objective-C 2.0 总结"
date: 2015-06-23 10:09:46
tags: iOS
---
《Effective Objective-C 2.0》超级经典的一本OC进阶的书，买了有一年了，平时只是随手翻翻，而且终究没有仔细地看完，今天试图用写篇博客的方式，去读一本书:)全书共7章、列出了52条相关的总结，那我就一条条来记录喽.  
<h5 id="1">Chapter 1: Accustoming Yourself to Objective-C</h5>
<h6 id="1.1">Familiarize Yourself with ObjectiveC's Roots</h6>
Objective-C由Smaltalk演化而来，而其是消息型语言的鼻祖.Objective-C的对象总是分配在堆空间(heap)上.
<h6 id="1.2">Minimize Importing Headers in Headers</h6>
在类的头文件中尽量少引入其他头文件.如果不是继承某个超类，可以使用“向前声明”(forward declaring)的方式,即在头文件中用@class来导入.这样可以告诉编译器有某个方法或属性，但无需知道其中的细节，可以节省编译时间且有时候还可以防止循环引用.  
<h6 id="1.3">Prefer Literal Syntax over the Equivalent Methods</h6>
多用字面量语法，少用等价方法.比如NSNumber *someNumber = @1;要好过NSNumber *someNumber = [NSNumber numberWithInt:1];
<h6 id="1.4">Prefer Typed Constants to Preprocessor #define</h6>
多用类型常量，少用#define预处理命令.当我们定义一个#define HELLO 11时,所以引入该头文件的代码中有HELLO都会被替换成11.

