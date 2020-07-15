---
description: 删除群成员
---

# 删除群成员

**简要描述：**

* 删除群成员

**请求URL：**

* `http://域名地址/deleteChatRoomMember`

**请求方式：**

* POST 

**请求头Headers：**

* Content-Type：application/json
* Authorization：login接口返回

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :---: | :---: | :---: | :---: |
| wId | 是 | string | 微信实例ID |
| chatRoomId | 是 | String | 群号 |
| userList | 是 | String | 群成员微信号，多个已 "," 分割 |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :---: | :---: | :---: |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |

**请求参数示例**

```javascript
{
    "wId": "349be9b5-8734-45ce-811d-4e10ca568c67",
    "chatRoomId":"24187765053@chatroom",
    "userList":"wxid_ew6i9qdxlinu12,wxid_nqo37ves8w5t22"
}
```

**成功返回示例**

```javascript
{
    "message": "成功",
    "code": "1000",
    "data":null
}
```

**错误返回示例**

```javascript
{
    "message": "失败",
    "code": "1001",
    "data": null
}
```

