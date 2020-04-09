---
description: 朋友圈评论
---

# 朋友圈评论

**简要描述：**

* 朋友圈评论

**请求URL：**

* `http://localhost:18081/snsComment`

**请求方式：**

* POST

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| wId | 是 | string | 微信实例ID |
| wcId | 是 | string | 好友微信号（一定传wx\_开头的，不知道的可以调用[获取联系人列表](../kai-shi-kai-fa/huo-qu-yong-hu-ji-ben-xin-xi.md)取） |
| sns | 是 | string | 朋友圈ID |
| content | 是 | string | 内容 |

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
    "sns": "13205404970681503871",
    "content": "充满力量"
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

