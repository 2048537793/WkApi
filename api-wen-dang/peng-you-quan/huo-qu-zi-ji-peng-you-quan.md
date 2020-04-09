---
description: 获取自己朋友圈
---

# 获取自己朋友圈

**简要描述：**

* 获取朋友圈

**请求URL：**

* `http://localhost:18081/getCircle`

**请求方式：**

* POST

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| wId | 是 | string | 微信实例ID |
| statusId | 是 | int | 获取首页的话传0，获取下一页的话，传上一页的最后一条朋友圈id |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |
| data |  |  |
| id | string | 朋友圈ID |
| userName | string | 微信号 |
| nickName | string | 昵称 |
| createTime | string | 时间 |
| objectDesc | string | 朋友圈内容 |
| commentUserList | json | 评论用户列表 |
| userName | string | 微信号 |
| nickName | string | 昵称 |
| content | string | 评论内容 |
| commentId | int | 评论ID |
| likeUserList | json | 点赞用户列表 |
| userName | string | 微信号 |
| nickName | string | 昵称 |
| commentId | int | 点赞ID |

**请求参数示例**

```text
{
    "wId": "0000016e-abcd-0ea8-0002-d8c2dfdb0bf3",
    "statusId":0
}
```

**成功返回示例**

```text
{
    "message": "成功",
    "code": "1000",
    "data": {
    "message": "成功",
    "code": "1000",
    "data": [
        {
            "id": "13213854325885243534",
            "userName": "zhongweiyu789",
            "nickName": "海上钢琴师",
            "createTime": 1575214186,
            "objectDesc": "<TimelineObject><id><![CDATA[13213854325885243534]]></id><username><![CDATA[zhongweiyu789]]></username><createTime><![CDATA[1575214186]]></createTime><contentDescShowType>0</contentDescShowType><contentDescScene>0</contentDescScene><private><![CDATA[0]]></private><appInfo><id><![CDATA[wx8dd6ecd81906fd84]]></id><version>49</version><appName><![CDATA[网易云音乐]]></appName><installUrl></installUrl><fromUrl></fromUrl><clickable>0</clickable></appInfo><contentDesc></contentDesc><contentattr><![CDATA[0]]></contentattr><sourceUserName></sourceUserName><sourceNickName></sourceNickName><statisticsData></statisticsData><weappInfo><appUserName></appUserName><pagePath></pagePath></weappInfo><canvasInfoXml></canvasInfoXml><ContentObject><contentStyle><![CDATA[4]]></contentStyle><contentSubStyle><![CDATA[0]]></contentSubStyle><title></title><description></description><contentUrl><![CDATA[http://music.163.com/song/1371343513/?userid=78090728]]></contentUrl><mediaList><media><id><![CDATA[13213854326165999717]]></id><type><![CDATA[3]]></type><title><![CDATA[空心 （Cover：廖野天）]]></title><description><![CDATA[乔琳糖]]></description><private><![CDATA[0]]></private><url type=\"0\"><![CDATA[http://music.163.com/song/media/outer/url?id=1371343513&userid=78090728]]></url><thumb type=\"1\"><![CDATA[http://shmmsns.qpic.cn/mmsns/XFJ8HdGGwGDDZolGiaF27SxyBlwLfXKsowBUWavfk4BbcZwuiaxQOdD62icUKvCZ7iapSicjtyrMFJwg/150]]></thumb><size totalSize=\"1778.0\" width=\"90.0\" height=\"90.0\"></size></media></mediaList></ContentObject><actionInfo><appMsg><mediaTagName></mediaTagName><messageExt></messageExt><messageAction></messageAction><appid>wx8dd6ecd81906fd84</appid></appMsg><scene>0</scene><type>0</type><url></url><newWordingKey></newWordingKey><newtype>0</newtype><installedWording></installedWording><uninstalledWording></uninstalledWording></actionInfo><statExtStr><![CDATA[GhQKEnd4OGRkNmVjZDgxOTA2ZmQ4NA==]]></statExtStr><location poiClassifyId=\"\" poiName=\"\" poiAddress=\"\" poiClassifyType=\"0\" city=\"\"></location><publicUserName></publicUserName><streamvideo><streamvideourl></streamvideourl><streamvideothumburl></streamvideothumburl><streamvideoweburl></streamvideoweburl></streamvideo></TimelineObject>",
            "commentUserList": [
                {
                    "username": "wxid_6mq1pu8ngj3r22",
                    "nickname": "为了更美好的明天而战",
                    "content": "充满力量",
                    "commentId": 131
                }
            ],
            "likeUserList": [
                {
                    "username": "wxid_6mq1pu8ngj3r22",
                    "nickname": "为了更美好的明天而战",
                    "content": null,
                    "commentId": 0
                }
            ]
        },
        {
            "id": "13212937497573593161",
            "userName": "xuxianpingabc",
            "nickName": "徐贤萍",
            "createTime": 1575104891,
            "objectDesc": "<TimelineObject><id><![CDATA[13212937497573593161]]></id><username><![CDATA[xuxianpingabc]]></username><createTime><![CDATA[1575104891]]></createTime><contentDescShowType>0</contentDescShowType><contentDescScene>0</contentDescScene><private><![CDATA[0]]></private><contentDesc><![CDATA[全智能维也纳酒店（资阳店）春节前开业。\n普杰无线客控+百度语音\n普杰无线方案节约60%成本[胜利][胜利][胜利]]]></contentDesc><contentattr><![CDATA[0]]></contentattr><sourceUserName></sourceUserName><sourceNickName></sourceNickName><statisticsData></statisticsData><weappInfo><appUserName></appUserName><pagePath></pagePath></weappInfo><canvasInfoXml></canvasInfoXml><ContentObject><contentStyle><![CDATA[1]]></contentStyle><contentSubStyle><![CDATA[0]]></contentSubStyle><title></title><description></description><contentUrl></contentUrl><mediaList><media><id><![CDATA[13212937497857298485]]></id><type><![CDATA[2]]></type><title></title><description></description><private><![CDATA[0]]></private><url type=\"1\" md5=\"874fe71d76133a67559120c05d2047af\"><![CDATA[http://shmmsns.qpic.cn/mmsns/I1OPdTuWhE83ibVLibAFEmribSY0sKX5AaGiarFbicialUSHW0hw5ZpfrPaVZO5KeE5dr1ticgBGwPMa2k/0]]></url><thumb type=\"1\"><![CDATA[http://shmmsns.qpic.cn/mmsns/I1OPdTuWhE83ibVLibAFEmribSY0sKX5AaGiarFbicialUSHW0hw5ZpfrPaVZO5KeE5dr1ticgBGwPMa2k/150]]></thumb><size totalSize=\"83469.0\" width=\"800.0\" height=\"600.0\"></size></media><media><id><![CDATA[13212937497890000957]]></id><type><![CDATA[2]]></type><title></title><description></description><private><![CDATA[0]]></private><url type=\"1\" md5=\"e6deb375edcea745660d489929d63886\"><![CDATA[http://shmmsns.qpic.cn/mmsns/I1OPdTuWhE83ibVLibAFEmricalBLMiaewWr8wxngueODCrRdJbKVdunfNH7WRxm3wrdFHcFFsUANvM/0]]></url><thumb type=\"1\"><![CDATA[http://shmmsns.qpic.cn/mmsns/I1OPdTuWhE83ibVLibAFEmricalBLMiaewWr8wxngueODCrRdJbKVdunfNH7WRxm3wrdFHcFFsUANvM/150]]></thumb><size totalSize=\"98129.0\" width=\"830.0\" height=\"540.0\"></size></media></mediaList></ContentObject><actionInfo><appMsg><mediaTagName></mediaTagName><messageExt></messageExt><messageAction></messageAction></appMsg></actionInfo><appInfo><id></id></appInfo><location poiClassifyId=\"\" poiName=\"\" poiAddress=\"\" poiClassifyType=\"0\" city=\"\"></location><publicUserName></publicUserName><streamvideo><streamvideourl></streamvideourl><streamvideothumburl></streamvideothumburl><streamvideoweburl></streamvideoweburl></streamvideo></TimelineObject>",
            "commentUserList": null,
            "likeUserList": null
        },
        {
            "id": "13212936751919992894",
            "userName": "xuxianpingabc",
            "nickName": "徐贤萍",
            "createTime": 1575104803,
            "objectDesc": "<TimelineObject><id><![CDATA[13212936751919992894]]></id><username><![CDATA[xuxianpingabc]]></username><createTime><![CDATA[1575104803]]></createTime><contentDescShowType>0</contentDescShowType><contentDescScene>0</contentDescScene><private><![CDATA[0]]></private><contentDesc><![CDATA[普杰科技打造的全智能酒店——谷兹•铂雅名人酒店（犀浦凯德广场店）春节前开业！]]></contentDesc><contentattr><![CDATA[0]]></contentattr><sourceUserName></sourceUserName><sourceNickName></sourceNickName><statisticsData></statisticsData><weappInfo><appUserName></appUserName><pagePath></pagePath></weappInfo><canvasInfoXml></canvasInfoXml><ContentObject><contentStyle><![CDATA[1]]></contentStyle><contentSubStyle><![CDATA[0]]></contentSubStyle><title></title><description></description><contentUrl></contentUrl><mediaList><media><id><![CDATA[13212936752153563230]]></id><type><![CDATA[2]]></type><title></title><description></description><private><![CDATA[0]]></private><url type=\"1\" md5=\"9ef7c398ca335a39dd9b87555e4641be\"><![CDATA[http://shmmsns.qpic.cn/mmsns/I1OPdTuWhE83ibVLibAFEmr1U8l82PXQ4picVWHBxEYlw7RiauhrMBLH6zJB9X7AjJNH5iajaTUycQlA/0]]></url><thumb type=\"1\"><![CDATA[http://shmmsns.qpic.cn/mmsns/I1OPdTuWhE83ibVLibAFEmr1U8l82PXQ4picVWHBxEYlw7RiauhrMBLH6zJB9X7AjJNH5iajaTUycQlA/150]]></thumb><size totalSize=\"275296.0\" width=\"1080.0\" height=\"1556.0\"></size></media><media><id><![CDATA[13212936752179449910]]></id><type><![CDATA[2]]></type><title></title><description></description><private><![CDATA[0]]></private><url type=\"1\" md5=\"a676fafe6324810cf122256d648ea659\"><![CDATA[http://shmmsns.qpic.cn/mmsns/I1OPdTuWhE83ibVLibAFEmr3FCsGibP02xE3qq6VN4TJbgtyYfTQx9wxic2yN46bLuq50B88udicqV0U/0]]></url><thumb type=\"1\"><![CDATA[http://shmmsns.qpic.cn/mmsns/I1OPdTuWhE83ibVLibAFEmr3FCsGibP02xE3qq6VN4TJbgtyYfTQx9wxic2yN46bLuq50B88udicqV0U/150]]></thumb><size totalSize=\"71192.0\" width=\"600.0\" height=\"800.0\"></size></media></mediaList></ContentObject><actionInfo><appMsg><mediaTagName></mediaTagName><messageExt></messageExt><messageAction></messageAction></appMsg></actionInfo><appInfo><id></id></appInfo><location poiClassifyId=\"\" poiName=\"\" poiAddress=\"\" poiClassifyType=\"0\" city=\"\"></location><publicUserName></publicUserName><streamvideo><streamvideourl></streamvideourl><streamvideothumburl></streamvideothumburl><streamvideoweburl></streamvideoweburl></streamvideo></TimelineObject>",
            "commentUserList": null,
            "likeUserList": null
        },
        {
            "id": "13212935846435098696",
            "userName": "xuxianpingabc",
            "nickName": "徐贤萍",
            "createTime": 1575104695,
            "objectDesc": "<TimelineObject><id><![CDATA[13212935846435098696]]></id><username><![CDATA[xuxianpingabc]]></username><createTime><![CDATA[1575104695]]></createTime><contentDescShowType>0</contentDescShowType><contentDescScene>0</contentDescScene><private><![CDATA[0]]></private><contentDesc><![CDATA[京元丽呈酒店开业大吉\n普杰科技再下一城]]></contentDesc><contentattr><![CDATA[0]]></contentattr><sourceUserName></sourceUserName><sourceNickName></sourceNickName><statisticsData></statisticsData><weappInfo><appUserName></appUserName><pagePath></pagePath></weappInfo><canvasInfoXml></canvasInfoXml><ContentObject><contentStyle><![CDATA[1]]></contentStyle><contentSubStyle><![CDATA[0]]></contentSubStyle><title></title><description></description><contentUrl></contentUrl><mediaList><media><id><![CDATA[13212935846675026012]]></id><type><![CDATA[2]]></type><title></title><description></description><private><![CDATA[0]]></private><url type=\"1\" md5=\"bd932f43506dfcafdfe6c405f7641223\"><![CDATA[http://shmmsns.qpic.cn/mmsns/I1OPdTuWhE83ibVLibAFEmr7pm80W8WdlwmCLiaOQ1wax7uwuLv3BETOfQf8fLtyrLEQVgeCrOmtC4/0]]></url><thumb type=\"1\"><![CDATA[http://shmmsns.qpic.cn/mmsns/I1OPdTuWhE83ibVLibAFEmr7pm80W8WdlwmCLiaOQ1wax7uwuLv3BETOfQf8fLtyrLEQVgeCrOmtC4/150]]></thumb><size totalSize=\"350418.0\" width=\"1080.0\" height=\"1440.0\"></size></media><media><id><![CDATA[13212935846703599688]]></id><type><![CDATA[2]]></type><title></title><description></description><private><![CDATA[0]]></private><url type=\"1\" md5=\"82d08dd9ddd63135744be1725ae50561\"><![CDATA[http://shmmsns.qpic.cn/mmsns/I1OPdTuWhE83ibVLibAFEmr6PLdevYny2IVI9IR7DQyay0yXzibia3D9zc7BJPMDh9Vauf4OzTGNlyU/0]]></url><thumb type=\"1\"><![CDATA[http://shmmsns.qpic.cn/mmsns/I1OPdTuWhE83ibVLibAFEmr6PLdevYny2IVI9IR7DQyay0yXzibia3D9zc7BJPMDh9Vauf4OzTGNlyU/150]]></thumb><size totalSize=\"251559.0\" width=\"1440.0\" height=\"1080.0\"></size></media><media><id><![CDATA[13212935846728437816]]></id><type><![CDATA[2]]></type><title></title><description></description><private><![CDATA[0]]></private><url type=\"1\" md5=\"f6412291c346caea5e3e67905506e3fa\"><![CDATA[http://shmmsns.qpic.cn/mmsns/I1OPdTuWhE83ibVLibAFEmr6PLdevYny2Itib9H7omE8kicPQG1fS4go8QJ7EbRDFdlEvMib630eUzMg/0]]></url><thumb type=\"1\"><![CDATA[http://shmmsns.qpic.cn/mmsns/I1OPdTuWhE83ibVLibAFEmr6PLdevYny2Itib9H7omE8kicPQG1fS4go8QJ7EbRDFdlEvMib630eUzMg/150]]></thumb><size totalSize=\"240226.0\" width=\"1440.0\" height=\"1080.0\"></size></media><media><id><![CDATA[13212935846757142621]]></id><type><![CDATA[2]]></type><title></title><description></description><private><![CDATA[0]]></private><url type=\"1\" md5=\"4b3fd9140e2e32b5e6ff6a9e6cf34630\"><![CDATA[http://shmmsns.qpic.cn/mmsns/I1OPdTuWhE83ibVLibAFEmr6PLdevYny2IsLj2Y7N1sySrIYxQ1UpYqH7Hj1iaLlw4u5ozRLR7Erf4/0]]></url><thumb type=\"1\"><![CDATA[http://shmmsns.qpic.cn/mmsns/I1OPdTuWhE83ibVLibAFEmr6PLdevYny2IsLj2Y7N1sySrIYxQ1UpYqH7Hj1iaLlw4u5ozRLR7Erf4/150]]></thumb><size totalSize=\"133422.0\" width=\"1080.0\" height=\"1620.0\"></size></media><media><id><![CDATA[13212935846767562849]]></id><type><![CDATA[2]]></type><title></title><description></description><private><![CDATA[0]]></private><url type=\"1\" md5=\"bf43de68c3376cffaeaee5b0d5d55532\"><![CDATA[http://shmmsns.qpic.cn/mmsns/I1OPdTuWhE83ibVLibAFEmrzzeUJ6iateN6OekEHFLEbVg621gnqHxSUTWfN0dqpO11KdH0hngU8P0/0]]></url><thumb type=\"1\"><![CDATA[http://shmmsns.qpic.cn/mmsns/I1OPdTuWhE83ibVLibAFEmrzzeUJ6iateN6OekEHFLEbVg621gnqHxSUTWfN0dqpO11KdH0hngU8P0/150]]></thumb><size totalSize=\"120838.0\" width=\"1080.0\" height=\"1620.0\"></size></media><media><id><![CDATA[13212935846805770320]]></id><type><![CDATA[2]]></type><title></title><description></description><private><![CDATA[0]]></private><url type=\"1\" md5=\"9ed1b15a16b5b8d9b5ae55f06d320e6b\"><![CDATA[http://shmmsns.qpic.cn/mmsns/I1OPdTuWhE83ibVLibAFEmrzzeUJ6iateN6ZT3DzoTXxJ7P5fuzuEYvrcfWmmbabTRL4Okl1yYu6jU/0]]></url><thumb type=\"1\"><![CDATA[http://shmmsns.qpic.cn/mmsns/I1OPdTuWhE83ibVLibAFEmrzzeUJ6iateN6ZT3DzoTXxJ7P5fuzuEYvrcfWmmbabTRL4Okl1yYu6jU/150]]></thumb><size totalSize=\"284123.0\" width=\"1080.0\" height=\"1440.0\"></size></media></mediaList></ContentObject><actionInfo><appMsg><mediaTagName></mediaTagName><messageExt></messageExt><messageAction></messageAction></appMsg></actionInfo><appInfo><id></id></appInfo><location poiClassifyId=\"\" poiName=\"\" poiAddress=\"\" poiClassifyType=\"0\" city=\"\"></location><publicUserName></publicUserName><streamvideo><streamvideourl></streamvideourl><streamvideothumburl></streamvideothumburl><streamvideoweburl></streamvideoweburl></streamvideo></TimelineObject>",
            "commentUserList": null,
            "likeUserList": null
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

