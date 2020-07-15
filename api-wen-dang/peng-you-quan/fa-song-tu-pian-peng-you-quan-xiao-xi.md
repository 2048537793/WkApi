---
description: 发送图片朋友圈消息
---

# 发送图片朋友圈

**简要描述：**

* 发送图片朋友圈消息

**请求URL：**

* `http://域名地址/snsSendImage`

**请求方式：**

* POST 

**请求头Headers：**

* Content-Type：application/json
* Authorization：login接口返回

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :---: | :---: | :---: | :---: |
| wId | 是 | String | 微信实例ID |
| content | 是 | String | 文本内容 |
| paths | 是 | String | 图片url\(多个用;分隔\) |
| groupUser | 否 | String | 对谁可见（传微信号,多个用;分隔） |
| blackList | 否 | String | 对谁不可见（传微信号,多个用;分隔） |

**请求参数示例**

```javascript
{
    "wId": "0000016e-6382-4be4-0001-e6b4e3cd1bbd",
    "content": "这是一条图文朋友圈消息",
    "paths": "http://1563240615548.jpg;http://1563253424796.png"
}
```

**成功返回示例**

```javascript
{
    "message": "成功",
    "code": "1000",
    "data": {
        "status": 1,
        "object": {
            "id": "xxxxxx",
            "userName": "xxxxxx",
            "createTime": xxxxxx,
            "objectDesc": "xxxxxx"
        }
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
| code | int | 1000成功，10001失败 |
| msg | String | 反馈信息 |
| data |  |  |
| id | String | ID |
| userName | String | 微信号 |
| createTime | String | 发送时间 |
| objectDesc | String | 内容 |

