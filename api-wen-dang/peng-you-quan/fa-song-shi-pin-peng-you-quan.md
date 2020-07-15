---
description: 发送视频朋友圈消息
---

# 发送视频朋友圈

**简要描述：**

* 发送视频朋友圈

**请求URL：**

* `http://域名地址/snsSendVideo`

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
| videoPath | 是 | String | 视频链接URL |
| thumbPath | 是 | String | 视频封面URL |
| groupUser | 否 | String | 对谁可见（传微信号,多个用;分隔） |
| blackList | 否 | String | 对谁不可见（传微信号,多个用;分隔） |

**请求参数示例**

```javascript
{
    "wId": "0000016e-68f9-99d5-0002-3a1cd9eaaa17",
    "content": "今天还是可以的",
    "videoPath": "https://wkgjonlines.oss-cn-shenzhen.aliyuncs.com/movies/20191113/d7c616569ac342ad1fa8e3301682844e.mp4",
    "thumbPath": "http://cdn.duitang.com/uploads/item/201412/21/20141221161645_2MSeA.jpeg"
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
            "id": "xxxxxxx",
            "userName": "xxxxxxx",
            "createTime": xxxxxxx,
            "objectDesc": "xxxxxxx"
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
| objectDesc | String | 文本内容 |

