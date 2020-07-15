---
description: 发送语音消息
---

# 发送语音消息

**请求URL：**

* `http://域名地址/sendVoice`

**请求方式：**

* POST 

**请求头Headers：**

* Content-Type：application/json
* Authorization：login接口返回

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :---: | :---: | :---: | :---: |
| wId | 是 | string | 微信实例ID |
| wcId | 是 | string | 单聊被发送人账号，群聊群账号 |
| content | 是 | string | 语音 （silk格式,可以[先下载消息中的语音](../xiao-xi-jie-shou/xia-zai-xiao-xi-nei-rong-ji-jiang-kai-fang/xia-zai-yu-yin-ji-jiang-kai-fang.md)） |
| length | 是 | int | 语音时长（回调消息xml数据中的voicelength字段） |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :---: | :---: | :---: |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |

**请求参数示例**

```javascript
{
   "wId": "0000016f-a719-5b44-0003-a567f79011fc",
   "wcId":"jack_623555049",
   "content": "https://xc-1300726975.cos.ap-shanghai.myqcloud.com/msgVoice/e17dd0a9-5c59-4a54-a3cd-1a4817f5dd29-1579005558791.silk",
    "length": 1
}
```

**成功返回示例**

```javascript
{
    "message": "发送成功",
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

