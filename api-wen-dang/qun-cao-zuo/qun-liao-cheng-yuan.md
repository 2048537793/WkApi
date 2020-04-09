---
description: 群聊@
---

# 群聊@

**简要描述：**

* 群聊@成员（此接口就是发送文本消息接口 新增了个参数）

**请求URL：**

* `http://localhost:18081/sendText`

**请求方式：**

* POST

**请求头Headers：**

* Content-Type：application/json
* Authorization：Authorization值（登录获取二维码信息接口中返回的认证信息值）

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| wId | 是 | string | 微信实例ID |
| wcId | 是 | string | 群号 |
| content | 是 | string | 文本内容消息 |
| ant | 否 | string | 微信号原始Id\(获取好友信息接口取得userName字段\)  |
| **返回数据：** |  |  |  |

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |

**请求参数示例**

```text

------------------------ 群艾特某人 -------------------------------
{
 "wId": "0000016f-8911-484a-0001-db2943fc2786",
 "wcId": "22270365143@chatroom",
 "at": "wxid_lr6j4nononb921,wxid_i6qsbbjenjuj22",
 "content": "@微控Team_Mr Li@你微笑时真美 测试"
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

