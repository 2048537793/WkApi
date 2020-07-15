---
description: 此接口会将所有在本系统登录的微信号下线！！！
---

# 退出微控平台

{% hint style="info" %}
* 此接口会将所有在本系统登录的微信号下线！！！
* 此接口也会导致Authorization失效，需要调用登录微控平台
{% endhint %}

**简要描述：**

* 退出登录

**请求URL：**

* `http://localhost:18081/member/logout`

**请求方式：**

* POST

**请求头Headers：**

* Content-Type：application/json
* Authorization：l**ogin接口返回**

**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |
| data |  |  |

```text
 **成功返回示例**

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

