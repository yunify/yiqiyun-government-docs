---
title: "NAT网关"
draft: false
weight: 1
---

NAT 网关 (Network Address Transmition Gateway) 是一个分布式的网络地址转换服务。用户的多个私有网络可以通过一个统一的 NAT 网关访问外网，同时通过路由规则来配置网络访问的路径。

NAT 网关为私有网络的主机提供了复用公网 IP 的能力，目前支持源 NAT 功能，主机可以通过 NAT 网关绑定的公网 IP 地址访问互联网。NAT网关的SNAT功能还可以作为防火墙使用，因为私有网络的主机可以主动通过 NAT 网关访问互联网，但是互联网的主机不可以主动访问私有网络内的主机。 NAT 网关具备高达 10 Gbps 的转发能力以及 Region 级别的多活容灾能力。


