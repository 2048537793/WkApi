---
description: 发送链接消息
---

# 发送链接消息

**请求URL：**

* `http://域名地址/sendUrl`

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
| title | 是 | string | 标题 |
| url | 是 | string | 链接 |
| description | 是 | string | 描述 |
| thumbUrl | 是 | string | 图标url |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :---: | :---: | :---: |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |

**请求参数示例**

```javascript
{
    "wId": "0000016f-63d2-ea61-000e-a659a75ea445",
    "wcId": "jack_623555049",
    "title": "这是测试链接",
    "url": "https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1577945612638&di=81a0281095a337037abf85f29929b55f&imgtype=0&src=http%3A%2F%2Fimage5.92bizhi.com%2Funclassified_unclassified--122_26-1600x1200.jpg",
    "description": "",
    "thumbUrl": "https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1577945612638&di=81a0281095a337037abf85f29929b55f&imgtype=0&src=http%3A%2F%2Fimage5.92bizhi.com%2Funclassified_unclassified--122_26-1600x1200.jpg"
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

