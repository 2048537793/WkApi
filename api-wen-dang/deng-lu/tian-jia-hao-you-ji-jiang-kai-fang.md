---
description: 添加好友
---

# 添加好友

**简要描述：**

* 添加微信好友

**请求URL：**

* `http://域名地址/addUser`

**请求方式：**

* POST 

**请求头Headers：**

* Content-Type：application/json
* Authorization：login接口返回

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :---: | :---: | :---: | :---: |
| wId | 是 | string | 微信实例ID |
| v1 | 是 | string | v1 从[搜索好友接口](cha-zhao-yong-hu-ji-jiang-kai-fang.md)获取 |
| v2 | 是 | string | v2 从[搜索好友接口](cha-zhao-yong-hu-ji-jiang-kai-fang.md)获取 |
| type | 是 | int | 添加来源  1 ：QQ号搜索   3 ：微信号搜索  4 ：QQ好友  8 ：通过群聊  12 ：来自QQ好友  14 ：通过群聊  15 ：手机号 |
| verify | 是 | String | 验证消息 |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :---: | :---: | :---: |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |

**请求参数示例**

```javascript
{
   "wId": "0000016f-a2f0-03e3-0003-65e826091614",
   "v1": "v1_aaf94e13d0058cdc888e388b98952e0fc23212d180e4dacb38b96dfe4b078c488e72772f907517470ac0b9b7311826da@stranger",
   "v2": "v2_13ced007472228cd1545feecf78b99f9a57a88843374513747afc7ac25d8a4cccb77590b7a9b01a96c941e047d137bbb@stranger",
   "type": 3,
   "verify": ""

}
```

**成功返回示例**

```javascript
{
    "message": "成功",
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

