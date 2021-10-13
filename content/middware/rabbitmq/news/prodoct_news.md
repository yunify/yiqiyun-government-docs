---
title: "产品动态"
collapsible: false
weight: 10

product:
    - time: 2021-09-15
      title: RabbitMQ 3.8.19 版本正式上线
      content: 升级到 RabbitMQ 3.8.19 版本，并进行以下功能更新：<br>1.新增集群节点发现功能：将集群节点信息放入etcd中，服务启动时集群从etcd集群中获取集群节点信息。<br>2.为系统服务systemd、rabbitmq、appctl、keepalived、haproxy和rabbitmq加上日志信息，统一放到挂载盘固定位置。<br>3.增加caddy服务，通过caddy能够获取访问服务日志。<br>4.去掉ram角色。<br>5.若干优化。
      url: ../../intro/artic/
      tags: 
      - 新功能
      - 体验优化
      - 修复问题


    - time: 2021-05-24
      title: RabbitMQ 3.7.23 - YiQiYu 1.5.0 版本正式上线
      content: 1.提升网络性能。将集群节点信息放入etcd中，服务启动时集群从etcd集群中获取集群节点信息。多个rabbitmq集群支持使用同一个etcd。<br>2.提升计算性能。<br>3.提升安全性。<br>4.用户体验改进。
      url: ../../quickstart/quick_start/

    - time: 2021-05-01
      title: RabbitMQ 3.7.23 - YiQiYun 1.4.3 版本正式上线
      content: 本次版本主要做了节点调整，以提升性能。
      url: ../../quickstart/quick_start/



---

