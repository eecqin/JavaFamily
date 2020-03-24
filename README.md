# 目录

- 优秀github
  - [成为专业程序员路上用到的各种优秀资料、神器及框架 ](https://github.com/stanzhai/be-a-professional-programmer)
  

- 系统设计面试的评分标准
  - 可行解 Work Solution 25% 
  - 特定问题 Special Case 20% 
  - 分析能力 Analysis 25%
  - 权衡 Tradeoff 15%
  - 知识储备 Knowledge Base 15%

- 网站架构及演进
  - [京东架构专家分享京东架构之路](https://cloud.tencent.com/developer/article/1102801)
  - [淘宝架构](https://github.com/davideuler/architecture.taobao-alibaba/tree/master/%E6%B7%98%E5%AE%9D%E6%9E%B6%E6%9E%84)
  - [各大互联网公司架构演进之路汇总](http://www.hollischuang.com/archives/1036)
  - [网站架构](https://github.com/nemoTyrant/manong/blob/master/category/%E7%BD%91%E7%AB%99%E6%9E%B6%E6%9E%84.md)
  - [大型网站技术架构演进与性能优化](https://me.csdn.net/u011915230)
  
- System design interview tips (One claim always followed by one evidence)
  - Understand requirement: what key features/scenarios to support?
  - Understand necessary? 根据需求, e,g. QPS, 来设计多牛的系统，单机->分布式，monolithic to microservice
  - Design a workable solution
  - Evaluate again Performance, Availability, Scalability and find bottleneck/pain points
  - Evolve design incrementally
  - 从小到大，按需求进化，而不是直接抛出一个microservice 来overdesign, 发现问题比解决问题更重要

- System design githubs
  - [System Design Primer](https://github.com/donnemartin/system-design-primer)
  - [System Design Interview](https://github.com/checkcheckzz/system-design-interview)
  - [System Design Cheat Sheet](https://gist.github.com/vasanthk/485d1c25737e8e72759f)
  - [System Design Preparation](https://github.com/shashank88/system_design)
  - [Awesome Scalablity](https://gist.github.com/vasanthk/485d1c25737e8e72759f)
  - [System-design-interview](https://github.com/plasm0dium/system-design-interview)
  - [搞定面试中的系统设计题](https://jiajunhuang.com/articles/2019_04_29-system_design.md.html)
  - [如何答好面试中的系统设计题](https://www.zhihu.com/question/26312148)
  - [一亩三分地](https://www.1point3acres.com/bbs/forum.php?mod=forumdisplay&fid=323&filter=typeid&typeid=1025)
  - [米群](http://www.meetqun.net/forum-83-1.html)

- [Web](https://jiajunhuang.com/articles/2017_10_19-web_dev_series.md.html)

- 分布式系统理论
  - [总结分布式系统的核心就是解决一个问题：不同节点间如何达成共识](https://zhuanlan.zhihu.com/p/25074310): 看似简单的问题因网络丢包、节点宕机恢复等场景变得复杂，由此才衍生出很多概念、协议和理论。为探究共识问题最大能解决的程度，于是有FLP、CAP边界理论；为在特定条件和范围内解决该问题，于是有一致性协议Paxos、Raft、Zab和Viewstamped Replication；为构建这些协议，于是有多数派、Leader选举、租约、逻辑时钟等概念和方法。
  - [一致性、2PC和3PC](https://link.zhihu.com/?target=http%3A//www.cnblogs.com/bangerlee/p/5268485.html)
  - [时间、时钟和事件顺序](https://link.zhihu.com/?target=http%3A//www.cnblogs.com/bangerlee/p/5448766.html)
  - [选举、多数派和租约](https://link.zhihu.com/?target=http%3A//www.cnblogs.com/bangerlee/p/5767845.html)
  - [CAP](https://link.zhihu.com/?target=http%3A//www.cnblogs.com/bangerlee/p/5328888.html)
  - [Paxos](https://link.zhihu.com/?target=http%3A//www.cnblogs.com/bangerlee/p/5655754.html)
  - [Raft、Zab](https://link.zhihu.com/?target=http%3A//www.cnblogs.com/bangerlee/p/5991417.html)
  - [Paxos变种和优化](https://link.zhihu.com/?target=http%3A//www.cnblogs.com/bangerlee/p/6189646.html)  

- 高并发/高可用
  - [别扯了，这才是应对高并发的正确处理思路！](https://www.cnblogs.com/Howinfun/articles/11946952.html)
  - [一文读懂分布式架构知识体系](https://www.cnblogs.com/Howinfun/articles/11840841.html)
  
- Web server
  - 功能
     - Load balance
     - Cache
     - Container?
  - [三大WEB服务器对比分析（apache ,lighttpd,nginx)](http://www.blogjava.net/daniel-tu/archive/2008/12/29/248883.html)
  
- QPS
  - 分析出 QPS 有什么用?		
     - QPS = 100： 用你的笔记本做 Web 服务器就好了					
     - QPS=1k: 用一台好点的 Web 服务器就差不多了，但需要考虑 Single Point Failure								
     - QPS=1m: 需要建设一个1000台 Web 服务器的集群, 还需要考虑如何 Maintainance(某一台挂了怎么办)
  - QPS和 
  (服务器) / Database (数据库) 之间的关系	
     - 一台 Web Server 约承受量是 1k 的 QPS (考虑到逻辑处理时间以及数据库查询的瓶颈)
     - 一台 SQL Database 约承受量是 1k 的 QPS(如果 JOIN 和 INDEX query比较多的话，这个值会更小)
     - 一台 NoSQL Database (Cassandra) 约承受量是 10k 的 QPS			
     - 一台 NoSQL Database (Memcached) 约承受量是 1M 的 QPS
  - [如何提高系统的吞吐量（QPS/TPS)](https://juejin.im/post/5af645f651882567105fd1b2)
  - [服务器性能指标解释：QPS、TPS、RT、Load、PV、UV](https://blog.csdn.net/qq_39416311/article/details/84892625)
  - [深入浅出QPS、RT和最佳线程数](https://www.jianshu.com/p/8532ac88ce72)
  - [关于服务器性能的一些思考](https://juejin.im/entry/58244432d203090055276f19)
  - [闲谈性能优化之QPS](https://blog.51cto.com/memoryless/1017948)
  
- Java基础核心串讲
  - [Java知识体系最强总结(2020版)](https://blog.csdn.net/ThinkWon/article/details/103592572)
  - 计算机操作系统与Linux[[novice]](https://blog.csdn.net/zhenguo26/article/details/80754991)[master](https://www.redhat.com/zh/topics/linux/what-is-linux)[guru]
  - [学习linux命令，看这篇2w多字的命令详解就够了](https://mp.weixin.qq.com/s/7bSwKiPmtJbs7FtRWZZqpA)
  - [图解HTTP协议](https://mp.weixin.qq.com/s/AK1Pb9rx0q5Hf8dq6HNOhw)
  - [计算机网络](https://www.jianshu.com/p/acce938468c4)
  - [7种常见的设计模式和使用场景](https://blog.csdn.net/wymrdjm/article/details/79122955)
  - [Java必会基础与新版本特性](https://www.javazhiyin.com/54702.html)
  - [HashMap](https://github.com/AobingJava/JavaFamily/blob/master/docs/basics/HashMap.md)
  - [万万没想到，HashMap默认容量的选择，竟然背后有这么多思考！？](https://mp.weixin.qq.com/s/ktre8-C-cP_2HZxVW5fomQ)
  - [ConcurrentHashMap & Hashtable（文末送书）](https://mp.weixin.qq.com/s/AixdbEiXf3KfE724kg2YIw)
  - [ArrayList](https://mp.weixin.qq.com/s/WoGclm7SsbURGigI3Mwr3w)
  - [跟着动画学习TCP三次握手和四次挥手](https://mp.weixin.qq.com/s/NL7Jzh0lYoA395yzaGxBHw)
  - [面试官问我同步容器（如Vector）的所有操作一定是线程安全的吗？我懵了！](https://mp.weixin.qq.com/s/0cMrE87iUxLBw_qTBMYMgA)
  
- [深入浅出JVM](https://zhuanlan.zhihu.com/p/84298509)
  - [JVM内存模型](https://juejin.im/post/5ad5c0216fb9a028e014fb63)
  - [【JVM故事】了解JVM的结构，好在面试时吹牛](https://mp.weixin.qq.com/s/fit90VdZUa2pG9lbET0i7w)
  - [看完这篇垃圾回收，和面试官扯皮没问题了](https://mp.weixin.qq.com/s/_AKQs-xXDHlk84HbwKUzOw)
  - [性能调优、线上问题排查](https://blog.csdn.net/ycb1689/article/details/89669691)
  - [类加载机制详解](https://gaohueric.github.io/2019/02/15/Java%E7%B1%BB%E5%8A%A0%E8%BD%BD%E6%9C%BA%E5%88%B6%E8%AF%A6%E8%A7%A3/)
  - [垃圾回收机制](https://blog.csdn.net/justloveyou_/article/details/71216049)
  - [垃圾回收器、垃圾回收算法](https://segmentfault.com/a/1190000010463373)

- 并发与多线程
  - [线程状态转换与通信机制](https://www.cnblogs.com/ygj0930/p/6561589.html)
  - [线程同步与互斥](https://songlee24.github.io/2015/04/29/linux-syn-mut-difference/)
  - [线程池知识点](https://blog.csdn.net/llengnuo/article/details/77918746)
  - [常见的JUC工具类](https://blog.csdn.net/luoyoub/article/details/80635652)
  - [【面试】如果把线程当作一个人来对待，所有问题都瞬间明白了](https://mp.weixin.qq.com/s/PrUa0tFyu3UZllP2FRDyVA)
  - [Java 并发进阶常见面试题总结](https://mp.weixin.qq.com/s/cdHfTTvMpH60SwG2bjTMBw)
  - [如果你这样回答“什么是线程安全”，面试官都会对你刮目相看（建议珍藏）](https://mp.weixin.qq.com/s/WDeewsvWUEBIuabvVVhweA)
  - [乐观锁、悲观锁](https://mp.weixin.qq.com/s/WtAdXvaRuBZ-SXayIKu1mA)
  - [乐观锁和悲观锁的AQS、sync和Lock](https://blog.csdn.net/qq_35190492/article/details/104691668)

- 常用工具集
  - JVM问题排查工具-JMC
  - IDEA开发神器
  - 线上调试神器-btrace
  - [Git原理与工作流](http://www.ruanyifeng.com/blog/2015/12/git-workflow.html)
  - [Linux常用分析工具](https://blog.csdn.net/tjcwt2011/article/details/73903538)
 
- 数据结构与算法
  - [从二叉搜索树到B+树](https://blog.csdn.net/z702143700/article/details/49079107)
  - [经典问题之字符串](https://juejin.im/post/5b8f9aed6fb9a05d2e1b75d9)
  - [经典问题之TOPK](https://juejin.im/entry/5c565fb7f265da2d84105958)
  - [图解红黑树](https://mp.weixin.qq.com/s/-8JFh5iLr88XA4AJ9mMf6g)
  
- 必会框架

  - [Spring全家桶以及源码分析](https://zhuanlan.zhihu.com/p/102534886)
  - [外行人都能看懂的SpringCloud，错过了血亏！](https://mp.weixin.qq.com/s/MJrahcDXwxgDr5zBdO3XWw)
  - [高性能NIO框架-Netty](http://www.52im.net/thread-2190-1-1.html)
  - [分布式框架基石-RPC](https://zhuanlan.zhihu.com/p/20951077)[[geeks4geeks]](https://www.geeksforgeeks.org/remote-procedure-call-rpc-in-operating-system/)
  - ORM框架Mybatis源码分析
  - [20000 字的 Spring Cloud 总结](https://mp.weixin.qq.com/s/pGSx8eKFH3YnUos3SM2ITw)
  - [什么是Zookeeper](https://mp.weixin.qq.com/s/gphDLJMO3QcRoN3zkco4EA)
  - [什么是单点登录(SSO)](https://mp.weixin.qq.com/s/drPVkRbCsDIlX6Ls2pDmqA)
  
- [高并发架构基石-缓存](https://github.com/AobingJava/JavaFamily/tree/master/docs/redis)
  - [高并发场景下缓存处理的一些思路！](https://www.cnblogs.com/Howinfun/p/11661450.html)
  - [Redis基础知识](https://github.com/AobingJava/JavaFamily/blob/master/docs/redis/Redis%E5%9F%BA%E7%A1%80.md)
  - [缓存击穿、雪崩、穿透](https://github.com/AobingJava/JavaFamily/blob/master/docs/redis/%E7%BC%93%E5%AD%98%E5%87%BB%E7%A9%BF%E3%80%81%E9%9B%AA%E5%B4%A9%E3%80%81%E7%A9%BF%E9%80%8F.md)
  - [集群高可用、哨兵、持久化、LRU](https://github.com/AobingJava/JavaFamily/blob/master/docs/redis/%E9%9B%86%E7%BE%A4%E9%AB%98%E5%8F%AF%E7%94%A8%E3%80%81%E5%93%A8%E5%85%B5%E3%80%81%E6%8C%81%E4%B9%85%E5%8C%96%E3%80%81LRU.md)
  - [分布式锁、并发竞争、双写一致性](https://github.com/AobingJava/JavaFamily/blob/master/docs/redis/%E5%88%86%E5%B8%83%E5%BC%8F%E9%94%81%E3%80%81%E5%B9%B6%E5%8F%91%E7%AB%9E%E4%BA%89%E3%80%81%E5%8F%8C%E5%86%99%E4%B8%80%E8%87%B4%E6%80%A7.md)
  - [Redis常见面试题](https://github.com/AobingJava/JavaFamily/blob/master/docs/redis/Redis%E5%B8%B8%E8%A7%81%E9%9D%A2%E8%AF%95%E9%A2%98.md)
  - [布隆过滤器(BloomFilter)](https://github.com/AobingJava/JavaFamily/blob/master/docs/redis/%E5%B8%83%E9%9A%86%E8%BF%87%E6%BB%A4%E5%99%A8(BloomFilter).md)
  - [秒杀系统设计](https://github.com/AobingJava/JavaFamily/blob/master/docs/redis/%E7%A7%92%E6%9D%80%E7%B3%BB%E7%BB%9F%E8%AE%BE%E8%AE%A1.md)
  - [课代表总结](https://github.com/AobingJava/JavaFamily/blob/master/docs/redis/%E8%AF%BE%E4%BB%A3%E8%A1%A8%E6%80%BB%E7%BB%93.md)
  - [短小精悍之 Redis 命令行工具有趣的罕见用法](https://mp.weixin.qq.com/s/eSx4aL7iaMZlW0cPZswghA)
  - [布隆过滤器实战【防止缓存击穿】](https://mp.weixin.qq.com/s/BdwZViiAqnFhCde4ZsxwPg)
  - [布隆过滤器过时了，未来属于布谷鸟过滤器？](https://mp.weixin.qq.com/s/XxY3b5FoVXCvHJWMxQH29g)
  - [什么鬼，面试官竟然让敖丙用Redis实现一个消息队列！！？](https://mp.weixin.qq.com/s/5NOTLJ6AM3QJfhvXMSR-MA)
  - [Redis—分布式锁深入探究](https://mp.weixin.qq.com/s/49hgH3COla3wU0rgyiUVgg)
  - [Redis—跳跃表](https://mp.weixin.qq.com/s/NOsXdrMrWwq4NTm180a6vw)
  - [Redis—5种基本数据结构](https://mp.weixin.qq.com/s/MT1tB2_7f5RuOxKhuEm1vQ)

- [消息队列](https://github.com/AobingJava/JavaFamily/tree/master/docs/mq)
  - [面试官问我：什么是消息队列？什么场景需要他？用了会出现什么问题](https://blog.csdn.net/qq_35190492/article/details/103153444)
  - [消息队列基础知识](https://github.com/AobingJava/JavaFamily/blob/master/docs/mq/%E6%B6%88%E6%81%AF%E9%98%9F%E5%88%97%E5%9F%BA%E7%A1%80.md)
  - [消息重复消费、分布式事务、顺序消费](https://github.com/AobingJava/JavaFamily/blob/master/docs/mq/%E9%87%8D%E5%A4%8D%E6%B6%88%E8%B4%B9%E3%80%81%E9%A1%BA%E5%BA%8F%E6%B6%88%E8%B4%B9%E3%80%81%E5%88%86%E5%B8%83%E5%BC%8F%E4%BA%8B%E5%8A%A1.md)
  - [Kafka架构与原理](https://mp.weixin.qq.com/s/-IPfWPS1WQMEgcIu0Ak2VQ)
  - [RocketMQ](https://github.com/AobingJava/JavaFamily/blob/master/docs/mq/RocketMQ.md)

- 爬虫
 - 【用简单的方式讲scrapy-redis爬虫分布式策略】(https://blog.csdn.net/qiulin_wu/article/details/104872217)
 
- 数据库
  - 【“有了数据库，为什么还要使用搜索引擎？”】（https://github.com/lanlin/notes/issues/27）
  - 【分布式数据库与搜索引擎的搜索效率，区别在哪里？】（https://www.zhihu.com/question/30930816）
  - [MySQL](http://c.biancheng.net/mysql/)
  - [MySQL死锁](https://www.cnblogs.com/zejin2008/p/5262751.html)
  - [Mysql并发时经典常见的死锁原因及解决方法](https://www.cnblogs.com/zejin2008/p/5262751.html)
  - [MySQL千万级数据库查询怎么提高查询效率](https://blog.csdn.net/qq_39416311/article/details/82315090)
  - [索引、锁机制](https://juejin.im/post/5b55b842f265da0f9e589e79)
  - [事务特性、隔离级别](https://www.jianshu.com/p/4963c5e038eb)
  - [MySQL调优与最佳实践](https://www.jianshu.com/p/9d438bbd2afc)
  - [MySQL的索引是怎么加速查询的？](https://mp.weixin.qq.com/s/7TPVOT7sloDUKmhldf9uvg)
  - [数据库索引](https://mp.weixin.qq.com/s/_9rDde9wRYoZeh07EASNQQ)
  - [MySql主从复制，从原理到实践！](https://mp.weixin.qq.com/s/eEWMSTAUF1H-gFBx26jujw)
  - [MySQL 的 InnoDB 存储引擎是怎么设计的？](https://mp.weixin.qq.com/s/wr2gJGQSA8QH_lmPh1XOkw)
  - [数据库基础知识](https://mp.weixin.qq.com/s/NDL1Q6nqdPq5oMBWSpq4ug)
  - [原来MySQL面试还会问这些(undo log)](https://mp.weixin.qq.com/s/Lx4TNPLQzYaknR7D3gmOmQ)
  - [数据库连接池到底应该设多大？这篇文章可能会颠覆你的认知](https://mp.weixin.qq.com/s/dQFSrXEmgBMh1PW835rlwQ)
  - [不用找了，大厂在用的分库分表方案，都在这里！](https://www.cnblogs.com/Howinfun/articles/11887916.html)
  
- 大数据
  - ODPS离线分析
  - Hive
  - Spark
  - Hadoop
  - Hbase
  - HDFS
  
- 搜索引擎

  - ElasticSearch
  - Canal
  - Kibana
  - Lucene
  - Logstash
  
- 优秀开源框架推荐

  - [阿里巴巴开源限流系统 Sentinel 全解析](https://mp.weixin.qq.com/s/NgS9tL4IVwGZrssz7fURpA)

- 架构演进之路

  - [从All in one 到微服务](https://www.jianshu.com/p/421cb5351bad)
  - [互联网架构之路](https://zhuanlan.zhihu.com/p/42115757)
  - 怎么设计一个能顶住双十一的系统？[[1]](https://blog.csdn.net/gb4215287/article/details/90173705),[[2]](https://www.lagou.com/lgeduarticle/68325.html)
  - [吊到面试官](https://zhuanlan.zhihu.com/p/92307325)
  - [微服务的架构介绍发展](https://blog.csdn.net/qq_42897427/article/details/104921630)

- 互联网前沿技术

  - 容器化：[Docker与k8s详解](https://zhuanlan.zhihu.com/p/53260098)

- 面试技巧

  - [简历怎么写?](https://mp.weixin.qq.com/s/0pNv6pMnenKn1A9PE61VnQ)
  - [能不能好好写简历？](https://mp.weixin.qq.com/s/LxVeT49GMKu72PZJ-rDHpA)
  - 语言组织
  - 加分项
  - 扬长避短
  - [自我介绍](https://github.com/AobingJava/JavaFamily/blob/master/docs/coderLife/%E6%95%96%E4%B8%99%E7%94%A820%E8%A1%8C%E4%BB%A3%E7%A0%81%E6%8B%BF%E4%BA%86%E6%AF%94%E8%B5%9B%E5%86%A0%E5%86%9B.md)
  
- 研发规范

  - [为什么阿里巴巴禁止开发人员使用isSuccess作为变量名？](https://mp.weixin.qq.com/s/xvTCaBXkRc7e6dGCUJxRPQ)
  - [为什么阿里巴巴要求谨慎使用ArrayList中的subList方法](https://mp.weixin.qq.com/s/9y89Hy-YnpPjXpcmXpy_GQ)
  
- 面试真题
  - [8年互联网老兵，2个月面试20家大厂的知识点总结和建议](https://blog.csdn.net/qq_35190492/article/details/104914487)
  - [这61道面试题（阿里，美团，携程，百度）](https://blog.csdn.net/Sqdmn/article/details/104908489)
  - [远程面试了几个大厂成功拿到阿里offer，分享面试大厂你需要具备哪些能力](https://blog.csdn.net/cxytony/article/details/104922771)
  - [2020 字节跳动后端面经分享！已拿 offer!](https://mp.weixin.qq.com/s/hr2pDs2wsiHQuDzW7jmOow)
  - [春招字节跳动、蘑菇街四轮面试，分别问了啥？](https://mp.weixin.qq.com/s/xBC1IRr6v8hmIJ9lqCp5pQ)
  - [敖丙8年经验读者，疫情期间面20家大厂总结](https://mp.weixin.qq.com/s/AQvDX0n8wBBaWl2OmcpnrA)
  - [京东+百度一面，不小心都拿了Offer](https://mp.weixin.qq.com/s/VVonP6MgGRUnBnWa2ukkyw)
  - [蚂蚁金服2019实习生面经总结(已拿口头offer)](https://mp.weixin.qq.com/s/0opKiGbKjAfJkRVeVHzpZg)
  - [Bigo的Java面试，我挂在了第三轮技术面上......](https://mp.weixin.qq.com/s/3_HnVzGm16zU2zhk7BnwFw)
  - [15个经典的Spring面试常见问题](https://mp.weixin.qq.com/s/OMlwHHnGcN7iZ8lerUvW7w)
  - [Spring常见问题总结（补充版）](https://mp.weixin.qq.com/s/wcK2qsZxKDJTLIGqEIyaNg)
  - [我是如何在面试别人Spring事务时“套路”对方的](https://mp.weixin.qq.com/s/JcHt99SAbNIlY063rmylpA)
  - [我和阿里面试官的一次“邂逅”(附问题详解)](https://mp.weixin.qq.com/s/-DZj158-LOQmnCayf1_n3A)
  - [一份还热乎的蚂蚁金服面经（已拿Offer）！附答案！！](https://mp.weixin.qq.com/s/HtLwChoLzqhbM4pKldLDng)
  - [十道校招常见的面试题](https://mp.weixin.qq.com/s/wTKSvziyEXrSyf21iMjhZQ)
  - [JVM必问知识点:类加载过程](https://mp.weixin.qq.com/s/eHqFONXXNc-LD4ugaKM6UA)
  - [迄今为止把同步/异步/阻塞/非阻塞/BIO/NIO/AIO讲的这么清楚的好文章（快快珍藏）](https://mp.weixin.qq.com/s/EVequWGVMWV5Ki2llFzdHg)
- 程序人生系列
  - [我知道互联网不相信眼泪，但是敖丙今天还是没忍住](https://mp.weixin.qq.com/s/UC6NsEFlNfqMdEkzvHxKRA)
  - [2020无畏年少青春，迎风潇洒前行](https://mp.weixin.qq.com/s/66ZDj60KPEfohHg0g8Cggw)
  - [写作一个月的感受](https://github.com/AobingJava/JavaFamily/blob/master/docs/coderLife/%E5%86%99%E4%BD%9C%E4%B8%80%E4%B8%AA%E6%9C%88%E5%9C%A8%E6%84%9F%E6%81%A9%E8%8A%82%E5%AF%B9%E5%A4%A7%E5%AE%B6%E8%AF%B4%E7%9A%84%E8%AF%9D.md)
  - [敖丙用20行代码拿了比赛冠军](https://github.com/AobingJava/JavaFamily/blob/master/docs/coderLife/%E6%95%96%E4%B8%99%E7%94%A820%E8%A1%8C%E4%BB%A3%E7%A0%81%E6%8B%BF%E4%BA%86%E6%AF%94%E8%B5%9B%E5%86%A0%E5%86%9B.md)
  - [应届毕业生工作7个月小结](https://mp.weixin.qq.com/s/XcrBvdlh1At_V42qfQZ9Kw)
  - [教你在服务器搭建个人面试项目](https://github.com/AobingJava/JavaFamily/blob/master/docs/coderLife/%E6%95%99%E4%BD%A0%E5%9C%A8%E6%9C%8D%E5%8A%A1%E5%99%A8%E6%90%AD%E5%BB%BA%E4%B8%AA%E4%BA%BA%E9%9D%A2%E8%AF%95%E9%A1%B9%E7%9B%AE.md)
  - [记一次害敖丙差点丢工作的线上P0事故](https://github.com/AobingJava/JavaFamily/blob/master/docs/coderLife/%E8%AE%B0%E4%B8%80%E6%AC%A1%E5%B7%AE%E7%82%B9%E5%AE%B3%E6%95%96%E4%B8%99%E4%B8%A2%E5%B7%A5%E4%BD%9C%E7%9A%84%E7%9A%84%E7%BA%BF%E4%B8%8AP0%E4%BA%8B%E6%95%85.md)
  - [阿里五年老员工有什么话想对大家说？](https://mp.weixin.qq.com/s/9vPZd1q1vpKuE2qZazLQmA)
  - [从毕业到技术专家我做了啥](https://github.com/AobingJava/JavaFamily/blob/master/docs/coderLife/%E9%A3%8E%E9%9B%A8%E5%8D%81%E5%B9%B4%E4%BB%8E%E6%AF%95%E4%B8%9A%E5%88%B0%E6%8A%80%E6%9C%AF%E4%B8%93%E5%AE%B6%E6%88%91%E5%81%9A%E4%BA%86%E5%95%A5.md)
  - [50天全网2W粉，感谢坚持！](https://mp.weixin.qq.com/s/_5tVdE9oFPBUK3Z0gKH26g)
  - [恰饭道歉](https://mp.weixin.qq.com/s/T-SNohqpF01NT0_GUiQHxQ)
  - [MacBook Pro 入手一年了，到底香不香？](https://mp.weixin.qq.com/s/SKzzAT-jBZ2l2R1Evr75ig)
  

- 日常生活

  - [请照顾好自己，周末病魔差点一套带走我。](https://mp.weixin.qq.com/s/5C4UjGtHoZVu8uI4yP5wRg)
  - [敖丙我参加了蘑菇街年会，流了一晚上鼻血](https://mp.weixin.qq.com/s/fkByjmdaqdw0TELDzdm5mQ)
  - [曾经我们并肩作战，敬未来一杯，敬资本一杯](https://mp.weixin.qq.com/s/s9HPYYi9VfYMt7UGCTqWVw)
  - [敖丙我写了一个新手都写不出的低级bug，被骂惨了。](https://mp.weixin.qq.com/s/yB9s771gDz6oMKZsUnJuyg)
  - [敖丙的第一次相亲，还没开始，就已经结束了。](https://mp.weixin.qq.com/s/mLLbpnI1pVnlUzL7H3EuNQ)
  
- 过年特辑

  - [贵州打工仔回家过年，遭遇流感，被隔离，偶遇读者，偶遇直播同行...](https://mp.weixin.qq.com/s/MXSWBVQyVD4OW0tjy5UO8Q)
  - [敖丙回家过年，外婆说没带女朋友别回来了？喝了老爸89年的酒，当场反目。](https://mp.weixin.qq.com/s/pQrepZAbgP59gmj42Z1kdA)
  - [书房翻杂物，看到初恋的信件，看到奖牌，看到梅西、力宏，帅丙的眼角又湿了.....](https://mp.weixin.qq.com/s/VECNJbVV0Bz8PKlG8pYwVw)
  - [疫情之下，从一座空城，到另一座空城，贵州小伙带你看不一样的杭州](https://mp.weixin.qq.com/s/8blBtbBLJtVvpnrJ7tmh_g)
  - [昂，我24岁了](https://mp.weixin.qq.com/s/_HCBjYI9bcNy-zBHu58l7g)
  
- **福利**
    - [Java/后端学习路线](https://mp.weixin.qq.com/s/5QpuDtXAalR-pz59B5t27g)
    - [整理的书单(附个人喜欢的文学书)](https://github.com/AobingJava/JavaFamily/blob/master/docs/creative/%E3%80%8A%E5%90%90%E8%A1%80%E6%95%B4%E7%90%86%E3%80%8B%E5%8D%81%E5%B9%B4%E9%A3%8E%E9%9B%A8%E6%8A%80%E6%9C%AF%E4%BA%BA%E7%9A%84%E4%B9%A6%E5%8D%95%E6%95%B4%E7%90%86.md)
    - [整理好用的工具集](https://github.com/AobingJava/JavaFamily/blob/master/docs/creative/%E9%A1%B6%E7%BA%A7%E7%A8%8B%E5%BA%8F%E5%91%98%E7%9A%84%E7%99%BE%E5%AE%9D%E7%AE%B1.md)
    - [通用的学习方法](https://mp.weixin.qq.com/s/JX72OoiNrZ9R0DTuOOtcoA)
    - [IDEA破解(请勿传播)](https://github.com/AobingJava/JavaFamily/blob/master/docs/idea/idea.md)
    - [电子书(请勿传播)](https://github.com/AobingJava/JavaFamily/blob/master/docs/idea/%E7%94%B5%E5%AD%90%E4%B9%A6.md)
    - [面试资料(持续更新)](https://github.com/AobingJava/JavaFamily/blob/master/docs/idea/%E8%B5%84%E6%96%99.md)
    - [简历模板(欢迎补充)](https://github.com/AobingJava/JavaFamily/blob/master/docs/idea/%E8%B5%84%E6%96%99.md)
    - [概要设计模板](https://github.com/AobingJava/JavaFamily/blob/master/docs/idea/%E8%B5%84%E6%96%99.md)
 

