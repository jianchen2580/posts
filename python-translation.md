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

本书基于MIT的一门课程，自2006年开始，该课程每年开课两次。该课程针对那些没有编程经验或具备少量编程经验的学生，但他们有需要（或至少是希望）了解使用计算理论解决问题。每年都有一些学生利用该课程作为学习高级计算机课程的基础。但是对大多学生而言，该课程将是他们唯一的计算机科学课程。

Because the course will be the only computer science course for most of the
students, we focus on breadth rather than depth. The goal is to provide
students with a brief introduction to many topics, so that they will have an idea
of what's possible when the time comes to think about how to use computation
to accomplish a goal. That said, it is not a "computation appreciation" course.
It is a challenging and rigorous course in which the students spend a lot of time
and effort learning to bend the computer to their will.

因为该课程将成为大多数学生唯一的计算机科学课程，所以我们注重广度而不是深度。本书目标是通过大量相关主题的简介，让学生了解如何利用计算达到一个目标。也就是说，本课程不是一个“计算欣赏”课程，而是一个具有挑战性的严格课程，学生需要花费大量的时间和精力学习如何让计算机遵从自己的意愿行事。

The book is a bit eccentric. Part 1 (Chapters 1-8) is an unconventional
introduction to programming in Python. We braid together four strands of
material:

• The basics of programming,
• The Python programming language,
• Concepts central to understanding computation, and
• Computational problem solving techniques.

本书与其它书不同。第一部分（1-8章）以非常规的方式介绍了Python编程。 
内容按以下四部分组织：
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

本书覆盖了大多数Python的特性，但着重于我们能用编程语言实现什么，而不是编程语言本身。例如，到第三章末为止，本书只覆盖了少部分的Python内容，但是已经介绍了完全枚举（exhaustive enumeration）的概念，猜测-检查（guess and check)算法，二分搜索（bisection search）和高效近似（efficient approximation）算法.
编程方法的诸貌与Python特性的介绍将贯穿全书。本书将帮助你学习Python并且在使用计算解决一些有趣问题方面成为一个好的程序员。

Part 2 (Chapters 9-16) is primarily about using computation to solve problems.
It assumes no knowledge of math ematics beyond high school algebra, but it
does assume that the reader is comfortable with rigorous thinking and not
intimidated by mathematical concepts. It covers some of the usual topics found。

第二部分（9-16章）是主要关于使用计算解决问题。本书不假设您具备高中代数之上的数学能力， 但是假设读者可以接受严谨的思维和数学概念。本书涵盖了一些常见主题。

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

计算机做并且只做两件事情： 执行计算并且存储计算结果。计算机擅长于这两件事。典型的计算机是放置于桌面或者手提包中，它每秒钟执行10亿次左右的计算。我们很难想象它是如此的快。如果将球举离地板一米，然后让球掉落，在球落地的这一短时间里头，你的电脑已经执行了超过十亿次指令。
至于存储，一个典型的电脑可以有拥有几百G的存储空间。这是有多大呢？如果一个字节（一般是8个bits表示一字符）重一盎司（which it doesn‘t），100G将重达3，000，000吨。相比之下，这大约是美国一年的煤炭产量。

For most of human history, computation was limited by the speed of calculation
of the human brain and the ability to record computational results with the
human hand. This meant that only the smallest problems could be attacked
computationally. Even with the speed of modern computers, there are still
problems that are beyond modern computational models (e. g., understanding
climate change), but more and more problems are proving amenable to
computational solution. It is our hope that by the time you finish this book, you
will feel comfortable bringing computational thinking to bear on solving many of
the problems you encounter during your studies, work, and even everyday life.
 
在人类历史的大多数时间里头， 计算限制于人类大脑运算的速度和记忆运算结果的能力。这意味着我们的计算仅限于解决较小的问题。甚至以现在计算机的速度，依然存在超出现代计算模型的问题（例如，了解气候变化），但是越来越多的问题被证实存在适合的计算方案。我们希望在你完成本书后，能收获如何使用计算思维解决一些学习，工作和日常生活中的问题。

What do we mean by computational thinking？
All knowledge can be thought of as either declarative or imperative. Declarative
knowledge is composed of statements of fact. For example, "the square root of x
is a number y such that y•y = x." This is a statement of fact. Unfortunately it
doesn 't tell us how to find a square root.


