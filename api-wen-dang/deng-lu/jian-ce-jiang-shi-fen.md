---
description: 检测僵尸粉
---

# 检测僵尸粉

**简要描述：**

* 检测僵尸粉

**请求URL：**

* `http://localhost:18081/checkZombie`

**请求方式：**

* POST

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| wId | 是 | string | 微信实例ID |
| wcId | 是 | string | 检测微信号 |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |
| data |  |  |
| int | string | 1:僵尸粉 |

**请求参数示例**

```text
{
    "wId": "0000016e-afaf-2169-0003-14037ae9f96f",
    "wcId": "wzc199198"
}
```

**成功返回示例**

```text
{
    "message": "成功",
    "code": "1000",
    "data": {
        "status": 1
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

