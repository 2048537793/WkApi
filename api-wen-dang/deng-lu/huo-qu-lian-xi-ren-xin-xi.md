# 获取联系人信息

**简要描述：**

* 获取联系人信息

**请求URL：**

* `http://域名地址/getContact`

**请求方式：**

* POST 

**请求头Headers：**

* Content-Type：application/json
* Authorization：login接口返回

**参数：**

<table>
  <thead>
    <tr>
      <th style="text-align:center">&#x53C2;&#x6570;&#x540D;</th>
      <th style="text-align:center">&#x5FC5;&#x9009;</th>
      <th style="text-align:center">&#x7C7B;&#x578B;</th>
      <th style="text-align:center">&#x8BF4;&#x660E;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:center">wId</td>
      <td style="text-align:center">&#x662F;</td>
      <td style="text-align:center">String</td>
      <td style="text-align:center">&#x5FAE;&#x4FE1;&#x5B9E;&#x4F8B;&#x6807;&#x8BC6;</td>
    </tr>
    <tr>
      <td style="text-align:center">wcId</td>
      <td style="text-align:center">&#x662F;</td>
      <td style="text-align:center">String</td>
      <td style="text-align:center">
        <p>&#x5FAE;&#x4FE1;&#x53F7;,&#x591A;&#x4E2A;&#x597D;&#x53CB;/&#x7FA4; &#x4EE5;&quot;,&quot;&#x5206;&#x9694;</p>
        <p>&#x6BCF;&#x6B21;&#x6700;&#x591A;&#x652F;&#x6301;20&#x4E2A;&#x5FAE;&#x4FE1;/&#x7FA4;&#x53F7;,</p>
        <p>&#x8BB0;&#x5F97;&#x672C;&#x63A5;&#x53E3;&#x968F;&#x673A;&#x95F4;&#x9694;1-3S&#xFF0C;&#x9891;&#x7E41;&#x8C03;&#x7528;&#x5BB9;&#x6613;&#x5BFC;&#x81F4;&#x6389;&#x7EBF;</p>
      </td>
    </tr>
  </tbody>
</table>

**请求参数示例**

```javascript
{
    "wId": "349be9b5-8734-45ce-811d-4e10ca568c67",
    "wcId": "LoChaX,wxid_wl9qchkanp9u22"
}
```

**成功返回示例**

```javascript
{
    "message": "成功",
    "code": "1000",
    "data": [
        {
            "userName": "test558666",
            "nickName": "追风少年666",
            "remark": "",
            "signature": "66666",
            "sex": 1,
            "aliasName": "test558666",
            "country": "CN",
            "bigHead": "http://wx.qlogo.cn/mmhead/PiajxSqBRaEL8iaRQBnStn37LYat3fREC4Y2iaStECzbX3icxntWBhWQ3w/0",
            "smallHead": "http://wx.qlogo.cn/mmhead/PiajxSqBRaEL8iaRQBnStn37LYat3fREC4Y2iaStECzbX3icxntWBhWQ3w/132",
            "labelList": "",
            "v1": "v1_584e7774024c79af0e7304bf7afba775b31bf075651c16c964b1b5bf16369924ebf1ee7bc151c1feee1979e1dd40f0dd@stranger"
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
| userName | String | 微信号 |
| nikeName | String | 昵称 |
| remark | String | 备注 |
| signature | String | 签名 |
| sex | int | 性别 |
| aliasName | String |  |
| country | String | 国家 |
| bigHead | String | 大头像 |
| smallHead | String | 小头像 |
| labelList | String | 标签列表 |
| v1 | String | 用户的wxId，都是以v1开头的一串数值，v2数据，则是作为v1数据的辅助 |

