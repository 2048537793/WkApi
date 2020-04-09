---
description: 自动同意入群邀请
---

# 自动同意入群邀请

{% hint style="info" %}
收到群邀请时，您所配置的接收消息的服务器会收到一条邀请消息，目前还需请求两个接口，才会入群成功，具体如下：

* 您接收消息的服务器会收到一条群邀请信息，将邀请信息里的url通过本接口转化后得到一个新的接口地址，就是本接口返回的data字段。
* Post请求新接口地址，并且参数传入“{}”，方可自动入群成功。
{% endhint %}

**简要描述：**

* 自动同意入群邀请

**请求URL：**

* `http://localhost:18081/decodeUrl`

**请求方式：**

* POST

**请求头Headers：**

* Content-Type：application/json
* Authorization：Authorization值（登录获取二维码信息接口中返回的认证信息值）

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| wId | 是 | string | 微信实例ID |
| url | 是 | string | 原始 url，如入群邀请消息收到的链接 |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |
| data | Stirng | 新的接口地址 |

**请求参数示例**

```text
{
     "wId": "0000016f-b270-b2cd-0000-4e27e92f4502",
     "url": "http://shmmsns.qpic.cn/mmsns/CJ35Z2cnZA0zggcHCKIiaqOu0wO1gaOTaxL2Wd9StGfS1GdbbfKvJic1icfjfMXia7iaAd1B4fgN61g4/150"
}
```

**成功返回示例**

```text
{
    "message": "成功",
    "code": "1000",
    "data": "http://shmmsns.qpic.cn/mmsns/CJ35Z2cnZA0zggcHCKIiaqOu0wO1gaOTaxL2Wd9StGfS1GdbbfKvJic1icfjfMXia7iaAd1B4fgN61g4/150"
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

