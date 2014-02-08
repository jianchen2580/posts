title: Python Translation
date: 2014-02-08 10:55:44
tags:
---

The book is based on an MIT course that has been offered twice a year since
2006. The course is aimed at students with little or no prior programming
experience, but who have a need (or at least a desire) to understand
computational approaches to problem solving. Each year, a few of the students
in the class use the course as a stepping stone to more advanced computer
science courses. But for most of the students it will be their only computer
science course.

本书是基于MIT的一门课程， 该课程每年开课两次。该课程针对于那些具备少量或者没有编程经验，但是需要（或至少希望）理解解决问题的计算方法。每年都有一些学生利用该课程作为学习更进一步计算机课程的基础。但是对大多学生而言，该课程将是他们唯一的计算机科学课程。

Because th e course will be the only computer science course for most of the
students, we focus on breadth rather than depth. The goal is to provide
students with a brief introduction to many topics, so that they will have an idea
of what's possible when the time comes to think about how to use computation
to accomplish a goal. That said, it is not a "computation appreciation" course.
It is a challenging and rigorous course in which the students spend a lot of time
and effort learning to bend the computer to their will.

因为该课程将是大多数学生唯一的计算机科学课程，所以我们注重广度而不是深度。**本书目标是简要介绍许多主题，所以学生将要了解当利用计算完成一个目标时什么是可能的**。那就是说，这不是一个“计算欣赏”课程。它是一个具有挑战性的严格的课程，学生需要花费大量的时间和精力学习如何让计算机服从自己的意愿。

The book is a bit eccentric. Part 1 (Chapters 1-8) is an unconventional
introduction to programming in Python. We braid together four strands of
material:

• The basics of programming,
• The Python programming language,
• Concepts central to understanding computation, and
• Computational problem solving techniques.


本书有点古怪。第一部分（1-8章）以非常规的方式介绍了Python编程。 

* 编程基础
* Python编程语言
* 理解计算的核心概念
* 解决计算问题的技巧

We cover most of Python's features, but the emphasis is on what one can do with
a programming language, not on the language itself. For example, by the end of
Chapter 3 the book has covered only a small fraction of Python, but it has
already introduced the notions of exhaustive enumeration, guess and check
algorithms, bisection search, and efficient approximation algorithms. We
introduce features of Python throughout the book. Similarly, we introduce
aspects of programming methods throughout the book. The idea is to help you
learn Python and how to be a good programmer in the context of using
computation to solve interesting problems.

本书覆盖了大多数Python的特性，但是着重于我们能用编程语言实现什么，而不是语言自身。到第三章末为止，本书只是覆盖了少部分的Python内容，但是已经介绍了完全枚举（exhaustive enumeration）的概念，猜测核对（guess and check)算法，二分搜索（bisection search）和高效近似（efficient approximation）算法.
编程方法的诸貌与Python特性的介绍贯穿全书。帮助你学习Python并且在使用计算解决一些有趣问题上成为一个好的程序员。

Part 2 (Chapters 9-16) is primarily about using computation to solve problems.
It assumes no knowledge of math ematics beyond high school algebra, but it
does assume that the reader is comfortable with rigorous thinking and not
intimidated by mathematical concepts. It covers some of the usual topics found

第二部分（9-16章）是主要关于使用计算解决问题。本书假设您不具备高中代数之上的数学能力， 但是本书假设读者接受严谨的思维和不惧怕数学概念。本书涵盖了一些常见主题。

# 入门

