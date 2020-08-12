---
description: 获取微信二维码（第二步）
---

# 获取微信二维码\(第二步）



**请求URL：**

* `http://域名地址/iPadLogin`

**请求方式：**

* POST JSON

**请求头Headers:（别忘了传）**

* Content-Type：application/json
* **Authorization：login接口返回 ！！！**

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
      <td style="text-align:left"><b><code>string</code></b>
      </td>
      <td style="text-align:left">
        <p><b><code>&#x767B;&#x5F55;&#x7684;&#x5FAE;&#x4FE1;id &#xFF08;&#x9996;&#x6B21;&#x626B;&#x7801;&#x4E0D;&#x9700;&#x8981;&#x4F20;&#xFF0C;&#x5386;&#x53F2;&#x626B;&#x7801;&#x5FC5;&#x987B;&#x4F20;&#xFF01;&#xFF01;&#xFF01;&#xFF01;&#x7528;&#x6765;&#x627E;&#x4E0A;&#x6B21;&#x767B;&#x5F55;&#x8BBE;&#x5907;&#xFF09;</code></b>
        </p>
        <p><a href="https://docs.wkteam.cn/api-wen-dang/kai-shi-kai-fa/untitled">&#x6267;&#x884C;&#x767B;&#x5F55;&#x63A5;&#x53E3;</a>&#x4F1A;&#x8FD4;&#x56DE;&#x6B64;&#x5B57;&#x6BB5;&#xFF0C;&#x8BB0;&#x5F97;&#x4FDD;&#x5B58;&#x6570;&#x636E;&#x5E93;&#x91CC;</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">type</td>
      <td style="text-align:left">&#x662F;</td>
      <td style="text-align:left">int</td>
      <td style="text-align:left">&#x767B;&#x9646;&#x65B9;&#x5F0F;&#xFF0C;&#x4F20;2&#x5373;&#x53EF;</td>
    </tr>
    <tr>
      <td style="text-align:left">proxy</td>
      <td style="text-align:left">&#x5426;</td>
      <td style="text-align:left">int</td>
      <td style="text-align:left">&#x4EE3;&#x7406;IP&#x901A;&#x9053;&#xFF1A;1:&#x5E7F;&#x5DDE; 2: &#x5357;&#x4EAC;
        3:&#x676D;&#x5DDE; 4:&#x4E0A;&#x6D77; 5:&#x6DF1;&#x5733;&#xFF08;&#x5EFA;&#x8BAE;&#x5F00;&#x53D1;&#x8005;&#x968F;&#x610F;&#x9009;&#x62E9;&#x4E00;&#x4E2A;&#x767B;&#x5F55;&#x901A;&#x9053;&#x5373;&#x53EF;&#xFF09;</td>
    </tr>
  </tbody>
</table>

**返回数据：**

| 参数名 | 类型 | 说明 |  |
| :--- | :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |  |
| msg | string | 反馈信息 |  |
| data |  |  |  |
| wId | string | 微信实例ID  **（本值非固定的，每次重新扫码登录会返回新的，数据库记得实时更新wid）** |  |
| qrCodeUrl | string | 扫码登录地址 |  |

{% hint style="danger" %}
* 调用本接口得到二维码图片地址
* 调用[执行登录接口](https://docs.wkteam.cn/api-wen-dang/kai-shi-kai-fa/untitled)（第三步）（**此时第三步的接口不会立即返回，是根据用户是否扫码返回数据，最长等待150S**）
* 开发者将本接口**返回的二维码让用户去扫码**
* **扫码结束后，方才的**[**执行登录接口**](https://docs.wkteam.cn/api-wen-dang/kai-shi-kai-fa/untitled)**会返回登录成功或者登录失败**
* 注意：请求所有**接口**需在**header包裹Authorization\(必须\)**
{% endhint %}

**请求参数示例**

```javascript
{
    "wcId": "wxid_wl9qchkanp9u22",
    "type": 2,
    "proxy":1
}
```

**成功返回示例**

```javascript
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

```javascript
{
    "message": "用户名或密码错误",
    "code": "1001",
    "data": null
}
```

