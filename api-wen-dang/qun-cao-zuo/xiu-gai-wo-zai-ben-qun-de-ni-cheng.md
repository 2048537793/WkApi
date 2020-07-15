# 修改我在本群的昵称

**简要描述：**

* 修改我在某群的昵称

**请求URL：**

* `http://域名/updateIInChatRoomNickName`

**请求方式：**

* POST 

**请求头Headers：**

* Content-Type：application/json
* Authorization：login接口返回

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :---: | :---: | :---: | :---: |
| wId | 是 | String | 微信实例标识 |

**请求参数示例**

```javascript
{
    "wId": "4941c159-48dc-4271-b0d0-f94adea39127",
    "chatRoomId": "23282491030@chatroom",
    "nickName":"啦啦啦"
}
```

**成功返回示例**

```javascript
{
    "message": "成功",
    "code": "1000",
    "data": null
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
| code | int | 1000成功  10001失败 |
| msg | string | 反馈信息 |
| data | JSONObject |  |

