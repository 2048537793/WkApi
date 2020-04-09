---
description: 修改标签
---

# 修改标签

**简要描述：**

* 修改某好友标签

**请求URL：**

* `http://localhost:18081/modifyContactLabel`

**请求方式：**

* POST

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| wId | 是 | string | 微信实例ID |
| userName | 是 | string | 用户wcId |
| labelIdList | 是 | string | 用户标签，用逗号分隔，如"14,1" |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |
| data |  |  |

**请求参数示例**

```text
{
    "wId": "0000016e-f8b1-3e1b-0004-4cbf87535542",
    "userName":"wxid_lr6j4nononb921",
    "labelIdList":"3"

}
```

**成功返回示例**

```text
{
    "message": "成功",
    "code": "1000",
    "data": "修改成功"
}
```

**错误返回示例**

```text
{
    "message": "失败",
    "code": "1001",
    "data": "修改失败"
}
```

