---
description: 设置消息接收地址
---

# 设置消息接收地址

{% hint style="warning" %}
* 用户需提供接收 微信消息的公网接口URL，并将此url在此接口配置（PS：简单理解就是腾讯服务器会将消息发送到你们编写的服务器接口。）
* 用户网络需流畅，Http 请求默认最高6 秒内建立连接并发送数据。通讯时长超过 6秒，不发送回调消息。
* 回调消息返回结构是 String类型的JSON数据格式
{% endhint %}

**简要描述：**

* 设置http回调地址

**请求URL：**

* `http://localhost:18081/setHttpCallbackUrl`

**请求方式：**

* POST

**请求头Headers：**

* Content-Type：application/json
* Authorization：Authorization值（登录获取二维码信息接口中返回的认证信息值）

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| httpUrl | 是 | string | http回调地址 |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |

**请求参数示例**

```text
{
    "httpUrl": "http://192.168.40.14:18081/userInfo/webHttpTest"
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

{% hint style="info" %}
**配置成功后，即可生效**
{% endhint %}



