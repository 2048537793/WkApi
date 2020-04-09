---
description: 下载图片
---

# 下载图片

**简要描述：**

* 下载消息中的图片

**请求URL：**

* `http://localhost:18081/getMsgImg`

**请求方式：**

* POST

**请求头Headers：**

* Content-Type：application/json
* Authorization：Authorization值（登录获取二维码信息接口中返回的认证信息值）

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| wId | 是 | string | 微信实例ID |
| msgId | 是 | string | 消息id |
| fromUser | 是 | string | 发送人的微信号 |
| toUser | 是 | string | 接收人的微信号 |
| content | 是 | string | 收到的消息的xml数据 |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |

**请求参数示例**

```text
{
    "wId": "00000171-0504-4e11-0005-89183b61f7e4",
    "msgId": 1114390854,
    "fromUser": "wxid_i6qsbbjenjuj22",
    "toUser": "wxid_wl9qchkanp9u22",
  	"content": "<?xml version=\"1.0\"?>\n<msg>\n\t<img aeskey=\"cf4e4e8e30ce96543c5e1a025929b026\" encryver=\"0\" cdnthumbaeskey=\"cf4e4e8e30ce96543c5e1a025929b026\" cdnthumburl=\"30580201000451304f0201000204ced8878302032f55f90204b80260b402045e7815f4042a777875706c6f61645f777869645f776c397163686b616e70397532323238305f313538343932383234340204010438010201000400\" cdnthumblength=\"5376\" cdnthumbheight=\"80\" cdnthumbwidth=\"120\" cdnmidheight=\"0\" cdnmidwidth=\"0\" cdnhdheight=\"0\" cdnhdwidth=\"0\" cdnmidimgurl=\"30580201000451304f0201000204ced8878302032f55f90204b80260b402045e7815f4042a777875706c6f61645f777869645f776c397163686b616e70397532323238305f313538343932383234340204010438010201000400\" length=\"428753\" cdnbigimgurl=\"30580201000451304f0201000204ced8878302032f55f90204b80260b402045e7815f4042a777875706c6f61645f777869645f776c397163686b616e70397532323238305f313538343932383234340204010438010201000400\" hdlength=\"7706923\" md5=\"f97298b06aba35c3f4d3c74c39f92a51\" />\n</msg>\n"
}
```

**成功返回示例**

```text
{
    "message": "成功",
    "code": "1000",
    "data": "https://weikong-1301028514.cos.ap-shanghai.myqcloud.com//msgImg/05e18a08-956a-427b-ba1f-461cb047ecd8-1584928377894.png"
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

