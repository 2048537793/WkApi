# 发送Emoji消息

**简要描述：**

* 发送emoji动图表情

**请求URL：**

* `http://域名地址/sendEmoji`

**请求方式：**

* POST 

**请求头Headers：**

* Content-Type：application/json
* Authorization：login接口返回

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :---: | :---: | :---: | :---: |
| wId | 是 | string | 微信实例ID |
| wcId | 是 | string | 微信号/群号 |
| imageMd5 | 是 | string | 取回调中xml中md5字段值 |
| imgSize | 是 | string | 取回调中xml中len字段值 |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :---: | :---: | :---: |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |

**请求参数示例**

```javascript
{
    "wId": "00000171-78df-0aad-000c-70e4a3ce7d70",
    "wcId": "LoChaX",
    "imageMd5": "4cc7540a85b5b6cf4ba14e9f4ae08b7c",
    "imgSize":"102357"
}
```

**成功返回示例**

```javascript
{
    "message": "发送成功",
    "code": "1000",
    "data": null
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

