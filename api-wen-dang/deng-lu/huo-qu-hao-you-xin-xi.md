---
description: 获取好友信息
---

# 获取好友信息

**简要描述：**

* 获取某个好友的信息

**请求URL：**

* `http://localhost:18081/getContact`

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
| userName | string | 微信号 |
| aliasName | string | 别名 |
| nickName | string | 昵称 |
| bigHead | string | 头像 |
| smallHead | string | 头像（缩略图） |
| sex | string | 性别（1：男；2女） |
| remark | string | 备注 |
| signature | string | 签名 |
| description | string | 描述 |
| country | string | 国家 |

\|province \|string \| 省份 \| \|city \|string \| 城市 \| \|v1 \|string \| v1 \| \|v2 \|string \| v2 \|

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
        "userName": "zhongweiyu789",
        "aliasName": null,
        "nickName": "海上钢琴师",
        "bigHead": "http://wx.qlogo.cn/mmhead/ver_1/4wh9qm9VMiaavn6DBb6TlxzOfNHYxIRtk8y129miacAaPYRs2L8Jxziab4AIyiaoFnje2kzoArfFqRQopIzXT14Bfg/0",
        "smallHead": "http://wx.qlogo.cn/mmhead/ver_1/4wh9qm9VMiaavn6DBb6TlxzOfNHYxIRtk8y129miacAaPYRs2L8Jxziab4AIyiaoFnje2kzoArfFqRQopIzXT14Bfg/132",
        "sex": 1,
        "signature": "心存高远，脚踏实地",
        "remark": null,
        "description": null,
        "country": "中国",
        "province": "江苏",
        "city": "宿迁",
        "v1": null,
        "v2": null,
        "labelIDList": null,
        "chatRoomOwner": null,
        "chatRoomData": null,
        "roomInfoList": null
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

