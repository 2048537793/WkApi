---
description: 初始化好友列表
---

# 初始化通讯录列表

{% hint style="info" %}
**获取通讯录列表之前必须调用此接口。**
{% endhint %}

**请求URL：**

* `http://域名地址/initAddressList`

**请求方式：**

* POST 

**请求头Headers：**

* Content-Type：application/json
* Authorization：login接口返回

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :---: | :---: | :---: | :---: |
| wId | 是 | String | 微信实例标识 |

**请求参数示例**

```javascript
{
    "wId": "6a696578-16ea-4edc-ac8b-e609bca39c69"
}
```

**成功返回示例**

```javascript
{
    "code": "1000",
    "message": "初始化通讯录成功",
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

**返回数据：**

| 参数名 | 类型 | 说明 |
| :---: | :---: | :---: |
| code | int | 1000成功、10001失败 |
| msg | string | 反馈信息 |
| data | JSONObject | 无 |

