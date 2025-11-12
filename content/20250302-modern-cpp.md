---
id: 20250302-modern-cpp
aliases:
  - modern-cpp
tags: []
created: 2025-09-08
modified: 2025-09-08T23:44:46
---

# modern-cpp

[huihut/interview: 📚 C/C++ 技术面试基础知识总结，包括语言、程序库、数据结构、算法、系统、网络、链接装载库等知识及面试经验、招聘、内推等信息。This repository is a summary of the basic knowledge of recruiting job seekers and beginners in the direction of C/C++ technology, including language, program library, data structure, algorithm, system, network, link loading library, interview experience, recruitment, recommendation, etc.](https://github.com/huihut/interview)

std:library resources : codereport: youtube + explain




[codereport/Algorithms: STL Algorithm Cheat Sheet + example code from STL Algorithm Video Series.](https://github.com/codereport/Algorithms)

[Asio C++ Library](https://think-async.com/Asio/index.html) -> for cpp 20 network, low levelI/O (cross platforum)
> - [C++ 语言超详细系统学习路线（2025年最新） | 编程指北-计算机学习指南](https://csguide.cn/roadmap/cpp/how_to_learn_cpp.html) -> useful

- [Linux C++ 后台开发系统学习路线（2025年最新） | 编程指北-计算机学习指南](https://csguide.cn/roadmap/cpp/linux_cpp.html#_8-1-%E4%BB%80%E4%B9%88%E6%98%AF%E7%B3%BB%E7%BB%9F%E7%BA%A7%E7%BC%96%E7%A8%8B) -> part 2 , os csapp , low level courses
  [超全 C/C++ 技术面试八股文面试题！（2025 年更新） | 编程指北-计算机学习指南](https://csguide.cn/cpp/intro.html)
  [wuye9036/CppTemplateTutorial: 中文的C++ Template的教学指南。与知名书籍C++ Templates不同，该系列教程将C++ Templates作为一门图灵完备的语言来讲授，以求帮助读者对Meta-Programming融会贯通。(正在施工中)](https://github.com/wuye9036/CppTemplateTutorial)

[Redis 超详细系统学习路线（2025） | 编程指北-计算机学习指南](https://csguide.cn/roadmap/backend_middleware/how_to_learn_redis.html#%E4%B8%89%E3%80%81%E5%AD%A6%E4%B9%A0%E8%B5%84%E6%96%99)
[Career_planning_path/c_cpp项目合集 at main · 0voice/Career_planning_path](https://github.com/0voice/Career_planning_path/tree/main/c_cpp%E9%A1%B9%E7%9B%AE%E5%90%88%E9%9B%86) -> **cpp lib, project**
[interview_internal_reference/2023adding.md at master · 0voice/interview_internal_reference](https://github.com/0voice/interview_internal_reference/blob/master/2023adding.md#309-%E4%B8%BA%E4%BB%80%E4%B9%88%E6%9E%90%E6%9E%84%E5%87%BD%E6%95%B0%E8%A6%81%E5%AE%9A%E4%B9%89%E4%B8%BA%E8%99%9A%E5%87%BD%E6%95%B0%E5%93%AA%E4%BA%9B%E5%87%BD%E6%95%B0%E4%B8%8D%E8%83%BD%E6%98%AF%E8%99%9A%E5%87%BD%E6%95%B0) -> **cpp 1000 interview question**

- **your own question bank form competiteve programming , either form testdata or usaco**

- [madskjeldgaard/cppman.nvim: Search cppman (cplusplus.com and cppreference) from within neovim](https://github.com/madskjeldgaard/cppman.nvim) nvim plugin
  [nvim/lua/plugins/tips.lua at master · BaoSiZe-bot/nvim](https://github.com/BaoSiZe-bot/nvim/blob/master/lua/plugins/tips.lua)

  2.1 系統入門書籍

      《Accelerated C++》（美國斯坦福大學的經典教材）
      《C++ Primer》（經常被推薦的一本書，大而全，字典書）
      《The C++ Programming Language》（C++之父 Bjarne Stroustrup 所著）

這三本，其實各有優缺點，第一本優點是簡短，僅僅兩三百頁，只有最爲核心和主幹的知識點。

而後兩本則都是大而全，尤其是《The C++ Programming Language》。

這兩本區別在於，一個是 C++ 大師所著，一本是 C++ 之父所著。

網上有人說 《C++Primer》是目前市面上唯一一本真正的從入門到精通的書，適合初學者，當你對C++比較熟悉之後，就可以把這本書當做字典，遇到不太清晰的點再回過頭去看
《C++ Programming language》 是C++專家自學指南，顧名思義，適合有較深厚 C++ 功底的讀者。

2.2 推薦閱讀順序

所以小北推薦的順序是：
**《Accelerated C++》->《C++ Primer》->《The C++ Programming Language》**

對於這種上前頁大部頭我推薦的閱讀方式是，以主題爲劃分，比如 C++ Primer 就明確的分爲了：

    C++ 基礎
    C++ 標準庫
    類設計者的工具
    高級主題
    並且越到後面，你越可以直接翻書的目錄，跳躍着找你感興趣或者說還不太清楚的知識點看，不用再像看第一本書一樣從頭翻到尾。

入門結束你應該掌握以下內容：

    基礎語言
    類與面向對象
    輸入輸出
    字符串處理（類庫和正則表達式）
    指針&引用
    容器類庫
    泛型算法

看着只有幾個關鍵字，實際上每個展開都有很多內容需要學習。

學習過程中把後面的每一個練習題都自己敲一遍，自己多思考對比一下。
多用代碼去驗證自己的想法，尤其是指針、引用、構造、析構這些地方。

---

1. [C++ Core Guidelines](http://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines) 2. cpp conference presentation
   [cpp-best-practices/cppbestpractices: Collaborative Collection of C++ Best Practices. This online resource is part of Jason Turner's collection of C++ Best Practices resources. See README.md for more information.](https://github.com/cpp-best-practices/cppbestpractices/tree/master)

> [Learn Contemporary C++ | Concise&Visual Examples | hacking C++](https://hackingcpp.com/index.html)
> my favorite cpp learning web

- [hsutter/cppfront: A personal experimental C++ Syntax 2 -> Syntax 1 compiler](https://github.com/hsutter/cppfront)
  enhanced Cpp

[carbon-language/carbon-lang: Carbon Language's main repository: documents, design, implementation, and related tools. (NOTE: Carbon Language is experimental; see README)](https://github.com/carbon-language/carbon-lang)

- Nvida c++ tutorial
  [federico-busato/Modern-CPP-Programming: Modern C++ Programming Course (C++03/11/14/17/20/23/26)](https://github.com/federico-busato/Modern-CPP-Programming)

[changkun/modern-cpp-tutorial: 📚 Modern C++ Tutorial: C++11/14/17/20 On the Fly | https://changkun.de/modern-cpp/](https://github.com/changkun/modern-cpp-tutorial)

[All C++20 core language features with examples | Oleksandr Koval’s blog](https://oleksandrkvl.github.io/2021/04/02/cpp-20-overview.html)

---

source: https://matt.might.net/articles/what-cs-majors-should-know/

---

#### ISO C++

C++ is a necessary evil.

But, since it must be taught, it must be taught in full.

In particular, computer science majors should leave with a grasp of even [template meta-programming](http://matt.might.net/articles/c++-template-meta-programming-with-lambda-calculus/).

##### Recommended reading

- [The C++ Programming Language](http://www.amazon.com/gp/product/0201700735/ref=as_li_ss_tl?ie=UTF8&tag=mmamzn06-20&linkCode=as2&camp=217145&creative=399369&creativeASIN=0201700735)![](http://www.assoc-amazon.com/e/ir?t=&l=as2&o=1&a=0201700735&camp=217145&creative=399369) by Stroustrup.
- [C++ Templates: The Complete Guide](http://www.amazon.com/gp/product/0201734842/ref=as_li_ss_tl?ie=UTF8&tag=mmamzn06-20&linkCode=as2&camp=217145&creative=399369&creativeASIN=0201734842)![](http://www.assoc-amazon.com/e/ir?t=&l=as2&o=1&a=0201734842&camp=217145&creative=399369) by Vandevoorde and Josuttis.
- [Programming Pearls](http://www.amazon.com/gp/product/0201657880/ref=as_li_ss_tl?ie=UTF8&camp=1789&creative=390957&creativeASIN=0201657880&linkCode=as2&tag=mmamzn06-20)![](http://www.assoc-amazon.com/e/ir?t=mmamzn06-20&l=as2&o=1&a=0201657880) by Bentley.

standford cpp

cpp Operating system course
cpp cmu database course

os wiki + USOAP

- his cv is pretty good:
  ◦As engineer: design and developing automated pricing system to support price decisions; making existing systems approx. 300x faster ◦Involved techniques: Go; C++; Python; Kubernetes; Jenkins; Promethues; Postgres; Redis; AWS; etc.
  [2023 读书清单 - Changkun's Blog](https://changkun.de/blog/posts/2023-reading/)

  最后就是工程类了，工程类的书籍对于今天的我反而比较提不起兴趣，一方面是因为做过太多的工程类的问题，对技术了解积累了一定的广度，能够直接看穿一个技术背后到底是什么在驱动，到底是纯粹的理性还是开发人员的固执等等。另一方面，我对计算机技术的理解从原来的希望了解“如何做”变成了“为什么要做”，其中一个很重要的原因是“如何做”这一问题对于现在的我，更多的是要么能立刻建立起如何做的认知、要么就就是能够立刻判断这个问题是否可解。所以如果如何做已经不是问题，更多的问题则是做这件事情背后的动机是什么，影响有多大，我到底要不要在这件事情上花时间。

  ***

  > “C++ is for people who want to use hardware very well and manage the complexity of doing that through abstraction” Bjarne Stroustrup
  > “a language like C++ is not for everybody. It is generated via sharp and effective tool for professional basically and definitely for people who aim at some kind of precision” Bjarne Stroustrup

  > “The problem with using C++...is that there’s already a strong tendency in the language to require you to know everything before you can do anything” Larry Wall, Creator of the Perl language

  > “C makes it easy to shoot yourself in the foot; C++ makes it harder, but when you do, it blows your whole leg off” Bjarne Stroustrup, Creator of the C++ language

  aim for hardware and precision
  not for beginners

  Rust (1.0, 2015) has been Stack Overflow’s most loved language for eight years in a row. Rust focuses on performance and zero-abstraction overhead as C++. It is designed to prevent many vulnerabilities that affect C++, especially memory bugs, enforcing constraints at compile type. In addition, it promotes cross-platform compatibility

  ***

  grok:

  The flip side is C++’s complexity creeps up. Those segfaults or memory leaks (Google’s memory safety nemesis) hit when you least expect it. Libraries help, but you’ll still need to grok pointers, manual memory management, and undefined behavior quirks. It’s forgiving for small projects, brutal for big ones if you’re sloppy.

  ***

  Optimizing the C++ build
  :
  [Is coding in Rust as bad as in C++?](https://quick-lint-js.com/blog/cpp-vs-rust-build-times/)

When working on the original C++ project, quick-lint-js, I already optimized build times using common techniques, such as using PCH, disabling exceptions and RTTI, tweaking build flags, removing unnecessary #includes, moving code out of headers, and externing template instantiations. But there are several C++ compilers and linkers to choose from. Let's compare them and choose the best before I compare C++ with Rust:

> Every second spent trying to understand the language is one not spent understanding the problem

- language complexity

> “The only way to learn a new programming language is by writing programs in it”

![books](20250302-modern-cpp/cpp-suggested-books.png)

---

# office reference:

[cppreference.com](https://en.cppreference.com/w/)

[isocpp/CppCoreGuidelines: The C++ Core Guidelines are a set of tried-and-true guidelines, rules, and best practices about coding in C++](https://github.com/isocpp/CppCoreGuidelines/tree/master)
https://www.stroustrup.com/programming.html

---

[Decoded: GNU coreutils – MaiZure's Projects](https://www.maizure.org/projects/decoded-gnu-coreutils/)

---

- [C++ Is An Absolute Blast](https://learncodethehardway.com/blog/31-c-plus-plus-is-an-absolute-blast/)
- [Very Deep Not Boring Beginner Projects](https://learncodethehardway.com/blog/32-very-deep-not-boring-beginner-projects/)

---

created: 2025-03-09T08:19:25 (UTC -04:00)
tags: []
source: https://learncodethehardway.com/blog/28-minimum-educational-c-plus-plus/
author:

---

# Minimum Educational C++

> ## Excerpt
>
> I go through various style guides and attempt to extract the minimum C++ someone can learn to be functional on many code bases, and in your own code.

---

## The Style Guides

With that in mind, I spent the last _few months_ reviewing many different guides, but three came out on top as the most practical and/or commonly referenced:

1.  [Google's C++ Style Guide](https://google.github.io/styleguide/cppguide.html)
2.  [Epic Games C++ Style Guide](https://dev.epicgames.com/documentation/en-us/unreal-engine/epic-cplusplus-coding-standard-for-unreal-engine)
3.  [C++ Core Guidelines](https://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines)
    [cmu-db/bustub: The BusTub Relational Database Management System (Educational)](https://github.com/cmu-db/bustub)

---

[Read Learn C++ the Hard Way For Free](https://learncodethehardway.com/courses/learn-cpp-the-hard-way/)
[C++ Is An Absolute Blast](https://learncodethehardway.com/blog/31-c-plus-plus-is-an-absolute-blast/)

> [Stroustrup: FAQ](https://www.stroustrup.com/bs_faq.html#generic)

- [0voice/Awesome_c-cpp_Projects: 2025年 最新收录整理 500+ 个高质量的 C/C++ 项目，包括但不限于核心开发、基础工具、系统与并发、系统编程、图形处理、网络通信、数据处理、应用框架、开源工具、嵌入式开发等多个领域。适合学习、参考和实战。](https://github.com/0voice/Awesome_c-cpp_Projects?tab=readme-ov-file) github project reference

- [0voice/cpp_new_features: 2021年最新整理， C++ 学习资料，含C++ 11 / 14 / 17 / 20 / 23 新特性、入门教程、推荐书籍、优质文章、学习笔记、教学视频等](https://github.com/0voice/cpp_new_features?tab=readme-ov-file)
- [C++ 参考手册](https://c-cpp.com/cpp)

---

# CMU Database

---

created: 2025-03-10T19:07:06 (UTC -04:00)
tags: []
source: https://15445.courses.cs.cmu.edu/fall2024/project0/
author: Andy Pavlo

---

# Project #0 - C++ Primer | CMU 15-445/645 :: Intro to Database Systems (Fall 2024)

> ## Excerpt
>
> Do not post your project on a public Github repository. Overview All the programming projects this semester will be written on the BusTub database management system. This system is written in C++. To make sure that you have the necessary C++ background, you must complete a simple programming assignment to …

---

All the programming projects this semester will be written on the [BusTub](https://github.com/cmu-db/bustub) database management system. This system is written in C++. To make sure that you have the necessary C++ background, you must complete a simple programming assignment to assess your knowledge of basic C++ features. You will not be given a grade for this project, but you **must complete the project with a perfect score** before being allowed to proceed in the course. Any student unable to complete this assignment before the deadline will be asked to drop the course.

All of the code in this programming assignment must be written in C++. The projects will be specifically written for C++17, but we have found that it is generally sufficient to know C++11. If you have not used C++ before, here are some resources to help:

- [15-445 Bootcamp](https://github.com/cmu-db/15445-bootcamp), which contains several small examples to get you familiar with C++11 features.
- [Learncpp](https://www.learncpp.com/) is a useful resource that includes quizzes to test your knowledge.
- [cppreference](https://en.cppreference.com/w/) has more detailed documentation of language internals.
- [A Tour of C++](https://cmu.primo.exlibrisgroup.com/discovery/fulldisplay?docid=alma991019600108604436&context=L&vid=01CMU_INST:01CMU&search_scope=MyInst_and_CI&isFrbr=true&tab=Everything&lang=en) and [Effective Modern C++](https://cmu.primo.exlibrisgroup.com/discovery/fulldisplay?docid=alma991019578256104436&context=L&vid=01CMU_INST:01CMU&search_scope=MyInst_and_CI&tab=Everything&lang=en) are also digitally available from the CMU library.

If you are using VSCode, we recommend you to install [CMake Tools](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cmake-tools), [C/C++ Extension Pack](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools-extension-pack) and [clangd](https://marketplace.visualstudio.com/items?itemName=llvm-vs-code-extensions.vscode-clangd). After that, follow this tutorial to learn how to use the visual debugger in VSCode: [Debug a C++ project in VS Code](https://www.youtube.com/watch?v=G9gnSGKYIg4).

If you are using CLion, we recommend you to follow this tutorial: [CLion Debugger Fundamentals](https://www.youtube.com/watch?v=5wGsRdumueU).

If you prefer to use `gdb` for debugging, there are many tutorials available to teach you how to use `gdb`. Here are some that we have found useful:

- [Debugging Under Unix: gdb Tutorial](https://www.cs.cmu.edu/~gilpin/tutorial/)
- [GDB Tutorial: Advanced Debugging Tips For C/C++ Programmers](http://www.techbeamers.com/how-to-use-gdb-top-debugging-tips/)
- [Give me 15 minutes & I'll change your view of GDB](https://www.youtube.com/watch?v=PorfLSr3DDI) \[VIDEO\]

This is a single-person project that will be completed individually (i.e. no groups).

All the programming projects this semester will be written on the [BusTub](https://github.com/cmu-db/bustub) database management system. This system is written in C++. To make sure that you have the necessary C++ background, you must complete a simple programming assignment to assess your knowledge of basic C++ features. You will not be given a grade for this project, but you **must complete the project with a perfect score** before being allowed to proceed in the course. Any student unable to complete this assignment before the deadline will be asked to drop the course.

All of the code in this programming assignment must be written in C++. The projects will be specifically written for C++17, but we have found that it is generally sufficient to know C++11. If you have not used C++ before, here are some resources to help:

- [15-445 Bootcamp](https://github.com/cmu-db/15445-bootcamp), which contains several small examples to get you familiar with C++11 features.
- [Learncpp](https://www.learncpp.com/) is a useful resource that includes quizzes to test your knowledge.
- [cppreference](https://en.cppreference.com/w/) has more detailed documentation of language internals.
- [A Tour of C++](https://cmu.primo.exlibrisgroup.com/discovery/fulldisplay?docid=alma991019600108604436&context=L&vid=01CMU_INST:01CMU&search_scope=MyInst_and_CI&isFrbr=true&tab=Everything&lang=en) and [Effective Modern C++](https://cmu.primo.exlibrisgroup.com/discovery/fulldisplay?docid=alma991019578256104436&context=L&vid=01CMU_INST:01CMU&search_scope=MyInst_and_CI&tab=Everything&lang=en) are also digitally available from the CMU library.

If you are using VSCode, we recommend you to install [CMake Tools](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cmake-tools), [C/C++ Extension Pack](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools-extension-pack) and [clangd](https://marketplace.visualstudio.com/items?itemName=llvm-vs-code-extensions.vscode-clangd). After that, follow this tutorial to learn how to use the visual debugger in VSCode: [Debug a C++ project in VS Code](https://www.youtube.com/watch?v=G9gnSGKYIg4).

If you are using CLion, we recommend you to follow this tutorial: [CLion Debugger Fundamentals](https://www.youtube.com/watch?v=5wGsRdumueU).

If you prefer to use `gdb` for debugging, there are many tutorials available to teach you how to use `gdb`. Here are some that we have found useful:

- [Debugging Under Unix: gdb Tutorial](https://www.cs.cmu.edu/~gilpin/tutorial/)
- [GDB Tutorial: Advanced Debugging Tips For C/C++ Programmers](http://www.techbeamers.com/how-to-use-gdb-top-debugging-tips/)
- [Give me 15 minutes & I'll change your view of GDB](https://www.youtube.com/watch?v=PorfLSr3DDI) \[VIDEO\]

This is a single-person project that will be completed individually (i.e. no groups).

---

# My own research of cpp sources:

cmu database course -> cpp bootcamp

Usaco : three books
[Choosing a Language · USACO Guide](https://usaco.guide/general/choosing-lang?lang=cpp)

- standford cs106B , CS106L

- CS4414 operating system with cpp 2025-03-27

- modern cpp nvida

- codecraft maybe?

- cmu database

- oswiki (china speedy coding)

- csdiywiki for more advance cpp course

- gaming maybe, using source trail to look high in coding

- [[20250321-essentialist---software-essentialist-2024-7|Essentialist - Software Essentialist 2024-7]]
  for craftsmanship , but typescript like

- cpp datastruce, from pcloud

- cpp pikuma , gaming (godot new c++ gaming framework)

- cpp nanodegreelol

- [Read Learn C++ the Hard Way For Free](https://learncodethehardway.com/courses/learn-cpp-the-hard-way/)
  [C++ Is An Absolute Blast](https://learncodethehardway.com/blog/31-c-plus-plus-is-an-absolute-blast/)

- using repl cling

- maybe learning unit test

---

## another books list recommended 2025-03-31

- from 102-現代C++實戰30講\_kobo

Alexander A. Stepanov and Daniel E. Rose, From Mathematics to Generic Programming. Addison-Wesley, 2014

Alexander Stepanov 是 STL 之父，這本書寫的卻不是具體的編程技 巧或某個庫，而是把泛型編程和抽象代數放在一起討論了。説來慚 愧，我是讀了這本書之後才對羣論稍稍有了點理解：之前看到的介紹 材料都過於抽象，沒能理解。事實上，Alexander 之前還寫了一本同 一題材、但使用公理推導風格的 Elements of Programming（裘宗燕 譯《編程原本》），那本就比較抽象艱深，從受歡迎程度上看遠遠不 及這一本。我也只是買了放在書架上沒看多少頁😝。​

非 C++ 的經典書目 W. Richard Stevens, TCP/IP Illustrated Volume 1: The Protocols. Addison-Wesley, 1994 Gary R. Wright and W. Richard Stevens, TCP/IP Illustrated Volume 2: The Implementation. Addison-Wesley, 1995 W. Richard Stevens, TCP/IP Illustrated Volume 3: TCP for Transactions, HTTP, NNTP and the Unix Domain Protocols. AddisonWesley 1996 中文版翻譯不佳，不推薦。 推薦指數：★★★★☆ 不是所有的書都是越新越好，《TCP/IP 詳解》就是其中一例。W. Richard Stevens 寫的卷一比後人補寫的卷一第二版評價更高，就是

---

1. Real-Time C++ by Christopher Kormanyos. - For using C++ in embedded systems.

2. Software Architecture with C++ by Adrian Ostrowski and Piotr Gaczkowski. - Gives the overall picture of how to use C++ plus relevant modern tools as a complete development system.

3. The C++ Programming Language by Bjarne Stroustrup. - The bible/reference with programming techniques for the language.

> Learning C++ is not difficult and don't let the size of the language intimidate you. Survey the different ways of programming in C++ i.e. Imperative/Object-Oriented/Generic/Meta-programming and use them as needed in your project without trying to master everything; that will only happen over time as you gain more experience.

---

- [使用cquery：C++ language server | MaskRay](https://maskray.me/blog/2017-12-03-c++-language-server-cquery)
- [Welcome to Extra Clang Tools's documentation! — Extra Clang Tools 21.0.0git documentation](https://clang.llvm.org/extra/)
- clang tools extra

- again [abseil / C++ Developer Guide](https://abseil.io/docs/cpp/) twice 🤩

[rbaker1776/Intro-to-Modern-Cxx](https://github.com/rbaker1776/Intro-to-Modern-Cxx/tree/main)

---

# TW cpp notes2025-04-27

[Numerical Software Development - Yung-Yu's Notes](https://yyc.solvcon.net/en/latest/nsd/index.html)
[yungyuc/nsd: Numerical Software Development](https://github.com/yungyuc/nsd)

---

- [Quick C++ Benchmarks](https://quick-bench.com/q/jA6xdpp-UhQrteQjAjiIgJwjKbw) + cpp insight + compiler

[Ccache — Compiler cache](https://ccache.dev/)

[tehrengruber/Defrustrator: Cling integration in LLDB](https://github.com/tehrengruber/Defrustrator)

[inspector-repl/inspector: A drop-anywhere C++ REPL](https://github.com/inspector-repl/inspector)

and sccache(rust version of ccacehe)

---

```cpp

  // 1. 与运算：有假必假
  cout << (0 && -1) << endl;
  cout << (0 && 2) << endl;
  cout << (2 && 0) << endl;
  cout << (2 && 2) << endl;
  cout << "---" << endl;
  // 2. 或运算：有真必真
  cout << (0 || 0) << endl;
  cout << (0 || 2) << endl;
  cout << (2 || 0) << endl;
  cout << (2 || 2) << endl;
  cout << "---" << endl;
  // 3. 非运算：非真即假，非假即真
  cout << !0 << endl;
  cout << !2 << endl;
```

0 != -1 !!!!, only `0&&` will have the case, `-1 ` treat as `1` in T/ F situation

```cpp

/*
     &     有0必0 -> bit operation
   &&    有假必假
*/
```

```cpp
	// 2. 奇偶性
	cout << 5 % 2 << endl;      // % 优先级高、效率高
	cout << (5 & 1) << endl;    // & 优先级低、效率高

  // the prime number must be (5 & 1) = 1 as bit pattern
  int main() {
    // 1. 位与运算符的定义
    int a = 0b1010;   // 10
    int b = 0b0110;   // 6
    //      0b0010;   // 2
    cout << (a & b) << endl;
    cout << "--" << endl;

    // 2. 奇偶性
    cout << 5 % 2 << endl;      // % 优先级高、效率高
    cout << (5 & 1) << endl;    // & 优先级低、效率高
    //   0b101
    //   0b001
    cout << "--" << endl;

    // 3. 获取一个数二进制的末5位
    int c = 0b1010010101001;  // 后五位 01001
    cout << (c & 0b11111) << endl;
    cout << "--" << endl;

    // 4. 将末五位归零
    int d = 0b11111111111111111111111111100000;
    cout << (c & d) << endl; // 0b1010010100000
    cout << "--" << endl;

    // 5. 消除末尾连续的1
    int e = 0b101010111111;
    // e+1= 0b101011000000;
    //  & = 0b101010000000;
    cout << (e & (e + 1)) << endl;
    // using bit +1 pattern to erase after 0

    // 6. 2的幂判定
    int f = 0b100000000;
    // f-1= 0b011111111;
    //   &= 0b000000000 = 0;
    (f > 0) && ((f & (f - 1)) == 0);
    // so that the number must be 2**n, e.g. 2.4,8,16 etc
    return 0;
  }

```

however , must adding `() ` for && as the priority is low

31 video

```cpp
/*
      |    位或  ：有1即1
	  ||   逻辑或：有真即真
*/
int main() {
	// 1. 位或的定义
	int a = 0b1010;     // 10
	int b = 0b0110;     // 6
	//  | = 0b1110      // 14
	cout << (a | b) << endl;
	cout << "---" << endl;

	// 2. 设置标记位
	int c = 0b100111;
	//      0b101111;
	cout << (c | (0b1000)) << endl;
	cout << "---" << endl;

	// 3. 置空标记位
	// 0b100111
	int d = 0b000001;
	cout << ((c | d) - d) << endl;
	cout << "---" << endl;

	// 4. 低位连续0变成1
	int e = 0b1010010000;
	// e-1= 0b1010001111;
	//   -> 0b1010011111;
	int f = 0b1010011111;
	cout << f << endl;
	cout << (e | (e - 1)) << endl;


	return 0;
}

```

    // 3. 置空标记位
    // 0b100111
    int d = 0b000001;
    cout << ((c | d) - d) << endl;
    cout << "---" << endl;

- this is useful, without this , u have to manual & the whole correct number

`c|d` making sure both case (1or 0 case ) can be ` - 1` -> empty out the last number

// 4. is useful as well, make all last number to be `111`

```cpp

/*
       ^  异或 XOR
       only keep the `1 0 ` or `0 1 ` case
*/

  // 2. 標記位取反
cout << "Why XOR twice restores original:" << endl;
cout << "Step 1: 01000101 ^ 00001000 = 01001101 (flip bit 3)" << endl;
cout << "Step 2: 01001101 ^ 00001000 = 01000101 (flip bit 3 again)" << endl;
cout << "Property: A ^ B ^ B = A (XOR is its own inverse)" << endl;
int main() {
  // 1. 異或的定義
  int a = 0b1010;
  int b = 0b0110;
  //  ^ = 0b1100;
  cout << (a ^ b) << endl;
  cout << "---" << endl;

  // 2. 標記位取反
  int c = 0b1000101;
  //      0b0001000
  cout << c << endl;
  cout << (c ^ 0b1000) << endl;
  cout << ((c ^ 0b1000) ^ 0b1000) << endl;
  cout << "---" << endl;

  // 3. 變量交換
  int d = 17;
  int e = 19;
  d = d ^ e;
  e = d ^ e; // = d' ^ e = d ^ e ^ e = d ^ 0 = d
  d = d ^ e; // = d' ^ d = d ^ e ^ d = d ^ d ^ e = 0 ^ e = e
  cout << d << ' ' << e << endl;
  cout << "---" << endl;
  // 3.1 任何數和0異或，還是它本身
  // 3.2 兩個相同的數異或，結果為0
  // 3.3 異或滿足交換律和結合律
  // 異或：不帶進位的二進制加法

  // 4. 出現奇數次的數

  // 5. 加密
  int x = 1314;
  cout << "520" << x << endl;
  int y = (x ^ 3135);
  cout << "520" << y << endl;
  cout << "520" << (y ^ 3135) << endl;

  return 0;
}

```

3, 5 is pretty useful
3.1 任何數和0異或，還是它本身
3.2 兩個相同的數異或，結果為0
3.3 異或滿足交換律和結合律
異或：不帶進位的二進制加法

```cpp
/*
    ~, opposite, flip
*/

int main() {
  // 1. 按位取反的定義
  int a = 0b1;
  int b = 0b11111111111111111111111111111110;
  cout << (~a) << endl; // = -2
  cout << b << endl;    // -2
  // **Key insight**: In two's complement, `~n = -(n+1)` because:
  // - `~0 = -1`
  // - `~1 = -2`
  // - `~2 = -3`

  // 0b00000000000000000000000000000000   = 0
  // 0b11111111111111111111111111111111   = -1
  // 0b11111111111111111111111111111110   = -2
  // ...

  int c = 0b0;
  cout << (~c) << endl;

  // 2. 求相反數
  int d = 18;
  cout << (~d + 1) << endl; // 原碼、反碼、補碼、移碼

  return 0;
}

```

```cpp
/*

     x << y   =   x * 2^y

*/
int main() {
  // 1. 正數的左移
  int x = 0b11; // 3
  x = (x << 1); // 0b110
  cout << x << endl;
  cout << "---" << endl;
  cout << (x << 4) << endl; // 2 ** 4 =>16 , 9 *16 = 96
  cout << "---" << endl;

  // 2. 負數的左移
  int y = -1;
  y = (y << 1);
  cout << y << endl;
  cout << "---" << endl;

  // 3. 左移負數位
  int z = 64;
  z = (z << (-1)); // 不能這麼寫
  cout << z << endl;
  cout << "---" << endl;

  // 4. 左移溢出
  int a = 64;
  a = (a << 31);
  cout << a << endl;
  // 64   = 0b1000000
  // <<31 = 0b1...00000000000000000000000000000000

  return 0;
  // so left shift (operator ) must be positive and can' exceel the max bit for
  // the data type
}

```

```cpp

/*
     x >> y    x / 2^y
*/
int main() {
  // 1. 正數的右移
  int a = 0b111; // 7
  a = (a >> 1);  // removed the last 1 , so it is 3
  cout << a << endl;

  // 2. 負數的右移
  int b = -1;
  cout << (-1 >> 1) << endl;
  // 11111111 11111111 11111111 11111111  =-1
  // 111111111 11111111 11111111 1111111  =-1

  // 3. 去掉低 k 位
  int c = 0b10000101;
  cout << (c >> 7) << endl;

  // 4. 取到第低k位的值
  int d = 0b101010101;
  cout << ((d >> 4) & 1) << endl;

  return 0;
}

```

negative number will automatically keeping 1 even shifting right,
positive number will not, so it can be used for removing number

3,4 is useful

`(x&1) == (x%m) `

35.video

59.video

seconds to minute -> am / 60
as %60 -> add back to am

```cpp
int main() {
    int t;
    cin >> t;
    while (t--) {
        int n;
        double x;
        double max = 0;
        cin >> n;
        for (int i = 0; i < n; ++i) {
            cin >> x;
            if (x > max) {
                max = x;
            }
        }
        printf("%.2lf\n", max);
    }
    return 0;
}
// For each case output the highest height, the height to two decimal plases;
//
// Sample Input
//
// 2
// 3 170.00 165.00 180.00
// 4 165.00 182.00 172.00 160.00
//
```

---

```cpp
int main() {
	int a = 1;
	a = (5 - 6, 8 + 9, 100 / 7);   // -1, 17, 14
	cout << a << endl;

```

`,` have low priority in cpp, it only consider the rightest value as a , so a == 14

isPrime

```cpp

using namespace std;

//
//   x   有一個因子叫 i，那麼必然有另一個因子叫 x/i
//    i 和 x/i 必然有個大小關係，無論大小關係怎樣，都能推導出 i <= 根號x
bool isPrime(int x) {
    for (int i = 2; i*i <= x; ++i) {
        if (x % i == 0) {
            return false;
        }
    }
    return true;
}

```

```cpp
  cout << (*&a) << endl;
  cout << "-------" << endl;
  cout << (*(&a)) << endl;
  cout << "-------" << endl;
  cout << (*pa) << endl;
  cout << "-------" << endl;
  cout << (a) << endl;
  // pointer dereference
  // all same

  // 3. * 和 &
  // *&a = *(&a) = *pa = a;
  // &*pa = &(*pa) = &a = pa;


```

- `*&a = *(&a) = *pa = a;`
- &*pa = &(*pa) = &a = pa;

**- counting from right hand side damn**

const 和 指針的關係
指針常量
指針的值是一個常量

```cpp

int main() {
    int a = 1;
    int b = 2;
    // 指針常量
    // 指針的值是一個常量
    int* const p = &a;
    // p = &b;   錯誤
    *p = 6;
    cout << "a = " << a << endl;

    return 0;
}

```

`   int* const p = &a;`

- you can't change the p address value like `p=&b`, but you can change `*p=6` (deferenced value)

---

常量指針
指向常量的指針

```cpp

    const int* p = &a;
```

```cpp
int main() {
    int a = 1;
    int b = 2;
    // 常量指針
    // 指向常量的指針
    const int* p = &a;
    // *p = 6; 錯誤
    p = &b;
    cout << "p = " << *p << endl;

    return 0;
}
```

can't change the deferences value `*p = 6` => wrong, but you can change the address of that pointer pointing to

---

both cant' be change pointer

```cpp
/*
指針常量          tpye* const        指針值是一個常量                指針無法被賦值
常量指針          const type*        指向常量的指針                  指針解引用後無法被賦值
常量指針常量      const type* const  指針值和指針指向的值都是常量    指針和解引用都無法被賦值
*/

int main() {
    int a = 1;
    int b = 2;
    // 常量指針常量
    const int* const p = &a;
    // *p = 6;  錯誤
    // p = &b;  錯誤

    return 0;
}
```

this is aka pointer array

```cpp
int main() {
    char a[] = "I";
    char b[] = "love";
    char c[] = "you";

    cout << b << endl; // -> this will print the whole char  as well

    char* p[3];
    p[0] = a;
    p[1] = b;
    p[2] = c;
    for (int i = 0; i < 3; ++i) {
        cout << p[i] << ' ';
    }
    cout << endl;
// output
//  I love you


```

```cpp
    int mat[3][4] = {
        {1,2,3,4},
        {5,6,7,8},
        {9,10,11,12}
    };
    int* pmat[3];
    pmat[0] = mat[0];
    pmat[1] = mat[1];
    pmat[2] = mat[2];
    for (int i = 0; i < 3; ++i) {
        for (int j = 0; j < 4; ++j) {
            cout << *(pmat[i] + j) << ' ';
        }
        cout << endl;
    }

// 1 2 3 4
// 5 6 7 8
// 9 10 11 12

```

array pointer:

```cpp
int main() {
    int(*p)[5];
    int a[4][5] = {
        {4,3,2,1,0},
        {9,8,7,6,5},
        {6,7,8,9,0},
        {5,6,7,8,9}
    };
    p = a;
    cout << p << endl;      // E0    -> EF  ->  F4
    cout << p + 1 << endl;  // F4
    // 20 bit (moved 20 bit)
    // 20 = 4 * 5 = sizeof(int) * 5
    cout << p << ':' << &a[0] << endl; // left : right same address
    cout << p + 1 << ':' << &a[1] << endl; // same address
    return 0;
}
```

- if pointing `a[4][6]` won't work, as size exceed `[5]`
- **it basically point as skipping column**

![](20250302-modern-cpp/2025-09-18-01-02-04.png)

- `p[i] == &(a[i][0])==a[i]` -> storing way

- `int(*p)[5]` -> int pointer that point (\*5) each movement

![](20250302-modern-cpp/2025-09-18-01-11-26.png)

- jumping column
  `&(p[2])` `p+2` -> jumping

![](20250302-modern-cpp/2025-09-18-01-14-11.png)

**- pointer to a pointer -> representing the whole row , damn**

![](20250302-modern-cpp/2025-09-18-01-15-47.png)

```cpp
#include <iostream>
using namespace std;

string getHex(int x) {
    char buff[10];
    sprintf_s(buff, "%X", (x & 0xFFFF));
    return (string)buff;
}

int main() {
    int a[3][4] = {
        {1,2,3,4},
        {5,6,7,8},
        {9,10,11,12}
    };
    for (int i = 0; i < 3; ++i) {
        for (int j = 0; j < 4; ++j) {
            if (j) {
                cout << ",";
            }
            int *p = &a[i][j];
            cout << getHex( (int)p);
        }
        cout << endl;
    }
    // 指針數組
    int* q[3] = { &a[0][0], &a[1][0], &a[2][0] };
    // 數組指針
    int(*p)[4];
    p = &a[0];

    cout << "1、指針 + i" << endl;
    // q + i \ p + i
    cout << "數組指針" << endl;
    for (int i = 0; i < 3; ++i) {
        string s = getHex((int)(p + i));
        cout << "第" << i << "個[4]數組的地址是" << s << endl;
    }
    cout << "指針數組（沒啥用）" << endl;
    for (int i = 0; i < 3; ++i) {
        string s = getHex((int)(q + i));
        cout << "第" << i << "個q元素的地址是" << s << endl;
    }

    cout << "2、*(指針 + i)" << endl;
    // *(q + i)  \   *(p + i)
    cout << "數組指針" << endl;
    for (int i = 0; i < 3; ++i) {
        string s = getHex((int)*(p + i));
        cout << "a數組的第" << i << "行第 0 個元素的地址是" << s << endl;
    }
    cout << "指針數組" << endl;
    for (int i = 0; i < 3; ++i) {
        string s = getHex((int)*(q + i));
        cout << "a數組的第" << i << "行第 0 個元素的地址是" << s << endl;
    }

    cout << "3、*(指針 + i) + j" << endl;
    for (int i = 0; i < 3; ++i) {
        string s = getHex((int)(*(p + i) + 1) );
        cout << "a數組的第" << i << "行第 1 個元素的地址是" << s << endl;
    }
    cout << "指針數組" << endl;
    for (int i = 0; i < 3; ++i) {
        string s = getHex((int)(*(q + i) + 2) );
        cout << "a數組的第" << i << "行第 2 個元素的地址是" << s << endl;
    }


    return 0;
}
```

result:

![](20250302-modern-cpp/2025-09-18-01-25-39.png)

![](20250302-modern-cpp/2025-09-18-01-28-28.png)

```cpp
    cout << "3、*(指針 + i) + j" << endl;
    for (int i = 0; i < 3; ++i) {
        string s = getHex((int)(*(p + i) + 1) );
        cout << "a數組的第" << i << "行第 1 個元素的地址是" << s << endl;
    }
    cout << "指針數組" << endl;
    for (int i = 0; i < 3; ++i) {
        string s = getHex((int)(*(q + i) + 2) );
        cout << "a數組的第" << i << "行第 2 個元素的地址是" << s << endl; // here is + 2 as a `j` example
    }

```

![](20250302-modern-cpp/2025-09-18-01-29-39.png)

---

```cpp
// 函數的值傳遞
void swap(int a, int b) {
  cout << "調用函數後 a 的地址 = " << &a << endl;
  cout << "調用函數後 b 的地址 = " << &b << endl;
  int temp = a;
  a = b;
  b = temp;
}

// 函數的址傳遞
void swap(int *a, int *b) {
  cout << "調用函數後 a 的地址 = " << a << endl;
  cout << "調用函數後 b 的地址 = " << b << endl;
  cout << "----------------" << endl;
  int temp = *a;
  cout << "調用函數後 a 的值p2 = " << *a << endl;
  cout << "調用函數後 b 的值 = " << *b << endl;
  cout << "調用函數temp 的值 = " << temp << endl;
  cout << "----------------" << endl;
  *a = *b;
  cout << "調用函數後 a 的值p3 = " << *a << endl;
  cout << "調用函數後 b 的值 = " << *b << endl;
  cout << "調用函數temp 的值 = " << temp << endl;
  cout << "----------------" << endl;
  *b = temp;
  cout << "調用函數後 a 的值p4 = " << *a << endl;
  cout << "調用函數後 b 的值 = " << *b << endl;
  cout << "調用函數temp 的值 = " << temp << endl;
  cout << "----------------" << endl;
}

int main() {
  int a = 1;
  int b = 2;
  cout << "調用函數前 a 的地址 = " << &a << endl;
  cout << "調用函數前 b 的地址 = " << &b << endl;
  swap(&a, &b);
  cout << "a = " << a << endl;
  cout << "b = " << b << endl;
  cout << "a = " << &a << endl;
  cout << "b = " << &b << endl;
  cout << "----------------" << endl;
  return 0;
}

```

- the address did'nt change , the value did

fuction pointer:

```cpp
#include <iostream>
using namespace std;

// function pointer
double (*ptr)(int a, int b, int c);
void (*ptr1)(int a, int b);

double func(int a, int b, int c) {
  cout << a << "," << b << "," << c << endl;
  return 0.0;
}

void func1(int a, int b) { cout << a << "," << b << endl; }

int main() {
  ptr = func;
  ptr(4, 5, 6);
  // ptr = func1; error becasuse the type of pointer has to match the function as well
  ptr1 = func1;
  ptr1(5, 6);

  return 0;
}
```

- need to match the return type, parameter type

```cpp
// 函數指針的定義
void (*fptr1) (int a, int b, int c, float d, char e);
void (*fptr2) (int a, int b, int c, float d, char e);

void func1(int a, int b, int c, float d, char e) {
    cout << "func1" << endl;
}

// 函數指針的類型定義
typedef void (*fptr) (int a, int b, int c, float d, char e);

```

- typedef -> easy way to use function pointer

self define datatype

```cpp
    fptr1 = func1;
    fptr1(1, 2, 3, 4, 5);

    fptr2 = func1;
    fptr2(9, 8, 7, 6, 5);

    fptr fp1 = func1; //-> much easy, typedef void
    //int  x = 6;
    fp1(7, 6, 5, 4, 3);

```

// 函數指針數組
// (函數指針1, 函數指針2, ... )

```cpp
typedef void (*fptr) (int a, int b, double c, float d, char e);
typedef void (*fptrs[56]) (int a, int b, double c, float d, char e); // here

void func1(int a, int b, double c, float d, char e) {
    cout << "func1" << endl;
}
void func2(int a, int b, double c, float d, char e) {
    cout << "func2" << endl;
}
void func3(int a, int b, double c, float d, char e) {
    cout << "func3" << endl;
}


int main() {
    //int  a[]= {1 ,2, 3 }; similer to this , except `[]` is put in front , defined first
    fptrs fps = {func1, func2, func3};
    cout << fps[0] << endl;
    cout << fps[1] << endl;
    cout << fps[2] << endl;
    cout << fps[3] << endl;

    fptr fp[] = { func1, func2, func3 }; // easier to understand
    cout << fp[0] << endl;
    cout << fp[1] << endl;
    cout << fp[2] << endl;

    return 0;
}

```

- int a[]= {1 ,2, 3 }; similer to this , except `[]` is put in front , defined first for // 函數指針數組

array that contains bunch of function
`typedef void (*fptrs[56]) (int a, int b, double c, float d, char e); // here `

any output exceed the `[max]` will output `0` or `NULL`

`typedef void (*fptr) (int a, int b, double c, float d, char e); `
`   fptr fp[] = { func1, func2, func3 };` -> this way is easier to understand

---

exercise:

```cpp
/*
HDOJ 2081 手機短號
https://acm.hdu.edu.cn/showproblem.php?pid=2081

輸入：輸入 t 組數據，每組數據是一個11位的手機號
輸出：每組數據輸出一個6，再跟上手機號的末五位
*/

#include <iostream>
using namespace std;


//             s+6
// s = 123456   78901
int main() {
    int t;
    cin >> t;
    while (t--) {
        char s[12];
        cin >> s;
        cout << '6' << s + 6 << endl;
    }
    return 0;
}
```

- in cpp , cout<<s will print the whole `char s [12]`, `s +6 ` will print the 6 after

```cpp
/*
HDOJ 2099 整除的尾數
https://acm.hdu.edu.cn/showproblem.php?pid=2099


*/

#include <iostream>
using namespace std;

// a=200, b=40, 返回值[00, 40, 80], *returnSize = 3
int *calcTail(int a, int b,
              int *returnSize) { // 1、返回值代表結果數組的首地址，returnSize
                                 // 是外部傳進來的一個地址
  *returnSize = 0;               // 2、對外部傳進來的數組大小，進行初始化
  int *ret = new int[100];       // 3、申請一個數組內存，最多100個元素
  for (int i = 0; i < 100; ++i) {
    if ((a * 100 + i) % b ==
        0) { // 4、枚舉所有的末兩位，並且判斷是否整除，如果整除則塞入結果數組
      ret[(*returnSize)++] = i; // 5、(*returnSize)++ 代表將數組的大小 + 1
    }
  }
  return ret;
}

int main() {
  int a, b;
  while (cin >> a >> b) {
    if (!a && !b) {
      break;
    }
    int size;
    int *ret = calcTail(a, b, &size);
    // int* ret = calcTail(a, b, &size); ← passes the address so the function
    // can write into size
    // If size were only declared inside the function, the caller wouldn’t know
    // how many elements to print.
    for (int i = 0; i < size; ++i) {
      if (i) {
        cout << " ";
      }
      if (ret[i] < 10) {
        cout << "0";
        // It ensures each tail is printed as two digits (with a leading zero
        // when needed).
        // So 0..9 are printed as 00..09, matching the required format like 00
        // 40 80. Equivalent modern formatting would be cout << setw(2) <<
        // setfill('0') << ret[i];.
      }
      cout << ret[i];
    }
    cout << endl;
    delete[] ret;
  }
  return 0;
}
```

cpp struct:

```cpp
#include <iostream>
#include <string>
using namespace std;

// 1. 結構體定義
// struct 結構體名 { 結構體成員變量列表 };
struct Book {
	string name;
	double price;
	int value;
}cpp; // method 3

// 2. 創建結構體

int main() {
	// 2.1
	Book c;
	c.name = "C語言程序設計";
	c.price = 39.99;
	c.value = 10;
	cout << c.name << ' ' << c.price << ' ' << c.value << endl;

	// 2.2
	Book py = { "Python編程", 1999, 10 }; // method 2
	cout << py.name << ' ' << py.price << ' ' << py.value << endl;

	// 2.3
	cpp.name = "C++零基礎編程";
	cpp.price = 9999999;
	cpp.value = 10000000;
	cout << cpp.name << ' ' << cpp.price << ' ' << cpp.value << endl;

	return 0;
}
```

more :

```cpp
// 1. 結構體定義
// struct 結構體名 { 結構體成員變量列表 };
struct Book {
	string name;
	double price;
	int value;
}cpp;

int main() {
	// 2. 創建一個結構體數組
	// Book 數組名[元素個數] = { {}, {}, {}, ... };
	Book books[3] = {
		{"C語言程序設計", 199.99, 7},
		{"Python零基礎", 399.99, 9},
		{"C++零基礎", 39.99, 1000000}
	};
	books[2].name = "C++入門到入土！";
	for (int i = 0; i < 3; ++i) {
		cout << books[i].name << ' ' << books[i].price << ' ' << books[i].value << endl;
	}

	return 0;
}

```

```cpp
// 1. 結構體定義
// struct 結構體名 { 結構體成員變量列表 };
struct Book {
	string name;
	double price;
	int value;
};

int main() {
	Book b = {"C語言", 99.99, 7};
	Book c = b;
	c.name = "C語言入門";
	Book* pb = &b;
	pb->name = "C++";
	cout << b.name << ' ' << b.price << ' ' << b.value << endl;

	return 0;
}

```

have to use pointer address to modify the value
python will work though just using `Book c = b; c.name == "xxx"`

- nested struct damn:

```cpp
#include <iostream>

using namespace std;

struct Point {
    double x, y;
};

struct Circle {
    Point pt;
    double radius;
};

struct Circles {
    int size;
    Circle c[100];
};


int main() {
    Circle c;
    c.pt.x = 9;
    c.pt.y = 8;
    c.radius = 5;

    Circles cs = {
        2, {
            { {9,8}, 5 },
            { {2,1}, 1 }
        }
    };
    for (int i = 0; i < cs.size; ++i) {
        Circle tmp = cs.c[i];
        cout << "(" << tmp.pt.x << "," << tmp.pt.y << ") " << tmp.radius << endl;
    }

    return 0;
}
```

for three usage of circle, use three `{{{ }}}` to initiate the nested struct

- `  Circle tmp = cs.c[i];` using second level struct tmp to get the value

continue:

```cpp
void printCircle(const Circle *c) {
    // c->pt.x += 1; 常量不可修改
    cout << "(" << c->pt.x << "," << c->pt.y << ") " << c->radius << endl;
}

void moveCircle(Circle *c, int x, int y) {
    //cout << &c << endl;
    c->pt.x += x;
    c->pt.y += y;
}

int main() {
    Circle c = { {9,8}, 5 };
    //cout << &c << endl;
    moveCircle(&c, 1, -2);
    printCircle(&c);
    return 0;
}

```

- the `main()` and `moveC()` have different `& c` if not setting `Circle *c ` c as pointer AND
- have to use pointer `->` `c->pt.x`

- `void printCircle(const Circle *c) { ` is very useful , adding `const` -> read only or
  just printCircle(c) will work as well -> but this way will copy the memory again, not change the og though

```cpp
void printCircle(Circle c) { // copy another one version
  // c->pt.x += 1; 常量不可修改
  cout << "(" << c.pt.x << "," << c.pt.y << ") " << c.radius << endl;
}

```

```cpp
/*
HDOJ 2037 今年暑假不AC
https://acm.hdu.edu.cn/showproblem.php?pid=2037

輸入：反覆輸入一個n，代表有n個區間，然後輸入n個區間
輸出：輸出選擇最多的區間數，保證所有的區間都不重疊

*/

#include <iostream>
#include <algorithm>
using namespace std;

struct Interval {
    int s;
    int e;
}I[100];

bool cmp(const Interval& a, const Interval& b) {
    return a.e < b.e;
}

int main() {
    int n;
    while (cin >> n && n) {
        for (int i = 0; i < n; ++i) {
            cin >> I[i].s >> I[i].e;
        }
        sort(I, I + n, cmp);
        int end = -1;
        int ans = 0;
        for (int i = 0; i < n; ++i) {
            if (I[i].s >= end) {
                ans++;
                end = I[i].e;
            }
        }
        cout << ans << endl;

    }
    return 0;
}
```

using greedy algo sort, start with end time of each tv show
**Why this works:**

- Selecting the earliest-ending activity leaves maximum room for future activities
- This ensures we never "waste" time slots unnecessarily

### Algorithm Steps

1. **Sort all activities by end time** (earliest first)
2. **Select the first activity** (earliest ending)
3. **For each remaining activity:**
   - If it starts after the last selected activity ends → select it
   - Otherwise → skip it

**Step 1: Sort by end time**

```
Original:  (1,3) (3,4) (0,7) (3,8) (5,10) (6,12) (2,9) (4,14) (10,15) (8,18) (15,19) (15,20)
Sorted:    (1,3) (3,4) (0,7) (3,8) (5,10) (2,9) (6,12) (4,14) (10,15) (8,18) (15,19) (15,20)
End times:   3     4     7     8    10     9    12    14    15    18    19    20
```

**Step 2: Greedy Selection**

```
Activity 1: (1,3) - end=3
  - start(1) >= end(-1) ✓ → Select, end = 3

Activity 2: (3,4) - end=4
  - start(3) >= end(3) ✓ → Select, end = 4

Activity 3: (0,7) - end=7
  - start(0) < end(4) ✗ → Skip

Activity 4: (3,8) - end=8
  - start(3) < end(4) ✗ → Skip

Activity 5: (5,10) - end=10
  - start(5) >= end(4) ✓ → Select, end = 10
```

### Common Mistakes to Avoid

1. **Sorting by start time instead of end time** - This doesn't guarantee optimality
2. **Sorting by duration** - Longer activities aren't necessarily better
3. **Not checking for conflicts properly** - Must ensure `start >= previous_end`

### Applications

This algorithm applies to many real-world problems:

- **Resource scheduling** (meeting rooms, CPU scheduling)
- **Event planning** (conferences, classes)
- **Job scheduling** (non-preemptive tasks)
- **Memory allocation** (non-overlapping memory blocks)

```cpp
// CORRECT: This prevents overlapping
if (I[i].s >= end) {
// CORRECT: Ensures first activity is considered
int end = -1;

```

```cpp
int end = -1;  // Initialize to impossible value
int ans = 0;   // Counter for selected activities

for (int i = 0; i < n; ++i) {
    if (I[i].s >= end) {  // Check for no overlap
        ans++;             // Increment counter
        end = I[i].e;      // Update end time
    }
}
```

---

## union vs struct

- struct each elements contains its own memory
- union each elements share memory

#### Step 2: Determine Alignment Requirement

The union must be aligned to accommodate the **strictest alignment requirement**:

- `int i`: requires 4-byte alignment
- `double d`: requires 8-byte alignment ← STRICTEST
- `char s[10]`: requires 1-byte alignment

**Result**: Union must be 8-byte aligned

#### Step 3: Calculate Minimum Size

```
Largest member: 10 bytes
Alignment requirement: 8 bytes
Minimum size: max(10, 8) = 10 bytes
```

#### Step 4: Add Padding for Alignment

```
Current size: 10 bytes
Required alignment: 8 bytes
Padding needed: 8 - (10 % 8) = 8 - 2 = 6 bytes
Final size: 10 + 6 = 16 bytes

```

```cpp
#include <iostream>
using namespace std;

struct DataS {
  int i;
  double d;
  char s[10];
};

union DataU {
  int i;      // 4
  double d;   // 8
  char s[10]; // 10
};

/*
1、定義和使用分開
union DataU {
    int i;     // 4
    double d;  // 8
    char s[10];// 10
};
DataU a, b, c;

2、定義和使用結合
union DataU {
    int i;     // 4
    double d;  // 8
    char s[10];// 10
}a, b, c;

3、匿名：不想讓別人使用
union {
    int i;     // 4
    double d;  // 8
    char s[10];// 10
}a, b, c;

*/

int main() {
  DataS ds;
  cout << &ds.i << "," << &ds.d << "," << (void *)ds.s << endl;

  DataU du;
  cout << &du.i << "," << &du.d << "," << (void *)du.s << endl;
  cout << sizeof(ds) << endl;
  cout << sizeof(du) << endl;

  return 0;
}
```

```cpp
#include <iostream>
using namespace std;

union DataU {
    int i;      // 4
    double d;   // 8
    char s[7];  // 7
};

int main() {
    cout << sizeof(DataU) << endl;
    DataU du;
    du.s[0] = 255;      // 11111111
    du.s[1] = 1;        // 00000001
    du.s[2] = 0;        // 00000000
    du.s[3] = 0;        // 00000000
    cout << du.i << endl; // 00000000 00000000 00000001 11111111 // output 511
    du.i = 256;
    cout << (int)du.s[0] << (int)du.s[1] << (int)du.s[2] << (int)du.s[3] << endl;

    return 0;
}
```

**What happens:**

- **The same memory is interpreted** as a 4-byte integer
- Little-endian byte order: least significant byte first
- The 4 bytes are: `[255, 1, 0, 0]`

Result: 00000000 00000000 00000001 11111111 = 511

du.i = 256;
cout << (int)du.s[0] << (int)du.s[1] << (int)du.s[2] << (int)du.s[3] << endl;

-> out put 0100 (Big - endian)

however if du.i =255 (int) -> negative -> -1000

---

```cpp
#include <cstring>
#include <iostream>
using namespace std;

struct Info {
  char _name[20];
  int _role;
  union {
    double score;
    char course[20];
  } _sc;

  Info(const char name[20], int role, double s, const char c[20]) {
    strcpy(_name, name);
    _role = role;
    if (s > 0)
      _sc.score = s;
    if (strlen(c) > 0)
      strcpy(_sc.course, c);
  }
};

int main() {
  Info a[4] = {
      Info("周老師", 0, -1, "CGaGa"),
      Info("周老師", 0, -1, "Python"),
      Info("周同學", 1, 90, ""),
      Info("肖同學", 1, 88, ""),
  };
  for (int i = 0; i < 4; ++i) {
    if (a[i]._role == 0) {
      cout << a[i]._name << "是一位老師，他是教" << a[i]._sc.course << "的"
           << endl;
    } else if (a[i]._role == 1) {
      cout << a[i]._name << "是一位學生，他的分數是" << a[i]._sc.score << endl;
    }
  }

  return 0;
}
```

- union make is either xx or xx type, save memory

## 12、内存管理

// 代碼區、全局區、棧區、堆區
代碼區:

```cpp

#include <iostream>
using namespace std;

// 代碼區、全局區、棧區、堆區

void printMessage() {
    cout << "Hello world!" << endl;
}
int main() {
    printMessage();
    while(1) {}
    return 0;
}

```

全局區:

```cpp
#include <iostream>
using namespace std;

// 全局區
// 全局變量、全局常量、靜態變量(inside main)、字符串常量 (inside main) they are put in the same memory location

int g_a = 1;
int g_b = 2;
const int c_g_a = 3;
const int c_g_b = 4;

int main() {
    cout << "全局變量g_a的地址：" << &g_a << endl;
    cout << "全局變量g_b的地址：" << &g_b << endl;

    int c = 3;
    int d = 4;
    static int e = 5;
    static int f = 6;
    cout << "局部變量c的地址：" << &c << endl;
    cout << "局部變量d的地址：" << &d << endl;
    cout << "靜態變量e的地址：" << &e << endl;
    cout << "靜態變量f的地址：" << &f << endl;

    cout << "字符串常量的地址：" << &"英雄哪裏出來" << endl;

    const int g = 7;
    const int h = 8;
    cout << "局部常量g的地址：" << &g << endl;
    cout << "局部常量h的地址：" << &h << endl;

    cout << "全局常量c_g_a的地址：" << &c_g_a << endl;
    cout << "全局常量c_g_b的地址：" << &c_g_b << endl;

    return 0;
}
```

全局區
全局變量、全局常量、靜態static變量(inside main)、字符串常量 (inside main) they are put in the same memory location

inside main() variable:

stack memory

```cpp
#include <iostream>
using namespace std;

//stack memory

char* func() {
    char c[20] = "英雄哪裏出來";
    return c;
}

void test(int a, int b) {
    int c, d;
    cout << "形式參數a的地址：" << &a << endl;
    cout << "形式參數b的地址：" << &b << endl;
    cout << "局部變量c的地址：" << &c << endl;
    cout << "局部變量d的地址：" << &d << endl;
  // stack memory , close address
}


int main() {
    cout << func() << endl;
    test(5, 6);
    return 0;
}
```

the string memory of `c[20]` store in heap memory , stack memory will erase that memory after return c;, so this func()
won't work

Memory Management Best Practices

### DO's

1. **Use stack** for local variables and temporary data
2. **Use heap** for data that needs to persist beyond function scope
3. **Always free** heap memory after use
4. **Use RAII** (Resource Acquisition Is Initialization)
5. **Use smart pointers** for automatic memory management

### DON'Ts

1. **Never return** addresses of local variables
2. **Never use** freed memory
3. **Never forget** to free heap memory
4. **Never assume** memory layout
5. **Never use** uninitialized pointers

### Common Memory Errors

#### 1. Dangling Pointer

```cpp
char* func() {
    char c[20] = "hello";
    return c;  // DANGEROUS!
}
```

#### 2. Memory Leak

```cpp
char* func() {
    char* c = new char[20];
    return c;  // OK, but must free later
}
// If not freed: MEMORY LEAK
```

#### 3. Double Free

```cpp
char* c = new char[20];
delete[] c;
delete[] c;  // ERROR: Double free
```

#### 4. Use After Free

```cpp
char* c = new char[20];
delete[] c;
strcpy(c, "hello");  // ERROR: Use after free
```

### Modern C++ Solutions

#### Smart Pointers

```cpp
##include <memory>

std::unique_ptr<char[]> func() {
    auto c = std::make_unique<char[]>(20);
    strcpy(c.get(), "英雄哪裏出來");
    return c;  // Automatic cleanup
}
```

#### RAII Classes

```cpp
class StringBuffer {
    char* data;
    size_t size;
public:
    StringBuffer(size_t s) : size(s) {
        data = new char[size];
    }
    ~StringBuffer() {
        delete[] data;  // Automatic cleanup
    }
    // ... other methods
};
```

---

heap memory:

// malloc free
// new delete

```cpp
#include <iostream>
using namespace std;

// malloc free (c) -> function
// new delete (cpp) -> +*/ -> math operation

int* getV(int v) {
    int* a = new int(v);  // int *a 是一個棧 stack上的變量
    cout << a << endl;    // *a 也就是 a 解引用以後得到的值，是存儲在堆上面的
    return a;             // 函數返回的時候，雖然棧上的變量 a 被操作系統釋放了，但是 a 指向的內存，還是存在的
}

int main() {
    int *p = getV(1314);
    cout << *p << endl;   // 所以，這裏還是可以解引用，得到堆上的數據的
    cout << p << endl;
    return 0;
}
```

so usig new () for creating heap memory , even the stack variable is erase after the return , but it successfully pass
the task to heap memory and then disappear

### Code Analysis

```cpp
int *getV(int v) {
    int *a = new int(v);  // Stack: pointer 'a', Heap: value 'v'
    cout << a << endl;    // Prints heap address
    return a;             // Returns heap address (safe!)
}
```

### Memory Creation Timeline

#### 1. **Stack Memory Creation**

- **When**: Function `getV()` is called
- **What**: Local pointer variable `a` is created on stack
- **Lifecycle**: Exists only during function execution
- **Cleanup**: Automatically destroyed when function returns

#### 2. **Heap Memory Creation**

- **When**: `new int(v)` is executed
- **What**: Integer value `1314` is allocated on heap
- **Lifecycle**: Exists until manually freed with `delete`
- **Cleanup**: Must be manually managed by programmer

### Visual Memory Layout

```
During getV(1314) execution:

STACK MEMORY:
Address: 0x7ffdc7f870e0
         |------|
         |  a   |  ← Pointer variable (stack)
         |0x6000|  ← Points to heap address
         |------|

HEAP MEMORY:
Address: 0x600000000000
         |------|
         | 1314 |  ← Actual value (heap)
         |------|
```

### After Function Returns

```
STACK MEMORY:
Address: 0x7ffdc7f870e0
         |------|
         | ???  |  ← Variable 'a' destroyed
         |------|

HEAP MEMORY:
Address: 0x600000000000
         |------|
         | 1314 |  ← Value still exists!
         |------|
```

### Why Heap Memory Persists

#### Key Points:

1. **Stack variable `a`**: Destroyed when function returns
2. **Heap value `1314`**: Remains until `delete` is called
3. **Returned address**: Points to persistent heap memory
4. **Safe dereference**: `*p` works because heap memory still exists

### Memory Management Rules

#### Stack Memory:

- ✅ **Automatic allocation/deallocation**
- ✅ **Fast access**
- ❌ **Function-scoped only**
- ❌ **Cannot return addresses**

#### Heap Memory:

- ✅ **Persists beyond function scope**
- ✅ **Can return addresses safely**
- ❌ **Manual management required**
- ❌ **Must call `delete` to free**

### Complete Example Flow

```cpp
int main() {
    int *p = getV(1314);    // p gets heap address
    cout << *p << endl;     // ✅ Works: heap memory exists
    cout << "what" << endl;
    cout << p << endl;      // ✅ Works: prints heap address
    // delete p;            // ❌ Missing: memory leak!
    return 0;
}
```

### Key Takeaways

1. **Stack variables**: Destroyed when function returns
2. **Heap memory**: Persists until manually freed
3. **Returning heap addresses**: Safe and valid
4. **Returning stack addresses**: Dangerous (dangling pointer)
5. **Memory leak**: Forgot to call `delete p` in main()

### Memory Leak Fix

```cpp
int main() {
    int *p = getV(1314);
    cout << *p << endl;
    cout << "what" << endl;
    cout << p << endl;
    delete p;  // ✅ Free heap memory
    return 0;
}
```

**Summary**: Stack pointer `a` is destroyed, but heap value `1314` persists, making the returned address safe to dereference.

---

new , delete (controlling heap memory)

```cpp
// new ºÍ delete

#include <iostream>
using namespace std;

int main() {
  // int *ptr1 = new int; // non initiate example
  // cout << *ptr1 << endl;
  int *ptr = new int(1314);
  *ptr = 520;
  cout << *ptr << endl;

  delete ptr;
  ptr = NULL; // using this for late people using if status to decide use it or
              // not
  return 0;
}
```

array new , and delete

```cpp
#include <iostream>
using namespace std;

int* getGapList(int *arr, int size) {
    int *p = new int[size - 1];
    // int a[size-1];  return a;  a 是棧上的內存，不能作為返回值返回
    for (int i = 0; i < size - 1; ++i) {
        p[i] = arr[i + 1] - arr[i];
    }
    return p;
}

int main() {
    int arr[] = { 1,5,6,4,4,3,3,2,1,9 };
    int* p = getGapList(arr, 10);
    for (int i = 0; i < 9; ++i) {
        cout << p[i] << " ";
    }
    cout << endl;
    delete[] p;
    p = NULL;

    return 0;
}
```

---

## 引用：給變量取一個別名 (reference) easy way of pointer

- stl using a lot of this, just a easier way to use pointer

```cpp
#include <iostream>
using namespace std;

int main(int argc, char *argv[]) {
  int a = 1314;
  int *b = &a;
  *b = 520;
  std::cout << "a  " << a << endl;
  std::cout << "b  " << *b << endl;
  return 0;
}

#include <iostream>
using namespace std;

int main(int argc, char *argv[]) {
  int a = 1314;
  int &b = a;
  b = 520;
  std::cout << "a  " << a << endl;
  return 0;
}

```

- they are same, once using pointer and address, one just directly setting address as a
  but less code, only one `&` replacing ` 3 * and 1 &` pointer way

```cpp
#include <iostream>
using namespace std;

// 指針：所以愛會消失，對嘛？
// 引用：給變量取一個別名
// &
// 數據類型& 變量名 = 變量;

void test() {
    int a_very_very_very_very_very_very_very_long_array[8] = { 1, 1 };
    for (int i = 2; i < 8; ++i) {
        a_very_very_very_very_very_very_very_long_array[i] = a_very_very_very_very_very_very_very_long_array[i - 1] * a_very_very_very_very_very_very_very_long_array[i - 1] + a_very_very_very_very_very_very_very_long_array[i - 2] * a_very_very_very_very_very_very_very_long_array[i - 2];
    }
    for (int i = 0; i < 8; ++i) {
        cout << a_very_very_very_very_very_very_very_long_array[i] << " "; // just print
    }
    cout << endl;
    for (int i = 2; i < 8; ++i) {
        a_very_very_very_very_very_very_very_long_array[i] = 0; // clean that up for next
    }

    for (int i = 2; i < 8; ++i) {
        int& pre1 = a_very_very_very_very_very_very_very_long_array[i - 1];
        int& pre2 = a_very_very_very_very_very_very_very_long_array[i - 2];
        int& now = a_very_very_very_very_very_very_very_long_array[i];
        now = pre1 * pre1 + pre2 * pre2;
    }
    for (int i = 0; i < 8; ++i) {
        cout << a_very_very_very_very_very_very_very_long_array[i] << " ";
    }
    cout << endl;
}

int main() {
    /*
    int a = 1314;
    int& b = a;
    b = 520;
    cout << "a = " << a << endl;
    cout << "b = " << b << endl;
    */
    int a = 1314;
    int* b = &a;
    *b = 520;
    cout << "a = " << a << endl;
    cout << "b = " << *b << endl;

    test();

    return 0;
}
```

---

cpp reference rules , **difference btw pointer** ,

**// 1、必須初始化
// 2、初始化以後無法修改**

```cpp
#include <iostream>
using namespace std;

// 1、必須初始化
// 2、初始化以後無法修改

int main() {
    // int& a; 錯誤寫法
    int a = 3, c = 6;
    int& b = a;
    b = c;  // b = 6;
    cout << a << b << c << endl;
    return 0;
}

//output is 666 , it changed all the variable into one
```

- cpp reference is using pointer const from assembly

```cpp
#include <iostream>
using namespace std;

// 引用    解引用

int main() {
  int a = 520;
  // int &b = a; // 00007FF7D5C81865  lea         rax,[a]
  //  00007FF7D5C81869  mov         qword ptr[b], rax

  // b = 1314; // 00007FF7D5C8186D  mov         rax,qword ptr [b]
  //  00007FF7D5C81871  mov         dword ptr[rax], 522h

  int *const b = &a; // 00007FF77E9B1865  lea         rax,[a]
  //                    // 00007FF77E9B1869  mov         qword ptr[b], rax
  *b = 1314; // 00007FF77E9B186D  mov         rax, qword ptr[b]
  // 00007FF77E9B1871  mov         dword ptr[rax], 522h

  return 0;
}

```

#### Constant Pointer (C):

```cpp
int *const b = &a;  // Constant pointer to 'a'
*b = 1314;         // Changes 'a' through pointer
```

### What `const` Means Here

#### `int *const b`:

- **`b` is constant** - cannot be reassigned
- **`*b` is mutable** - the value it points to can be changed

#### Examples:

```cpp
int a = 520;
int c = 100;
int *const b = &a;

// ✅ Valid operations:
*b = 1314;        // Change the value 'b' points to
cout << *b;       // Read the value 'b' points to

// ❌ Invalid operations:
b = &c;           // ERROR: Cannot reassign constant pointer
b = nullptr;      // ERROR: Cannot reassign constant pointer
```

```cpp
#include <iostream>
using namespace std;

int countAndSum(int arr[], int size, int target, int& count) {
    int sum = 0;
    cout << &count << endl;
    for (int i = 0; i < size; ++i) {
        if (arr[i] == target) {
            count++;
            sum += arr[i];
        }
    }
    return sum;
}

struct S {
    int a, b, c, d, e, f, g;
};

void printS(S& s) {
    cout << &s << endl;
    cout << s.a << s.b << s.c << s.d << s.e << s.f << s.g << endl;
}

int main() {
    int arr[] = { 1,2,3,2,4,5,6,4,3,2 };  // 10
    int c = 0;
    cout << &c << endl;
    int sum = countAndSum(arr, 10, 2, c);
    cout << sum << " " << c << endl;

    S s = { 1,2,3,4,5,6,7 };
    cout << &s << endl;
    printS(s);

    return 0;
}
```

just a study of memory btw reference , and c pointer dereference

---

117_13-5引用作为函数返回值

```cpp
#include <iostream>
using namespace std;

int& getArrayValue(int arr[], int index) {
    return arr[index];
}

int main() {
    int a[] = { 8,7,6,5,4,3 };
    cout << getArrayValue(a, 3) << endl;

    getArrayValue(a, 3) = 999;   // a[3] = 999;

    cout << getArrayValue(a, 3) << endl;

    return 0;
}
```

- so that you don't need to write anoter setArrayvalue but just change the address

---

118_13-6常量引用

```cpp
#include <iostream>
#include <vector>
using namespace std;

struct S {
    int a, b, c, d, e, f;
};

void printS(const S& s) {
    // s.b = 520;
    cout << s.a << s.b << s.c << s.d << s.e << s.f << endl;
}

int main() {
    int a;
    const int& b = a;
    // 引用 = 指針常量
    // 常量引用 = 常量指針常量
    S s = { 1,2,3,4,5,6 };
    printS(s);

    vector<int> a;

    return 0;
}
```

```cpp

void printS(const S& s) {
}

//ban people changing the value of that deference value
```

---

119_13-7指针引用 done

`*&`

```cpp
#include <iostream>
using namespace std;

// *&

void allocMemory1(char *ptr, int bytes) {
  ptr = new char[bytes];
  cout << "ptr 的地址：" << &ptr << endl;
}

void test1() {
  char *p = NULL;
  allocMemory1(p, 5);
  cout << (void *)p << endl;
  cout << "  p 的地址：" << &p << endl;
}

void allocMemory2(char *&ptr, int bytes) {
  ptr = new char[bytes];
  cout << "ptr 的地址：" << &ptr << endl;
}

void test2() {
  char *p = NULL;
  allocMemory2(p, 5);
  cout << (void *)p << endl;
  cout << "  p 的地址：" << &p << endl;
}

int main() {
  // test1();
  test2();
  return 0;
}
```

- using `void allocMemory2(char *&ptr, int bytes) { ` `*& tr`
  to make `ptr = new char[bytes];` to have same heap memory address

---

```cpp
#include <iostream>
using namespace std;

/*
訪問權限
公共權限   public         類內可以訪問，類外也可以訪問
保護權限   protected      類內可以訪問，類外不可以訪問    子類可以訪問
私有權限   private        類內可以訪問，類外不可以訪問    子類不可以訪問

B -> A

A  父類、基類       名字、房子、支付密碼
B  子類、派生類     公有、保護、私有

*/


class People {
    // 公有權限
public:
    int m_Id;

    // 保護權限
protected:
    int m_HouseId;

    // 私有權限
private:
    int m_PayPass;

public:
    void work() {
        // 所有成員變量，類內均可以訪問
        m_Id = 1;
        m_HouseId = 2;
        m_PayPass = 1314;
    }
private:
    void work1() {
        // 所有成員變量，類內均可以訪問
        m_Id = 1;
        m_HouseId = 2;
        m_PayPass = 1314;
    }

};


class Son : public People {
    void func() {
        m_Id = 1;
        m_HouseId = 4;    // 保護成員，子類可以訪問
        // m_PayPass = 123;  // 私有成員，子類無法訪問
    }
};

int main() {
    // 實例化
    People p;
    p.m_Id = 1;       // 公有成員，類外可以訪問
    //p.m_HouseId = 5;  // 保護成員，類外不可以訪問
    //p.m_PayPass = 10; // 私有成員，類外不可以訪問
    p.work();
    // p.work1();        // 私有成員函數，類外不可訪問
    return 0;
}
```

---

```cpp
#include <iostream>
using namespace std;

/*
struct && class


struct 默認是公共的
class  默認是私有的
*/

class C {
    int m_a;
};

struct S {
    int m_a;

    void func() {
        m_a = 666;
    }
};

int main() {
    C c;
    S s;
    // c.m_a;      // 私有的
    s.m_a = 4;  // 公有的
    s.func();
    cout << s.m_a << endl;

    return 0;
}
```

- cpp struct ( could define fn) vs c struct (couldn't)

---

```cpp
#include <iostream>
#include <string>
using namespace std;

// 接口、方法、函數 是同一個概念
// 1、可以控制讀寫權限
// 2、可以檢測數據的有效性

class Hero {
public:
    void SetName(string name) {
        m_Name = name;
    }
    string GetName() {
        return m_Name;
    }

    int GetSkillCount() {
        return m_SkillCount;
    }

    void SetSpeed(int speed) {
        if (speed < 100 || speed > 500) {
            cout << "速度設置不合法" << endl;
            return;
        }
        m_Speed = speed;
    }

private:
    string   m_Name;            // 可讀，可寫
    int      m_SkillCount = 4;  // 只讀
    int      m_Speed;           // 只寫
};

int main() {
    Hero h;
    /*
        h.m_Name = "123";
        h.m_SkillCount = 4;
        h.m_Speed = 10;
    */
    h.SetName("劍聖");
    cout << "英雄的名字叫：" << h.GetName() << endl;
    cout << "英雄的技能數是：" << h.GetSkillCount() << endl;
    h.SetSpeed(666);


    return 0;
}
```

2、可以檢測數據的有效性
set -> one time to let later set use same fn

---

```cpp
#include <iostream>
#include <string>
using namespace std;

/*
構造函數需要注意的點

1、函數名稱和類名保持一致
2、返回值類型 不需要寫
3、構造函數可以有參數
*/
class Hero {
public:
  // 默認構造函數
  Hero() {
    m_Name = "";
    m_SkillCount = 4;
    m_Speed = 100;
    cout << "默認構造函數：Hero 構造完畢！" << endl;
  }
  // 有參構造函數1
  Hero(string name) {
    m_Name = name;
    m_SkillCount = 4;
    m_Speed = 100;
    cout << "有參構造函數1：Hero 構造完畢！" << endl;
  }
  // 有參構造函數2
  Hero(string name, int skillCount) {
    m_Name = name;
    m_SkillCount = skillCount;
    m_Speed = 100;
    cout << "有參構造函數2：Hero 構造完畢！" << endl;
  }

private:
  string m_Name;
  int m_SkillCount;
  int m_Speed;
};

int main() {
  Hero h1;
  Hero h2("劍聖");
  std::cout << "test";
  Hero h3(); // 函數聲明    int main();   、   int work(); not gonna build (function declaration)
  std::cout << "test2" << endl;
  Hero h4{};
  std::cout << "test3" << endl;
  Hero h5 = Hero("劍聖");
  Hero h6{"猴子", 4};

  return 0;
}
```

`Hero h5 = Hero("劍聖");`

` Hero h3(); // 函數聲明    int main();   、   int work(); not gonna build (function declaration)`

1、函數名稱和類名保持一致
2、返回值類型 不需要寫
3、構造函數可以有參數

---

## 析構函數注意點 Destructor

```cpp
#include <iostream>
using namespace std;

/*
析構函數注意點 Destructor

1、函數名稱和類名一致，並且在最前面加上一個 ~ 波浪號
2、函數返回值不需要寫
3、不能有參數

*/
class Hero {
public:
  // 構造函數
  Hero() { cout << "Hero 默認構造函數調用完畢！" << endl; }
  // 析構函數
  ~Hero() { cout << "Hero 析構函數調用完畢！" << endl; }
};

void test() { Hero h; }

int main() {
  test();
  Hero h;
  int a;
  cin >> a;
  // it will wait until the program really finish (after cin)
  return 0;
}
```

- it will wait until the program really finish (after cin) , no ~hero() immediatly

---

拷貝構造函數的定義

```cpp
#include <iostream>
using namespace std;


/*
拷貝構造函數的定義
類名(const 類型& 變量名) {}

*/
class Hero {
public:
    // 默認構造函數
    Hero() {
        m_Hp = 100;
        cout << "Hero 默認構造函數調用完畢！" << endl;
    }

    // 有參構造函數
    Hero(int hp) {
        m_Hp = hp;
        cout << "Hero 有參構造函數調用完畢！" << endl;
    }

    Hero(const Hero& h) {
        m_Hp = h.m_Hp;
        cout << "Hero 拷貝構造函數調用完畢！" << endl;
    }

    // 析構函數
    ~Hero() {
        cout << "Hero 析構函數調用完畢！" << endl;
    }

private:
    int   m_Hp;
};


/*
拷貝構造函數的調用時機

1、用已經創建的對象來初始化對象
2、函數的傳參
3、函數的返回值

*/

// 1、用已經創建的對象來初始化對象
void func1() {
    cout << "--------------func1--------------" << endl;
    Hero h1(20);
    Hero h2(h1);
}

void test1(Hero h) {

}

void test2(Hero* h) {

}

// 2、函數的傳參
void func2() {
    cout << "--------------func2--------------" << endl;
    Hero h1;
    // test1(h1);
    test2(&h1);
}

// 3、函數的返回值
Hero test3() {
    Hero h(40);
    return h;
}

void func3() {
    cout << "--------------func3--------------" << endl;
    Hero h = test3();
}

int main() {
    func1();
    func2();
    func3();
    return 0;
}
```

```cpp
    Hero(const Hero& h) { // need to use const
        m_Hp = h.m_Hp;
        cout << "Hero 拷貝構造函數調用完畢！" << endl;
    }

```

`const Hero&` make it unchangeable , then copy it

/_
拷貝構造函數的調用時機
1、用已經創建的對象來初始化對象
2、函數的傳參
3、函數的返回值
_/

2`fun2 wont work because it the para is pointer , pointer won't create a new object so it is not going **copy the object**
you can call the function and destruct it , but missing copy there in func2 and func3

func3 will show copy success , but compiler `rvo ` optimized it , so it won't show without config

---

靜態成員函數

```cpp

#include <iostream>
#include <string>
using namespace std;

/*
靜態成員變量的特點：
1、所有的對象共享同一份數據
2、編譯階段分配內存
3、需要在類中進行聲明，在類外進行初始化
*/

class Hero {
public:
  Hero() {
    m_Name = "英雄";
    m_Hp = 100;
  }

  ~Hero() {}
  // 3.1 聲明
  static int m_HeroCount;

private:
  string m_Name;
  int m_Hp;
};

// 3.2 初始化
int Hero::m_HeroCount = 100;

int main() {
  Hero h;
  cout << h.m_HeroCount << endl;
  h.m_HeroCount = 101;
  cout << Hero::m_HeroCount << endl;

  cout << &(h.m_HeroCount) << endl;
  cout << &(Hero::m_HeroCount) << endl;
  return 0;
}
```

```cpp

  // 3.1 聲明
  static int m_HeroCount;
// 3.2 初始化
int Hero::m_HeroCount = 100;

  cout << h.m_HeroCount << endl;
  h.m_HeroCount = 101;
  cout << Hero::m_HeroCount << endl;

  cout << &(h.m_HeroCount) << endl;
  cout << &(Hero::m_HeroCount) << endl;

```

- they are the same address, h. and Hero::

/_
靜態成員函數
1、所有對象共享函數
2、靜態成員函數只能使用靜態成員變量，無法使用普通成員變量3. **Inside class declaration, than class outside initiate it **
_/

---

```cpp
#include <iostream>
#include <string>
using namespace std;

/*
靜態成員函數
1、所有對象共享函數
2、靜態成員函數只能使用靜態成員變量，無法使用普通成員變量
*/

class Hero {
public:
  Hero() {
    m_Name = "英雄";
    m_Hp = 100;
  }
  ~Hero() {}

  static int m_HeroCount;

  static int GetHeroCount() {
    // m_Hp += 1;
    return m_HeroCount;
  }

private:
  string m_Name;
  int m_Hp;

  static int GetHeroCount1() {
    // m_Hp += 1;
    return m_HeroCount;
  }
};

int Hero::m_HeroCount = 100;

int main() {
  Hero h;
  cout << h.GetHeroCount() << endl;
  cout << Hero::GetHeroCount() << endl;
  // h.GetHeroCount1();
  return 0;
}
```

- Static func cant' modify `   // m_Hp += 1;`

---

## this指針

```cpp
this指針
1、解決命名衝突
2、*this 就可以獲取到這個對象本身

this     *this
 &h      *(&h) == h

```

```cpp
#include <iostream>
using namespace std;

/*
this指針
1、解決命名衝突
2、*this 就可以獲取到這個對象本身


this     *this
 &h      *(&h) == h

*/

class Hero {
public:
  Hero(int hp) {
    this->hp = hp;
    cout << this << endl;
    cout << (*this).hp << endl;
  }
  int hp;
};

int main() {
  Hero h(100);
  cout << "what " << endl;
  cout << h.hp << endl;
  cout << &h << endl;// same as this, pointer
  cout << (*(&h)).hp << endl; //dereference
  return 0;
}
```

---

05_08_const修飾成員函數

```cpp
  int getHp() const {
    // m_Hp = m_Hp + 1;
    return m_Hp;
  }


```

- this will not allow you to modify left hand side variable value

```cpp
#include <iostream>
#include <vector>
using namespace std;

// constant fn
class Hero {
public:
  Hero() : m_Hp(0) {} //inititae as 0

  int getHp() const {
    // m_Hp = m_Hp + 1;
    return m_Hp;
  }
  int setHp(int hp) { m_Hp = hp; }

private:
  int m_Hp;
};

int main() {
  const Hero h;
  // h.setHp(100);
  h.getHp();
  return 0;
}
```

```cpp
const Hero h;  // const objec
h.setHp() //  int getHp() const {

```

const object can only use the fn() const , as they both won't modify the left side value

---

## mutable <-> const

```cpp
private:
  int m_Hp;
  mutable int m_getHpCounter;
};

mutable // for fn() const
int getHp() const {
    m_getHpCounter++;
    return m_Hp;
  }

```

---

## 友元(friend)

```cpp
/*
友元的目的

讓一個類 或者 函數
能夠訪問另一個類的私有成員

友元的關鍵字： friend

三種友元
1、全局函數作為友元
2、類作為友元
3、成員函數作為友元
*/

```

1、全局函數作為友元
2、類作為友元
3、成員函數作為友元

讓一個類 或者 函數
能夠訪問另一個類的私有成員

```cpp
#include <iostream>
#include <string>
using namespace std;

/*
友元的目的

讓一個類 或者 函數
能夠訪問另一個類的私有成員

友元的關鍵字： friend

三種友元
1、全局函數作為友元
2、類作為友元
3、成員函數作為友元
*/

class People{
    friend void friendVisit(People* p);
public:
    People() {
        m_House = "別墅";
        m_Car = "跑車";
    }
public:
    string    m_House;

private:
    string   m_Car;
};

void friendVisit(People* p) {
    cout << "好朋友來訪問你的" << p->m_House << endl;
    cout << "好朋友來訪問你的" << p->m_Car << endl;
}

int main() {
    People p;
    friendVisit(&p);
    return 0;
}
```

just declared friend fn(); first -> to let them access private var

---

## 133_6-2類作爲友元

```cpp
#include <iostream>
using namespace std;

// 類作為友元
// 讓一個類去訪問另一個類的私有成員

class People; // declaration , for below visit() compile

class PeopleFriend {
public:
  PeopleFriend() {}
  void visit(People *p);
};

class People {
  friend class PeopleFriend;

public:
  People() {
    m_House = "別墅";
    m_Car = "跑車";
  }

public:
  string m_House;

private:
  string m_Car;
};

void PeopleFriend::visit(People *p) {
  cout << "好朋友來訪問你的" << p->m_House << endl;
  cout << "好朋友來訪問你的" << p->m_Car << endl;
}

int main() {
  People p;
  PeopleFriend pf;
  pf.visit(&p);
  return 0;
}
```

```cpp
class People; // declaration , for below visit() compile

friend class PeopleFriend;

void PeopleFriend::visit(People *p) { // using this when above declaration  don't have priate var info
  cout << "好朋友來訪問你的" << p->m_House << endl;
  cout << "好朋友來訪問你的" << p->m_Car << endl;
}

```

---

## 134_6-3成員函數作爲友元.mp4

成員函數作為友元
PeopleFriend 的某個函數能夠訪問 People 的私有成員變量

```cpp
#include <iostream>
#include <string>
using namespace std;

//  成員函數作為友元
// PeopleFriend 的某個函數能夠訪問  People 的私有成員變量

class People;

class PeopleFriend {
public:
  PeopleFriend() {}

  void visitAll(People *p);
  void visitPub(People *p);
};

class People {
  // friend class PeopleFriend;
  friend void PeopleFriend::visitAll(People *p);

public:
  People() {
    m_House = "別墅";
    m_Car = "跑車";
  }

public:
  string m_House;

private:
  string m_Car;
};

void PeopleFriend::visitAll(People *p) {
  cout << "好朋友訪問了你的" << p->m_House << endl;
  cout << "好朋友訪問了你的" << p->m_Car << endl;
}
void PeopleFriend::visitPub(People *p) {
  cout << "好朋友訪問了你的" << p->m_House << endl;
  // cout << "好朋友訪問了你的" << p->m_Car << endl;
}

int main() {
  People p;
  PeopleFriend pf;
  pf.visitAll(&p);
  pf.visitPub(&p);

  return 0;
}
```

---

## 135_7-1運算符重載概念.mp4

```cpp
#include <iostream>
#include <string>
using namespace std;

/*
+
4 + 5 = 9

class A {
};

A a;
A b;
a + b;

*/
int main() {
    // 1、加法運算符
    int a = 520;
    int b = 1314;
    cout << a + b << endl;

    // 2、字符串拼接
    string c = "520";
    string d = "1314";
    cout << c + d << endl;

    string e = "我";
    string f = "愛你";
    cout << e + f << endl;
    return 0;
}
```

`#include <string>` -> is a class

---

## 137_7-2加號重載.mp4

- difference btw pointer `->` and reference `x.add`

```cpp
#include <iostream>
using namespace std;

/*
+
*/
// ¸´ÊıÀà
class Complex {
    friend Complex operator+(Complex& a, Complex& b);
    friend Complex operator-(Complex& a, Complex& b);
public:
    Complex() : real(0), image(0) {

    }
    Complex(int real, int image) {
        this->real = real;
        this->image = image;
    }
    /*
    Complex operator+(Complex& other) {
        Complex ret;
        ret.real = this->real + other.real;
        ret.image = this->image + other.image;
        return ret;
    }*/

    // a + bi
    void Print() {
        cout << real << '+' << image << 'i' << endl;
    }

private:
    int   real;
    int   image;
};

Complex operator+(Complex& a, Complex& b) {
    Complex ret;
    ret.real = a.real + b.real;
    ret.image = a.image + b.image;
    return ret;
}

Complex operator-(Complex& a, Complex& b) {
    Complex ret;
    ret.real = a.real - b.real;
    ret.image = a.image - b.image;
    return ret;
}

int main() {
    Complex a(10, 20);
    Complex b(5, 8);
    // Complex c = a.operator+(b);
    Complex c = a + b;
    Complex d = a - b;
    c.Print();
    d.Print();
    return 0;
}
```

within class fn

```cpp

    Complex operator+(Complex& other) {
        Complex ret;
        ret.real = this->real + other.real;
        ret.image = this->image + other.image;
        return ret;

```

global fn version:

```cpp
Complex operator-(Complex& a, Complex& b) {
    Complex ret;
    ret.real = a.real - b.real;
    ret.image = a.image - b.image;
    return ret;
}

```

---

## 138_7-3-1左移重載.mp4

```cpp
#include <iostream>
using namespace std;

/*
<<

Complex c;
cout.operator<<(c)

// 成員函數
c.operator<<(cout)
c << cout
*/
// 複數類
class Complex {
  friend Complex operator+(Complex &a, Complex &b);
  friend Complex operator-(Complex &a, Complex &b);
  friend ostream &operator<<(ostream &cout, Complex a);

public:
  Complex() : real(0), image(0) {}
  Complex(int real, int image) {
    this->real = real;
    this->image = image;
  }
  /*
  Complex operator+(Complex& other) {
      Complex ret;
      ret.real = this->real + other.real;
      ret.image = this->image + other.image;
      return ret;
  }*/

  // a + bi
  void Print() { cout << real << '+' << image << 'i' << endl; }

private:
  int real;
  int image;
};

Complex operator+(Complex &a, Complex &b) {
  Complex ret;
  ret.real = a.real + b.real;
  ret.image = a.image + b.image;
  return ret;
}

Complex operator-(Complex &a, Complex &b) {
  Complex ret;
  ret.real = a.real - b.real;
  ret.image = a.image - b.image;
  return ret;
}

ostream &operator<<(ostream &cout, Complex a) {
  cout << a.real << '+' << a.image << 'i';
  return cout;
}

int main() {
  Complex a(10, 20);
  Complex b(5, 8);
  // Complex c = a.operator+(b);
  Complex c = a + b;
  Complex d = a - b;
  // c.Print();
  d.Print();
  // operator<<(cout, c)
  cout << c << endl << endl;
  return 0;
}
```

The `operator<<` for `Complex` is special for these reasons:

### 1. **Stream integration**

Unlike `+` and `-`, it works with C++ streams (`cout`, `cerr`, file streams, etc.), so you can write:

```cpp
cout << c << endl;  // Instead of c.Print();
```

### 2. **Global function, not a member**

It’s a global function because:

- The left operand is `ostream&` (e.g., `cout`), not a `Complex`
- You can’t modify `ostream` to add a member
- This is the standard C++ pattern for stream operators

### 3. **Chaining support**

Returning `ostream&` enables chaining:

```cpp
cout << c << endl << "Result: " << d << endl;
```

### 4. **Friend access**

Declared as `friend` to access private `real` and `image`:

```cpp
friend ostream &operator<<(ostream &cout, Complex a);
```

### 5. **Automatic invocation**

When you write `cout << c`, the compiler calls this function.

### 6. **Standard convention**

This is the idiomatic way to make custom types work with streams.

### Comparison with other operators:

- `operator+` and `operator-`: return `Complex`, can be members or globals
- `operator<<`: returns `ostream&`, must be global, enables stream output

This is why `cout << c` works instead of `c.Print()`.

---

## Chaining in C++

Chaining lets you call multiple operations in one expression. It works when each operation returns the same object (or a reference to it).

### 1. Stream Chaining (Most Common)

#### How it works:

```cpp
cout << "Hello" << " " << "World" << endl;
//     ↑        ↑     ↑        ↑
//     |        |     |        └─ Returns cout
//     |        |     └─ Returns cout
//     |        └─ Returns cout
//     └─ Returns cout
```

#### Step-by-step breakdown:

```cpp
// Step 1: cout << "Hello"
ostream& temp1 = cout.operator<<("Hello");  // Returns cout

// Step 2: temp1 << " "
ostream& temp2 = temp1.operator<<(" ");     // Returns cout

// Step 3: temp2 << "World"
ostream& temp3 = temp2.operator<<("World"); // Returns cout

// Step 4: temp3 << endl
ostream& temp4 = temp3.operator<<(endl);    // Returns cout
```

### 2. Assignment Chaining

```cpp
int a, b, c;
a = b = c = 10;  // All variables get value 10
```

#### How it works:

```cpp
// c = 10 returns c (now equals 10)
// b = (c = 10) returns b (now equals 10)
// a = (b = (c = 10)) returns a (now equals 10)
```

#### Step-by-step:

```cpp
// Step 1: c = 10
int& temp1 = c.operator=(10);  // c = 10, returns c

// Step 2: b = temp1 (which is c)
int& temp2 = b.operator=(temp1);  // b = 10, returns b

// Step 3: a = temp2 (which is b)
int& temp3 = a.operator=(temp2);  // a = 10, returns a
```

### 3. Arithmetic Chaining

```cpp
int result = 10 + 20 + 30;  // result = 60
```

#### How it works:

```cpp
// 10 + 20 = 30 (temporary)
// 30 + 30 = 60 (final result)
```

### 4. Custom Class Chaining Example

Let's create a class that supports chaining:

```cpp
class Calculator {
private:
    int value;

public:
    Calculator(int v = 0) : value(v) {}

    // Method chaining - returns *this
    Calculator& add(int n) {
        value += n;
        return *this;  // Return reference to this object
    }

    Calculator& multiply(int n) {
        value *= n;
        return *this;
    }

    Calculator& subtract(int n) {
        value -= n;
        return *this;
    }

    int getValue() const { return value; }

    // Stream operator for output
    friend ostream& operator<<(ostream& os, const Calculator& calc) {
        os << calc.value;
        return os;
    }
};
```

#### Usage:

```cpp
Calculator calc(10);
calc.add(5).multiply(2).subtract(3);  // Chaining!
cout << calc << endl;  // Output: 27

// Step by step:
// calc.add(5)     → calc.value = 15, returns calc
// .multiply(2)    → calc.value = 30, returns calc
// .subtract(3)    → calc.value = 27, returns calc
```

### 5. The Key: Return by Reference

#### ✅ Correct (enables chaining):

```cpp
Calculator& add(int n) {
    value += n;
    return *this;  // Returns reference to this object
}
```

#### ❌ Wrong (breaks chaining):

```cpp
Calculator add(int n) {  // Returns by value (copy)
    value += n;
    return *this;  // Returns a COPY of this object
}
```

#### Why the difference matters:

```cpp
Calculator calc(10);
calc.add(5).add(3);  // What happens?

// With reference return:
// calc.add(5) returns calc (same object)
// .add(3) operates on the same calc object
// Final result: calc.value = 18

// With value return:
// calc.add(5) returns a COPY of calc
// .add(3) operates on the COPY, not the original
// Original calc.value = 15, copy.value = 18
```

### 6. More Complex Chaining Examples

#### String manipulation:

```cpp
string str = "Hello";
str.append(" ").append("World").append("!");  // str = "Hello World!"
```

#### Container operations:

```cpp
vector<int> vec;
vec.push_back(1).push_back(2).push_back(3);  // If push_back returned vector&
```

#### Function call chaining:

```cpp
class Builder {
public:
    Builder& setWidth(int w) { width = w; return *this; }
    Builder& setHeight(int h) { height = h; return *this; }
    Builder& setColor(string c) { color = c; return *this; }

private:
    int width, height;
    string color;
};

// Usage:
Builder builder;
builder.setWidth(100).setHeight(200).setColor("red");
```

### 7. When Chaining Doesn't Work

#### Functions that return void:

```cpp
void print() { cout << "Hello"; }
obj.print().print();  // ERROR! print() returns void
```

#### Functions that return different types:

```cpp
int getValue() { return 42; }
obj.getValue().add(5);  // ERROR! getValue() returns int, not object
```

#### Functions that return by value:

```cpp
Calculator add(int n) {  // Returns by value
    Calculator temp = *this;
    temp.value += n;
    return temp;  // Returns a copy
}
```

### 8. Best Practices

#### ✅ Do:

- Return references for chaining methods
- Use consistent return types
- Make chaining operations clear and intuitive

#### ❌ Don't:

- Chain operations that have side effects
- Make chains too long (hard to read)
- Return references to temporary objects

### 9. Real-World Example: Fluent Interface

```cpp
class Query {
private:
    string table;
    vector<string> columns;
    string whereClause;

public:
    Query& select(const string& cols) {
        columns.push_back(cols);
        return *this;
    }

    Query& from(const string& tbl) {
        table = tbl;
        return *this;
    }

    Query& where(const string& condition) {
        whereClause = condition;
        return *this;
    }

    string build() {
        // Build SQL query string
        return "SELECT " + join(columns, ", ") +
               " FROM " + table +
               " WHERE " + whereClause;
    }
};

// Usage:
Query query;
string sql = query.select("name, age")
                  .from("users")
                  .where("age > 18")
                  .build();
```

### Summary

Chaining works when:

1. Each operation returns the same object (or reference to it)
2. The return type matches what the next operation expects
3. You return by reference, not by value

The pattern is: **Return `*this` by reference** for method chaining, and **return the stream by reference** for stream chaining.

---

the thing why using `&` in ostrem is because it both don't want outside and inside using this cout, not even private
should use that, `&` only allow one global `cout ` for using that

---

## 140_7-4-1遞增重載.mp4

![](20250302-modern-cpp/2025-10-02-04-37-57.png)

why is `a` different to `x` in here?
because missing `&` , without it, it will only add 1 and then create another new object

```cpp
Complex& operator++() {
        this->real += 1;
        return *this;
    }
```

this is `++a`

```cpp
Complex operator++(int) {
        Complex c = *this;
        this->real += 1;
        return c;
    }
```

this is `a++` , just adding (int) outthere

```cpp
Complex operator++(int) {
        Complex c = *this;// if having this , the above setting need to change it to without `&`
        this->real += 1;
        return c; //rather than return *this
    }
```

![](20250302-modern-cpp/2025-10-02-04-57-59.png)
only diff 1 , but it should be 3 , why?

turn out it is normal in cpp, that later ++ need left value

```cpp

7_04_递增运算符/main.cpp:67:14: error: lvalue required as increment operand
   67 |   cout << ((b++)++)++ << endl;
      |            ~~^~~

```

```cpp
  Complex &operator++() { // front : ++a, returning *this
    this->real += 1;
    return *this;
  }

  Complex operator++(int) { // later : a++, require object
    Complex c = *this; // if having this , the above setting need to change it
                       // to without `&`
    this->real += 1;
    return c; // rather than return *this
  }

```

---

## 141_7-4-2遞增重載補充.mp4

```cpp
#include <iostream>
using namespace std;

class Hero {
public:
  Hero() : m_Data(NULL) {}
  Hero(int data) {
    m_Data = new int;
    *m_Data = data;
  }
  // double delete
  ~Hero() {
    if (m_Data) {
      delete m_Data;
      m_Data = NULL;
    }
  }

  Hero &operator=(Hero &h) {
    // m_Data = h.m_Data;
    if (m_Data) {
      delete m_Data;
      m_Data = NULL;
    }
    m_Data = new int;
    *m_Data = *h.m_Data;
    return *this;
  }

  int *m_Data;
};

int main() {
  Hero h1(1);
  Hero h2(2);
  Hero h3(3);

  cout << h1.m_Data << endl;
  cout << h2.m_Data << endl;
  cout << "damn1" << endl;
  h1 = h2; // ÄÚ´æÐ¹Â©
  cout << h1.m_Data << endl;
  cout << h2.m_Data << endl;
  cout << "damn" << endl;

  h3 = (h2 = h1);
  cout << h1.m_Data << endl;
  cout << h2.m_Data << endl;
  cout << h3.m_Data << endl;

  return 0;
}
```

```cpp
~Hero() {
    if (m_Data) {
      delete m_Data;
      m_Data = NULL;
    }
  }


Hero &operator=(Hero &h) {
    // m_Data = h.m_Data;
    if (m_Data) {
      delete m_Data;
      m_Data = NULL;
    }
    m_Data = new int;
    *m_Data = *h.m_Data;
    return *this;
  }
```

the key is setting up destructor , and `& ` for operator`=`, so that it will change the value directly and make double
`=` work

---

## 143_7-6關係運算符重載.mp4

```cpp
bool operator==(const Point& other) const {
        return m_x == other.m_x && m_y == other.m_y;
    }
```

- make it both const, const Point is for non changeable `other`, const{} is for read only

class default operator won't let you compare 2 object automatically, you have to manually make that thing

```cpp
bool operator>(const Point& other) const {
        if (*this == other) { //using above operator `==`
            return false;
        }
        if (*this < other) {
            return false;
        }
        return true;
    }
```

---

## 144_7-7函數調用運算符重載.mp4

```cpp
class AddFunctor {
public:
    AddFunctor() {
        m_acc = 0;
    }
    int operator() (int a, int b) {
        m_acc++;
        return a + b + m_acc;
    }
private:
    int m_acc;
}
```

vs

```cpp
int Add(int a, int b) {
    return a + b;
}
```

```cpp
int main() {
    AddFunctor add;
    cout << add(5, 6) <<endl;
    cout << add(5, 6) << endl;
    cout << add(5, 6) << endl;
    cout << add(5, 6) << endl;
    cout << add(5, 6) << endl;

    cout << Add(5, 6) << endl;
    cout << Add(5, 6) << endl;
    cout << Add(5, 6) << endl;
    cout << Add(5, 6) << endl;
    cout << Add(5, 6) << endl;

    return 0;
}
```

```cpp
//result

12
13
14
15
16
11
11
11
11
11
```

---

## 145_8-1繼承的語法.mp4

```cpp
/*
*       動物
*      /    \
*    貓      狗
*
* 繼承的語法
* class 子類 : 繼承方式 父類 {}
* 子類 -> 派生類
* 父類 -> 基類
*/

```

- class 子類 : 繼承方式 父類 {}

```cpp
#include <iostream>
using namespace std;

/*
*       動物
*      /    \
*    貓      狗
*
* 繼承的語法
* class 子類 : 繼承方式 父類 {}
* 子類 -> 派生類
* 父類 -> 基類
*/

class Animal {
public:
    void eat() {
        cout << "吃" << endl;
    }
};

class Cat : public Animal {
public:
    void sayHi() {
        cout << "喵~" << endl;
    }
};

class Dog : public Animal {
public:
    void sayHi() {
        cout << "汪汪汪~" << endl;
    }
};

int main() {
    Cat c;
    Dog d;
    c.eat();
    d.eat();

    c.sayHi();
    d.sayHi();

    return 0;
}
```

---

## 146_8-2繼承方式.mp4

```cpp
/*
繼承方式

class 子類名 : 繼承方式 父類名 {};

公共 public
保護 protected
私有 private

3 x 3 = 9

             |    public     |     protected      |   private
  public     |    public     |     protected      |   無法訪問
  protected  |   protected   |     protected      |   無法訪問
  private    |    private    |      private       |   無法訪問

public:   類內可以訪問，類外也可以訪問
protected：  類內可以訪問，類外不可訪問，且子類可以訪問
private：    類內可以訪問，類外不可訪問，且子類不可訪問
*/

```

```cpp
class Animal {
public:
  int m_pub;

protected:
  int m_pro;

private:
  int m_pri;
};

class Cat : public Animal {
public:
  Cat() {
    m_pub = 1;
    m_pro = 2;
    // m_pri = 3; 父類私有成員，子類公有繼承，無法訪問
  }
};

class BossCat : public Cat {
public:
  BossCat() {
    m_pub = 1;
    m_pro = 2; // 父類Cat中不是私有
  }
};

void testCat() {
  Cat c;
  c.m_pub = 1;
  // c.m_pro = 2;   // 要麼是私有，要麼是保護
}

class Dog : protected Animal {
public:
  Dog() {
    m_pub = 1;
    m_pro = 2;
    // m_pri = 3; // 父類私有成員，子類保護繼承，無法訪問
  }
};

class PoliceDog : public Dog {
public:
  PoliceDog() {
    m_pub = 1; // 這個變量，在父類 Dog 中一定不是私有成員
    m_pro = 2; // 這個變量，在父類 Dog 中一定不是私有成員
  }
};

void testDog() {
  Dog d;
  // d.m_pub = 1;   // 要麼是保護，要麼是私有
  // d.m_pro = 2;   // 要麼是保護，要麼是私有
}

class Pig : private Animal {
public:
  Pig() {
    m_pub = 1;
    m_pro = 2;
    // m_pri = 3;   // 父類私有成員，子類私有繼承，無法訪問
  }
};

class WildPig : public Pig {
public:
  WildPig() {
    // m_pub = 1;   // 該變量在父類 Pig 中是私有的
    // m_pro = 2;   // 該變量在父類 Pig 中是私有的
  }
};

void testPig() {
  Pig p;
  // p.m_pub = 1;     // 要麼是保護，要麼是私有
  // p.m_pro = 2;     // 要麼是保護，要麼是私有
}

int main() { return 0; }

```

---

## 147_8-3構造和析構順序.mp4

```cpp
#include <iostream>
using namespace std;

/*
繼承中，構造鏈裏，先構造的後析構

d -> c -> b -> a

a b c d d c b a
*/

class Animal {
public:
  Animal() { cout << "Animal 構造" << endl; }
  ~Animal() { cout << "Animal 析構" << endl; }
};

class Cat : public Animal {
public:
  Cat() { cout << "Cat 構造" << endl; }
  ~Cat() { cout << "Cat 析構" << endl; }
};

class BossCat : public Cat {
public:
  BossCat() { cout << "BossCat 構造" << endl; }
  ~BossCat() { cout << "BossCat 析構" << endl; }
};

void Test() {
  // Animal a;
  // Cat c;
  BossCat b;
}

int main() {
  Test();
  return 0;
}
```

the order kind of like `(())`

result:
Animal 構造
Cat 構造
BossCat 構造
BossCat 析構
Cat 析構
Animal 析構

----------

## 148_8-4同名屬性訪問.mp4

```cpp
#include <iostream>
using namespace std;

class Animal {
public:
    Animal() {
        m_Data = 17891;
    }
    int m_Data;
};

class Cat : public Animal {
public:
    Cat() {
        m_Data = 29812;
    }
    int m_Data;
};

void Test() {
    Cat c;
    cout << c.m_Data << endl;
    cout << c.Animal::m_Data << endl;

    cout << &(c.m_Data) << endl;
    cout << &(c.Animal::m_Data) << endl;
}

int main() {

    Test();
    return 0;
}
```

the inheritance it won't overwrite the father property even having the same name , different memory location

----------
## 149_8-5同名函數訪問.mp4

```cpp
#include <iostream>
using namespace std;

class Animal {
public:
    Animal() {

    }
    void eat() {
        cout << "動物吃東西" << endl;
    }
};

class Cat: public Animal {
public:
    Cat() {

    }
    void eat() {
        Animal::eat();
        cout << "貓吃東西" << endl;
    }
};


int main() {
    Cat c;
    c.eat();
    // c.Animal::eat();

    return 0;
}
```


```cpp
void eat() {
        Animal::eat(); // call back parent fn()
        cout << "貓吃東西" << endl;
    }
//or 
int main() {
    Cat c;
    c.eat();
    // c.Animal::eat(); // direct call

    return 0;
}


```


----------

## 150_8-6多繼承.mp4

```cpp
#include <iostream>
using namespace std;

class BaseA {
public:
    int m_A;
    int m_Base;

    BaseA() : m_A(0), m_Base(520) {}
};

class BaseB {
public:
    int m_B;
    int m_Base;

    BaseB() : m_B(0), m_Base(1314) {}
};

class BaseC {
public:
    int m_C;

    BaseC() : m_C(0) {}
};

class Son : public BaseA, public BaseB, public BaseC {

};

int main() {
    Son s;
    s.m_A = 1;
    s.m_B = 2;
    s.m_C = 3;
    // s.m_Base = 8;
    s.BaseA::m_Base = 8;
    s.BaseB::m_Base = 9;
    cout << &s.BaseA::m_Base << endl;
    cout << &s.BaseB::m_Base << endl;
    cout << sizeof(s) << endl;

    return 0;
}
```

```cpp
class Son : public BaseA, public BaseB, public BaseC {

}
```


----------

## 151_9-1多態的語法.mp4

```cpp
#include <iostream>
using namespace std;

class Animal {
public:
    // 虛函數
    virtual void eat() {
        cout << "動物在吃東西" << endl;
    }
};

class Cat : public Animal {
public:
    void eat() {
        cout << "貓在吃東西" << endl;
    }
};

class Pig : public Animal {
public:
    void eat() {
        cout << "豬在吃東西" << endl;
    }
};


// main -> test -> eat -> Animal::eat
// 函數傳參是個動物，但是傳入不同的動物，會產生不同的行為，這就叫多態
void eat(Animal& a) {
    a.eat();
}

void Test() {
    Cat c;
    Pig p;
    eat(c);
    eat(p);
}

int main() {
    Test();
    return 0;
}
```


- main -> test -> eat -> Animal::eat
- 函數傳參是個動物，但是傳入不同的動物，會產生不同的行為，這就叫多態


```cpp
virtual void eat() {
        cout << "動物在吃東西" << endl;
    }
```
using this allow 函數傳參是個動物，但是傳入不同的動物，會產生不同的行為

otherwise , it will only show動物在吃東西, as 
```cpp
void eat(Animal& a) { // reference to animal address , so 動物在吃東西
    a.eat();
}
```

----------

## 152_9-2虛函數.mp4

```cpp
#include <iostream>
using namespace std;

class Animal {
public:
    virtual void eat() {
        cout << "動物在吃東西" << endl;
    }
    virtual void run() {
        cout << "動物在跑" << endl;
    }
};

class Cat: public Animal {
public:
    void eat() {
        cout << "貓在吃東西" << endl;
    }
};

void eat(Animal& a) {
    Animal b;
    a.eat();
}

void Test() {
    Cat c;
    eat(c);
    cout << "Animal's size = " << sizeof(Animal) << endl;
}


int main() {
    Test();
    return 0;
}
```

the animal size = 8 -> pointer


![](20250302-modern-cpp/2025-10-03-01-02-32.png)

it overwrite the pointer `vtptr` -> address memory of parent eat


----------

## 153_9-3純虛函數和抽象類.mp4

```cpp
#include <iostream>

using namespace std;

class Animal {
public:
    virtual void eat() = 0;
};

class Cat : public Animal {
public:
    virtual void eat() {
        cout << "cat is eating" << endl;
    }
};

int main() {
    Cat c;
    c.eat();

    return 0;
}
```

----------

## 154_9-4虛析構和純虛析構.mp4

```cpp
#include <iostream>
using namespace std;

class BaseA {
public:
    BaseA() {}
    ~BaseA() {
        cout << "BaseA 銷燬了" << endl;
    } 
};

class SonA : public BaseA {
public:
    SonA() : m_Value(NULL) {
        m_Value = new int(10);
    }
    ~SonA() {
        cout << "SonA 銷燬了" << endl;
        delete m_Value;
    }
    int* m_Value;
};


class BaseB {
public:
    BaseB() {}
    /*virtual ~BaseB() {
        cout << "BaseB 銷燬了" << endl;
    }*/
    virtual ~BaseB() = 0;
};

BaseB::~BaseB() {
    cout << "BaseB 銷燬了" << endl;
}

class SonB : public BaseB {
public:
    SonB() : m_Value(NULL) {
        m_Value = new int(10);
    }
    ~SonB() {
        cout << "SonB 銷燬了" << endl;
        delete m_Value;
    }
    int* m_Value;
};

int main() {
    BaseA* a = new SonA();
    delete a;

    BaseB* b = new SonB();
    delete b;

    // BaseB x; 抽象類無法進行實例化

    return 0;
}
```

```cpp
    virtual ~BaseB() {
        cout << "BaseB 銷燬了" << endl;
    }

```
- 虛析構


```cpp


class BaseB {
public:
    BaseB() {}
    /*virtual ~BaseB() {
        cout << "BaseB 銷燬了" << endl;
    }*/
    virtual ~BaseB() = 0; // virtual ~Base()
}

//with outside:
BaseB::~BaseB() { cout << "BaseB 銷燬了" << endl; }

```

- aka 純虛析構


this make :

```cpp
SonB 銷燬了
BaseB 銷燬了

```

without virtual ~BaseB()=0

only 
```cpp
BaseA 銷燬了

```

after 154_9-4虛析構和純虛析構

```cpp
    // BaseB x; 抽象類無法進行實例化 as a abstract class

```


----------

# data structure
- [基础数据结构（C++版本） - Feishu Docs](https://ufbva3m5zn.feishu.cn/mindnotes/Yvqib874vm8WA6nrryLcWW4JnHf#mindmap)


## 順序表模板
```cpp
#include <iostream>
using namespace std;

#define eleType double

struct SequentialList {
    eleType* elements;
    int size;
    int capacity;
};

void initializeList(SequentialList* list, int capacity) {
    list->elements = new eleType[capacity]();
    list->size = 0;
    list->capacity = capacity;
}

void destroyList(SequentialList* list) {
    delete[] list->elements;
}

bool isEmpty(SequentialList* list) {
    return list->size == 0;
}

int size(SequentialList* list) {
    return list->size;
}

void insert(SequentialList* list, int index, eleType element) {
    if (index < 0 || index > list->size) {
        throw std::invalid_argument("Invalid index");
    }

    if (list->size == list->capacity) {
        int newCapacity = list->capacity * 2;
        eleType* newElements = new eleType[newCapacity]();
        for (int i = 0; i < newCapacity / 2; i++) {
            newElements[i] = list->elements[i];
        }
        delete[] list->elements;
        list->elements = newElements;
        list->capacity = newCapacity;
    }
    list->size++;
    if (list->size <= list->capacity) {
        for (int i = list->size - 1; i > index; i--) {
            list->elements[i] = list->elements[i - 1];
        }
        list->elements[index] = element;
    }
}

void deleteElement(SequentialList* list, int index) {
    if (index < 0 || index >= list->size) {
        throw std::invalid_argument("Invalid index");
    }

    for (int i = index; i < list->size - 1; i++) {
        list->elements[i] = list->elements[i + 1];
    }
    list->size--;
}

int findElement(SequentialList* list, eleType element) {
    for (int i = 0; i < list->size; i++) {
        if (list->elements[i] == element) {
            return i;
        }
    }
    return -1;
}

eleType getElement(SequentialList* list, int index) {
    if (index < 0 || index >= list->size) {
        throw std::invalid_argument("Invalid index");
    }
    return list->elements[index];
}

void updateElement(SequentialList* list, int index, eleType value) {
    if (index < 0 || index >= list->size) {
        throw std::invalid_argument("Invalid index");
    }

    list->elements[index] = value;
}

int main() {
    SequentialList myList;
    initializeList(&myList, 10);

    for (int i = 0; i < 10; i++) {
        insert(&myList, i, i * 10);
    }

    cout << "Size: " << size(&myList) << endl;
    cout << "Is empty: " << isEmpty(&myList) << endl;

    for (int i = 0; i < size(&myList); i++) {
        cout << getElement(&myList, i) << " ";
    }
    cout << endl;

    deleteElement(&myList, 5);
    updateElement(&myList, 1, 1314);

    int idx = findElement(&myList, 20);
    updateElement(&myList, idx, 520);

    cout << "Size: " << size(&myList) << endl;
    cout << "Is empty: " << isEmpty(&myList) << endl;

    for (int i = 0; i < size(&myList); i++) {
        cout << getElement(&myList, i) << " ";
    }
    cout << endl;

    destroyList(&myList);

    return 0;
}
```


----------


首字母變大寫

```cpp
#include <cstring>
#include <iostream>
#include <string>
using namespace std;

int main() {
  char s[110];
  while (gets(s)) {
    int len = strlen(s);
    for (int i = 0; i < len; i++) {
      if (i == 0 || s[i - 1] == ' ') {
        if (s[i] != ' ') {
          if (s[i] >= 'a' && s[i] <= 'z') {
            s[i] -= 'a';
            s[i] += 'A';
          }
        }
      }
    }
    printf("%s\n", s);
  }
  return 0;
}
```

---
