---
description: 获取群二维码
---

# 获取群二维码

**简要描述：**

* 获取群二维码

**请求URL：**

* `http://localhost:18081/getGroupQrCode`

**请求方式：**

* POST

**请求头Headers：**

* Content-Type：application/json
* Authorization：login接口返回

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| wId | 是 | string | 微信实例ID |
| wcId | 是 | string | 群id |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |

**请求参数示例**

```text
{
   "wId": "0000016f-a340-c2d7-0003-6ab83bc1e64a",
   "wcId": "22270365143@chatroom"
}
```

**成功返回示例**

```text
{
    "message": "成功",
    "code": "1000",
    "data": {
        "groupQrCodeUrl": "https://xc-1300726975.cos.ap-shanghai.myqcloud.com/groupQrcode/21923674740@chatroom-1582614820960.png"
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

