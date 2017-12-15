既然这样，那我就把我写的无与伦比的websocket聊天室拿出来吧。

虽然只是一个渣的一比的DEMO，但是能聊...

基于 swoole 做的。 先贴图片再贴代码：


当然你得先装了 Swoole 扩展才可以，并且该PHP文件是在 CLI 模式下执行的。不要在浏览器执行。please

PHP代码：
```
<?php
/**
 *  基于Swoole的聊天室系统
 */

$server = new Swoole\Websocket\Server("0.0.0.0", 9502);

$server->on(&#39;open&#39;, function (swoole_websocket_server $server, $frame) {
    //每一次客户端连接 最大连接数将增加
    $message = "欢迎 连接号{$frame->fd}：进入了聊天室";
    echo $message."\n";
    foreach ($server->connections as $key => $value) {
        if($frame->fd != $value){
            $server->push($value, $message);
        }
    }
});