Imperative knowledge is "how to" knowledge, or recipes for deducing
information. Heron of Alexandria was the first to document a way to compute
th e square root of a number 2 His method can be summarized as:
• Start with a guess, g,
• If g•g is close enough to x , stop and say that g is the answer
• Otherwise create a new guess, by averaging g and x/g, i.e. (g + x/g)/2
• Using this new guess, which we again call g, repeat the process until g•g
is close enough to x.

什么是计算思维？所有的知识都可以被认为是声明性或命令性。陈述性知识是由事实的陈述构成。例如，”x的平方根是y，满足y*y=x。“。这是一个事实的陈述。不幸的是，这没有告诉我们如何求平方根。
命令性的知识是关于“如何实现”的知识，或者是演绎信息的配方。海伦第一个提出如何计算平方根，他的方法归纳如下：
* 首先给出一个猜测数g
* 如果g*g足够接近x，那g就是x的平方根
* 否则，创建一个新的猜测数，该猜测数是g和x/g的平均数,即，(g+x/g)/2
* 使用这个新的猜测数g，重复上述过程直到g*g逼近x
 
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
正式一点的表述，算法是一个表示为有限长列表的指令，它描述一组运算，在提供一组的输入下执行，通过一组良好定义的状态，并最终生成一个输出。

An algorithm is a bit like a recipe from a cookbook,
1. Put custard mixture over heat.
2. Stir.
3. Dip spoon in custard.
4. Remove spoon and run finger across back of spoon.
5. If clear path is left, remove custard from heat and let cool.
6. Otherwise repeat.

一个算法类似烹饪书上的一个菜谱，-- 此处太变态了
* 1. 加热奶油蛋羹。
* 2. 搅拌。
* 3. 用勺舀起奶油蛋羹。
* 4. 移除勺子，Remove spoon and run finger across back of spoon。
* 5. if clear path is left,停止加热并让奶油冷却.
* 6. 其它情况下重复以上过程

It includes some tests for deciding when the process is complete, as well as
instructions about the order in which to execute instructions, sometimes
jumping to some instruction based on a test.

为了判定过程是否完成，算法需要包括一些测试，以及指令顺序的说明, 有时候需要基于测试结果执行指令跳转。

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
machine, one has to replace the circuitry.

如何在这一个机械般的过程中提炼出食谱？一种方法是设计一个机器专门用于计算平方根。听起来可能觉得奇怪，事实上最早的计算机是固定程序计算机，意味着它是设计目的是实现非常特定的事情，大多是解决一个特定数学问题的工具，例如计算炮弹轨迹。
最早计算机中的一个（Atanasoff and Berry 建于1941)，它用于解线性方程, 但是做不了其它事情。 Alan Truing's bombe machine, 开发于二战时期，设计用来破解德国Enigma codes. 一些非常简单的计算机目前仍然用于该目的。 例如， a (four-function) 计算器is a fixed-program computer. 它能完成基本的数学运算，
但是不能用于字处理或者执行视频游戏。改造类似的机器， 需要更换电路。


The first truly modern computer was the Manchester Mark 1.5 It was
distinguished from its predecessors by the fact that it was a stored-program
computer. Such a computer stores (and manipulates) a sequence of
instructions, and has a set of elements that will execute any instruction in that
sequence. By creating an instru ction-set architecture and detailing the
computation as a sequence of instructions (i.e., a program), we make a highly
flexible machine. By treating those instructions in the same way as data, a
stored-program machine can easily change the program, and can do so under
program control. Indeed, th e heart of the computer then becomes a program
(called an interpreter) that can execute any legal set of instructions, and thus
can be used to compute anything that one can describe using some basic set of
instructions.

第一台真正意义上的现代计算机当属Manchester Mark 1.5。相比以往的计算机，它是一台存储程序式计算机（
stored-program computer）。这一类型的计算机能够存储并使用一系列的指令，同时，它具备执行其中指令的组件。通过创建指令集架构，以及把计算的过程详细地描述为一系列计算机指令，一台高度灵活的机器形成了。通过将指令以数据的方式，存储程序式计算机可方便地更改程序，同时也可以在程序的控制下执行。事实上，计算机的核心就变成了能够执行任何合法的指令集合的程序（称其为解释器），这样它就可以被用于计算任何能够用一些基本的指令集合描述的事情。

Both the program and th e data it manipulates reside in memory. Typically th ere
is a program counter that points to a particular location in memory, and
compu tation starts by executing the instruction at that point. Most often, th e
interpreter simply goes to the next instruction in th e sequence, but not always. In
some cases, it performs a test, and on the basis of that test, execution may jump
to some other point in the sequ ence of instructions. This is called flow of
control, and is essential to allowing us to write programs that perform complex
tasks.

