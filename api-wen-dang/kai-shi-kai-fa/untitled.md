---
description: 执行微信登录（第三步）
---

# 执行微信登录（第三步）

**请求URL：**

* `http://域名地址/getIPadLoginInfo`

**请求方式：**

* POST

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| wId | 是 | string | 微信实例ID |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :---: | :---: | :---: |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |
| data |  |  |
| wcId | string | 微信号 |
| nickName | string | 昵称 |
| headUrl | string | 头像url |
| wAccount | string | 手机上显示的微信号 |
| sex | int | 性别 |
| status | string | 状态: 0已失效、1等待扫码、2扫码待确定、3扫码登录成功 |

**请求参数示例**

```javascript
{
    "wId": "0000016e-63eb-f319-0001-ed01076abf1f"
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
    "message": "失败",
    "code": "1001",
    "data": null
}
```

{% hint style="danger" %}
* 别忘了**header**传**Authorization字段哦**
* **此步骤成功后手机上会显示mac登录成功，才可以收发消息及调用其它接口！**
{% endhint %}

