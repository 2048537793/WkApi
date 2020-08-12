# 账号密码登录

{% hint style="info" %}
* **自2020年7月份以来，因扫码登录集体降权，导致所有新号登录无法直接评论，需等待7天，此方式为账号密码登录，如若对朋友圈无过多要求无需调用此接口，用扫码登录即可。**
* **本接口调用后，会挤掉手机登录，请注意！！！**
{% endhint %}

**请求URL：**

* `http://域名地址/wxAccountLogin`

**请求方式：**

* POST JSON

**请求头Headers:（别忘了传）**

* Content-Type：application/json
* **Authorization：login接口返回 ！！！**

**参数：**

| 参数名   | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| wxAccount | 是 | string | 微信账号 |
| wxPassword | 是 | string | 微信密码 |
| wcId | 否 | string | 登录的微信id （首次登录不需要传，历史登录必须传，用来找上次登录设备的） |

**返回数据：**

| 参数名 | 类型 | 说明 |  |
| :--- | :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |  |
| message | string | 微信返回xml |  |
| data | string | null |  |

{% hint style="danger" %}
* **此接口需要post多次，**
* **第一次post** -&gt; 返回xml里面有url  web网页打开，根据提示滑块，滑块完成后，界面卡住，无需多管，继续Post
* **第二次Post-**》返回xml里面url是二维码，手机需扫码确认登录
* **第三次Post-》**返回成功，此刻手机微信已退出，用户**需手机再次登录手机微信，**[**调用**获取微信二维码接口并且必须传w](huo-qu-token.md)Id扫码成功后，[执行第三步](untitled.md)，然后返回JSON里type返回2则是升权成功
{% endhint %}

**请求参数示例**

```javascript
{
    "wxAccount": "18021211213",
    "wxPassword":"CCQWQEQE"
}
```

#### **成功返回示例** 

```http
{
    "code": "1001",
    "message": "<e>\n<ShowType>8</ShowType>\n<Content><![CDATA[系统检测到环境存在异常，为了你的帐号安全， 请轻触“确定”进行安全验证。]]></Content>\n<Url><![CDATA[https://weixin110.qq.com/security/readtemplate?t=x/x&wechat_real_lang=zh_CN&aid=x&clientype=1&lang=x&apptype=undefined&captype=7&x=1&secticket=x]]></Url>\n<DispSec>0</DispSec>\n<Title><![CDATA[]]></Title>\n<Action>1</Action>\n<DelayConnSec>0</DelayConnSec>\n<Countdown>0</Countdown>\n<Ok><![CDATA[]]></Ok>\n<Cancel><![CDATA[]]></Cancel>\n</e>\n",
    "data": null
}
```

#### 失败返回示例

```javascript
{
    "message": "用户名或密码错误",
    "code": "1001",
    "data": null
}
```

