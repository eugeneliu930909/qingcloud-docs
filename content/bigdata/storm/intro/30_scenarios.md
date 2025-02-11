---
title: "常见应用场景"
description: 本小节主要介绍 Storm 应用场景。 
keywords: Storm 应用场景
weight: 30
collapsible: false
draft: false
---

- 求 TopN

  相信大家对 TopN 类的业务需求也比较熟悉，在规定时间窗口内，统计数据出现的 TopN，该类处理在购物及电商业务需求中，比较常见。

- 实时推荐系统

  例如电商业务中基于用户的历史行为、查询、点击、地理信息等信息获得，其中有很多实时数据，可以使用 Storm 进行处理，在此基础上进行精准的商品推荐和放置广告。

- 实时风控系统

  使用 Storm 实时统计分析为规则引擎提供实时数据，可在毫秒延迟内检测、拦截潜在的风险行为。

- 分布式 RPC

  Storm 有对 RPC 进行专门的设计，分布式 RPC 用于对 Storm 上大量的函数进行并行计算，最后将结果返回给客户端。

- 热度统计

  热度统计实现依赖于 Storm 提供的 TimeCacheMap 数据结构，也推荐使用 RotatingMap，该结构能够在内存中保存近期活跃的对象。我们可以使用它来实现例如论坛中热帖排行计算等。

- 日志分析与处理

  监控系统中的事件日志，使用 Storm 检查每条日志信息，把符合匹配规则的消息保存到数据库。一般从类 Kafka 的 MQ 或者基于 HBase 的 timetunnel 中读取实时日志消息，经过一系列处理，最终将处理结果写入到一个分布式存储中，提供给应用程序访问。

  除此之外，官方也列举出了很多公司使用 Storm 的场景，[官方场景参考](http://storm.apache.org/releases/current/Powered-By.html)。
