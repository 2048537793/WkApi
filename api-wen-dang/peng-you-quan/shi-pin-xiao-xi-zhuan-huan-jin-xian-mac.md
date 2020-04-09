---
description: 视频消息转换
---

# 视频消息转换

### 获取视频消息 <a id="&#x83B7;&#x53D6;&#x89C6;&#x9891;&#x6D88;&#x606F;"></a>

**简要描述：**

* 获取视频消息

**请求URL：**

* `http://localhost:18081/getMsgVideo`

**请求方式：**

* POST

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| wId | 是 | string | 微信实例标识 |
| msgId | 是 | long | 消息标识 |
| content | 是 | string | 收到的消息的xml数据 |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |
| data |  |  |

**请求参数示例**

```text
{
    "wId": "0000016e-ed84-9156-0003-a23b4a6aa2ab",
    "msgId":1075988683,
    "content":"<?xml version=\"1.0\"?><msg><videomsg aeskey=\"4d3b5c9c9bc96d8190d64f11daf1cb35\" cdnthumbaeskey=\"4d3b5c9c9bc96d8190d64f11daf1cb35\" cdnvideourl=\"30570201000450304e020100020466883f5202032f55f90204250260b402045deefb8b0429777875706c6f61645f777869645f676961316e776367706f627a323231325f313537353934333034350204010400040201000400\" cdnthumburl=\"30570201000450304e020100020466883f5202032f55f90204250260b402045deefb8b0429777875706c6f61645f777869645f676961316e776367706f627a323231325f313537353934333034350204010400040201000400\" length=\"9336782\" playlength=\"60\" cdnthumblength=\"4742\" cdnthumbwidth=\"288\" cdnthumbheight=\"162\" fromusername=\"wxid_lr6j4nononb921\" md5=\"c73e25144f3f8c2c3a3c24cf17c91035\" newmd5=\"5e71e1a043c1fc423fddbe3c7660215d\" isad=\"0\" />/msg>"


}
```

**成功返回示例**

```text
{
    "message": "成功",
    "code": "1000",
    "data": "http://192.168.40.19:18081/26311a2e-c322-4cfe-93bb-c5a6c090c069-1575943436699.mp4"
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

