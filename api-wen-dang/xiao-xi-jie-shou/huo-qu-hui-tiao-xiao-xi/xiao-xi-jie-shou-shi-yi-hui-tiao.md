---
description: 微信消息内容释义
---

# 回调消息内容释义

{% hint style="warning" %}
因回调事件过多，本释义未包含全部内容，开发者可以自行调试，无需处理所有事件，根据业务需求，选择性处理即可。
{% endhint %}

**简要描述：**

* 获取回调消息字段说明（文字消息、图片消息、视频消息等信息）

**返回数据：**

<table>
  <thead>
    <tr>
      <th style="text-align:center">&#x53C2;&#x6570;&#x540D;</th>
      <th style="text-align:center">&#x7C7B;&#x578B;</th>
      <th style="text-align:center">&#x8BF4;&#x660E;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:center">message</td>
      <td style="text-align:center">JSONObject</td>
      <td style="text-align:center">&#x8FD4;&#x56DE;&#x6570;&#x636E;</td>
    </tr>
    <tr>
      <td style="text-align:center">wcId</td>
      <td style="text-align:center">String</td>
      <td style="text-align:center">&#x5FAE;&#x4FE1;&#x53F7;</td>
    </tr>
    <tr>
      <td style="text-align:center">account</td>
      <td style="text-align:center">String</td>
      <td style="text-align:center">&#x8D26;&#x53F7;</td>
    </tr>
    <tr>
      <td style="text-align:center">messageType</td>
      <td style="text-align:center">int</td>
      <td style="text-align:center">
        <p>0:&#x597D;&#x53CB;&#x8BF7;&#x6C42;</p>
        <p>1:&#x7FA4;&#x9080;&#x8BF7;</p>
        <p>2&#xFF1A;&#x7FA4;&#x540D;&#x7247;</p>
        <p>3:&#x4E2A;&#x4EBA;&#x540D;&#x7247;</p>
        <p>4:&#x4E0B;&#x7EBF;</p>
        <p>5:&#x79C1;&#x804A;&#x6587;&#x672C;&#x6D88;&#x606F;</p>
        <p>6: &#x79C1;&#x804A;&#x56FE;&#x7247;&#x6D88;&#x606F;</p>
        <p>7:&#x79C1;&#x804A;&#x89C6;&#x9891;&#x6D88;&#x606F;</p>
        <p>8:&#x79C1;&#x804A;&#x8BED;&#x97F3;&#x6D88;&#x606F;</p>
        <p>9:&#x7FA4;&#x804A;&#x6587;&#x672C;&#x6D88;&#x606F;</p>
        <p>10:&#x7FA4;&#x804A;&#x56FE;&#x7247;&#x6D88;&#x606F;</p>
        <p>11:&#x7FA4;&#x804A;&#x89C6;&#x9891;&#x6D88;&#x606F;</p>
        <p>12:&#x7FA4;&#x804A;&#x8BED;&#x97F3;&#x6D88;&#x606F;</p>
        <p>13:&#x79C1;&#x804A;&#x5176;&#x4ED6;&#x7C7B;&#x578B;&#x6D88;&#x606F;</p>
        <p>14:&#x7FA4;&#x804A;&#x5176;&#x4ED6;&#x7C7B;&#x578B;&#x6D88;&#x606F;</p>
        <p>15&#xFF1A;&#x597D;&#x53CB;&#x76F8;&#x5173;&#x901A;&#x77E5;&#x6D88;&#x606F;&#xFF08;&#x540C;&#x610F;&#x6DFB;&#x52A0;&#x597D;&#x53CB;&#x7B49;&#xFF09;&#x3001;</p>
        <p>16&#xFF1A;&#x4FEE;&#x6539;&#x597D;&#x53CB;&#x5907;&#x6CE8;&#x901A;&#x77E5;&#x6D88;&#x606F;&#x3001;</p>
        <p>17&#xFF1A;&#x5220;&#x9664;&#x76F8;&#x5173;&#x901A;&#x77E5;&#x6D88;&#x606F;</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:center">data</td>
      <td style="text-align:center">JSONObject</td>
      <td style="text-align:center">&#x6D88;&#x606F;&#x4F53;</td>
    </tr>
    <tr>
      <td style="text-align:center">data.fromUser</td>
      <td style="text-align:center">String</td>
      <td style="text-align:center">&#x53D1;&#x9001;&#x5FAE;&#x4FE1;&#x53F7;</td>
    </tr>
    <tr>
      <td style="text-align:center">data.fromGroup</td>
      <td style="text-align:center">String</td>
      <td style="text-align:center">&#x53D1;&#x9001;&#x7FA4;&#x53F7;</td>
    </tr>
    <tr>
      <td style="text-align:center">data.toUser</td>
      <td style="text-align:center">String</td>
      <td style="text-align:center">&#x63A5;&#x6536;&#x5FAE;&#x4FE1;&#x53F7;</td>
    </tr>
    <tr>
      <td style="text-align:center">data.msgId</td>
      <td style="text-align:center">long</td>
      <td style="text-align:center">&#x6D88;&#x606F;msgId</td>
    </tr>
    <tr>
      <td style="text-align:center">data.newMsgId</td>
      <td style="text-align:center">long</td>
      <td style="text-align:center">&#x6D88;&#x606F;newMsgId</td>
    </tr>
    <tr>
      <td style="text-align:center">data.msgType</td>
      <td style="text-align:center">int</td>
      <td style="text-align:center">&#x5176;&#x4ED6;&#x6D88;&#x606F;&#x5177;&#x4F53;&#x7C7B;&#x578B;&#xFF08;47&#x8868;&#x793A;&#x52A8;&#x56FE;&#xFF1B;48&#x8868;&#x793A;&#x5730;&#x56FE;&#x4F4D;&#x7F6E;&#x6D88;&#x606F;&#xFF09;49&#x8868;&#x793A;&#x7EA2;&#x5305;&#x3001;&#x6587;&#x4EF6;&#x3001;&#x94FE;&#x63A5;&#x3001;&#x5C0F;&#x7A0B;&#x5E8F;&#x7B49;&#x7C7B;&#x578B;&#xFF0C;&#x5177;&#x4F53;&#x6839;&#x636E;content&#x4E2D;&#x7684;type&#x5B57;&#x6BB5;&#x533A;&#x5206;&#xFF0C;&#x5F53;type&#x4E3A;2001&#x65F6;&#x8868;&#x793A;&#x7EA2;&#x5305;&#xFF0C;2000&#x8868;&#x793A;&#x6536;&#x4ED8;&#x6B3E;&#x6D88;&#x606F;&#xFF0C;5&#x8868;&#x793A;&#x94FE;&#x63A5;&#xFF0C;19&#x8868;&#x793A;&#x7FA4;&#x804A;&#x7684;&#x804A;&#x5929;&#x8BB0;&#x5F55;&#xFF0C;33&#x548C;36&#x8868;&#x793A;&#x5C0F;&#x7A0B;&#x5E8F;&#xFF0C;6&#x8868;&#x793A;&#x6587;&#x4EF6;&#xFF0C;8&#x8868;&#x793A;&#x624B;&#x673A;&#x8F93;&#x5165;&#x6CD5;&#x81EA;&#x5E26;&#x8868;&#x60C5;</td>
    </tr>
    <tr>
      <td style="text-align:center">data.timestamp</td>
      <td style="text-align:center">long</td>
      <td style="text-align:center">&#x65F6;&#x95F4;</td>
    </tr>
    <tr>
      <td style="text-align:center">data.content</td>
      <td style="text-align:center">String(&#x6587;&#x672C;&#x6D88;&#x606F;) &#x6216; XML&#xFF08;&#x56FE;&#x7247;&#x3001;&#x89C6;&#x9891;&#x6D88;&#x606F;&#xFF09;</td>
      <td
      style="text-align:center">&#x6D88;&#x606F;&#x4F53;</td>
    </tr>
    <tr>
      <td style="text-align:center">data.self</td>
      <td style="text-align:center">boolean</td>
      <td style="text-align:center">&#x662F;&#x5426;&#x662F;&#x81EA;&#x5DF1;&#x53D1;&#x9001;&#x7684;&#x6D88;&#x606F;</td>
    </tr>
  </tbody>
</table>

**成功返回示例**

```javascript
#私聊文字消息返回
{
    "account": "18351837032",
    "data": {
        "content": "私聊文字消息测试",
        "fromUser": "zhongweiyu789",
        "msgId": 1114311117,
        "newMsgId": 7032628722018977792,
        "self": false,
        "timestamp": 1591325316,
        "toUser": "wxid_fj9ghhitl4qm22",
        "wId": "d6a0cb7d-da8c-488a-a119-f8594984e0c7"
    },
    "messageType": 5,
    "wcId": "wxid_fj9ghhitl4qm22"
}
#群聊文字消息返回
{
    "account": "18351837032",
    "data": {
        "content": "测试",
        "fromGroup": "21923674740@chatroom",
        "fromUser": "zhongweiyu789",
        "msgId": 1711183098,
        "newMsgId": 4419871429570021376,
        "self": false,
        "timestamp": 1591324989,
        "toUser": "wxid_fj9ghhitl4qm22",
        "wId": "d6a0cb7d-da8c-488a-a119-f8594984e0c7"
    },
    "messageType": 9,
    "wcId": "wxid_fj9ghhitl4qm22"
}
#私聊图片消息
{
    "account": "18351837032",
    "data": {
        "content": "<?xml version=\"1.0\"?>\n<msg>\n\t<img aeskey=\"2c30f7356803d05f071d5f58c6680998\" encryver=\"1\" cdnthumbaeskey=\"2c30f7356803d05f071d5f58c6680998\" cdnthumburl=\"304e020100044730450201000204f032c33602032f55f90204bd0260b402045ed9b33f042065616333383134356639396466646137343731356332626365643665626634340204010400010201000400\" cdnthumblength=\"1011\" cdnthumbheight=\"150\" cdnthumbwidth=\"120\" cdnmidheight=\"0\" cdnmidwidth=\"0\" cdnhdheight=\"0\" cdnhdwidth=\"0\" cdnmidimgurl=\"304e020100044730450201000204f032c33602032f55f90204bd0260b402045ed9b33f042065616333383134356639396466646137343731356332626365643665626634340204010400010201000400\" length=\"2566\" cdnbigimgurl=\"304e020100044730450201000204f032c33602032f55f90204bd0260b402045ed9b33f042065616333383134356639396466646137343731356332626365643665626634340204010400010201000400\" hdlength=\"1162\" md5=\"35b062f48f4ce0b2d938b9d74b34b614\" />\n</msg>\n",
        "fromUser": "zhongweiyu789",
        "msgId": 1114311118,
        "newMsgId": 293750214862507968,
        "self": false,
        "timestamp": 1591325503,
        "toUser": "wxid_fj9ghhitl4qm22",
        "wId": "d6a0cb7d-da8c-488a-a119-f8594984e0c7"
    },
    "messageType": 5,
    "wcId": "wxid_fj9ghhitl4qm22"
}
群聊图片消息
{
    "account": "18351837032",
    "data": {
        "content": "zhongweiyu789:\n<?xml version=\"1.0\"?>\n<msg>\n\t<img aeskey=\"b33878a5ec9445a64db21602c4d1819b\" encryver=\"1\" cdnthumbaeskey=\"b33878a5ec9445a64db21602c4d1819b\" cdnthumburl=\"304e020100044730450201000204f032c33602032f55f90204bd0260b402045ed9b370042065633239313439633361633737613261326165373436383035623636343834350204010400010201000400\" cdnthumblength=\"1026\" cdnthumbheight=\"150\" cdnthumbwidth=\"149\" cdnmidheight=\"0\" cdnmidwidth=\"0\" cdnhdheight=\"0\" cdnhdwidth=\"0\" cdnmidimgurl=\"304e020100044730450201000204f032c33602032f55f90204bd0260b402045ed9b370042065633239313439633361633737613261326165373436383035623636343834350204010400010201000400\" length=\"1394\" cdnbigimgurl=\"304e020100044730450201000204f032c33602032f55f90204bd0260b402045ed9b370042065633239313439633361633737613261326165373436383035623636343834350204010400010201000400\" hdlength=\"654\" md5=\"2c39d1c88d72362a80a726ecee552b20\" />\n</msg>\n",
        "fromGroup": "21923674740@chatroom",
        "fromUser": "zhongweiyu789",
        "msgId": 1711183106,
        "newMsgId": 7981913941107135488,
        "self": false,
        "timestamp": 1591325552,
        "toUser": "wxid_fj9ghhitl4qm22",
        "wId": "d6a0cb7d-da8c-488a-a119-f8594984e0c7"
    },
    "messageType": 10,
    "wcId": "wxid_fj9ghhitl4qm22"
}
#私聊语音消息返回
{
    "account": "18351837032",
    "data": {
        "content": "<msg><voicemsg endflag=\"1\" length=\"2446\" voicelength=\"1955\" clientmsgid=\"41393633616139633463366266383600461054060520c6b3c3a800d104\" fromusername=\"zhongweiyu789\" downcount=\"0\" cancelflag=\"0\" voiceformat=\"4\" forwardflag=\"0\" bufid=\"219120766489985424\" /></msg>",
        "fromUser": "zhongweiyu789",
        "length": 2446,
        "msgId": 1114311119,
        "newMsgId": 4796775688409458688,
        "self": false,
        "timestamp": 1591325687,
        "toUser": "wxid_fj9ghhitl4qm22",
        "voiceLength": 1955,
        "wId": "d6a0cb7d-da8c-488a-a119-f8594984e0c7"
    },
    "messageType": 8,
    "wcId": "wxid_fj9ghhitl4qm22"
}
#群聊语音消息返回
{
    "account": "18351837032",
    "data": {
        "content": "zhongweiyu789:\n<msg><voicemsg endflag=\"1\" length=\"3032\" voicelength=\"2064\" clientmsgid=\"41393633616139633463366266383600201055060520c6b3c3a0488103\" fromusername=\"zhongweiyu789\" downcount=\"0\" cancelflag=\"0\" voiceformat=\"4\" forwardflag=\"0\" bufid=\"288433335328178510\" /></msg>",
        "fromGroup": "21923674740@chatroom",
        "fromUser": "zhongweiyu789",
        "length": 3032,
        "msgId": 1711183108,
        "newMsgId": 6667097279114018816,
        "self": false,
        "timestamp": 1591325721,
        "toUser": "wxid_fj9ghhitl4qm22",
        "voiceLength": 2064,
        "wId": "d6a0cb7d-da8c-488a-a119-f8594984e0c7"
    },
    "messageType": 12,
    "wcId": "wxid_fj9ghhitl4qm22"
}
#私聊视频消息返回
{
    "account": "18351837032",
    "data": {
        "content": "<?xml version=\"1.0\"?>\n<msg>\n\t<videomsg aeskey=\"7298894ba13b2c4eced3360c95279761\" cdnthumbaeskey=\"7298894ba13b2c4eced3360c95279761\" cdnvideourl=\"306c020100046530630201000204f032c33602032f55f90204a50260b402045ed9b49e043e617570766964656f5f343964613463623465336564376431385f313539313332353835315f313035373331303530363230633662336333613130363831300204010400040201000400\" cdnthumburl=\"306c020100046530630201000204f032c33602032f55f90204a50260b402045ed9b49e043e617570766964656f5f343964613463623465336564376431385f313539313332353835315f313035373331303530363230633662336333613130363831300204010400040201000400\" length=\"1305852\" playlength=\"10\" cdnthumblength=\"28203\" cdnthumbwidth=\"304\" cdnthumbheight=\"540\" fromusername=\"zhongweiyu789\" md5=\"3ecd03075e40d3cf00419d3bdcf7c2bf\" newmd5=\"6cd7931bc11caefa8c794eed62ec2142\" isad=\"0\" />\n</msg>\n",
        "fromUser": "zhongweiyu789",
        "msgId": 1114311120,
        "newMsgId": 6345723667844606976,
        "self": false,
        "timestamp": 1591325854,
        "toUser": "wxid_fj9ghhitl4qm22",
        "wId": "d6a0cb7d-da8c-488a-a119-f8594984e0c7"
    },
    "messageType": 7,
    "wcId": "wxid_fj9ghhitl4qm22"
}
#群聊视频消息返回
{
    "account": "18351837032",
    "data": {
        "content": "zhongweiyu789:\n<?xml version=\"1.0\"?>\n<msg>\n\t<videomsg aeskey=\"c213c047ac1789b01868d9338ee468e2\" cdnthumbaeskey=\"c213c047ac1789b01868d9338ee468e2\" cdnvideourl=\"306b020100046430620201000204f032c33602032f55f90204a50260b402045ed9b46f043d617570766964656f5f353165313866616466356231633066365f313539313332353830395f3130353632393035303632306336623363336139343535390204010400040201000400\" cdnthumburl=\"306b020100046430620201000204f032c33602032f55f90204a50260b402045ed9b46f043d617570766964656f5f353165313866616466356231633066365f313539313332353830395f3130353632393035303632306336623363336139343535390204010400040201000400\" length=\"6240157\" playlength=\"42\" cdnthumblength=\"25481\" cdnthumbwidth=\"304\" cdnthumbheight=\"540\" fromusername=\"zhongweiyu789\" md5=\"5289f6ca0c41b5d748697137944e1391\" newmd5=\"0382cefc0b3fdfd0b342290f7d34bd0b\" isad=\"0\" />\n</msg>\n",
        "fromGroup": "21923674740@chatroom",
        "fromUser": "zhongweiyu789",
        "msgId": 1711183109,
        "newMsgId": 6026885159785612288,
        "self": false,
        "timestamp": 1591325808,
        "toUser": "wxid_fj9ghhitl4qm22",
        "wId": "d6a0cb7d-da8c-488a-a119-f8594984e0c7"
    },
    "messageType": 11,
    "wcId": "wxid_fj9ghhitl4qm22"
}
#私聊其他消息返回
{
    "account": "18351837032",
    "data": {
        "content": "<msg>\n\t<appmsg appid=\"\" sdkver=\"\">\n\t\t<des><![CDATA[我给你发了一个红包，赶紧去拆!]]></des>\n\t\t<url><![CDATA[https://wxapp.tenpay.com/mmpayhb/wxhb_personalreceive?showwxpaytitle=1&msgtype=1&channelid=1&sendid=1000039901202006057105523212738&ver=6&sign=dbadf1a09f7d85b089757683c3bcb3e64386f166cf70d254624e18a4ce8ba12ed5c3a74831ed663e071b388777a540076a72a00fc1d5f88039bd7f6b1ea2b984bb791001cc28cf4b30f8cbb2bf98640e]]></url>\n\t\t<type><![CDATA[2001]]></type>\n\t\t<title><![CDATA[微信红包]]></title>\n\t\t<thumburl><![CDATA[https://wx.gtimg.com/hongbao/1800/hb.png]]></thumburl>\n\t\t<wcpayinfo>\n\t\t\t<templateid><![CDATA[7a2a165d31da7fce6dd77e05c300028a]]></templateid>\n\t\t\t<url><![CDATA[https://wxapp.tenpay.com/mmpayhb/wxhb_personalreceive?showwxpaytitle=1&msgtype=1&channelid=1&sendid=1000039901202006057105523212738&ver=6&sign=dbadf1a09f7d85b089757683c3bcb3e64386f166cf70d254624e18a4ce8ba12ed5c3a74831ed663e071b388777a540076a72a00fc1d5f88039bd7f6b1ea2b984bb791001cc28cf4b30f8cbb2bf98640e]]></url>\n\t\t\t<iconurl><![CDATA[https://wx.gtimg.com/hongbao/1800/hb.png]]></iconurl>\n\t\t\t<receivertitle><![CDATA[恭喜发财，大吉大利]]></receivertitle>\n\t\t\t<sendertitle><![CDATA[恭喜发财，大吉大利]]></sendertitle>\n\t\t\t<scenetext><![CDATA[微信红包]]></scenetext>\n\t\t\t<senderdes><![CDATA[查看红包]]></senderdes>\n\t\t\t<receiverdes><![CDATA[领取红包]]></receiverdes>\n\t\t\t<nativeurl><![CDATA[wxpay://c2cbizmessagehandler/hongbao/receivehongbao?msgtype=1&channelid=1&sendid=1000039901202006057105523212738&sendusername=zhongweiyu789&ver=6&sign=dbadf1a09f7d85b089757683c3bcb3e64386f166cf70d254624e18a4ce8ba12ed5c3a74831ed663e071b388777a540076a72a00fc1d5f88039bd7f6b1ea2b984bb791001cc28cf4b30f8cbb2bf98640e]]></nativeurl>\n\t\t\t<sceneid><![CDATA[1002]]></sceneid>\n\t\t\t<innertype><![CDATA[0]]></innertype>\n\t\t\t<paymsgid><![CDATA[1000039901202006057105523212738]]></paymsgid>\n\t\t\t<scenetext>微信红包</scenetext>\n\t\t\t<locallogoicon><![CDATA[c2c_hongbao_icon_cn]]></locallogoicon>\n\t\t\t<invalidtime><![CDATA[1591412343]]></invalidtime>\n\t\t\t<broaden />\n\t\t</wcpayinfo>\n\t</appmsg>\n\t<fromusername><![CDATA[zhongweiyu789]]></fromusername>\n</msg>\n",
        "fromUser": "zhongweiyu789",
        "msgId": 1114311121,
        "msgType": 49,
        "newMsgId": 7427743228535934976,
        "timestamp": 1591325943,
        "toUser": "wxid_fj9ghhitl4qm22",
        "wId": "d6a0cb7d-da8c-488a-a119-f8594984e0c7"
    },
    "messageType": 13,
    "wcId": "wxid_fj9ghhitl4qm22"
}
#群聊其他消息类型返回
{
    "account": "18351837032",
    "data": {
        "content": "zhongweiyu789:\n<msg>\n\t<appmsg appid=\"\" sdkver=\"\">\n\t\t<des><![CDATA[我给你发了一个红包，赶紧去拆!]]></des>\n\t\t<url><![CDATA[https://wxapp.tenpay.com/mmpayhb/wxhb_personalreceive?showwxpaytitle=1&msgtype=1&channelid=1&sendid=1000039901202006057296584784724&ver=6&sign=79923ed0702f69a14bfd662b3259c5d48488d3b8ba6601bcdde0aa843a13bacf214c62e79bb5f27db8368fa5f3777deb042535b56ce13f982d5ad68f51fc66fdebab653abadff498b0fcad1bfe7a3466]]></url>\n\t\t<type><![CDATA[2001]]></type>\n\t\t<title><![CDATA[微信红包]]></title>\n\t\t<thumburl><![CDATA[https://wx.gtimg.com/hongbao/1800/hb.png]]></thumburl>\n\t\t<wcpayinfo>\n\t\t\t<templateid><![CDATA[7a2a165d31da7fce6dd77e05c300028a]]></templateid>\n\t\t\t<url><![CDATA[https://wxapp.tenpay.com/mmpayhb/wxhb_personalreceive?showwxpaytitle=1&msgtype=1&channelid=1&sendid=1000039901202006057296584784724&ver=6&sign=79923ed0702f69a14bfd662b3259c5d48488d3b8ba6601bcdde0aa843a13bacf214c62e79bb5f27db8368fa5f3777deb042535b56ce13f982d5ad68f51fc66fdebab653abadff498b0fcad1bfe7a3466]]></url>\n\t\t\t<iconurl><![CDATA[https://wx.gtimg.com/hongbao/1800/hb.png]]></iconurl>\n\t\t\t<receivertitle><![CDATA[恭喜发财，大吉大利]]></receivertitle>\n\t\t\t<sendertitle><![CDATA[恭喜发财，大吉大利]]></sendertitle>\n\t\t\t<scenetext><![CDATA[微信红包]]></scenetext>\n\t\t\t<senderdes><![CDATA[查看红包]]></senderdes>\n\t\t\t<receiverdes><![CDATA[领取红包]]></receiverdes>\n\t\t\t<nativeurl><![CDATA[wxpay://c2cbizmessagehandler/hongbao/receivehongbao?msgtype=1&channelid=1&sendid=1000039901202006057296584784724&sendusername=zhongweiyu789&ver=6&sign=79923ed0702f69a14bfd662b3259c5d48488d3b8ba6601bcdde0aa843a13bacf214c62e79bb5f27db8368fa5f3777deb042535b56ce13f982d5ad68f51fc66fdebab653abadff498b0fcad1bfe7a3466]]></nativeurl>\n\t\t\t<sceneid><![CDATA[1002]]></sceneid>\n\t\t\t<innertype><![CDATA[0]]></innertype>\n\t\t\t<paymsgid><![CDATA[1000039901202006057296584784724]]></paymsgid>\n\t\t\t<scenetext>微信红包</scenetext>\n\t\t\t<locallogoicon><![CDATA[c2c_hongbao_icon_cn]]></locallogoicon>\n\t\t\t<invalidtime><![CDATA[1591412429]]></invalidtime>\n\t\t\t<broaden />\n\t\t</wcpayinfo>\n\t</appmsg>\n\t<fromusername><![CDATA[zhongweiyu789]]></fromusername>\n</msg>\n",
        "fromGroup": "21923674740@chatroom",
        "fromUser": "zhongweiyu789",
        "msgId": 1711183112,
        "msgType": 49,
        "newMsgId": 1881686411402847232,
        "timestamp": 1591326029,
        "toUser": "wxid_fj9ghhitl4qm22",
        "wId": "d6a0cb7d-da8c-488a-a119-f8594984e0c7"
    },
    "messageType": 14,
    "wcId": "wxid_fj9ghhitl4qm22"
}
#离线消息返回
{
    "account": "18351837032",
    "data": {
        "wId": "9d9db97b-1e3e-41de-816a-69321a6cee16"
    },
    "messageType": 4,
    "wcId": "wxid_fj9ghhitl4qm22"
}
```

