---
description: 发送文字朋友圈消息
---

# 发送文字朋友圈消息

**简要描述：**

* 发送文字朋友圈消息

**请求URL：**

* `http://localhost:18081/snsSend`

**请求方式：**

* POST

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| wId | 是 | string | 微信实例ID |
| content | 是 | string | 文本内容 |
| groupUser | 否 | string | 对谁可见（传微信号,多个用;分隔） |
| blackList | 否 | string | 对谁不可见（传微信号,多个用;分隔） |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |
| data |  |  |
| id | string | ID |
| userName | string | 微信号 |
| createTime | string | 发送时间 |
| objectDesc | string | 内容 |

**请求参数示例**

```text
{
    "wId": "0000016e-6343-089e-0001-e2ef939176f6",
    "content": "这是一条文本朋友圈消息"
}
```

**成功返回示例**

```text
{
    "message": "成功",
    "code": "1000",
    "data": {
        "id": "13200538655176208452",
        "userName": "wxid_6mq1pu8ngj3r22",
        "createTime": 1573626834,
        "objectDesc": "这是一条文本朋友圈消息"
    }
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

