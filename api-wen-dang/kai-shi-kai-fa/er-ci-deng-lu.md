---
description: 二次登录
---

# 二次登录

**说明：调用二次登录接口后，手机微信弹框确认。**

**简要描述：**

* 二次登录

**请求URL：**

* `http://localhost:18081/secondLogin`

**请求方式：**

* POST

**请求头Headers：**

* Content-Type：application/json
* Authorization：Authorization值（登录获取二维码信息接口中返回的认证信息值）

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| wcId | 是 | string | 微信号（[获取个人信息接口](../deng-lu/tui-chu-deng-lu.md)里返回） |
| type | 否 | int | 登陆方式传2 |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |
| data |  |  |
| wcId | string | 微信号 |
| wId | string | 微信实例ID |
| data | string |  |
| nickName | string | 微信昵称 |
| headUrl | string | 头像地址 |

**请求参数示例**

```text
{
 "wcId": "wxid_gia1nwcgpobz22",
 "type": 2
}
```

**成功返回示例**

```text
{
    "message": "二次登录成功",
    "code": "1000",
    "data": {
        "wcId": "wxid_wl9qchkanu22",
        "wId": "00000170-7a73-4d24-0010-3e5f2a8f7be0",
        "data": "AQnJmn+EQouHFDbuyEmXDN1MPWMAfJbVA7+Vfu3YXu2pSVJ/sPXR5DtwbEjJXIDHWbPjMhZ0rCp96e7XS5QPOa9GWiLv95UE5ic2mjFOQrqBVGiFoPx6loSKHfG4DPwWRjKjgL5Ti4U3SwkJc7RhXTJ18K+NV7UPSSWHjgcluTmM9MPKJ5bmpTGIArkHdq5M0XRSUP2+qUD3JfTqD3bEHsHDjCN8TaaeHc66JM7tJVX91uEjwaqf6U0gUsMjdGGvWEyr+JqhnsnvYZHSmumnO0edvwW7EoKOBmLJ1eglpKzeIw+1DkkTNyk9eIqp3hkZ/v0nUzq4Rq0505eObLjgWQivI7cpwrShYxTxo9ffJ5uc7e+aHzInbbCN6CO40klpGIDSzdqUAiQrgLkXI0p+4nd4ePLtWJTDWku2KQEvOg2j3DZDppmUtg6vqFlctbx9/V5PsHKzb4xDcJT5zz11KrXp4yeoUaxDtmgMk4xXKz+8ftLZNNmTK0EYGNxK+vA+3oz2sqrs6hVfwe8SZM8ecaesIEilznshDk8qm3rqn+GJ4XgqpImJl3yCxBcilboruT43zNoI5gGz8wIwOSys5Q==",
        "nickName": "微控Team",
        "headUrl": "http://wx.qlogo.cn//ver_1/uiaRoE4nXQFxib5H65NykkYsyc1icuyktg38ibAqlbSQOQibYhkCiaFpBOlXhiaibuWhccuopulzYFaSF0pFe2FLj8KDrc47p51OUfgw8NVEZJic8dAk/0",
        "status": 2,
        "token": "H7C6IwrQ5AyLSP0vFFGd8tg=="
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

{% hint style="danger" %}
**接口意义：**

* **首次登录微控平台的微信号**调用[登录获取二维码](huo-qu-token.md)和[登录信息验证](untitled.md)接口即可，以后再次登录调用[二次登录接口](er-ci-deng-lu.md)（防封号，防掉线）
* 假如微信掉线或者手动下线后，直接调用此接口登录即可
* 不需要扫码，只需要手机**微信点击确认登录**就好，如下图所示
{% endhint %}



![  &#x793A;&#x4F8B;](../../.gitbook/assets/image%20%2821%29.png)