程序和数据都驻留在内存中。通常会有一个程序计数器指向内存中的某个特定的位置，计算过程从这个位置的指令开始执行。多数情况下，解释器只是简单地顺序执行指令序列中指令，但并非总是这样。有时，它会做一些测试，并根据测试的结果，指令的执行会跳转到顺序指令序列的其它的位置。这被称作控制流，它在编写复杂任务的程序时至关重要。

Returning to th e recipe metaphor, given a fixed set of in gredients a good chef
can make an unbounded number of tasty dishes by combining them in different
ways. Similarly, given a small fixed set of primitive elements a good programmer
can produce an unbounded number of useful programs. This is what makes
programming such an amazing endeavor.

回到那个食谱的比喻，好的厨师能够在给定的一组食材中，以各种不同的方式组合，然后烹饪出许多可口的菜肴。相似的，在给定一组固定的基本元素中，好的程序员同样可以生产出大量有用的程序。这正是程序设计的追求。

To create recipes, or sequences of instructions, we need a programming
language in which to describe these things, a way to give th e computer its
marching orders.

为了创建食谱，或者指令序列，我们需要一种编程语言来描述这些事情，让计算机运转起来。

marching orders.
In 1936, the British mathematician Alan Turin g described a hypothetical
computing device that has come to be called a Universal Turing machine. The
machine had an unbounded memory in the form of tape on which on e cou ld
write zeros and ones and some very simple primitive instru ctions for moving,
reading, and writing to the tape. The Church-Turing thesis states that if a
function is computable, a Turing Machine can be programmed to compute it.

1936年，英国数学家阿伦图灵描述了一台假设的计算设备，它被称作通用图灵机（Universal Turing
machine）。该机器以磁带的形式拥有无限的存储空间，任何人可以写任意数量的零和一，以及一些非常简单的基本指令，用以移动、读取和向磁带写入。邱奇-图灵论题（Church-Turing
thesis）阐明：如果一个函数是可计算的，那么图灵机就可以通过编程把它算出来。

The "if ' in the Church-Turing thesis is important. Not all problems have
computational solutions. For example, Turing showed that it is impossible to
write a program that given an arbitrary program, call it P, prints true if and on ly
if P will run forever. This is known as the halting problem.

“If”在邱奇-图灵论题中是很重要的。不是所有的问题都有计算解（computational
solution）。例如，图灵展示了不可能写出任意一个程序，当且仅当它将永久运行的时候输出真值。这就是广为认知的停机问题（halting
problem）。

The Church-Turing thesis leads directly to the notion of Turing Completeness.
A programming language is said to be Turing complete if it can be used to
simulate a universal Turing Machine. All modern programming languages are
Turing complete. As a consequ ence, anything that can be programmed in one
programming language (e.g., Python) can be programmed in any other
programming language (e.g., Java). Of course, some things may be easier to
program in a particular language, but all languages are fundamentally equal
with respect to computational power.

邱奇-图灵论题直接引出了图灵完备性的概念。如果一种编程语言能够模拟一个通用图灵机，那么它就被认为是图灵完备的。所有现代的编程语言都是图灵完备的。因此，任何能够使用某一个编程语言（例如，Python）编程实现，也都可以用其他任何一个编程语言（例如，Java）实现。当然，某些编程语言更易于编写程序，但对于所有的语言来讲，它们拥有完全相等的计算的能力。

Fortunately, no programmer has to build programs out of Turing's primitive
instructions. Instead, modern programming languages offer a larger, more
convenient set of primitives. However, the fundamental idea of programming as
the process of assembling a sequence of operations remains central.

幸运的是，所有的程序员都在图灵的基本指令集中构造程序。现代的编程语言提供了大量更便于使用的基本指令。然而，编程基本理念的核心依旧是组合一系列操作。


Whatever set of primitives one has, and whatever methods one has for using
them, the best thing and th e worst thing about programming are the same: the
computer will do exactly what yo u tell it to do. This is a good thing because it
means that you can make it do all sorts of fun and useful things. It is a bad
thing because when it doesn't do what you want it to do, you usually have
nobody to blame but yourself.

无论一个编程语言拥有一组什么样的基本指令，无论它具备哪些方法去使用那些指令，对编程来说，好事和坏事是并存的，即计算机总是能精确地完成你让做的事情。之所以是好事是因为你可以利用计算机做各种各样有意思和有用的事，坏事是，一旦它不按你的意愿工作，你只能从自身寻找原因。

