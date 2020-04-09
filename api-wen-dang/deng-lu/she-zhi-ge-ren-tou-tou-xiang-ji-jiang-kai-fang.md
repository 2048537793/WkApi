---
description: 设置个人头头像
---

# 设置个人头头像

**简要描述：**

* 设置个人头像

**请求URL：**

* `http://localhost:18081/sendHeadImage`

**请求方式：**

* POST

**请求头Headers：**

* Content-Type：application/json
* Authorization：Authorization值（登录获取二维码信息接口中返回的认证信息值）

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| wId | 是 | string | 微信实例ID |
| path | 是 | string | 图片url链接 |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |

**请求参数示例**

```text
{
   "wId": "0000016f-a2cb-9a5c-0003-63bc8acbec08",
   "path": "https://xc-1300726975.cos.ap-shanghai.myqcloud.com/timg.jpg"

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

{% hint style="info" %}
**生效需等待10秒~1分钟，点头像即可查看**
{% endhint %}

