---
description: 获取某个标签好友列表
---

# 获取某个标签好友列表

**简要描述：**

* 获取标签列表

**请求URL：**

* `http://localhost:18081/getLabelContacts`

**请求方式：**

* POST

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| wId | 是 | string | 微信实例ID |
| labelId | 是 | string | 标签ID |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |
| data | jsonArray | 微信号数组列表 |

**请求参数示例**

```text
{
    "wId": "0000016e-afaf-2169-0003-14037ae9f96f",
    "labelId": 12
}
```

**成功返回示例**

```text
{
    "message": "成功",
    "code": "1000",
    "data": [
        "wxid_znokudqcgvnr22",
        "LoChaX"
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

