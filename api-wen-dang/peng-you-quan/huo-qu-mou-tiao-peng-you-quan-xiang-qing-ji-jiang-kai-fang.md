---
description: 获取某条朋友圈详情
---

# 获取某条朋友圈详情



**简要描述：**

* 获取某条朋友圈详细内容

**请求URL：**

* `http://localhost:18081/getSnsObject`

**请求方式：**

* POST

**请求头Headers：**

* Content-Type：application/json
* Authorization：Authorization值（登录获取二维码信息接口中返回的认证信息值）

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| wId | 是 | string | 微信实例ID |
| statusId | 是 | int | 朋友圈id |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |

**请求参数示例**

```text
{
   "wId": "0000016f-a340-c2d7-0003-6ab83bc1e64a",
   "statusId": 13243502469259006108
}
```

**成功返回示例**

```text
{
	"message": "成功",
	"code": "1000",
	"data": {
		"id": "-5201150674964828098",
		"userName": "wxid_wl9qchkanp9u22",
		"nickName": "微控小助理",
		"createTime": 1578997778,
		"objectDesc": "<TimelineObject><id><![CDATA[13245593398744723518]]></id><username><![CDATA[wxid_wl9qchkanp9u22]]></username><createTime><![CDATA[1578997778]]></createTime><contentDescShowType>0</contentDescShowType><contentDescScene>0</contentDescScene><private><![CDATA[0]]></private><contentDesc><![CDATA[-\n能瘦着就不要胖着！\n能美着就不要丑着！\n能富着就不要穷着！\n接下来给大家分享我稳变瘦变美变有💰的秘诀[奸笑][奸笑]]]></contentDesc><contentattr><![CDATA[0]]></contentattr><sourceUserName></sourceUserName><sourceNickName></sourceNickName><statisticsData></statisticsData><weappInfo><appUserName></appUserName><pagePath></pagePath></weappInfo><canvasInfoXml></canvasInfoXml><ContentObject><contentStyle><![CDATA[1]]></contentStyle><contentSubStyle><![CDATA[0]]></contentSubStyle><title></title><description></description><contentUrl></contentUrl><mediaList><media><id><![CDATA[13245593399169396822]]></id><type><![CDATA[2]]></type><title></title><description></description><private><![CDATA[0]]></private><url type=\"1\" md5=\"f5733dca86312d6f050aea74fa67ea94\"><![CDATA[http://shmmsns.qpic.cn/mmsns/6mXOeYa4HU9WGicjDCdKy7Per1Fsdcnjg9kicPtgNFFpE7ow6wNI0hNKCYrtPyVBMDhEr1lWRRlMo/0]]></url><thumb type=\"1\"><![CDATA[http://shmmsns.qpic.cn/mmsns/6mXOeYa4HU9WGicjDCdKy7Per1Fsdcnjg9kicPtgNFFpE7ow6wNI0hNKCYrtPyVBMDhEr1lWRRlMo/150]]></thumb><videoDuration><![CDATA[0.0]]></videoDuration><size totalSize=\"118055.0\" width=\"1080.0\" height=\"1080.0\"></size></media></mediaList></ContentObject><actionInfo><appMsg><mediaTagName></mediaTagName><messageExt></messageExt><messageAction></messageAction></appMsg></actionInfo><appInfo><id></id></appInfo><location poiClassifyId=\"\" poiName=\"\" poiAddress=\"\" poiClassifyType=\"0\" city=\"\"></location><publicUserName></publicUserName><streamvideo><streamvideourl></streamvideourl><streamvideothumburl></streamvideothumburl><streamvideoweburl></streamvideoweburl></streamvideo></TimelineObject>",
		"commentUserList": null,
		"likeUserList": null
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

