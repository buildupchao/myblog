---
title: 在大数据时代，我们缺乏的到底是思维还是能力？
tags: ['tech-talking']
category: tech-talking
keywords: tech-talking,技术杂谈,大数据思维,大数据研发
layout: post
---

大学最重要的事情应该是锻炼自学的能力、培养自律的心性。
<br/><br/>
工作后，最重要的事情应该是执行力MAX的可靠性以及严谨处事的态度。
<br/><br/>
似乎每件事都会有专门的目标性。
<br/><br/>
然而，工作久了，难免会<strong style="color:red;">“学会偷懒”</strong>，不再像从前哐哧哐哧就开始无想法的行动。

<!-- more -->

<br/>
## 1.按部就班固化思维

- <strong style="color:blue;">在遇到采集数据异常排查问题时，W总是习惯于从文件系统拉取log日志进行查询，然而采集机器数少则十几台，多则成百上千</strong>

  - 不是吧不是吧，这种耗时费力的事情，不会真的有人这么干吧？
  - 想必除了想要摸鱼的人，不会有人傻到大批量拉取日志进行分析。

> 正解：可以借助于Hive or Flink集群建表SQL分析，效率更高。（ 当然，有更方便快捷的方式欢迎推荐。）

## 2.从零造轮子为哪般

- <strong style="color:blue;">有工具可以辅助快速解决问题，然而经常习惯于自己从零造轮子？</strong>

  - 没错，说的就是你，有极速模式，为何要采用常规流程模式呢？难道是不想有自己的空闲时间充电学习？
  - 难道说你是在故意放松，给你拖延工作量，从而有时间跳槽走位？？？
<br/><br/>

> 正解：我们可以学习架构原理，运用思维，发散学习。（比如二叉树的中序遍历可以运用到自助式ETL中的表达式聚合计算中）

## 3.架构缺陷补丁不断

- <strong style="color:blue;">小文件合并功能，采用单纯的JAVA服务自己实现，每天平均有80W+的小文件合并任务量？？？</strong>

  - 如果数据都是存储在HDFS上的，那么你的NameNode压力是要多大啊？
  - 大量小文件问题根本原因还是架构设计有问题，如果日志切分合理，小文件量是极其少的。
  - 所以，你的工作量就是自己造就了架构问题，然后在此基础之上再开发一套服务来做小日志文件归并？别人从复杂入简，而你是从简单到复杂。（莫非你是安琪拉？要<strong style="color:red;">“缝缝补补又是一年？”</strong>）
  - 那么，你的思维是什么？是为了彰显你的研发能力以及代码量而生的吗？
<br/><br/>

> 正解：敢于推倒架构设计，架构师不是神人，也会有架构漏洞以及不足点，要以发展眼光看待问题，而不是尊崇。（毕竟活在前人阴影下很累。）

## 4.人云亦云普度众生

- <strong style="color:blue;">人云亦云，技术选型从来都是拍脑袋 or 看了几篇博客？？？</strong>

  - 不经大脑思考或者浅尝辄止就自认为了如指掌某门技术？是骡子是马敢拉出来溜溜吗？走两步？
  - 人云亦云？如果没有自己想法就坦言，慢慢培养自己的意识，而不是随声附和。（<strong style="color:red;">要有对外我是“辅助位”，对内深藏不露。</strong>）
  - 张口就来？这个用Flink？这个用Clickhouse？这个用RabbitMQ？你调研了吗？有数据依据吗？请发出来你的测试报告以及数据凭证。
<br/><br/>

> 正解：往往最站不住脚的是空口无凭。聪明的人，会直接发出上帝之手（有数据+测试报告），让你无力反驳。

## 5.如法炮制乐此不疲

- <strong style="color:blue;">经常会遇到一类人，总喜欢如法炮制，一个方案解万千难题。</strong>

  - 你可否考虑过在同一套架构模式下，前后二者数据量级 or 数据埋点相关的差距？
  - 你可否考虑过在同一套代码逻辑下，前后二者producer-consumer部署方案不同会有所差别？
  - 你可否考虑过在用一个HQL ETL问题时，前后时间跨度已经截然不同（一年前和一年后数据量差距有多大？dt范围有多大？）？
<br/><br/>

> 正解：世间没有银弹。我们总是习惯于如法炮制，一套方法冠以多用，但是往往得不偿失。


<br/><br/>
说了这么多，其实只是想表达一个点：多思考，多复盘，多反思，跳出极限。
