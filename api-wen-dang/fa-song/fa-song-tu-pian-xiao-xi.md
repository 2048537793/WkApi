---
description: 发送图片消息
---

# 发送图片消息

**请求URL：**

* `http://localhost:18081/sendImage`

**请求方式：**

* POST

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| wId | 是 | string | 微信实例ID |
| wcId | 是 | string | 微信号/群号 |
| content | 是 | string | 图片url链接 |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |

**请求参数示例**

```text
{
    "wId": "0000016e-63eb-f319-0001-ed01076abf1f",
    "wcId": "LoChaX",
    "content": "http://photocdn.sohu.com/20120323/Img338614056.jpg"
}
```

**成功返回示例**

```text
{
    "message": "发送成功",
    "code": "1000",
    "data": null
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

