---
description: 删除群成员
---

# 删除群成员

**简要描述：**

* 删除群成员

**请求URL：**

* `http://localhost:18081/deleteChatRoomMember`

**请求方式：**

* POST

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| wId | 是 | string | 微信实例ID |
| chatRoomWcId | 是 | string | 群微信号 |
| wcId | 是 | string | 微信号 |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |

**请求参数示例**

```text
{
    "wId": "0000016e-6343-089e-0001-e2ef939176f6",
    "chatRoomWcId": "21946847599@chatroom",
    "wcId": "zhongweiyu789"
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

