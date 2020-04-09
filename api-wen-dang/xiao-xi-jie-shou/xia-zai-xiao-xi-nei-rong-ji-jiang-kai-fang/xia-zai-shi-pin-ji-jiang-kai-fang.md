---
description: 下载视频
---

# 下载视频

**简要描述：**

* 下载消息中的视频

**请求URL：**

* `http://localhost:18081/getMsgVideo`

**请求方式：**

* POST

**请求头Headers：**

* Content-Type：application/json
* Authorization：Authorization值（登录获取二维码信息接口中返回的认证信息值）

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| wId | 是 | string | 微信实例ID |
| msgId | 是 | string | 消息id |
| content | 是 | string | 收到的消息的xml数据 |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |

**请求参数示例**

```text
{
    "wId": "",
    "msgId": "",
    "content": ""
}
```

**成功返回示例**

```text

```

**错误返回示例**

```text
{
    "message": "失败",
    "code": "1001",
    "data": null
}
```

