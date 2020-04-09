---
description: 添加标签
---

# 添加标签

**简要描述：**

* 添加标签

**请求URL：**

* `http://localhost:18081/addContactLabel`

**请求方式：**

* POST

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| wId | 是 | string | 微信实例ID |
| labelName | 是 | string | 标签名 |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |
| data |  |  |
| labelId | int | 标签ID |
| labelName | string | 标签名 |

**请求参数示例**

```text
{
    "wId": "0000016e-afaf-2169-0003-14037ae9f96f"，
    "labelName": "新标签"
}
```

**成功返回示例**

```text
{
    "message": "成功",
    "code": "1000",
    "data": [
        {
            "labelName": "新标签",
            "labelId": 3
        }
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

