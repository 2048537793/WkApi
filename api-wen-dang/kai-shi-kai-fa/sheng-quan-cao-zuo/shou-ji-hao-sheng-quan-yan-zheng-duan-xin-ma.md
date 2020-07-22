# 手机号升权-验证短信码



{% hint style="info" %}
* **自2020年7月份以来，因真机设备集体降权，导致所有新号登录无法直接发送朋友圈，或者无法评论，需等待7天，此方式为升权操作，如若对朋友圈无过多要求无需调用此接口。**
* **本接口调用一次后，以后无需再次调用，每个微信号升权一次即可**
* **和**[**账号密码升权**](zhang-hao-mi-ma-sheng-quan-xuan-qi-1-ji-ke.md)**选择任何一种方式都可以**
{% endhint %}



**请求URL：**

* `http://域名地址/smsLoginConfirm`

**请求方式：**

* POST JSON

**请求头Headers:（别忘了传）**

* Content-Type：application/json
* **Authorization：login接口返回 ！！！**

**参数：**

| 参数名   | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| mobile | 是 | string | 微信绑定的手机号 |
| code | 是 | string | 短信验证码 |

**返回数据：**

| 参数名 | 类型 | 说明 |  |
| :--- | :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |  |
| message | string | 微信返回xml |  |
| data | string | null |  |

{% hint style="danger" %}
* **此接口需要post多次，**
* **第一次post** -&gt; 返回xml包含安全验证，里面有url  web网页打开，根据提示验证，可选择扫码登录 扫码完成且授权完成后，继续Post。
* **第二次Post-**》返回成功，手机号10S左右收到短信验证码，[然后执行验证接口](shou-ji-hao-sheng-quan-yan-zheng-duan-xin-ma.md)
{% endhint %}

\*\*\*\*

**请求参数示例**

```javascript
{
    "mobile": "18021211213"
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

