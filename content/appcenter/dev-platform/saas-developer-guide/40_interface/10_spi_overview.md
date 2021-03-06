---
title: "接口概述"
description: SPI 接口概述
keyword: 山东省计算中心云平台, AppCenter, 云应用开发平台, SaaS 
draft: false
weight: 10
---

第三方 SaaS 应用接入山东省计算中心云平台应用市场需要实现相关的接口定义，服务商通过提供接口，获得应用订购成功的信息，从而为购买者开通应用。

山东省计算中心云平台saas提供了以下几个 SPI 接口，如下所示。

| 使用场景 | 事件名称           |
| -------- | ------------------ |
| 创建实例 | CreateAppInstance  |
| 续费实例 | RenewAppInstance   |
| 升级实例 | UpgradeAppInstance |
| 实例到期 | ExpireAppInstance  |
| 实例删除 | DeleteAppInstance  |
| 测试连接 | TestConnection     |

实现 SPI 接口需要开发者在配置应用时填入通知 URL，山东省计算中心云平台 app 平台将通过此 url 调用接入的 SaaS 应用。

**一个简单的 SPI 实现示例：** https://github.com/xiaoli9965/saas-demo