There are hundreds of programming languages in the world. Th ere is no best
language (though one could nominate some candidates for worst). Different
languages are better or worse for different kinds of applications. MATLAB, for
example, is an excellent language for manipulating vectors and matrices. C is a
good language for writing the programs that control data networks. PH P is a
good language for building W eb sites. And Python is a good general-purpose
language.

在这个世界中，有上百种编程语言。它们中没有哪一个能称的上是最好的语言。具体问题，具体分析。针对不同类型的应用，它们各有千秋。举几个例子，MATLAB是操作向量和矩阵的极好的语言，C非常适合用来编写控制数据网络的程序，而PHP就适合用来构建Web网站。Python则是一种通用型的语言了。

Each programmin g lan guage has a set of primitive constructs, a syntax, a static
seman tics, and a semantics. By analogy with a natural language, e.g. , English,
th e primitive constructs are words, the syntax describes which strin gs of words
constitute well-formed sentences, the static semantics defines which sentences
are meaningful, and the semantics defines the meaning of those sentences. The
primitive constructs in Python include literals (e.g., the number 3.2 and the
string 'abc') and infix operators (e.g.,+ and/).

每一种编程语言都有一些基本元素，语法，静态语义和语义。类比自然语言，比如英语，我们能看出，其基本构成是字。语法描述了一个完整的句子是由哪些文字构成的，静态语义定义了哪些句子是有意义的，而语义则定义了句子的含义。Python语言的基本构成包括**字面量（literals）**（例如，数字3.2,字符串'abc'),以及**中缀运算符（infix
operators）**(例如,加法运算符和除法运算符)。

The syntax of a language defines which strings of characters and symbols are
well formed. For example, in English the string "Cat dog boy." is not a
syntactically valid sentence, because the syntax of English does not accept
sentences of th e form <noun> <noun> <no un> . In Python, the sequ ence of
primitives 3.2 + 3.2 is syntactically well formed, but the sequence 3.2 3. 2 is
not.

语言的语法定义了哪些字符和符号是符合语法规则的。例如在英语中，字符串“Cat dog
boy.”不是一个合乎语法规则的句子，因为英语的语法不接受由三个名词构成的句子。在Python中，`3.2 +
3.2`是符合语法规则的，而`3.2 3.2`就不是了。

The static semantics defines which syntactically valid strings have a meaning. In
English, for example, the string "I are big," is of the form <pron oun> <linking
verb> <adjective>, which is a syntactically acceptable sequ ence. Nevertheless, it
is not valid English, because the nou n "!" is singular and the verb "are" is plural.
Thi s is an example of a static semantic error. In Python, the sequence
3.2/'abc' is syntactically well formed (<literal> <operator> <literal>), but
produces a static semantic error sin ce it is not meaningful to divide a number by
a string of characters.

静态语法定义了哪些合乎语法规则的字符串是有意义的。 仍旧以英语为例，字符串“I are big”是由代词，系动词（linking
verb）和形容词组成，在语法上是可以被接受的，但并不是正确的英语表述。因为，名词“I”是单数，动词“are”是复数。这是一个典型的静态语义错误。Python中，`3.2/'abc'`在语法上是正确的，它的格式是‘<字面量><操作符><字面量>'(`<literal><operator><literal>`)，然而由于一个数字除以一个字符串没有任何的意义，因此会产生静态语义错误。

The semantics of a language associates a meaning with each syntactically
correct string of symbols that has no static semantic errors. In natural
languages, the semantics of a sentence can be ambiguous. For example, the
sentence "I cannot praise this student too highly," can be either flattering or
damning. Programming languages are designed so that each legal program has
exactly one meaning.

语言的语义是把没有静态语义错误的正确的字符串与确切的含义关联起来。在自然语言中，一个句子的语义有可能会产生歧义。例如，“我不能过分的表扬这个学生（I
cannot praise this student too highly）”,可能是褒意，也可能是贬意。编程语言的设计确保了每一段合法的程序只有一个确切的含义。

Though syntax errors are the most common kind of error (especially for those
learning a new programming language) , they are the least dangerous kind of
error. Every serious programming language does a complete job of detecting
syntactic errors, and will not allow users to execute a program with even one
syntactic error. Furthermore, in most cases the language system gives a
sufficiently clear indication of the location of the error that it is obvious what
needs to be done to fix it.

