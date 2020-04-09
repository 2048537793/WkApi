---
description: 搜索 微信群/好友 的信息
---

# 搜索 微信群/好友 的信息

**简要描述：**

* 获取某个群的详细信息
* 获取某个微信号的详细信息（支持wxId开头）

{% hint style="info" %}
假如本接口的v2字段返回null，则添加好友时，v1、v2都填写此接口返回的v1的值。
{% endhint %}

**请求URL：**

* `http://localhost:18081/getContactFromServer`

**请求方式：**

* POST

**参数：**

<table>
  <thead>
    <tr>
      <th style="text-align:left">&#x53C2;&#x6570;&#x540D;</th>
      <th style="text-align:left">&#x5FC5;&#x9009;</th>
      <th style="text-align:left">&#x7C7B;&#x578B;</th>
      <th style="text-align:left">&#x8BF4;&#x660E;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">wId</td>
      <td style="text-align:left">&#x662F;</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x5FAE;&#x4FE1;&#x5B9E;&#x4F8B;ID</td>
    </tr>
    <tr>
      <td style="text-align:left">wcId</td>
      <td style="text-align:left">&#x662F;</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x7FA4;&#x53F7;/&#x5FAE;&#x4FE1;&#x53F7;</td>
    </tr>
    <tr>
      <td style="text-align:left">chatroom</td>
      <td style="text-align:left">&#x5426;</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <p>&#x7FA4;&#x53F7;&#xFF08;PS&#xFF1A;&#x67E5;&#x8BE2;&#x7FA4;&#x6210;&#x5458;&#x65F6;&#x4F20;&#x5165;&#xFF0C;</p>
        <p>&#x67E5;&#x8BE2;&#x7FA4;&#x8BE6;&#x60C5;&#x5219;&#x5FFD;&#x7565;&#x6B64;&#x5B57;&#x6BB5;&#xFF09;</p>
      </td>
    </tr>
  </tbody>
</table>**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |
| data |  |  |
| userName | string | 微信号 |
| aliasName | string | 别名微信号 |
| nickName | string | 昵称 |
| bigHead | string | 头像 |
| smallHead | string | 头像（缩略图） |
| sex | string | 性别（0：群；1：男；2：女） |
| remark | string | 备注 |
| signature | string | 签名 |
| description | string | 描述 |
| country | string | 国家 |
| province | string | 省份 |
| city | string | 城市 |
| v1 | string | v1 添加好友时专用 |
| v2 | string | v2 添加好友时专用 为Null代表已是好友 |
| labelIDList | string | labelIDList |
| chatRoomOwner | string | 群主微信号 |
| chatRoomData | string | chatRoomData |
| roomInfoList |  |  |
| userName | string | 微信号 |
| nickName | string | 昵称 |
| displayName | string | 群昵称 |
| smallHeadImgUrl | string | smallHeadImgUrl |
| inviteUser | string | 邀请人 |

**请求参数示例**

```text
{
    "wId": "00000170-4dc3-d7b2-000d-9486e0ae948d",
    "wcId": "wxid_i6qsbbjenjuj22",
    "chatroom": "24027551681@chatroom"
}
```

**成功返回示例**

```text
{
    "message": "成功",
    "code": "1000",
    "data": {
        "userName": "wxid_i6qsbbjenjuj22",
        "aliasName": "LoChaX",
        "nickName": "微控Team_Mr Li",
        "bigHead": "http://wx.qlogo.cn/mmhead/ver_1/Cib9CmPuphltlY9fZc3b7HQy2TUywQl6UBFicSXyMSdK6UmRiaXro3mad5ycaDgonkUGeH8hCfiaowdrIz5Tb9dl1vZGiaLu20iawF6vWibMW8vib7E/0",
        "smallHead": "http://wx.qlogo.cn/mmhead/ver_1/Cib9CmPuphltlY9fZc3b7HQy2TUywQl6UBFicSXyMSdK6UmRiaXro3mad5ycaDgonkUGeH8hCfiaowdrIz5Tb9dl1vZGiaLu20iawF6vWibMW8vib7E/132",
        "sex": 1,
        "type": 3,
        "signature": "微控Api商业合作对接，提供ipad协议，mac协议，微信sdk",
        "remark": null,
        "description": null,
        "country": "CN",
        "province": "Jiangsu",
        "city": "Nanjing",
        "v1": "v1_690eba1ba80ba5365ebd7a0bde5fe8073e71599f8389a056f31a0f8c04f34bfa06e1f795c39a4b0fce65c9b4328f37b6@stranger",
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

