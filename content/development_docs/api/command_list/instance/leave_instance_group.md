---
title: "LeaveInstanceGroup"
description: 
draft: false
weight: 18
---

云服务器离开指定的云服务器组。

**Request Parameters**

| Parameter name | Type | Description | Required |
| --- | --- | --- | --- |
| instances.n | String | 一个或多个云服务器ID | Yes |
| instance_group | String | 云服务器组 ID | Yes |
| zone | String | 区域 ID，注意要小写 | Yes |

[_公共参数_](../../../parameters/)

**Response Elements**

| Name | Type | Description |
| --- | --- | --- |
| action | String | 响应动作 |
| job_id | String | 执行任务的 Job ID |
| ret_code | Integer | 执行成功与否，0 表示成功，其他值则为错误代码 |

**Example**

_Example Request_

```
http://api.yiqiyun.sd.cegn.cn/iaas/?action=LeaveInstanceGroup
&instances.1=i-ipot8lz8
&instance_group=ig-st962mj0
&zone=gd2
&COMMON_PARAMS
```

_Example Response_:

```
{
  "action":"LeaveInstanceGroupResponse",
  "job_id":"j-mcacahmw",
  "ret_code":0
}
```
