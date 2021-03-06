---
title: "扩容集群"
description: 本小节主要介绍如何扩容 Redis Cluster 集群。 
keywords: redis cluster 扩容集群
weight: 30
collapsible: false
draft: false
---



在缓存服务运行过程中，会出现服务能力不足或者容量不够的情况，可以通过扩容来解决，或者服务能力过剩时可以删除节点。在纵向扩容中， 服务需要重启，所以这个时候业务需要停止。在横向伸缩中，数据会发生迁移，但并不影响业务的正常运行。

## 增加集群分片 (shard)

Redis 集群服务每个主节点写的能力与容量都有上限，当写的能力不满足业务需求或达到容量上限时，您可以通过增加节点组即缓存分片来提升写性能以及容量。 每增加一个节点组时将创建一个主节点和其它主节点同样的从节点数。Redis 集群会自动平衡各分片之间的 slots，即会发生 数据迁移，因此增加节点组的时间会有点长。如果事先知道需要增加的分片数建议一次性完成，这样比一次只加一个分片效率更高。 

![](../../_images/add-master.png)

## 增加集群从节点

Redis 集群服务每个主节点可以支持多个从节点。当读的能力不足时，您可以通过增加缓存从节点来提升读性能。 

![](../../_images/add-replica.png)

## 删除集群分片 (shard)

如果写服务能力或容量过剩，也可以删除多余的节点组，即删除主节点和它的所有从节点，删除的过程中系统会自动迁移数据到其它节点中，因此时间会稍长一点。

> **注意**
> 
> Redis 5.0.5 - YiQiYun 1.3.0 及之后的版本在删除 master 节点时添加了限制，以下情况是不允许节点被删除的:
>
> 1、集群存在节点状态异常
>
> 2、存在单节点的 redis 内存使用率大于 95% 
>
> 3、删除后的平均 redis 内存使用率大于 95% 

## 删除集群从节点

如果读服务能力过剩，您也可以删除多余的从节点。删除的时候需要从每个主节点下选择同样数目的从节点，从而保证整个集群不会是一个“畸形”。

> **注意**
>
> Redis 5.0.5 - YiQiYun 1.3.0 在删除 master-replica 节点时添加了限制，以下情况是不允许节点被删除的
> 集群待删除从节点中包含 redis 角色为主节点

## 增加缓存容量

当缓存容量不足时，您可以通过纵向扩容来提升缓存容量，右键点击集群，选择扩容。

![](../../_images/scale-up.png)

>**说明**
>
>硬盘存储容量只能扩容，不支持减少存储容量。在线扩容期间，缓存服务会被重启。