A computer does two things, and two things only: it performs calculations and it
remembers the results of those calculations. But it does those two things
extremely well. The typical computer that sits on a desk or in a briefcase
performs a billion or so calculations a second. It's hard to image how truly fast
that is. Think about holding a ball a meter above the floor, and letting it go. By
the time it reaches the floor, your computer could have executed over a billion
instructions. As for memory, a typical computer might have hundreds of
gigabytes of storage. How big is that? If a byte (the number of bits, typically
eight, required to represent one character) weighed one ounce (which it doesn 't),
100 gigabytes would weigh more than 3,000,000 tons. For comparison, that's
roughly the weight of all the coal produced in a year in the U.S.
  
计算机做并且只做两件事情： 执行计算并且存储计算结果。计算机擅长于这两件事。典型的计算机是位于桌面或者手提包中，每秒钟执行10亿次左右的计算。我们很难想象它是如此快。想像将球举离地板一米，然后让球掉落，在球落地的这一短短时间里头，你的电脑已经执行了超过一亿次指令。
至于存储， 一个典型的电脑可以有几百G的存储空间。这是有多大呢？如果一个字节（bits的数量， 一般是8个，表示一个字）重一盎司（which it doesn‘t），100G将重达3，000，000吨。相比之下，这大约是美国一年的煤炭产量。

For most of human history, computation was limited by the speed of calculation
of the human brain and the ability to record computational results with the
human hand. This meant that only the smallest problems could be attacked
computationally. Even with the speed of modern computers, there are still
problems that are beyond modern computational models (e. g., understanding
climate change), but more and more problems are proving amenable to
computational solution. It is our hope that by the time you finish this book, you
will feel comfortable bringing computational thinking to bear on solving many of
the problems you encounter during your studies, work, and even everyday life.
 
对于大多数人类历史来说， 计算限制于人类大脑运算的速度和存储运算结果的能力。这意味着只有计算上着手最小的问题。甚至于以现在的计算机速度，依然存在超出现代计算模型的问题（例如，了解气候变化），但是越来越多的问题被证实存在适合的计算方案。我们希望在你完成本书后能收获如何使用计算思维解决一些学习，工作和日常生活中的问题。

What do we mean by computational thinking？

什么是计算思维？

All knowledge can be thought of as either declarative or imperative. Declarative
knowledge is composed of statements of fact. For example, "the square root of x
is a number y such that y•y = x." This is a statement of fact. Unfortunately it
doesn 't tell us how to find a square root.

Imperative knowledge is "how to" knowledge, or recipes for deducing
information. Heron of Alexandria was the first to document a way to compute
th e square root of a number 2 His meth od can be summarized as:
• Start with a guess, g,
• If g•g is close enough to x , stop and say that g is the answer
• Otherwise create a new guess, by averaging g and x/g, i.e. (g + x/g)/2
• Using this new guess, which we again call g, repeat the process until g•g
is close enough to x.

考虑以下例子：求25的平方根

* 1. g赋一任意值，例如3;
* 2. 3*3=9，离25偏差较大.
* 3. 赋值g=(3+25/3)/2=5.663.
* 4. 5.66*5.66=32.04，离25依然偏差较大
* 5. 赋值g=(5.66+25/5.66)/2=5.04
* 6. 5.04*5.04=25.4，25.4已经足够接近25，所以我们宣告5.04充分逼近25的平方根。

Note that the description of the method is a sequence of simple steps, together
with a flow of control that specifies when each step is to be executed. Such a
description is called an algorithm4. This algorithm is an example of a guess-
and-check algorithm. It is based on the fact that it is easy to check whether or
not a guess is a good one.

A bit more formally, an algorithm is a finite list of instructions that describe a
computation that when executed on a provided set of inputs will proceed
through a set of well-defined states and eventually produce an output.


请注意，方法的描述是由一系列简单的步骤组成，结合具体说明每一步执行的控制流。该描述称为算法。以上算法是一个简单的猜测-检查算法（guess-and-check algorithm）。它是基于容易判断猜测是否是一个好的猜测这一事实。
正式一点的表述，算法是一个表示为有限长列表的指令，它描述一组运算，在提供一组的输入下执行并通过一组良好定义的状态并最终生成一个输出。

An algorithm is a bit like a recipe from a cookbook,
1. Put custard mixture over heat.
2. Stir.
3. Dip spoon in custard.
4. Remove spoon and run finger across back of spoon.
5. If clear path is left, remove custard from heat and let cool.
6. Otherwise repeat.

一个算法类似烹饪书籍上的一个菜谱，
* 1. 加热奶油蛋羹
* 2. 搅拌
* 3. 用勺舀起奶油蛋羹
* 4. 移除勺子，Remove spoon and run finger across back of spoon.
* 5. if clear path is left,停止加热并让奶油冷却 remove custard from .
* 6. 其它情况下重复以上过程

It includes some tests for deciding when the process is complete, as well as
instructions about the order in which to execute instructions, sometimes
jumping to some instruction based on a test.

So how does one capture this idea of a recipe in a mechanical process? One way
would be to design a machine specifically intended to compute square roots.
Odd as this may sound, in fact the earliest computing machines were fixed-
program computers, mean ing they were designed to do very specific things, and
were mostly tools to solve a specific mathematical problem, e.g., to compute the
trajectory of an artillery shell. One of th e first computers (built in 1941 by
Atanasoff and Berry) solved systems of linear equations, but cou ld do n othing
else. Alan Turing's bombe machine, developed during WWII, was designed strictly
for the purpose of breaking German Enigma codes. Some very simple computers
still u se this approach . For example, a four-function calcu lator is a fixed-
program computer. It can do basic math ematics, but it cannot be used as
a word processor or to run video games. To change the program of such a
machine, one has to replace th e circuitry.

为了判定过程是否完成，算法需要包括一些测试，以及指令顺序的说明, 有时候需要基于测试执行指令跳转。

如何在这一个机械般的过程中提炼出食谱？一种方法是设计一个机器专门用于计算平方根。听起来可能觉得奇怪，事实上最早的计算机是固定程序计算机，意味着它是设计目的是实现非常特定的事情，大多是解决一个特定数学问题的工具，例如计算炮弹轨迹。
最早计算机中的一个（Atanasoff and Berry 建于1941)，它用于解线性方程, 但是做不了其它事情。 Alan Truing's bombe machine, 开发于二战时期，设计用来破解德国Enigma codes. 一些非常简单的计算机目前仍然用于该目的。 例如， a (four-function) 计算器is a fixed-program computer. 它能完成基本的数学运算，
但是不能用于字处理或者执行视频游戏。改造类似的机器， 需要更换电路。


