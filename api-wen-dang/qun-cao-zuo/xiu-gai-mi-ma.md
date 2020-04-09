---
description: 获取群成员
---

# 获取群成员

**简要描述：**

* 获取群成员列表

**请求URL：**

* `http://localhost:18081/getChatRoomMember`

**请求方式：**

* POST

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| wId | 是 | string | 微信实例ID |
| wcId | 是 | string | 群微信号 |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |
| data |  |  |
| userName | String | 微信号 |
| nickName | String | 昵称 |
| displayName | String | 群昵称 |
| bigHeadImgUrl | String | 头像 |
| smallHeadImgUrl | String | 头像（缩略图） |
| inviteUser | String | 邀请人微信号 |

**请求参数示例**

```text
{
    "wId": "0000016e-6343-089e-0001-e2ef939176f6",
    "wcId": "23321854893@chatroom"
}
```

**成功返回示例**

```text
{
    "message": "成功",
    "code": "1000",
    "data": [
        {
            "userName": "wxid_o4g4lw3y8bvj12",
            "nickName": "飞飞飞",
            "displayName": null,
            "bigHeadImgUrl": "http://wx.qlogo.cn/mmhead/ver_1/Yic6yVibOib4ndwVGeic93u1cPZvtUibiclzQZiaaQSWLFBicNmtdHmMhfeFDkiaoEB6iaVlyPoK2Qp8pLA51UMbuAeORU2UcSmw79G9dibpDPTKRL4Eec/0",
            "smallHeadImgUrl": "http://wx.qlogo.cn/mmhead/ver_1/Yic6yVibOib4ndwVGeic93u1cPZvtUibiclzQZiaaQSWLFBicNmtdHmMhfeFDkiaoEB6iaVlyPoK2Qp8pLA51UMbuAeORU2UcSmw79G9dibpDPTKRL4Eec/132",
            "inviteUser": "wxid_6mq1pu8ngj3r22"
        },
        {
            "userName": "wxid_32g5el0eplju22",
            "nickName": "刘建宏",
            "displayName": null,
            "bigHeadImgUrl": "http://wx.qlogo.cn/mmhead/ver_1/AGdHfibweZiccfTNwPvyYoIjpr76XmNP6IqvcuW3ZY47Oj3BvtozFHklz3Dbrr1g1xOPHNVbhlS5ocjaYn2V2wTCOMWMxykBiclcgfN4LVeJDA/0",
            "smallHeadImgUrl": "http://wx.qlogo.cn/mmhead/ver_1/AGdHfibweZiccfTNwPvyYoIjpr76XmNP6IqvcuW3ZY47Oj3BvtozFHklz3Dbrr1g1xOPHNVbhlS5ocjaYn2V2wTCOMWMxykBiclcgfN4LVeJDA/132",
            "inviteUser": "wxid_6mq1pu8ngj3r22"
        },
        {
            "userName": "wxid_cf2r2mdypejh32",
            "nickName": "Gun🦑",
            "displayName": null,
            "bigHeadImgUrl": "http://wx.qlogo.cn/mmhead/ver_1/rIRpZ5WSDQuCs49sA6TicCatGu8MwdpnbAWqUk6CBg378jWAIXEAicaP2ias92dFcSlXPKE2Y9JpoDc3TAV6SuC8rXgEQrukicqiaVfvTbATyHN4/0",
            "smallHeadImgUrl": "http://wx.qlogo.cn/mmhead/ver_1/rIRpZ5WSDQuCs49sA6TicCatGu8MwdpnbAWqUk6CBg378jWAIXEAicaP2ias92dFcSlXPKE2Y9JpoDc3TAV6SuC8rXgEQrukicqiaVfvTbATyHN4/132",
            "inviteUser": "wxid_6mq1pu8ngj3r22"
        },
        {
            "userName": "wxid_6mq1pu8ngj3r22",
            "nickName": "为了更美好的明天而战",
            "displayName": null,
            "bigHeadImgUrl": "http://wx.qlogo.cn/mmhead/ver_1/8wIWia4DaMD9cf6gmmledibDOicW4FRI0LmicBOxHasH3JLcauD7CQX6dGXRC0XoMCoONzevicYFeMQcRVmYh1uPMxEnibDiagwCnQbPBcd0fdFT7s/0",
            "smallHeadImgUrl": "http://wx.qlogo.cn/mmhead/ver_1/8wIWia4DaMD9cf6gmmledibDOicW4FRI0LmicBOxHasH3JLcauD7CQX6dGXRC0XoMCoONzevicYFeMQcRVmYh1uPMxEnibDiagwCnQbPBcd0fdFT7s/132",
            "inviteUser": null
        }
    ]
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

