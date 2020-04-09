---
description: 获取微信二维码（第二步）
---

# 获取微信二维码（第二步）

### **简要描述：**

* 信息验证并获取登录二维码

**请求URL：**

* `http://localhost:18081/iPadLogin`

**请求方式：**

* POST

**请求头Headers:（别忘了传）**

* Content-Type：application/json
* **Authorization：login接口返回**

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
      <td style="text-align:left">wcId</td>
      <td style="text-align:left">&#x5426;</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <p>&#x767B;&#x5F55;&#x7684;&#x5FAE;&#x4FE1;id&#xFF08;&#x9996;&#x6B21;&#x767B;&#x5F55;&#x4E0D;&#x9700;&#x8981;&#x4F20;&#xFF0C;&#x5386;&#x53F2;&#x767B;&#x5F55;<b>&#x5FC5;&#x987B;&#x4F20;</b>&#xFF09;</p>
        <p><a href="untitled.md">&#x6267;&#x884C;&#x767B;&#x5F55;&#x63A5;&#x53E3;</a>&#x8FD4;&#x56DE;&#x6B64;&#x5B57;&#x6BB5;&#xFF0C;&#x8BB0;&#x5F97;&#x4FDD;&#x5B58;&#x6570;&#x636E;&#x5E93;&#x91CC;</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">type</td>
      <td style="text-align:left">&#x662F;</td>
      <td style="text-align:left">int</td>
      <td style="text-align:left">&#x767B;&#x9646;&#x65B9;&#x5F0F;&#xFF0C;&#x4F20;2&#x54E6;</td>
    </tr>
  </tbody>
</table>**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |
| data |  |  |
| wId | string | 微信实例ID |
| qrCodeUrl | string | 扫码登录地址 |

**请求参数示例**

```text
{
    "wcId": "wxid_wl9qchkanp9u22",
    "type": 2
}
```

**成功返回示例**

```text
{
    "message": "登录成功",
    "code": "1000",
    "data": {
        "wId": "0000016e-63ef-3a9c-0001-ed3311628ef4",
        "qrCodeUrl": "http://127.0.0.1:18081/1573634652963-500000.png"
    }
}
```

**错误返回示例**

```text
{
    "message": "用户名或密码错误",
    "code": "1001",
    "data": null
}
```

{% hint style="danger" %}
  
~~~~**登录完整步骤：** 

**1.调用**本接口得到二维码图片地址

2.调用执行登录接口（此时接口不会返回，是根据用户是否扫码返回数据，最长等待150S） 

3. 开发者将本接口返回的二维码让用户去扫码

4.扫码结束后，方才的执行登录接口会自动返回登录成功或者登录失败

注意：请求所有**接口**需在**header包裹Authorization\(必须\)**
{% endhint %}



