---
description: 下载图片
---

# 下载图片

**请求URL：**

* http://域名地址/getMsgImg

**请求方式：**

* POST

**请求头Headers：**

* Content-Type：application/json

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| wId | 是 | string | 微信实例ID  \(包含此参数 所有参数都是从消息回调中取） |
| msgId | 是 | long | 消息id |
| fromUser | 是 | string | 发送人的微信号 |
| toUser | 是 | string | 接收人的微信号 |
| content | 是 | string | 收到的消息的xml数据 |
| type | 否 | int | 0：普通图片（默认）  1：高清图片 |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |

**请求参数示例**

```javascript
{
   "wId": "0000016f-a3f4-7ac2-0001-4686486bb6c6",
   "msgId": 1102684156,
   "fromUser":"gh_6446e0983ae5",
   "toUser":"wxid_gia1nwcgpobz22",
   "content" :"<?xml version=\"1.0\"?><msg><img aeskey=\"07fea09b27952d512c0d71a52c914f3\" encryver=\"0\" cdnthumbaeskey=\"07fea09b27952d512c0d71a52c914f34\" cdnthumburl=\"30580201000451304f020100020466883f5202032f55f902048f0260b402045e1dbcac042a777875706c6f61645f777869645f676961316e776367706f627a32323135305f31353739303037313437020401051a020201000400\" cdnthumblength=\"3237\" cdnthumbheight=\"120\" cdnthumbwidth=\"80\" cdnmidheight=\"0\" cdnmidwidth=\"0\" cdnhdheight=\"0\" cdnhdwidth=\"0\" cdnmidimgurl=\"30580201000451304f020100020466883f5202032f55f902048f0260b402045e1dbcac042a777875706c6f61645f777869645f676961316e776367706f627a32323135305f31353739303037313437020401051a020201000400\" length=\"51361\" md5=\"449fb858f24416adcab831859011fb21\" hevc_mid_size=\"30042\" /></msg>"
}
```

**成功返回示例**

```javascript
{
    "message": "成功",
    "code": "1000",
    "data": {
        "url": "https://weikong-1301028514.cos.ap-shanghai.myqcloud.com//msgImg/dd32565c-78b0-4803-a330-6293b05674d9-1591347877463-600000.png"
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

