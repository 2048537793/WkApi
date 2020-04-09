---
description: 微信消息内容释义
---

# 微信消息内容释义

**简要描述：**

* 获取回调消息（文字消息、图片消息、视频消息等信息）

**请求方式：**

* `HTTP协议`

**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| message | JSONObject | 返回数据 |
| wcId | String | 微信号 |
| message.data | JSONObject | 消息体 |
| message.messageType | int | 0:好友请求 1:群邀请 2：消息 3:离线 4:其他消息 |
| message.data.msgType | int | 10000:表示添加别人成功;47:动图;48:地图位置;49:红包、文件、链接、小程序; （具体根据content中的type字段区分，当type为2001时表示红包，2000表示收付款消息，5表示链接，19表示群聊的聊天记录，33和36表示小程序，6表示文件，8表示手机输入法自带表情），100008表示手机上删除好友，from\_user表示好友的wxid |
| message.data.toUser | String | 接收微信号 |
| message.data.timestamp | long | 时间 |
| message.data.content | String\(文本消息\) 或 XML（图片、视频消息） | 消息体 |
| message.data.img | byte\[\] | 缩略图 |
| message.data.self | boolean | 是否是自己发送的消息 |
| message.data.type | int | 0:文本消息;1:图片消息；2：视频消息 |
| message.data.category | int | 0:私聊消息;1:群组消息 |
| message.data.msgId | long | 消息ID |
| message.data.atlist | String\[\] | 被艾特群成员微信号 |
| message.data.msgSource | String | 消息源 |
| message.data.pushContent | String | 谁艾特了你 |

* 离线消息返回时message.data为微信实例ID

**成功返回示例**

```text
#文字消息返回
{
    "message": {
    "data": {
        "category": 0,
        "content": "1",
        "fromUser": "wxid_lr6j4nononb921",
        "msgId": 0,
        "self": false,
        "timestamp": 1576548307000,
        "toUser": "wxid_gia1nwcgpobz22",
        "type": 0,
        "wId": "0000016f-1199-7f6f-0000-52a89e29eaa0"
    },
    "messageType": 2
    },
    "wcId": "wxid_gia1nwcgpobz22"
}
#图片消息
{
    "message": {
    "data": {
        "category": 0,
        "content": "<?xml version=\"1.0\"?>\n<msg>\n\t<img aeskey=\"2c285cb1b65dce639f63ea23be4844be\" encryver=\"1\" cdnthumbaeskey=\"2c285cb1b65dce639f63ea23be4844be\" cdnthumburl=\"304e02010004473045020100020466883f5202032f55f90204ad0060b402045df8280a042032636131353631643964353763383631343062323537633362313663323365330204010400010201000400\" cdnthumblength=\"3622\" cdnthumbheight=\"0\" cdnthumbwidth=\"0\" cdnmidheight=\"0\" cdnmidwidth=\"0\" cdnhdheight=\"0\" cdnhdwidth=\"0\" cdnmidimgurl=\"304e02010004473045020100020466883f5202032f55f90204ad0060b402045df8280a042032636131353631643964353763383631343062323537633362313663323365330204010400010201000400\" length=\"50833\" cdnbigimgurl=\"304e02010004473045020100020466883f5202032f55f90204ad0060b402045df8280a042032636131353631643964353763383631343062323537633362313663323365330204010400010201000400\" hdlength=\"294877\" md5=\"e32ee9206b88b3a2cc4c51734e60d478\" />\n</msg>\n",
        "fromUser": "wxid_lr6j4nononb921",
        "img": "/9j/4AAQSkZJRgABAQEAYABgAAD/2wBDAA55oooqTQ//2Q==",
        "msgId": 1075988784,
        "self": false,
        "timestamp": 1576548350000,
        "toUser": "wxid_gia1nwcgpobz22",
        "type": 1,
        "wId": "0000016f-1199-7f6f-0000-52a89e29eaa0"
    },
    "messageType": 2
    },
    "wcId": "wxid_gia1nwcgpobz22"
}
#语音消息返回
{
    "message": {
    "data": {
        "category": 0,
        "content": "<msg><voicemsg endflag=\"1\" cancelflag=\"0\" forwardflag=\"0\" voiceformat=\"4\" voicelength=\"2669\" length=\"3870\" bufid=\"291833489205952932\" clientmsgid=\"41646463313661666539333532323200171017121719ebb5706475b101\" fromusername=\"wxid_gia1nwcgpobz22\" /></msg>",
        "fromUser": "wxid_gia1nwcgpobz22",
        "msgId": 1677633783,
        "newMsgId": 7757378338643740597,
        "self": true,
        "timestamp": 1576549037000,
        "toUser": "wxid_lr6j4nononb921",
        "type": 3,
        "wId": "0000016f-11a4-def4-0000-53562861552d"
    },
    "messageType": 2
    },
    "wcId": "wxid_gia1nwcgpobz22"
}
#离线消息返回
{
    "message": {
        "data": "0000016f-11a4-def4-0000-53562861552d",
    "messageType": 3
    },
    "wcId": "wxid_gia1nwcgpobz22"
}
```

