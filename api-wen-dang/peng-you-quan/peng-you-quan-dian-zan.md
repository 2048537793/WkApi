---
description: 朋友圈点赞
---

# 朋友圈点赞

**简要描述：**

* 朋友圈点赞

**请求URL：**

* `http://localhost:18081/snsPraise`

**请求方式：**

* POST

**请求头Headers：**

* Content-Type：application/json
* Authorization：login接口返回

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| wId | 是 | string | 微信实例ID |
| wcId | 是 | string | 微信号 |
| sns | 是 | string | 朋友圈ID |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |

**请求参数示例**

```text
{
    "wId": "0000016e-abcd-0ea8-0002-d8c2dfdb0bf3",
    "wcId": "zhongweiyu789",
    "sns": "13205404970681503871"
}
```

**成功返回示例**

```text
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

