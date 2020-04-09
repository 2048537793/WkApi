---
description: 转发朋友圈(对谁可见，对谁不可见)
---

# 转发朋友圈\(对谁可见，对谁不可见\)

**简要描述：**

* 发送朋友圈\(对谁可见,对谁不可见\)

**请求URL：**

* `http://localhost:18081/snsSendXmlToWhomAndITW`

**请求方式：**

* POST

**请求头Headers：**

* Content-Type：application/json
* Authorization：Authorization值（登录获取二维码信息接口中返回的认证信息值）

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| wId | 是 | string | 微信实例ID |
| content | 是 | string | 收到的xml |
| groupUser | 是 | string | 对谁可见，可见用户wcId已逗号分隔 |
| blackUser | 是 | string | 对谁不可见，屏蔽标签的id |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |

**请求参数示例**

```text
{
	"wId": "{{wId}}",
	"content": "<TimelineObject><id><![CDATA[13244700339160101040]]></id><username><![CDATA[wxid_7khg7pr817k322]]></username><createTime><![CDATA[1578891317]]></createTime><contentDescShowType>0</contentDescShowType><contentDescScene>0</contentDescScene><private><![CDATA[0]]></private><contentDesc><![CDATA[-\n能瘦着就不要胖着！\n能美着就不要丑着！\n能富着就不要穷着！\n接下来给大家分享我稳变瘦变美变有💰的秘诀[奸笑][奸笑]]]></contentDesc><contentattr><![CDATA[0]]></contentattr><sourceUserName></sourceUserName><sourceNickName></sourceNickName><statisticsData></statisticsData><weappInfo><appUserName></appUserName><pagePath></pagePath></weappInfo><canvasInfoXml></canvasInfoXml><ContentObject><contentStyle><![CDATA[1]]></contentStyle><contentSubStyle><![CDATA[0]]></contentSubStyle><title></title><description></description><contentUrl></contentUrl><mediaList><media><id><![CDATA[13244700339702280350]]></id><type><![CDATA[2]]></type><title></title><description></description><private><![CDATA[0]]></private><url type=\"1\" md5=\"f5733dca86312d6f050aea74fa67ea94\"><![CDATA[http://shmmsns.qpic.cn/mmsns/6mXOeYa4HU9WGicjDCdKy7Per1Fsdcnjg9kicPtgNFFpE7ow6wNI0hNKCYrtPyVBMDhEr1lWRRlMo/0]]></url><thumb type=\"1\"><![CDATA[http://shmmsns.qpic.cn/mmsns/6mXOeYa4HU9WGicjDCdKy7Per1Fsdcnjg9kicPtgNFFpE7ow6wNI0hNKCYrtPyVBMDhEr1lWRRlMo/150]]></thumb><videoDuration><![CDATA[0.0]]></videoDuration><size totalSize=\"118055.0\" width=\"1080.0\" height=\"1080.0\"></size></media></mediaList></ContentObject><actionInfo><appMsg><mediaTagName></mediaTagName><messageExt></messageExt><messageAction></messageAction></appMsg></actionInfo><appInfo><id></id></appInfo><location poiClassifyId=\"\" poiName=\"\" poiAddress=\"\" poiClassifyType=\"0\" city=\"\"></location><publicUserName></publicUserName><streamvideo><streamvideourl></streamvideourl><streamvideothumburl></streamvideothumburl><streamvideoweburl></streamvideoweburl></streamvideo></TimelineObject>",
	"groupUser": "LoChaX",
	"blackUser":"2"
}
```

**成功返回示例**

```text
{
	"message": "成功",
	"code": "1000",
	"data": {
		"id": "13245593398744723518",
		"userName": "wxid_wl9qchkanp9u22",
		"nickName": null,
		"createTime": 1578997778,
		"objectDesc": "-\n能瘦着就不要胖着！\n能美着就不要丑着！\n能富着就不要穷着！\n接下来给大家分享我稳变瘦变美变有💰的秘诀[奸笑][奸笑]",
		"commentUserList": null,
		"likeUserList": null
	}
}
```

```text
{
    "message": "失败",
    "code": "1001",
    "data": null
}
```

