面试八股文系列的第二篇终于完成了，本期推出`八股文骚套路之 MySQL`，主要讲解如何应对面试过程中` MySQL` 的相关问题。另外我在这个系列，也会逐渐将自己在准备秋招面试过程中的一些心得，以及一些技巧穿插的进行讲述，希望对大家有帮助。

![img](https://img-blog.csdnimg.cn/20210620170646392.png)

**友情提示**

我写这个系列是为了给马上进行秋招的同学救急用的，目的是帮助他们节省复习的时间。不是今年就秋招的同学可以浏览下文章大致了解下秋招的需求，然后去我公众号后台回复计算机基础领点相关资料打好基础，也要多做点项目提升自己的动手能力。要是你才刚上大一你天天就跟着我背面试八股文，你可废了，我跟你说。

在上一篇文章中提到，面试大厂后端需要掌握的 Java 基础、JVM、Redis、MySQL、框架、设计模式、数据结够、计算机网络等要有两到三个要做到熟悉，能跟面试官进行深度交流，做为面试亮点。我在制定秋招准备计划时把 `Redis`、`MySQL` 以及 `Spring` 框架做为自己的面试亮点。为了准备  MySQL，我在准备 MySQL 上大约花费4周左右时间（在校招面试过程中也花了点时间对这方面知识进行反复学习），当然这段时间除了准备 MySQL ，每天一道的 LeetCode 代码题我是没有断的，中间也花少量时间穿插看了别的东西。如果大家不准备把 MySQL 当做面试亮点，只想应付面试官的常规问题的话，时间不需要用太长，然后隔一段时间反复背一下。

说明：我在本科时主要学习做 Java Web 开发的，但是读研时做了自然语言处理，整整两年没碰开发。我的基础是 MySQL 的基础操作还算熟悉，也在本科项目中实际用过 MySQL， 但是对 MySQL 的底层原理并不清楚。大家可以参考我的基础并和自己的基础做对比，来制定自己的学习计划。

![img](https://img-blog.csdnimg.cn/20210620170814345.png)

准备 MySQL 的过程中，我完成了以下几个任务：

（1）记住了 MySQL 面试常问的一些基础概念（后续在准备面试的过程中还会反复记）。

（2）对于 SQL 优化有了一些自己的理解。并把一部分理解应用在自己的秒杀系统项目中，具体怎么做我就不说了，希望大家在学完后也能自己思考下，比如怎样根据行锁的特性优化自己项目的 MySQL 的事务、比如怎样根据自己项目的实际场景去选择索引，诸如此类。大家能把八股文中的东西应用在自己的项目中，还是能让面试官提起兴趣的。

（3）对于 SQL 代码题也进行了一些训练，面试中有的面试官也会考。

如果大家不把 MySQL 当作准备面试的重点，做到（1）和（3）就可以了。另外如果把 MySQL 当成面试的重点，也要先准备（1）和（3），时间允许的话再去深入优化部分。

**准备面试小技巧**

推荐大家在准备到一定程度后，多进行面试"以面代练”。因为你在面试的时候，精神注意力是高度集中的，会发现很多你存在的问题，并且能在面试过程中把一些问题记牢。大部分人平时背一段几十字的文字，背好几分钟都背不下来，并且就算背下来隔一会就忘了。但是让他们复述过去一个小时面试官都问了什么问题，这能记得清清楚楚，还能写出一篇面经。另外，通过模拟面试能帮助你梳理回答问题的思路，回答问题条理对于面试也是很加分的。面试的形式可以找几个朋友或者学长学姐进行模拟面试，也可以在秋招前期投几个不太想去的公司进行面试（稍有些不道德，不过也算帮面试官完成面试 KPI 了吧）。

大家可以两周左右约一次朋友或者学长学姐进行模拟面试，这样对学习的促进作用也比较大。每天自己看十分容易懈怠，学习效率也不高。代码题也可以几个朋友轮着，每天其中一个人讲一道题，我当时就是这么干的。其实我感觉不管做什么，多合作还是能干成更多的事情。

## 如何准备MySQL面试八股文

好了，现在正式进入 MySQL 面试八股文的划重点流程。在这里要推荐一本书籍《深入浅出 MySQL 》。

![img](https://img-blog.csdnimg.cn/20210620170853137.png)

推荐理由：《深入浅出 MySQL》这本书是网易的数据库专家写的，从数据库的基础、开发、优化、管理维护、架构，五个层面讲述了 MySQL（大家面试后端的话管理维护篇就不用看了），内容层层递进。并且每讲解一个小的知识点都会相应的配有实例，更容易读者理解。

学习内容：学习内容按照《深入浅出 MySQL》的目录进行介绍。根据章节内容列出的问题我就不附上答案了，大家根据我的问题自己总结下会有更好的学校效果。在补充篇的问题我会给出答案。

**基础篇第2章 SQL 基础**

基础的SQL语句肯定要会，并且要熟练，这是最基础的。

针对本章内容的面试问题：

（1）增删改查这些问题面试官一般不会问的。不过万一问出来，比如“查询用哪个关键字”，你要是不知道你就惨了哈。

（2）ORDER BY、LIMIT、GROUP BY、HAVING 这些关键字分别是做什么用的。

（3）讲一下左链接和右链接的区别。

**基础篇第3章、第4章、第5章**

这三章分别是MySQL的数据类型、运算符、常用函数。简单过一遍，了解就行，这三章在面试中很少会被问到。

**开发篇第7章 表类型（存储引擎）的选择**

InnoDB是面试考察的重点，相关知识都要详细看。另外要拿 InnoDB 对比 MyISAM、MEMORY 去体会 InnoDB 引擎的特点。

针对本章内容的面试问题：

InnoDB 和 MyISM、MEMORY 的区别是什么。

**开发篇第10章 索引的设计和使用**

索引是 MySQL 面试考察的重点，BTree 索引和 Hash 索引要对比着进行学习。

针对本章内容的面试问题：

（1）索引所采用的数据结构，以及为什么要这样设计。

（1）在数据库中创建索引的原则。

（2）BTree 索引和 Hash 索引的适用范围。

**开发篇第11章 视图**

本章做到基本了解，面试过程中问的少。

**开发篇第14章 事务控制和锁定语句**

InnoDB 是行锁，MyISAM、MEMORY 是表锁面试过程中经常会问到。本章的事务控制实例值得好好的体会一下，有利于加深对数据库锁的理解。

**优化篇第18章 SQL优化**

如果你在简历中和开头的自我介绍中强调了你对 MySQL 熟悉，那么你这一章一定要好好看。面试官想考察你在 MySQL 方面的能力是否和你之前说的相符，会倾向于出一道场景问题，让你去设计并优化（当然只是好好看这一章并不能完全解决问题，一会我做一点补充）。

针对本章内容的面试问题：

（1）优化 SQL 语句的步骤有哪些。

（2）哪些场景可以使用索引。

（3）索引在哪些情况会失效。

虽然面试官不会直接问你在优化 SQL 语句时候有哪些技巧？比如怎样优化 Insert 语句，怎样优化 order by语句。但是可以在这一章学一些常用的优化 SQL 语句的技巧，在面试官问一个具体问题时，顺带说一下自己平时会采用这些技巧去优化。

**优化篇第20章 锁问题**

这一章属于第14章的拔高，大家主要看表锁和行锁，页锁被问到的比较少。

针对本章内容的面试问题：

（1）事务四大特性，并解释这四大特性的含义。

（2）并发事务处理会带来哪些问题？

（3）事务隔离级别。

（4）InnoDB 行锁实现方式

（5）你了解 Next-key 锁吗？

（6）如何避免 InnoDB 中的死锁。

（7）数据库多版本并发控制（MVCC 机制）

**优化篇第21章 优化 MySQL Server**

这一章在校招面试中是不会问到的，不过我把这里的相关知识学了去给面试官讲，效果还不错。大家根据自己的情况酌情选择看还是不看哈。

可以和面试官展开聊的知识点：

（1）MySQL 的内存管理及优化。

（2）InnoDB 重做日志的内部机制，这个可以和事务联系起来给面试官讲。

**架构篇第31章 MySQL 复制**

这一章的内容如果你不刻意提到，面试官一般很少主动问。如果大家不打算在 MySQL 这里和面试官多聊，那么这里就可以不看了。如果大家打算在 MySQL 这个环节和面试官展开聊，那么在这里和面试官展开聊是一个不错的选择。

可以和面试官展开聊的知识点：

（1）MySQL 的主从复制原理。

（2）MySQL 的三种复制方式。

（3）MySQL 的异步复制和半同步复制。

（4）如何提高复制的性能。

## 补充

接下来我再给大家补充一点知识，是我在学习林晓斌的《MySQL 实战45讲》时的笔记，这个课真心不错。这个知识在《深入浅出 MySQL》这本书中没有，但是学会以后在面试过程中还是挺有用的（面试官有时会问），在实践中也挺有帮助的。

**MySQL的基础架构**

![img](https://img-blog.csdnimg.cn/20210620170522346.png)

MySQL 的基础架构可分为 Server 层和存储引擎层两部分，Server 层包含 MySQL 的大多数核心服务功能，存储引擎层负责数据的存储和提取。各模块功能如下：

连接器：负责跟客户端建立连接。

查询缓存：之前执行过的查询语句会以 key-value 的形式存在缓存中，MySQL 收到一条查询语句会先去查一下缓存中是否有相同的 key，如果有直接把 value 返回。但是这个功能在表更新比较频繁的场景中别用，因为每次表更新都会刷新缓存。

分析器：会对输入的 SQL 语句进行词法分析和语法分析。

优化器：优化器制定SQL语句的执行方案，比如会从表里的多个索引中选择一个最合适的索引，或者在一个语句有多表关联的时候，决定表的连接顺序。

执行器：根据优化器定制的执行计划进行操作，返回结果。

存储引擎：存储数据，提供读写接口。

## MySQL代码练习

出 SQL 代码题在面试中不是很多，我在参加的几十场面试中仅有四五次让我写 SQL 代码题。不过还是要适当准备，这里不用花太多时间，把 LeetCode 上免费的代码题中简单题和中等题好好练一下就好，完全能应付了面试中的 SQL 代码题。

![img](https://img-blog.csdnimg.cn/20210620170945429.png)



好了，上述就是准备秋招过程中全部要学的 MySQL 知识点了，准备的过程中会出现背完就忘的情况，大家要时常对知识点进行反复的记。下一篇来跟我一起背 Redis 八股文呀。
