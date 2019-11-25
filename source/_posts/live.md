# live.md

## HLS
* 概念：HLS（HTTP Live Streaming）是苹果公司针对iPhone、iPod、iTouch和iPad等移动设备而开发的基于HTTP协议的流媒体解决方案，可实现流媒体的直播和点播。
* 原理：将视频流分片成一系列HTTP下载文件，即视频文件或视频流切分成小片(ts)并建立索引文件(m3u8)。支持的视频流编码为H.264，音频流编码为AAC。简单地理解，当播放视频时，用户下载的是m3u8文件，m3u8里面是ts文件的索引地址，通过m3u8文件的索引地址找到对应的音视频文件的网络地址就可以播放具体的每个小段视频，连接起来就是一段完整的视频。

## RTMP
* RTMP（Real Time Messaging Protocol），实时消息传输协议，主要用来在Flash/AIR平台和支持RTMP协议的流媒体/交互服务器之间进行音视频和数据通信，RTMP是Adobe开发的协议，无法在iPhone中兼容。

## HLS使用
* HLS在移动端具有非常大的优势，可以直接打开播放，HTML5自带的video标签嵌入m3u8视频地址即可，只要有网页浏览器会自己解析，不需要单独下载插件或者APP，在iOS和安卓系统中具有很高的兼容性。

## PC端兼容
* 按照在移动端相同的写法的话，可以看到，在PC端的大多主流浏览器都无法播放，显示黑屏。
* hls.js 是一个依赖HTTP Live Streaming客户端的JavaScript库。详细使用说明可参考官方文档hls.js 。
* 

