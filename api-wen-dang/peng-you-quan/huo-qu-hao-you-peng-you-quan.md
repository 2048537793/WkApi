---
description: 获取好友朋友圈
---

# 获取好友朋友圈

**简要描述：**

* 获取某个好友的朋友圈

**请求URL：**

* `http://localhost:18081/getFriendCircle`

**请求方式：**

* POST

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| wId | 是 | string | 微信实例ID |
| wcId | 是 | string | 好友微信号（一定传wx\_开头的，不知道的可以调用[获取联系人列表](../kai-shi-kai-fa/huo-qu-yong-hu-ji-ben-xin-xi.md)取） |
| statusId | 是 | int | 获取首页的话传0，获取下一页的话，传上一页的最后一条朋友圈id |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |
| data |  |  |
| id | string | 朋友圈ID |
| userName | string | 微信号 |
| createTime | string | 时间 |
| objectDesc | string | 朋友圈内容 |

**请求参数示例**

```text
{
    "wId": "0000016e-abcd-0ea8-0002-d8c2dfdb0bf3",
    "wcId": "wxid_uf44z2g3jge022",
    "statusId":0
}
```

**成功返回示例**

```text
{
    "message": "成功",
    "code": "1000",
    "data": [
        {
            "id": "13210450266873082001",
            "userName": "wxid_uf44z2g3jge022",
            "createTime": 1574808391,
            "objectDesc": "<TimelineObject><id><![CDATA[13210450266873082001]]></id><username><![CDATA[wxid_uf44z2g3jge022]]></username><createTime><![CDATA[1574808391]]></createTime><contentDescShowType>0</contentDescShowType><contentDescScene>0</contentDescScene><private><![CDATA[0]]></private><contentDesc><![CDATA[喝茶，看似是不断地消费茶叶，实际却是不断地投资自己。喝茶，让自己更健康、让自己更有气质、让自己更有品味。[爱心]]]></contentDesc><contentattr><![CDATA[0]]></contentattr><sourceUserName></sourceUserName><sourceNickName></sourceNickName><statisticsData></statisticsData><weappInfo><appUserName></appUserName><pagePath></pagePath></weappInfo><canvasInfoXml></canvasInfoXml><ContentObject><contentStyle><![CDATA[1]]></contentStyle><contentSubStyle><![CDATA[0]]></contentSubStyle><title></title><description></description><contentUrl></contentUrl><mediaList><media><id><![CDATA[13210450267449274477]]></id><type><![CDATA[2]]></type><title></title><description></description><private><![CDATA[0]]></private><url type=\"1\" md5=\"aa89578ecb99361f81a36c3b53be1607\"><![CDATA[http://shmmsns.qpic.cn/mmsns/ic3ibEjvYaKJx5f8OUKcPAQibaNhuV7ibKwjhthmdicBS3Szc3dIDEvexydngmACD6mjtRic7bHicGxdzM/0]]></url><thumb type=\"1\"><![CDATA[http://shmmsns.qpic.cn/mmsns/ic3ibEjvYaKJx5f8OUKcPAQibaNhuV7ibKwjhthmdicBS3Szc3dIDEvexydngmACD6mjtRic7bHicGxdzM/150]]></thumb><size totalSize=\"139233.0\" width=\"1080.0\" height=\"1440.0\"></size></media></mediaList></ContentObject><actionInfo><appMsg><mediaTagName></mediaTagName><messageExt></messageExt><messageAction></messageAction></appMsg></actionInfo><appInfo><id></id></appInfo><location poiClassifyId=\"\" poiName=\"\" poiAddress=\"\" poiClassifyType=\"0\" city=\"\"></location><publicUserName></publicUserName><streamvideo><streamvideourl></streamvideourl><streamvideothumburl></streamvideothumburl><streamvideoweburl></streamvideoweburl></streamvideo></TimelineObject>"
        },
        {
            "id": "13191812886660526197",
            "userName": "wxid_uf44z2g3jge022",
            "createTime": 1572586642,
            "objectDesc": "<TimelineObject><id><![CDATA[13191812886660526197]]></id><username><![CDATA[wxid_uf44z2g3jge022]]></username><createTime><![CDATA[1572586642]]></createTime><contentDescShowType>0</contentDescShowType><contentDescScene>0</contentDescScene><private><![CDATA[0]]></private><contentDesc><![CDATA[2006年一品佳熟茶。昆明纯干仓经过13个年头的转化，樟香迷人，口感醇厚香甜，滑口充盈，耐泡度高，无杂味。茶汤香气饱满，滋味香馥，条索均匀，叶底柔美。]]></contentDesc><contentattr><![CDATA[0]]></contentattr><sourceUserName></sourceUserName><sourceNickName></sourceNickName><statisticsData></statisticsData><weappInfo><appUserName></appUserName><pagePath></pagePath></weappInfo><canvasInfoXml></canvasInfoXml><ContentObject><contentStyle><![CDATA[1]]></contentStyle><contentSubStyle><![CDATA[0]]></contentSubStyle><title></title><description></description><contentUrl></contentUrl><mediaList><media><id><![CDATA[13191812887225381002]]></id><type><![CDATA[2]]></type><title></title><description></description><private><![CDATA[0]]></private><url type=\"1\" md5=\"be757d9078a8e49151cb7adb686451b4\"><![CDATA[http://shmmsns.qpic.cn/mmsns/ic3ibEjvYaKJx5f8OUKcPAQ04OcFZmLM85BNEZ6qWFZ2DqUmSOCXL7UqyB65vU2sNcSKB4riaiayHKs/0]]></url><thumb type=\"1\"><![CDATA[http://shmmsns.qpic.cn/mmsns/ic3ibEjvYaKJx5f8OUKcPAQ04OcFZmLM85BNEZ6qWFZ2DqUmSOCXL7UqyB65vU2sNcSKB4riaiayHKs/150]]></thumb><size totalSize=\"173667.0\" width=\"1080.0\" height=\"1440.0\"></size></media><media><id><![CDATA[13191812887221907575]]></id><type><![CDATA[2]]></type><title></title><description></description><private><![CDATA[0]]></private><url type=\"1\" md5=\"d9f366d9a3fdd389dc01e4e1f2c7d2d6\"><![CDATA[http://shmmsns.qpic.cn/mmsns/ic3ibEjvYaKJx5f8OUKcPAQ04OcFZmLM85icyfgHSVQ8MUkEMKeIomDibbultROGkrDMrbWLicxwNic7I/0]]></url><thumb type=\"1\"><![CDATA[http://shmmsns.qpic.cn/mmsns/ic3ibEjvYaKJx5f8OUKcPAQ04OcFZmLM85icyfgHSVQ8MUkEMKeIomDibbultROGkrDMrbWLicxwNic7I/150]]></thumb><size totalSize=\"185164.0\" width=\"1080.0\" height=\"1440.0\"></size></media><media><id><![CDATA[13191812887219941485]]></id><type><![CDATA[2]]></type><title></title><description></description><private><![CDATA[0]]></private><url type=\"1\" md5=\"692d854faa67b7684ce8c8b3978f5938\"><![CDATA[http://shmmsns.qpic.cn/mmsns/ic3ibEjvYaKJx5f8OUKcPAQ1u4ArG0lksaM2vyiccgDecDPBhmYh14S2AVD6B614ibNeOXzRuWTlysU/0]]></url><thumb type=\"1\"><![CDATA[http://shmmsns.qpic.cn/mmsns/ic3ibEjvYaKJx5f8OUKcPAQ1u4ArG0lksaM2vyiccgDecDPBhmYh14S2AVD6B614ibNeOXzRuWTlysU/150]]></thumb><size totalSize=\"210355.0\" width=\"1080.0\" height=\"1440.0\"></size></media><media><id><![CDATA[13191812887232458870]]></id><type><![CDATA[2]]></type><title></title><description></description><private><![CDATA[0]]></private><url type=\"1\" md5=\"e59ce3efc8be7bc1c3ef0f1b502c6405\"><![CDATA[http://shmmsns.qpic.cn/mmsns/ic3ibEjvYaKJx5f8OUKcPAQ1u4ArG0lksa61ibgtkJ089GPMsECBH3diaPMIO6nQnCLy9SULZ1F1IicQ/0]]></url><thumb type=\"1\"><![CDATA[http://shmmsns.qpic.cn/mmsns/ic3ibEjvYaKJx5f8OUKcPAQ1u4ArG0lksa61ibgtkJ089GPMsECBH3diaPMIO6nQnCLy9SULZ1F1IicQ/150]]></thumb><size totalSize=\"222838.0\" width=\"1080.0\" height=\"1440.0\"></size></media><media><id><![CDATA[13191812887229771904]]></id><type><![CDATA[2]]></type><title></title><description></description><private><![CDATA[0]]></private><url type=\"1\" md5=\"a282433f87c875dbf7ca514c9add2e3d\"><![CDATA[http://shmmsns.qpic.cn/mmsns/ic3ibEjvYaKJx5f8OUKcPAQ1u4ArG0lksa2qfPSl9cJ3IapCicHM4RLYuDgpU8ADnEAgeLBkaV6g2E/0]]></url><thumb type=\"1\"><![CDATA[http://shmmsns.qpic.cn/mmsns/ic3ibEjvYaKJx5f8OUKcPAQ1u4ArG0lksa2qfPSl9cJ3IapCicHM4RLYuDgpU8ADnEAgeLBkaV6g2E/150]]></thumb><size totalSize=\"164834.0\" width=\"1080.0\" height=\"1440.0\"></size></media><media><id><![CDATA[13191812887229051012]]></id><type><![CDATA[2]]></type><title></title><description></description><private><![CDATA[0]]></private><url type=\"1\" md5=\"862f56ce19215ec616ed83317afc94e7\"><![CDATA[http://shmmsns.qpic.cn/mmsns/ic3ibEjvYaKJx5f8OUKcPAQibHVFDuKwGBt7dNQljlvDSAXha3sIljTqpq5licEu8vJNF1ZlL3kjibnc/0]]></url><thumb type=\"1\"><![CDATA[http://shmmsns.qpic.cn/mmsns/ic3ibEjvYaKJx5f8OUKcPAQibHVFDuKwGBt7dNQljlvDSAXha3sIljTqpq5licEu8vJNF1ZlL3kjibnc/150]]></thumb><size totalSize=\"128174.0\" width=\"1080.0\" height=\"1440.0\"></size></media></mediaList></ContentObject><actionInfo><appMsg><mediaTagName></mediaTagName><messageExt></messageExt><messageAction></messageAction></appMsg></actionInfo><appInfo><id></id></appInfo><location poiClassifyId=\"\" poiName=\"\" poiAddress=\"\" poiClassifyType=\"0\" city=\"\"></location><publicUserName></publicUserName><streamvideo><streamvideourl></streamvideourl><streamvideothumburl></streamvideothumburl><streamvideoweburl></streamvideoweburl></streamvideo></TimelineObject>"
        }
    ]
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

