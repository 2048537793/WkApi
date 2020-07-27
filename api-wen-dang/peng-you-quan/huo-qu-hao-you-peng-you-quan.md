---
description: 获取好友朋友圈
---

# 获取好友朋友圈

**简要描述：**

* 获取某个好友的朋友圈

**请求URL：**

* `http://域名地址/getFriendCircle`

**请求方式：**

* POST 

**请求头Headers：**

* Content-Type：application/json
* Authorization：login接口返回

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :---: | :---: | :---: | :---: |
| wId | 是 | String | 微信实例ID |
| wcId | 是 | String | 微信号 |
| firstPageMd5 | 是 | int | 首次传:""，下次传返回的firstPageMd5，假如未返回，直接传上次的即可 |
| maxId | 是 | long | 首次传：0，第二次获取传列表中最后一项的id |

**请求参数示例**

```javascript
{
    "wId": "0000016e-68f9-99d5-0002-3a1cd9eaaa17",
    "wcId ": "xxxxxx",
    "firstPageMd5": "",
    "maxId":0
}
```

**成功返回示例**

```javascript
{
    "message": "成功",
    "code": "1000",
    "data": {
        "sns": [
             {
                "id": "xxxxxx",
                "userName": "xxxxxx",
                "nickName": "xxxxxx",
                "createTime": xxxxxx,
                "objectDesc": {
                    "xml": "xxxxxx",
                    "len": xxxxxx
                },
                "likeCount": xxxxxx,
                "snsLikes": [
                    {

                    }
                ],
                "commentCount": xxxxxx,
                "snsComments": []
            },
            ......
        ],
        "firstPageMd5": "xxxxxx"
    }
}
```

**错误返回示例**

```javascript
{
    "message": "失败",
    "code": "1001",
    "data": null
}
```

**返回数据：**

| 参数名 | 类型 | 说明 |
| :---: | :---: | :---: |
| code | int | 1000成功，10001失败 |
| msg | String | 反馈信息 |
| data |  |  |
| id | String | 朋友圈ID |
| userName | String | 微信号 |
| createTime | String | 时间 |
| objectDesc | JSONObject | 朋友圈内容 |
| xml | String | 朋友圈xml |
| len | int | xml 长度 |
| commentId | int | 评论标识 |
| replyCommentId | int | 回复评论标识 |
| deleteFlag | int | 删除标识 |
| isNotRichText | int | 是否试富文本 |
| content | String | 评论内容 |
| commentId | int | 评论ID |
| snsLikes | JSONArray | 点赞用户列表 |
| userName | String | 微信号 |
| nickName | String | 昵称 |
| type | int | 点赞类型 |
| createTime | int | 点赞时间 |
| firstPageMd5 | String |  |

