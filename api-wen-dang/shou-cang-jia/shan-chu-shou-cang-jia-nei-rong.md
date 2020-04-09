---
description: 删除收藏夹内容
---

# 删除收藏夹内容

**简要描述：**

* 获取收藏夹内容

**请求URL：**

* `http://localhost:18081/weChatFavorites/delFavItem`

**请求方式：**

* POST

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| wId | 是 | String | 微信实列ID |
| favId | 是 | int | 收藏标识 |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |
| data |  |  |

**请求参数示例**

```text
{
    "wId": "0000016e-c561-9bbd-0001-3dc796084901",
    "favId":1
}
```

**成功返回示例**

```text
{
    "message": "成功",
    "code": "1000",
    "data": "收藏删除成功"
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

