---
description: 添加企业微信群
---

# 添加企业微信群

**简要描述：**

* 添加企业微信群

**请求URL：**

* `http://localhost:18081/createOpenIMChatroom`

**请求方式：**

* POST

**请求头Headers：**

* Content-Type：application/json
* Authorization：Authorization值（登录获取二维码信息接口中返回的认证信息值）

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| wId | 是 | string | 微信实例ID |
| userNameList | 是 | string | 用户id列表，id可以是微信id，也可以是企业微信id，以逗号分隔，如wxid\_iftgtj85hbcv21,25984985187689167@openim |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |
| data |  |  |
| roomName | String | roomName |
| topic | String | topic |
| bigHeadImgUrl | string | bigHeadImgUrl |

**请求参数示例**

```text
{
    "wId": "0000016e-f8b1-3e1b-0004-4cbf87535542",
     "userNameList":"wxid_iftgtj85hbcv21"

}
```

**成功返回示例**

```text
{
    "message": "成功",
    "code": "1000",
    "data": {
        "roomName": "test",
    "topic": "test",
    "bigHeadImgUrl": "test"
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

