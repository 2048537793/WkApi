---
description: 登录微控平台（第一步）
---

# 登录微控平台（第一步）

**请求URL：**

* **`http://域名地址/member/login`**
* **`域名地址：http://xingshenwk.com/（后续所有接口记得替换）`**

**请求方式：**

* POST

**请求头Headers：**

* Content-Type：application/json

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| account | 是 | string | **开发者**账号 |
| password | 是 | string | 开发者密码 |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |
| data |  |  |
| Authorization | string | 认证信息 |
| name | string | 个人或企业名称 |
| account | string | 账号 |
| overdueTime | lonhg | 逾期时间 |
| createTime | lonhg | 创建时间 |
| modifyTime | lonhg | 修改时间 |
| lastTime | lonhg | 最近登录时间 |
| availableNumber | int | 可用数 |
| callbackType | string | 回调类型\(0: websocket 1：HTTP\) |
| callbackUrl | string | HTTP回调地址 |
| status | string | 状态（0：正常，1：冻结，2：到期） |

{% hint style="info" %}
**此接口调用一次即可，Authorization认证信息正常情况下永不失效**

**（除非调用退出微控平台、账户到期等）**
{% endhint %}

**请求参数示例**

```javascript
{    
   "account": "18013350963",
   "password": "123456"
}
```

**成功返回示例**

```javascript
{
    "message": "成功",
    "code": "1000",
    "data": {

        "name": "测试开通用户",
        "account": "18013350963",
        "accountType": 0,
        "overdueTime": 1584771600000,
        "createTime": 1582265588294,
        "modifyTime": 1582270031136,
        "lastTime": 1582526037880,
        "availableNumber": 1,
        "callbackType": 0,
        "callbackUrl": null,
        "status": 0,
        "wcIds": null,
        "Authorization": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJwYXNzd29yZCI6ImUxMGFkYzM5NDliYTU5YWJiZTU2ZTA1N2YyMGY4ODNlYXZ1cHE9SGNTNXQwKGJvJiIsImlzcyI6InhpbmdzaGVuZyIsImFjY291bnQiOiIxMjM0NTY3ODkxMCJ9.x9bT9wDPAwGhJg7rTo0k4I0FlteKqK4AW7G9FsANgce"
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

