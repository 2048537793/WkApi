---
description: 添加好友
---

# 添加好友

**简要描述：**

* 添加微信好友

**请求URL：**

* `http://localhost:18081/addUser`

**请求方式：**

* POST

**请求头Headers：**

* Content-Type：application/json
* Authorization：Authorization值（登录获取二维码信息接口中返回的认证信息值）

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
      <td style="text-align:left">v1</td>
      <td style="text-align:left">&#x662F;</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x4ECE;<a href="../qun-cao-zuo/huo-qu-wei-xin-qun-de-xin-xi.md">&#x641C;&#x7D22;&#x7528;&#x6237;&#x63A5;&#x53E3;</a>&#x83B7;&#x53D6;</td>
    </tr>
    <tr>
      <td style="text-align:left">v2</td>
      <td style="text-align:left">&#x662F;</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x4ECE;<a href="../qun-cao-zuo/huo-qu-wei-xin-qun-de-xin-xi.md">&#x641C;&#x7D22;&#x7528;&#x6237;&#x63A5;&#x53E3;</a>&#x83B7;&#x53D6;</td>
    </tr>
    <tr>
      <td style="text-align:left">type</td>
      <td style="text-align:left">&#x662F;</td>
      <td style="text-align:left">int</td>
      <td style="text-align:left">
        <p>&#x4F20;3&#x5373;&#x53EF;&#xFF0C;&#x6DFB;&#x52A0;&#x6765;&#x6E90;&#xFF1A;1-QQ&#x53F7;&#x641C;&#x7D22;&#xFF0C;3-&#x5FAE;&#x4FE1;&#x53F7;&#x641C;&#x7D22;&#xFF0C;</p>
        <p>4-QQ&#x597D;&#x53CB;&#xFF0C;8-&#x901A;&#x8FC7;&#x7FA4;&#x804A;&#xFF0C;12-&#x6765;&#x81EA;QQ&#x597D;&#x53CB;&#xFF0C;</p>
        <p>14-&#x901A;&#x8FC7;&#x7FA4;&#x804A;&#xFF0C;15-&#x624B;&#x673A;&#x53F7;</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">verify</td>
      <td style="text-align:left">&#x662F;</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x9A8C;&#x8BC1;&#x6D88;&#x606F;</td>
    </tr>
  </tbody>
</table>

**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |

**请求参数示例**

```text
{
   "wId": "0000016f-a2f0-03e3-0003-65e826091614",
   "v1": "v1_aaf94e13d0058cdc888e388b98952e0fc23212d180e4dacb38b96dfe4b078c488e72772f907517470ac0b9b7311826da@stranger",
   "v2": "v2_13ced007472228cd1545feecf78b99f9a57a88843374513747afc7ac25d8a4cccb77590b7a9b01a96c941e047d137bbb@stranger",
   "type": 3,
   "verify": ""

}
```

**成功返回示例**

```text
{
    "message": "成功",
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

{% hint style="danger" %}

{% endhint %}

