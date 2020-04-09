---
description: 获取自己的二维码
---

# 获取自己的二维码

**简要描述：**

* 获取自己的二维码

**请求URL：**

* 开发者域名 +`/getQrCode`

**请求方式：**

* POST

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| wId | 是 | string | 微信实例ID |
| wcId | 是 | string | 微信号 |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |
| data |  |  |
| qrCodeUrl | string | 二维码图片URL |

**请求参数示例**

```text
{
    "wId": "0000016e-68f9-99d5-0002-3a1cd9eaaa17",
    "wcId": "zhongweiyu789"
}
```

**成功返回示例**

```text
{
    "message": "成功",
    "code": "1000",
    "data": {
        "qrCodeUrl": "http://127.0.0.1:18081/zhongweiyu789.png"
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

