---
description: 二次登录
---

# 二次登录

**请求URL：**

* `http://域名地址/secondLogin`

**请求方式：**

* POST JSON

**请求头Headers：**

* Content-Type：application/json
* Authorization：login接口返回

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :---: | :---: | :---: | :---: |
| wcId | 是 | string | 微信号（登录接口返回的wcId） |
| type | 否 | int | 登陆方式传2 |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :---: | :---: | :---: |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |
| data |  |  |
| wId | string | 登录实例id,  **登录成功后，必须替换成本wid，否则可能会引起各种问题** |
| wcId | string | 微信号 |
| nickName | string | 昵称 |
| headUrl | string | 头像url |
| wAccount | string | 手机上显示的微信号 |
| sex | int | 性别 |
| status | string | 3 扫码登录成功 |

**请求参数示例**

```javascript
{

 "wcId": "wxid_gia1nwcgpobz22",
 "type": 2
}
```

**成功返回示例**

```javascript
{
    "message": "成功",
    "code": "1000",
    "data": {
        "wcId": "wxid_ylxtflcg0p8b22",
        "wAccount": "hirsi520",
        "country": "CN",
        "wId": "c7fcd475-3c86-4061-ba95-aaae52bf9620",
        "city": "Nanjing",
        "signature": "微控客服对接，api 系统，大家有问题可以找我咨询呀",
        "nickName": "售前客服-小诺 (工作日9:00-18:00)",
        "sex": 2,
        "headUrl": "http://wx.qlogo.cn/mmhead/ver_1/71icIciaZ1RvFpIJUGp6pCI6Uydndbib74FyUY6pPrEKO1F4cVTgfx5QjnoShlGZamsMicOYWccSqUicZ1LsKtQjtr5icyQiau5aAiaLafMPo9e1vQU/0",
        "smallHeadImgUrl": "http://wx.qlogo.cn/mmhead/ver_1/71icIciaZ1RvFpIJUGp6pCI6Uydndbib74FyUY6pPrEKO1F4cVTgfx5QjnoShlGZamsMicOYWccSqUicZ1LsKtQjtr5icyQiau5aAiaLafMPo9e1vQU/132",
        "status": 3
    }
}
```

**错误返回示例**

```javascript
{
    "message": "系统失败,请重试",
    "code": "1001",
    "data": null
}

{
    "message": "成功",
    "code": "1000",
    "data": {
        "message": "二次登录失败，请重新扫码登录",
        "code": "1001",
        "data": null
    }
}
```

**接口意义：**

{% hint style="danger" %}
* **首次登录微控平台的微信号**调用[登录获取二维码](huo-qu-token.md)和[登录信息验证](untitled.md)接口即可，以后再次登录调用[二次登录接口](er-ci-deng-lu.md)（防封号，防掉线）
* 假如微信掉线或者手动下线后，直接调用此接口登录即可
* 不需要扫码，只需要手机**微信点击确认登录**就好，如下图所示
{% endhint %}



![  &#x793A;&#x4F8B;](../../.gitbook/assets/image%20%2821%29.png)

