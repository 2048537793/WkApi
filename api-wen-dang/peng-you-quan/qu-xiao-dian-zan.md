# 取消点赞

**简要描述：**

* 取消点赞

**请求URL：**

* `http://域名地址/snsCancelPraise`

**请求方式：**

* POST 

**请求头Headers：**

* Content-Type：application/json
* Authorization：login接口返回

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :---: | :---: | :---: | :---: |
| wId | 是 | String | 微信实例ID |
| id | 是 | String | 微信号 |

**请求参数示例**

```javascript
{
     "wId": "b7ad08a6-77c2-4ad6-894a-29993b84c0e4",
     "id": "13351161735026061409"
}
```

**成功返回示例**

```javascript
{
    "message": "成功",
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

**返回数据：**

| 参数名 | 类型 | 说明 |
| :---: | :---: | :---: |
| code | int | 1000成功，10001失败 |
| msg | String | 反馈信息 |

