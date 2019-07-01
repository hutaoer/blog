# viewport 解析

## 基本概念

### viewport
* 简单的理解，viewport是严格等于浏览器的窗口。在桌面浏览器中，viewport就是浏览器窗口的宽度高度。移动端的viewport就是我们所能看到的手机端浏览器的可视窗口大小。
* 以 iphone 6 做测试，在 UC 以及 Safari 浏览器中，viewport 的默认尺寸为 980 * 1461
* 设置 `<meta name="viewport" content="width=100">`，只对无线页面有效。而 pc 页面的 viewport 还是跟浏览器窗口一致。


### 物理像素
* 又称为设备像素，他是显示设备中一个最微小的物理部件。

### 设备独立像素
* 设备独立像素也称为密度无关像素，可以认为是计算机坐标系统中的一个点，这个点代表一个可以由程序使用的虚拟像素(比如说CSS像素)，然后由相关系统转换为物理像素。

### CSS 像素
* CSS像素是一个抽像的单位，主要使用在浏览器上，用来精确度量Web页面上的内容。一般情况之下，CSS像素称为与设备无关的像素(device-independent pixel)，简称DIPs。

### 设备像素比(device pixel ratio)
* 设备像素比简称为dpr，其定义了物理像素和设备独立像素的对应关系。它的值可以按下面的公式计算得到：
* `设备像素比 ＝ 物理像素 / 设备独立像素`
* 在JavaScript中，可以通过`window.devicePixelRatio`获取到当前设备的dpr。而在CSS中，可以通过`-webkit-device-pixel-ratio`，`-webkit-min-device-pixel-ratio`和 `-webkit-max-device-pixel-ratio`进行媒体查询，对不同dpr的设备，做一些样式适配(这里只针对webkit内核的浏览器和webview)。

## 总结
* 在普通屏幕下1个CSS像素对应1个物理像素，而在Retina屏幕下，1个CSS像素对应的却是4个物理像素。
* 

## 参考
* [viewports剖析](http://www.w3cplus.com/css/viewports.html)
* [使用Flexible实现手淘H5页面的终端适配](https://github.com/amfe/article/issues/17)