第一台真正意义上的现代计算机当属Manchester Mark 1.5。与以往的计算机的区别在于它是一台存储程序式计算机（
stored-program computer）。这一类型的计算机能够存储和使用一些列的指令，还会有一些组件能够执行其中任何指令。通过创建指令集架构，以及把计算的过程详细地描述为一系列计算机指令，一台非常灵活的机器就可以被制作出来。把那些指令同数据以相同的方式同等对待，存储数据式计算机可轻易地更改程序，同时还可以在程序的控制下去这样做。事实上，计算机的核心就变成了能够执行任何合法的指令集合的程序（称其为解释器），这样它就可以被用于计算能够用一些基本的指令集合描述的任何事情。

程序和数据都驻留在内存中。通常会有一个程序计数器指向内存中的某个特定的位置，计算过程就是从这个位置开始执行指令。多数情况下，解释器会在指令序列中简单地一个接一个地执行指令，但不总是这样。有时，它会做一些测试，根据测试的结果，执行的过程会跳转到指令序列的另外的地方。这被称作控制流，是我们撰写完成复杂任务的程序所不可或缺的。

回到那个食谱的比喻，好的厨师能够在给定的一组食材中，以各种不同的方式组合它们烹饪出许多可口的菜肴。相似地，在给定的一组固定数量的基本元素中，好的程序员同样可以生产出大量有用的程序。This
is what makes programming such an amazing endeavor.

为了创建食谱，或者指令序列，我们需要一种编程语言来描述这些事情，让计算机整装待发。

1936年，英国数学家阿伦图灵描述了一台假设（hypothetical）的计算设备，将其称作通用图灵机（Universal Turing
machine）。该机器以磁带的形式拥有无限的存储空间，任何人可以写任意数量的零和一，和一些非常简单的基本指令，用以移动、读取和向磁带写入。邱奇-图灵论题（Church-Turing
thesis）阐明如果一个函数是可计算的，那么图灵机就可以被编程把它算出来。

“If”在邱奇-图灵论题中是很重要的。不是所有的问题都有计算解（computational
solution）。例如，图灵展示了不可能写出任意一个程序，当且仅当它将永久运行的时候输出真值。这就是广为认知的停机问题（halting
problem）。

邱奇-图灵论题直接引出了图灵完备性的概念。如果一种编程语言能够模拟一个通用图灵机，那么它就被认为是图灵完备的。所有现代的编程语言都是图灵完备的。因此，能够使用某一个编程语言（例如，Python）编程的任何事情，也都可以以其他任何一个编程语言（例如，Java）实现。当然，某些编程语言更易于用来编写程序，但对于所有的语言来讲，它们拥有完全相等的计算的能力。

幸运的是，所有的程序员都在图灵的基本指令集中构造程序。现代的编程语言提供了大量，更便于使用的基本指令。然而，把一系列操作组合起来这样的过程，其背后根本的编程思想仍然是没有变化的。

