CGI是外部应用程序（CGI程序）与WEB服务器之间的接口标准，是在CGI程序和Web服务器之间传递信息的过程。

web server (比如 nginx 或者 apache) 只是内容的分发者：
- 用户通过浏览器访问 html 静态文件，那么 web server 就会去目录中找到这个文件，返回给浏览器，浏览器解析文件展现给用户。
- 用户访问的是 php 文件，根据 nginx 配置，nginx 知道他处理不了这个请求，所以他会去 9000 端口找 php 让 php 来处理，同时 nginx 会传递 url，get/post的数据，http header头 等等，**CGI** 就是要规定传什么样的数据，以什么样的格式来传递给 PHP 的一个标准或者协议。

当 web server 收到了 php 文件的请求之后，会启动对应的 CGI 程序，这里就是 php 的解析器。然后 php 的解析器会首先解析 php.ini ，根据 ini 的配置初始化执行环境，接收参数执行处理，然后再以 CGI 规定的标准格式把处理后的数据返回给 web server （这里返回的就是 html ），然后这个进程就会结束掉。接下来 web server 再把这个结果返回给浏览器。

*CGI 是个协议，跟进程什么的没关系。*


*CGI 是个协议，跟进程什么的没关系。*