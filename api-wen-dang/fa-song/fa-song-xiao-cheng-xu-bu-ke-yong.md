---
description: 发送小程序
---

# 发送小程序

**简要描述：**

* 发送小程序

**请求URL：**

* `http://localhost:18081/sendApp`

**请求方式：**

* POST

**请求头Headers：**

* Content-Type：application/json
* Authorization：Authorization值（登录获取二维码信息接口中返回的认证信息值）

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| wId | 是 | string | 微信实例ID |
| wcId | 是 | string | 微信号/群号 |
| appName | 是 | string | 小程序id |
| title | 是 | string | 标题 |
| description | 是 | string | 描述 |
| thumbUrl | 是 | string | 图标url |
| thumbAesKey | 是 | string | 图标aeskey |
| pagePath | 是 | string | 点开小程序后到达的页面路径 |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |

**请求参数示例**

```text
{

    "wId": "0000016f-78bd-21c8-0001-29c4d004ae46",
     "wcId": "jack_623555049",
    "appName": "gh_0fc5d8395610@app",
    "title": "点击查看你的QQ未读消息",
    "description": "腾讯QQ",
    "thumbUrl": "30570201000450304e0201000204a6379e4e02032f55f902045f0260b402045e12a1820429777875706c6f61645f777869645f6f71756a7379386c63703375313232325f313537383237393239380204010400030201000400",
    "thumbAesKey": "484f9eb55cec7c93b67cd3a8908c981a",
    "pagePath": "pages/index/index.html"
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