无论一个编程语言拥有一组什么样的基本指令，无论它又有哪些方法去使用那些指令，对编程来说，好的方面和不尽如人意的方面是相同的，即计算机总是能精确地完成你让做的事情。之所以讲好的方面是因为你可以利用计算机做各种各样有意思和有用的事，相反不尽如人意的地方是，一旦它不听你的话干活了，你只能从自己找原因了。

在这个世界中，有上百种编程语言。它们中没有哪一个能称的上是最好的语言。具体问题，具体分析。针对不同类型的应用，它们各有千秋。举几个例子，MATLAB是操作向量和矩阵的极好的语言，C非常适合用来编写控制数据网络的程序，而PHP就适合用来构建Web网站。Python则是一种通用型的语言了。

每一种编程语言都有一些基本元素，语法，静态语义和语义。
与自然语言做一下类比，比如英语，我们能看出，其基本构成是字。语法描述了一个完整的句子是由哪些文字构成的，静态语义定义了哪些句子是有意义的，而语义则定义了句子的含义。Python语言的基本构成包括**字面值**（literals），例如数字3.2，和字符串'abc'，以及**中缀运算符**（infix
operators），例如加法运算符和除法运算符。

语言的语法定义了哪些字符和符号是格式良好的。例如在英语中，字符串“Cat dog
boy.”不是一个合乎语法规则的句子，因为英语的语法不接受由三个名词构成的句子。在Python中，`3.2 +
3.2`是语法上格式良好的，而`3.2 3.2`就不是了。

静态语法定义了哪些合乎语法规则的字符串是有意义的。 仍旧以英语为例，字符串“I are big”是由代词，连系动词（linking
verb）和形容词组成，在语法上是可以被接受的，但并不是正确的英语表述。因为，名词“I”是单数，动词“are”是复数。这是一个典型的静态语义错误。Python中，`3.2/'abc'`在语法上是正确的，它的格式是`<literal><operator><literal>`，然而由于一个数字除以一个字符串没有任何的意义，它会产生静态语义错误。

语言的语义是把没有静态语义错误的正确的字符串与确切的含义关联起来。在自然语言中，一个句子的语义有可能会产生歧义。例如，褒、贬之意都蕴藏在了句子“I
cannot praise this student too highly”中。编程语言的设计确保了每一段合法的程序只有一个确切的含义。

尽管语法错误是很常见的一类错误，特别是对于那些刚刚开始学习一门新的编程语言的程序员来讲，但也不是什么致命的问题。每一种严肃的编程语言都会尽职尽责地检查任何语法类型地错误，不会让用户执行包含哪怕那么一丁点儿语法错误的程序。除此之外，多数情况下，语言系统还会足够清晰地指出是什么地方出了错，以及你需要做些什么才能修复错误。

静态语义错误的处理稍显复杂。在程序能够能够被执行之前，某些编程语言，例如Java，会从多个方面检查是否存在这样的错误。相对来说，其他语言，包括C和Python，会做较少的静态语义错误检查。Python将多数的这类检查放在了运行时，同时不会捕捉所有的这类错误。当这些错误没有被提前侦测到的情况下，程序的行为就变得不可预测。在本书的后续章节中，我们会看到一些示例。

One doesn't usually speak of a program as having a semantic error.
如果程序没有语法错误和静态语义错误，意味着它具有一定的含义，也就是具有一定的语义。当然，这并不是说它所具有的语义就是作者想要表达的。当一个程序没有正确地表达出其作者的真正意图的时候，肯定是有地方出问题了。

如果一个程序出错了，会发生什么事情，会有怎样的异常行为呢？

- 或崩溃。在一个设计良好的计算系统中，一个程序崩溃了不会导致整个系统随之崩溃。当然，某些非常流行的计算机系统并不具备这样棒的特性。几乎每一个使用个人电脑的人都运行过那些试图重起整个系统的程序。

- 亦或一直运行下去，永远不会停止。如果不知道程序应该花费多久的时间完成正在执行的任务，那就很难认识到这个问题的存在了。

- 亦或会完成整个运行过程，得到正确或者不正确的结果。

上述的每一个都是糟糕的情况，然而，最后一个无疑是最糟的。如果一个程序貌似正在做正确的事情，但事实并非如此，那么你正在面临麻烦了。现实生活中，一旦遇到这样是情况，显然我们有可能丢失自己的财富，病人有可能接受致命剂量的放射治疗，甚至发生飞机坠毁事故，等等。
