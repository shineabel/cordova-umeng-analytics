# cordova-umeng-analytics

Cordova友盟统计插件

解决了cordova ios构建时的"UMMobClick/MobClick.h" not found错误
# 安装

1. 运行 ```cordova plugin add https://github.com/shineabel/cordova-umeng-analytics``` 

2. cordova各种衍生命令行都应该支持，例如phonegap或者ionic。

# 使用方法


```Javascript
Umeng.Analytics.config({
    appkey: 'your_app_key', 
    channel: 'your_channel'
}, function () {
    alert("友盟API初始化成功");
}, function (reason) {
    alert("友盟API初始化失败");
});
```