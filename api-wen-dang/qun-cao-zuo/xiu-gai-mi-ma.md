---
description: 获取群成员
---

# 获取群成员列表

**简要描述：**

* 获取群成员

**请求URL：**

* `http://域名地址/getChatRoomMember`

**请求方式：**

* POST 

**请求头Headers：**

* Content-Type：application/json
* Authorization：login接口返回

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :---: | :---: | :---: | :---: |
| wId | 是 | String | 微信实例标识 |
| chatRoomId | 是 | String | 群号 |

**请求参数示例**

```javascript
{
    "wId": "349be9b5-8734-45ce-811d-4e10ca568c67",
    "chatRoomId": "24343869723@chatroom"
}
```

**成功返回示例**

```javascript
{
    "message": "成功",
    "code": "1000",
    "data": [
       {
    "message": "成功",
    "code": "1000",
    "data": [
        {
            "chatRoomId": "24343869723@chatroom",
            "userName": "wxid_wl9qchkanp9u22",
            "nickName": "微控通知小助手（机器人）",
            "chatRoomOwner": null,
            "bigHeadImgUrl": "http://wx.qlogo.cn/mmhead/ver_1/jmfWqHiaA0aUN4N5py9N1Xn5ciaYBiaicnbsrqngibwM8TbDmmicPhZmBt0Lm71u6ToHLHLwN1UKsxaKu7BYSycVCwiaalSJm6OVeadLcR1w7RLgUU/0",
            "smallHeadImgUrl": "http://wx.qlogo.cn/mmhead/ver_1/jmfWqHiaA0aUN4N5py9N1Xn5ciaYBiaicnbsrqngibwM8TbDmmicPhZmBt0Lm71u6ToHLHLwN1UKsxaKu7BYSycVCwiaalSJm6OVeadLcR1w7RLgUU/132",
            "v1": null,
            "memberCount": 0,
            "chatRoomMembers": null
        },
        {
            "chatRoomId": "24343869723@chatroom",
            "userName": "wxid_i6qsbbjenjuj22",
            "nickName": "微控Team_Mr Li",
            "chatRoomOwner": null,
            "bigHeadImgUrl": "http://wx.qlogo.cn/mmhead/ver_1/3zrHQmnoxM5QgibxXZVBEmN0njuGsz7Jvam47xn4XG2IkiaAshFpET1E5TstsmmicF2eFWS5aibeozibO2Kc5Uibxic0DSpibDqcEHEB4krlS7XPycY/0",
            "smallHeadImgUrl": "http://wx.qlogo.cn/mmhead/ver_1/3zrHQmnoxM5QgibxXZVBEmN0njuGsz7Jvam47xn4XG2IkiaAshFpET1E5TstsmmicF2eFWS5aibeozibO2Kc5Uibxic0DSpibDqcEHEB4krlS7XPycY/132",
            "v1": null,
            "memberCount": 0,
            "chatRoomMembers": null
        },
        {
            "chatRoomId": "24343869723@chatroom",
            "userName": "wxid_ylxtflcg0p8b22",
            "nickName": "售前客服-小诺 (工作日9:00-18:00)",
            "chatRoomOwner": null,
            "bigHeadImgUrl": "http://wx.qlogo.cn/mmhead/ver_1/V886f8JuVBzJowFajp1E77ibbHB2PtoL42Hg5aP0icC8uk65ouzI5HzicmK0iaLiaJDghoYDCwInI59Cibd1esic39UlHGI5OzEZiaQkCRyapia23rBg/0",
            "smallHeadImgUrl": "http://wx.qlogo.cn/mmhead/ver_1/V886f8JuVBzJowFajp1E77ibbHB2PtoL42Hg5aP0icC8uk65ouzI5HzicmK0iaLiaJDghoYDCwInI59Cibd1esic39UlHGI5OzEZiaQkCRyapia23rBg/132",
            "v1": null,
            "memberCount": 0,
            "chatRoomMembers": null
        }
    ]
}

    ]
}
```

**错误返回示例**

```javascript
{
    "message": "失败",
    "code": "1001",
    "data": null
}
```

**返回数据：**

| 参数名 | 类型 | 说明 |
| :---: | :---: | :---: |
| code | String | 1000成功  10001失败 |
| msg | String | 反馈信息 |
| data | JSONObject |  |
| chatRoomId | String | 群号 |
| userName | String | 群成员微信号 （假如需要手机上显示的微信号或更详细的信息，则需要再调用[获取群成员详情接口获取](https://www.wkteam.cn/api-wen-dang2/qun-cao-zuo/queryGroupMemberDetail.html)） |
| nickName | String | 群成员昵称 |
| bigHeadImgUrl | String | 大头像 |
| smallHeadImgUrl | String | 小头像 |
| chatRoomMemberFlag | int |  |

