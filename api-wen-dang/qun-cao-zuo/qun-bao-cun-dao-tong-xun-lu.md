---
description: 群保存到通讯录
---

# 群保存到通讯录

**简要描述：**

* 群保存到通讯录

**请求URL：**

* `http://localhost:18081/showInAddressBook`

**请求方式：**

* POST

**请求头Headers：**

* Content-Type：application/json
* Authorization：Authorization值（登录获取二维码信息接口中返回的认证信息值）

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| wId | 是 | string | 微信实例ID |
| chatroom | 是 | string | 群id |
| isShow | 是 | boolean | true:保存到通讯录,false:从通讯录删除此群 |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |

**请求参数示例**

```text
{
    "wId": "0000016f-bcb0-666f-0000-051320fc242a",
    "chatroom": "21923674740@chatroom",
    "isShow": true
}
```

**成功返回示例**

```text
{
    "message": "成功",
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

