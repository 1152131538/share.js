[Share.js](http://overtrue.me/share.js/)
===

一键分享到微博，QQ空间，QQ好友，微信，豆瓣，使用字体图标。

或者直接浏览我的博客 http://overtrue.me 或者 http://laravel.so 内容页查看效果。

# 安装

引入js文件即可：

```html
<link rel="stylesheet" href="share.css">
<script src="share.js"></script>
```


# 使用

HTML:

```html
<div class="share-bar"></div>

<!-- 引入sns.js -->
<script src="http://cdn.bootcss.com/jquery/1.11.2/jquery.min.js"></script>
<script src="jquery.qrcode.min.js"></script> <!-- for QRcode -->
<script src="share.js"></script>
<script>
    $(function(){
        $('.share-bar').share();
    });
</script>
```

## 微信分享

微信的二维码生成依赖：https://github.com/jeromeetienne/jquery-qrcode, 请引入此项目中：jquery.qrcode.min.js 即可。

## 自定义配置

所有配置**可选**， 通常默认就满足需求：

```js
var $config = {
	//...
   };

$('.share-bar').share($config);
```

可用的配置有：

```js

url    : '', // 网址，默认使用 window.location.href
site   : '', // 来源（QQ空间会用到）, 默认读取head标签：<meta name="site" content="http://overtrue" />
title  : '', // 标题，默认读取 document.title 或者 <meta name="title" content="share.js" />
description : '', // 描述, 默认读取head标签：<meta name="description" content="PHP弱类型的实现原理分析" />
iamge    : '', // 图片, 默认取网页中第一个img标签
target : '_blank' //打开方式
qrcodeTitle: "微信扫一扫：分享", // 微信二维码提示文字
qrcodeWidth: 100, // 二维码宽度
sites: ['qzone', 'qq', 'weibo','wechat', 'douban'], // 启用的站点
```


# License

 MIT


