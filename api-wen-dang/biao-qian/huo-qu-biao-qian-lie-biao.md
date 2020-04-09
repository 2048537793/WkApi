---
description: 获取标签列表
---

# 获取标签列表

**简要描述：**

* 获取标签列表

**请求URL：**

* `http://localhost:18081/getContactLabelList`

**请求方式：**

* POST

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| wId | 是 | string | 微信实例ID |

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
    "wId": "0000016e-afaf-2169-0003-14037ae9f96f"
}
```

**成功返回示例**

```text
{
    "message": "成功",
    "code": "1000",
    "data": [
        {
            "labelName": "喜欢许巍的朋友",
            "labelId": 1
        },
        {
            "labelName": "看一看世界",
            "labelId": 3
        },
        {
            "labelName": "特别",
            "labelId": 2
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

