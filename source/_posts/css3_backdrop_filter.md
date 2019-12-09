# css3_backdrop_filter
* [毛玻璃效果](https://www.zhangxinxu.com/wordpress/2019/11/css-backdrop-filter/)

## 语法
```css
/* 关键字值 */
backdrop-filter: none;

/* URL方式外链SVG filter */
backdrop-filter: url(zxx.svg#filter);

/* <filter-function>值 */
backdrop-filter: blur(2px);  // 模糊
backdrop-filter: brightness(60%);  // 亮度
backdrop-filter: contrast(40%);  // 对比度
backdrop-filter: drop-shadow(4px 4px 10px blue); // 投影
backdrop-filter: grayscale(30%);  // 灰度
backdrop-filter: hue-rotate(120deg); // 色调变化
backdrop-filter: invert(70%); // 反相
backdrop-filter: opacity(20%); // 透明度
backdrop-filter: sepia(90%);  // 饱和度
backdrop-filter: saturate(80%); // 褐色
```

## 代码

```css
.some-class-zxx {
    background-color: #fff;  
}
@supports (-webkit-backdrop-filter:none) or (backdrop-filter:none) {
    .some-class-zxx {
        background: hsla(0, 0%, 100%, .75);
        -webkit-backdrop-filter: blur(5px);    
        backdrop-filter: blur(5px);   
    }
}
```