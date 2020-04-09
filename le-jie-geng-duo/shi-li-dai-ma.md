# 示例代码

### Java webSocket Demo（已废弃，建议查看postman示例）

```text
import org.java_websocket.WebSocket;
import org.java_websocket.client.WebSocketClient;
import org.java_websocket.drafts.Draft_6455;
import org.java_websocket.handshake.ServerHandshake;
import org.slf4j.Logger;
import org.slf4j.LoggerFactory;

import java.net.URI;
import java.net.URISyntaxException;

public class WebsocketClientWs {

    private static Logger logger = LoggerFactory.getLogger(WebsocketClientWs.class);

    public static WebSocketClient client;

    public static void main(String[] args) {
        try {
            client = new WebSocketClient(new URI("ws://localhost:18082/ws?wxId=zhongweiyu780"), new Draft_6455()) {
                @Override
                public void onOpen(ServerHandshake serverHandshake) {
                    logger.info("握手成功");
                }

                @Override
                public void onMessage(String msg) {
                    logger.info("收到消息==========" + msg);
                }

                @Override
                public void onClose(int i, String s, boolean b) {
                    logger.info("链接已关闭");
                }

                @Override
                public void onError(Exception e) {
                    e.printStackTrace();
                    logger.info("发生错误已关闭");
                }
            };
        } catch (URISyntaxException e) {
            e.printStackTrace();
        }

        client.connect();
        //logger.info(client.getDraft());
        while (!client.getReadyState().equals(WebSocket.READYSTATE.OPEN)) {
            logger.info("正在连接...");
        }

    }

}
```

### **H5 websocket demo**

```text
<!DOCTYPE HTML>
<html>
<head>
    <meta charset="utf-8">
    <title>websocketClient</title>

    <script type="text/javascript">
        function WebSocketTest()
        {
            if ("WebSocket" in window)
            {
                // 打开一个 web socket
                var ws = new WebSocket("ws://localhost:18082/ws?wxId=zhongweiyu780");

                ws.onopen = function()
                {
                    // Web Socket 已连接上，使用 send() 方法发送数据
                    // ws.send("发送数据1");
                   alert("连接成功")
                };

                ws.onmessage = function (evt)
                {
                    var received_msg = evt.data;
                    console.log(received_msg);
                };

                ws.onclose = function()
                {
                    // 关闭 websocket
                    alert("连接已关闭...");
                };
            }

            else
            {
                // 浏览器不支持 WebSocket
                alert("您的浏览器不支持 WebSocket!");
            }
        }
    </script>

</head>
<body>

<div id="sse">
    <a href="javascript:WebSocketTest()">运行 WebSocket</a>
</div>

</body>
</html>
```

