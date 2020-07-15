---
description: 获取微信二维码（第二步）
---

# 获取微信二维码（第二步）

**请求URL：**

* `http://域名地址/iPadLogin`

**请求方式：**

* POST

**请求头Headers:（别忘了传）**

* Content-Type：application/json
* **Authorization：login接口返回**

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| wcId | 否 | string | 登录的微信id （首次扫码不需要传，历史扫码必须传！！！用来找上次登录设备的）[执行登录接口](https://www.wkteam.cn/api-wen-dang2/deng-lu/zhi-xing-wei-xin-deng-lu.html)会返回此字段，记得保存数据库里 |
| type | 是 | int | 登陆方式，传2哦 |

**返回数据：**

| 参数名 | 类型 | 说明 |  |
| :--- | :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |  |
| msg | string | 反馈信息 |  |
| data |  |  |  |
| wId | string | 微信实例ID  **（本值非固定的，每次重新登录会返回新的，数据库记得实时更新wid）** |  |
| qrCodeUrl | string | 扫码登录地址 |  |

{% hint style="danger" %}
* 调用本接口得到二维码图片地址
* 调用执行登录接口（**此时接口不会返回，是根据用户是否扫码返回数据，最长等待150S**）
* 开发者将本接口**返回的二维码让用户去扫码**
* **扫码结束后，方才的执行登录接口会自动返回登录成功或者登录失败**
* 注意：请求所有**接口**需在**header包裹Authorization\(必须\)**
{% endhint %}

**请求参数示例**

```javascript
{
    "wcId": "wxid_wl9qchkanp9u22",
    "type": 2
}
```

**成功返回示例**

```javascript
{
    "message": "登录成功",
    "code": "1000",
    "data": {
        "wId": "0000016e-63ef-3a9c-0001-ed3311628ef4",
        "qrCodeUrl": "http://127.0.0.1:18081/1573634652963-500000.png"
    }
}
```

**错误返回示例**

```javascript
{
    "message": "用户名或密码错误",
    "code": "1001",
    "data": null
}
```

