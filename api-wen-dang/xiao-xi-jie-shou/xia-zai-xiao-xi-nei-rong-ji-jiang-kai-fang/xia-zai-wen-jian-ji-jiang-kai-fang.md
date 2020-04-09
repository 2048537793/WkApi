---
description: 下载文件
---

# 下载文件

**简要描述：**

* 下载消息中的文件

**请求URL：**

* `http://localhost:18081/getMsgFile`

**请求方式：**

* POST

**请求头Headers：**

* Content-Type：application/json
* Authorization：Authorization值（登录获取二维码信息接口中返回的认证信息值）

**参数：**

**下面所有参数都是从回调中取，非自己的数据，获取到受认可的url，才可以去发送文件**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| wId | 是 | string | 微信实例ID，\(消息回调取，非自己的wId\) |
| msgId | 是 | string | 消息id \(消息回调取\) |
| from\_user | 是 | string | 发送人的微信号 \(消息回调取,非自己的微信号\) |
| to\_user | 是 | string | 接收人的微信号 \(消息回调取，非好友的微信号\) |
| content | 是 | string | 收到的消息的xml数据 \(消息回调取\) |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |

**请求参数示例**

```text
{
    "wId": "00000171-0504-4e11-0005-89183b61f7e4",
    "msgId": 1114390853,
    "from_user": "wxid_i6qsbbjenjuj22",
    "to_user": "wxid_wl9qchkanp9u22",
    "content": "<?xml version=\"1.0\"?>\n<msg>\n\t<appmsg appid=\"\" sdkver=\"0\">\n\t\t<title>2019年(模拟地震3)11月25日广西百色市靖西市5.2级地震灾情简报第1期.doc</title>\n\t\t<des />\n\t\t<action />\n\t\t<type>6</type>\n\t\t<showtype>0</showtype>\n\t\t<mediatagname />\n\t\t<messageaction />\n\t\t<content />\n\t\t<url />\n\t\t<lowurl />\n\t\t<dataurl />\n\t\t<lowdataurl />\n\t\t<appattach>\n\t\t\t<totallen>2481152</totallen>\n\t\t\t<attachid>@cdn_304f020100044830460201000204ced8878302032f55f90204990260b402045e7814240421777869645f776c397163686b616e70397532323237345f313538343932373737390204010400050201000400_b26dc4e8fd8b7c6f431f236dfc749f93_1</attachid>\n\t\t\t<emoticonmd5></emoticonmd5>\n\t\t\t<fileext>doc</fileext>\n\t\t\t<cdnattachurl>304f020100044830460201000204ced8878302032f55f90204990260b402045e7814240421777869645f776c397163686b616e70397532323237345f313538343932373737390204010400050201000400</cdnattachurl>\n\t\t\t<aeskey>b26dc4e8fd8b7c6f431f236dfc749f93</aeskey>\n\t\t\t<encryver>0</encryver>\n\t\t</appattach>\n\t\t<extinfo />\n\t\t<sourceusername />\n\t\t<sourcedisplayname />\n\t\t<commenturl />\n\t\t<thumburl />\n\t\t<md5>79640f0b800bf2d143d7ba8c056412e1</md5>\n\t</appmsg>\n\t<fromusername>wxid_i6qsbbjenjuj22</fromusername>\n\t<scene>0</scene>\n\t<appinfo>\n\t\t<version>1</version>\n\t\t<appname />\n\t</appinfo>\n\t<commenturl />\n</msg>\n"
}
```

**成功返回示例**

```text
{
    "message": "成功",
    "code": "1000",
    "data": "https://weikong-1301028514.cos.ap-shanghai.myqcloud.com//msgVideo/5d2e161b-0f66-4543-a518-583493805b86-1584927861739-2019年(模拟地震3)11月25日广西百色市靖西市5.2级地震灾情简报第1期.doc"
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

