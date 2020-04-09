---
description: 查找用户
---

# 查找用户

**简要描述：**

* **此接口不支持直接获取wxid开头的微信号信息！！！**
* **wxid开头的微信号，调用**[**搜索用户接口**](../qun-cao-zuo/huo-qu-wei-xin-qun-de-xin-xi.md)**获取信息，！！！**

**请求URL：**

* `http://localhost:18081/searchUser`

**请求方式：**

* POST

**请求头Headers：**

* Content-Type：application/json
* Authorization：Authorization值（登录获取二维码信息接口中返回的认证信息值）

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| wId | 是 | string | 微信实例ID |
| wcId | 是 | string | 要搜索的微信号 |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |
| data |  |  |
| id | string | 朋友圈ID |
| userName | string | 微信号 |
| nickName | string | 昵称 |
| bigHead | string | 大头像 |
| smallHead | string | 小头像 |
| sex | int | 性别 0：女 1：男 |
| signature | string | 个性签名 |
| country | string | 国家 |
| province | string | 省/直辖市 |
| city | string | 市 |
| v1 | string | 添加好友需要 |
| v2 | string | 添加好友需要 |

**请求参数示例**

```text
{
   "wId": "0000016f-a22c-8bea-0003-5a4188a76ccc",
   "wcId": "jack_623555049"
}
```

**成功返回示例**

```text
{
    "message": "成功",
    "code": "1000",
    "data": {
        "userName": "v1_aaf94e13d0058cdc888e388b98952e0fc23212d180e4dacb38b96dfe4b078c488e72772f907517470ac0b9b7311826da@stranger",
        "nickName": "你微笑时真美",
        "bigHead": "http://wx.qlogo.cn/mmhead/ver_1/N7rnhsGTzNrSdzB2Cjf979UM9wQfcXAUeNjDk47bToHJofnbLYMQJgiaJdU4abt1pcwOnHH85gFgx1lbySSCRLfGhVP2HqJcbDugqicsbmVpA/0",
        "smallHead": "http://wx.qlogo.cn/mmhead/ver_1/N7rnhsGTzNrSdzB2Cjf979UM9wQfcXAUeNjDk47bToHJofnbLYMQJgiaJdU4abt1pcwOnHH85gFgx1lbySSCRLfGhVP2HqJcbDugqicsbmVpA/132",
        "sex": 1,
        "signature": "我只是单纯的想发财，如果一夜不行那就两夜！",
        "country": "CN",
        "province": "Jiangsu",
        "city": "Nanjing",
        "v1": "v1_aaf94e13d0058cdc888e388b98952e0fc23212d180e4dacb38b96dfe4b078c488e72772f907517470ac0b9b7311826da@stranger",
        "v2": "v2_13ced007472228cd1545feecf78b99f9a0f2558f109f10e52c14d496eca2ae1e8373220bad8829e36386eaedd1c46701@stranger"
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

{% hint style="info" %}
v1、v2两个字段是添加好友需要的信息，假如两个都返回Null,则代表
{% endhint %}

