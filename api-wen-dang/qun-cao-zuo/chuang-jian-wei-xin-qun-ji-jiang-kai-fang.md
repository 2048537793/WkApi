---
description: 创建微信群
---

# 创建微信群

**简要描述：**

* 创建微信群

**请求URL：**

* `http://localhost:18081/createChatroom`

**请求方式：**

* POST

**请求头Headers：**

* Content-Type：application/json
* Authorization：Authorization值（登录获取二维码信息接口中返回的认证信息值）

**创建后，如果返回结果中没有群头像，可以调用getContactFromServer获取群的详细信息。如果手机上没有显示该群，可以往该群主动发条消息。**

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| wId | 是 | string | 微信实例ID |
| topic | 是 | string | 群名称 |
| userNameList | 是 | string | 微信id列表，以逗号分隔（微信ID 从获取联系人列表接口取，friend字段下面的username） |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |

**请求参数示例**

```text
{
   "wId": "0000016f-a340-c2d7-0003-6ab83bc1e64a",
   "topic": "创建微信群-对外开放",
   "userNameList": "zhongweiyu789,wxid_lr6j4nononb921,wxid_ao4ziqc2g9b922"
}
```

**成功返回示例**

```text
{
    "message": "成功",
    "code": "1000",
    "data": {
        "roomName": "24086860353@chatroom",
        "topic": "chuangjianweixinqunduiwaikaifang",//手机上返回正确
        "bigHeadImgUrl": null
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

