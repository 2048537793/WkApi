---
description: 获取群二维码
---

# 获取群二维码

**简要描述：**

* 获取群二维码

**请求URL：**

* `http://域名地址/getGroupQrCode`

**请求方式：**

* POST 

**请求头Headers：**

* Content-Type：application/json
* Authorization：login接口返回

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :---: | :---: | :---: | :---: |
| wId | 是 | String | 微信实例标识 |
| chatRoomId | 是 | String | 群号 |

**请求参数示例**

```javascript
{
    "wId":"349be9b5-8734-45ce-811d-4e10ca568c67",
    "chatRoomId": "24187765053@chatroom"
}
```

**成功返回示例**

```javascript
{
    "message": "成功",
    "code": "1000",
    "data": {
        "imgUrl": "xxxxxx"
    }
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

**返回数据：**

| 参数名 | 类型 | 说明 |
| :---: | :---: | :---: |
| code | String | 1000成功  10001失败 |
| msg | String | 反馈信息 |
| data | JSONObject |  |

