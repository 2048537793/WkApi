---
description: ！
---

# 查询账号下已登录的微信号

**简要描述：**

* 查看本账号已登录的微信号

**请求URL：**

* `http://localhost:18081/member/getLoginWcIds`

**请求方式：**

* POST

**请求头Headers：**

* Content-Type：application/json
* Authorization：login接口返回

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| account | 是 | string | 账号 |
| password | 是 | string | 密码 |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |
| data |  |  |

**成功返回示例**

```text
{
    "message": "成功",
    "code": "1000",
    "data": [
        "wxid_wl9qchkanp9u22"
    ]
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

