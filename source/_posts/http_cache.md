# http 缓存
* 设置 `cache-control: no cache` 和 `cache-control: max-age=0`的效果一样。
* 浅聊HTTP缓存 (HTTP Cache): https://juejin.im/post/5bf3c28ee51d4514df5b7625

## 强制缓存
* 实现强缓存，主要是根据客户端保留的一个服务器端的response header中的两个字段：expires、cache-control。
* cache-control优先级比expires高。Cache-Control相比于expires是更好的选择，所以同时存在时，只有Cache-Control生效。

## 协商缓存
* 协商缓存就是强制缓存失效后，浏览器携带缓存标识向服务器发起请求，由服务器根据缓存标识决定是否使用缓存的过程。
* 协商缓存的标识也是在响应报文的HTTP头中和请求结果一起返回给浏览器的，控制协商缓存的字段分别有：Last-Modified / If-Modified-Since 和 Etag / If-None-Match。
* Etag / If-None-Match 优先级比 Last-Modified / If-Modified-Since 高。

## 两者异同
* 两者的共同点是：如果命中，都是从客户端缓存中加载资源，而不是从服务器加载资源数据；
* 两者的区别是：强缓存不发请求到服务器，协商缓存会发请求到服务器。
