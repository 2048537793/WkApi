---
description: 执行微信登录（第三步）
---

# 执行微信登录（第三步）

**简要描述：**

* 执行登录（确认登录）

**请求URL：**

* `http://localhost:18081/getIPadLoginInfo`

**请求方式：**

* POST

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| wId | 是 | string | 微信实例ID |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |
| data |  |  |
| nickName | string | 昵称 |
| headUrl | string | 头像url |
| wId | string | 实例Id |
| wcId | string | 微信id |

**请求参数示例**

```text
{
    "wId": "0000016e-63eb-f319-0001-ed01076abf1f"
}
```

**成功返回示例**

```text
{
    "message": "成功",
    "code": "1000",
    "data": {
        "wcId": "wxid_wl9qchkanp9u22",
        "wId": "00000170-962f-4819-0000-b158b7014b41",
        "data": "oouWRyIV8Xu4tGXpWKSbUP+6UWvWqirxWZP0nKgvTv0sgEBPOHHo4m5RI0aPwYkdTJ2ITVKkGqpCH2z2Nmk0ddShJ5Ti3eAZMhHxF2Lg2DhAfZc3ShEQsj/fyBUVSo5NdTMoneHdvOaG8RwLkPWNK2tlpANAcVkYc1UMMKJWravfSse71oxtIGegHb3WamjRTepBjZ9homOo4+aUISQHVryWvnMruqlGqjtgvFz5m396WKO6K8b5tYsa+j3ODaPSs3JPelc1HiZHtSBeoIRb6sUNPO9P7mo8nX29yr+uPsC/Cj027V5WwS9N0/fBJUP48Wqv9VwoTgmbduDxy9cSBxp3l2WbcrM9LnNl/mG/261NKMrQnXYYllbWoHZdx+qXe6jiY/K/f7+ZT8a5hjBJ6/p5TLGjQB0GmbVblQGchDvh9sk9NyL7keJZQzxmTEKr1ah686IGHUEGtCgNma1zgSTL8AwDLNoEJZPHs9Ky07DJvKa40XQcI+RFweiTAwqoTYfgHctDwGsTE825YnRD4xRL7nNnN8n6et1sidwUkElgDdH6d0arx6w9LYb4RBgkr5Z88UsdFUbQhSucj82xKUcEX1z8hucLNUzi16189M4=",
        "nickName": "微控官方小助手",
        "headUrl": "http://wx.qlogo.cn/mmhead/ver_1/oEiaIqbUwbOa6lNpoT9LN7Tq8R7skFdoElKVo19jBaiaT9qDjtTWqsfNh1Ulvh61NIqx3gVWrOfHXD0hLMic4vTX09aLRHl3foILAiaTkL78RSA/0"
    }
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

{% hint style="danger" %}
* 别忘了**header**传**Authorization字段哦**
* **此步骤成功后手机上会显示mac登录成功，才可以收发消息及调用其它接口！**
{% endhint %}

