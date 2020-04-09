---
description: 同意添加好友
---

# 同意添加好友

{% hint style="danger" %}
**参数中的v1 v2是从消息回调中取得的。（PS：收到好友请求时，消息回调会收到一条添加消息，v1 v2在里面。）**
{% endhint %}

**简要描述：**

* 同意添加好友

**请求URL：**

* `http://localhost:18081/acceptUser`

**请求方式：**

* POST

**请求头Headers：**

* Content-Type：application/json
* Authorization：Authorization值（登录获取二维码信息接口中返回的认证信息值）

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| wId | 是 | string | 微信实例ID |
| v1 | 是 | string | v1   |
| v2 | 是 | string | v2 |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |

**请求参数示例**

```text
{
   "wId": "0000016f-a2f0-03e3-0003-65e826091614",
   "v1": "v1_aaf94e13d0058cdc888e388b98952e0fc23212d180e4dacb38b96dfe4b078c488e72772f907517470ac0b9b7311826da@stranger",
   "v2": "v2_13ced007472228cd1545feecf78b99f9ba9f5d3de802292758a6f26b3bf707d6bcabdf16bc312dd703df8774ab86ff9d@stranger"
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