尽管语法错误是很常见的一类错误，特别是对于那些刚刚开始学习一门新的编程语言的程序员，但不是什么致命的问题。每一种严肃的编程语言都会尽职尽责地检查任何语法类型的错误，不会让用户执行包含哪怕包含那么一丁点儿语法错误的程序。除此之外，多数情况下，语言系统还会明确地指出是什么地方出了错，以及你需要做些什么才能修复错误。

The situation with respect to static semantic errors is a bit more complex. Some
programming languages, e.g., Java, do a lot of static semantic checking before
allowing a program to be executed. Others, e. g., C and Python (alas), do relatively
less static semantic checking. Python does do a considerable amount of static
semantic checking while running a program. However, it does not
catch all static semantic errors. When these errors are n ot detected, the
behavior of a program is often unpredictable. We will see examples of this later
in the book.

静态语义错误的处理稍显复杂。在程序能够能够被执行之前，某些编程语言，例如Java，会从多个方面检查是否存在这样的错误。相对来说，其他语言，包括C和Python，会做较少的静态语义错误检查。Python在运行时会做适当的静态语义错误检查，但不会捕捉所有的这类型错误。在这些错误没有被提前侦测到的情况下，程序的行为就变得不可预测。在本书的后续章节中，我们会看到一些示例。

One doesn't usually speak of a program as having a semantic error. If a
program has no syntactic errors and no static semantic errors, it has a meaning,
i.e., it has semantics. Of course, that isn't to say that it has th e semantics that
its creator intended it to have. When a program means something other than
what its creator thinks it means, bad things can happen.

程序的语义错误很少被提及。 如果程序没有语法错误和静态语义错误，意味着它具有一定的含义，也就是说它具有一定的语义。当然，这并不是说它所具有的语义就是作者想要表达的。当一个程序没有正确地表达出其作者的真正意图的时候，肯定是有地方出问题了。

One doesn't usually speak of a program as having a semantic error. If a
program has no syntactic errors and no static semantic errors, it has a meaning,
i.e., it has semantics. Of course, that isn't to say that it has th e semantics that
its creator intended it to have. When a program means something other than
what its creator thinks it means, bad things can happen.
What might happen if the program has an error, and behaves in an unintended
way?
* It might crash, i.e., stop running and produce some sort of obvious
indication that it has done so. In a properly designed computing system,
when a program crashes it does not do damage to the overall system. Of
course, some very popular computer systems don't have this nice
property. Almost everyone who uses a personal computer h as run a
program that has managed to make it necessary to restart the whole
computer.
* Or it might keep running, and running, and running, and never stop. If
one has no idea about how long the program is supposed to take to do its
job, this situation can be hard to recognize.
* Or it might run to completion and produce an answer that might, or
might not, be correct.

如果一个程序出错了，会发生什么事情，会有怎样的异常行为呢？

* 或崩溃。在一个设计良好的计算系统中，一个程序崩溃了不会导致整个系统随之崩溃。当然，某些非常流行的计算机系统并不具备这样优良的特性。几乎每一个使用个人电脑的人都运行过那些试图要求重起计算机的程序。

* 亦或一直运行下去，永远不会停止。如果不知道程序应该花费多长的时间完成正在执行的任务，那这种情况就很难被识别。

* 亦或会完成整个运行过程，得到正确或者不正确的结果。

Each of these is bad, but the last of them is certainly the worst. When a
program appears to be doing the right thing but isn 't, bad things can follow.
Fortunes can be lost, patients can receive fatal doses of radiation th erapy,
airplanes can crash, etc.

上述的每一个都是糟糕的情况，然而，最后一个无疑是最糟的。如果一个程序貌似正在做正确的事情，但事实并非如此，那么麻烦随之而来。我们有可能丢失自己的财富，病人有可能接受致命剂量的放射治疗，飞机坠毁事故等等。

Whenever possible, programs shou ld be written in such a way that when they
don't work properly, it is self-evident. We will discuss how to do this
throughout the book.
当程序不能正常工作时候，应该尽可能的让异常清晰自明。如何实现的讨论将贯穿整本书。

Finger Exercise: Computers can be annoyingly literal. If you don't tell them
exactly what you want them to do, they are likely to do the wrong thing. Try
writin g an algorithm for driving between two destinations. Write it th e way you
would for a person, and then imagine what wou ld happen if the person execu ted
th e algorithm exactly as written . For example, how many traffic tickets might
they get?

技巧练习：计算机非常缺乏想象力. 如果你不确切的告诉它你想让它做什么，它就可能做出错误的事情。试着为两个目的地间的驾车写一个算法，该算法以人的视角，想像如果一个人严格按照该算法执行将会发生什么。例如，多少交通罚单会收到。

