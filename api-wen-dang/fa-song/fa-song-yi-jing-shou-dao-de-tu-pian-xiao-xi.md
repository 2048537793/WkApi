---
description: 发送已经收到的图片消息
---

# 发送已经收到的图片消息

**简要描述：**

* 根据收到的xml信息发送图片消息

**请求URL：**

* `http://localhost:18081/sendRecvImage`

**请求方式：**

* POST

**请求头Headers：**

* Content-Type：application/json
* Authorization：Authorization值（登录获取二维码信息接口中返回的认证信息值）

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| wId | 是 | string | 微信实例ID |
| wcId | 是 | string | 微信号/群号 |
| content | 是 | string | xml图片内容 |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |

**请求参数示例**

```text
{
    "wId": "0000016f-4621-dde5-0002-390493cab4dc",
    "wcId": "zhongweiyu789",
    "content": "<?xml version=\"1.0\"?>\n<msg>\n\t<img aeskey=\"849481a442044ad3a3a8130c94d2b591\" encryver=\"0\" cdnthumbaeskey=\"849481a442044ad3a3a8130c94d2b591\" cdnthumburl=\"3053020100044c304a0201000204e7d9caed02032f55f90204900060b402045e05acc00425617570696d675f386634626639356134343465613063665f31353737343330323038303739020401053a010201000400\" cdnthumblength=\"3310\" cdnthumbheight=\"80\" cdnthumbwidth=\"120\" cdnmidheight=\"0\" cdnmidwidth=\"0\" cdnhdheight=\"0\" cdnhdwidth=\"0\" cdnmidimgurl=\"3053020100044c304a0201000204e7d9caed02032f55f90204900060b402045e05acc00425617570696d675f386634626639356134343465613063665f31353737343330323038303739020401053a010201000400\" length=\"19842\" cdnbigimgurl=\"3053020100044c304a0201000204e7d9caed02032f55f90204900060b402045e05acc00425617570696d675f386634626639356134343465613063665f31353737343330323038303739020401053a010201000400\" hdlength=\"99007\" md5=\"39fec3c8e1ebad09ef4289b9e712a716\" hevc_mid_size=\"13869\" />\n</msg>\n"
}
```

**成功返回示例**

```text
{
    "message": "发送成功",
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

