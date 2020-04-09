---
description: 发送名片消息
---

# 发送名片消息

**简要描述：**

* 发送名片

**请求URL：**

* `http://localhost:18081/sendNameCard`

**请求方式：**

* POST

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| wId | 是 | string | 微信实例ID |
| wcId | 是 | string | 发送人微信号（群/好友） |
| nameCardId | 是 | string | 要发送的名片微信号 |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |

**请求参数示例**

```text
{
     "wId": "0000016e-abef-bb44-0002-dad3f6230dad",
     "wcId": "azhichao",
     "nameCardId": "wxid_uf44z2g3jge022"
}
```

**成功返回示例**

```text
{
    "message": "成功",
    "code": "1000",
    "data":null
}
```

**错误返回示例**

```text
{
    "message": "失败",
    "code": "1001",
    "data": null
}
```

