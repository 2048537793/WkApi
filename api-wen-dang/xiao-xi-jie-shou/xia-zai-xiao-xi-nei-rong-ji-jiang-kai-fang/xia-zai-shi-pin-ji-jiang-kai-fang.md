---
description: 下载视频
---

# 下载视频

**请求URL：**

* `http://域名地址/getMsgVideo`

**请求方式：**

* POST 

**请求头Headers：**

* Content-Type：application/json
* Authorization：login接口返回

**参数：**

| 参数名 | 必选 | 类型 | 说明 |  |
| :---: | :---: | :---: | :---: | :--- |
| wId | 是 | string | 微信实例ID  \(包含此参数 所有参数都是从消息回调中取） |  |
| msgId | 是 | long | 消息id |  |
| content | 是 | string | 收到的消息的xml数据 |  |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :---: | :---: | :---: |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |
| data | string | 视频url（3月以内有效） |

**请求参数示例**

```javascript
{
   "wId": "0000016f-a3f4-7ac2-0001-4686486bb6c6",
   "msgId": 1102684153,
   "content" :"<?xml version=\"1.0\"?><msg><videomsg aeskey=\"cc054b6e3e98fe91a5bb16227de67023\" cdnthumbaeskey=\"cc054b6e3e98fe91a5bb16227de67023\" cdnvideourl=\"304f02010004483046020100020466883f5202032f5081020491eff98c02045e1db76004213439346431383637346131316634356332613338363436613530633439376233320204010400040201000400\" cdnthumburl=\"304f02010004483046020100020466883f5202032f5081020491eff98c02045e1db76004213439346431383637346131316634356332613338363436613530633439376233320204010400040201000400\" length=\"966424\" playlength=\"15\" cdnthumblength=\"5819\" cdnthumbwidth=\"0\" cdnthumbheight=\"0\" fromusername=\"wxid_lr6j4nononb921\" md5=\"5056a23087ce5a8fe97042f0e5f87503\" newmd5=\"8eb2172bf0c03b2bc5af09effcaaba3d\" isad=\"0\" /></msg>"
}
```

**成功返回示例**

```javascript
{
    "message": "成功",
    "code": "1000",
    "data": {
        "url": "https://weikong-1301028514.cos.ap-shanghai.myqcloud.com//msgImg/50720e30-064e-4429-82c5-b6f341aae226-1591347789541-200000.mp3"
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

