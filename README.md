# cordova-umeng-analytics

Cordova友盟统计插件
请使用v1.0.0版本，解决了cordova iOS构建时的"UMMobClick/MobClick.h" not found错误
# 安装

运行 ```cordova plugin add https://github.com/shineabel/cordova-umeng-analytics``` 


# 使用方法


```Javascript
Umeng.Analytics.config({
    appkey: 'your_app_key', 
    channel: 'your_channel'
}, function () {
    console.log("umeng init success");
}, function (err) {
    console.error("umeng init failed",err);
});
```