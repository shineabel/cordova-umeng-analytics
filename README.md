# cordova-umeng-analytics

Cordova友盟统计插件
请使用v1.0.0版本解决了cordova iOS构建时的"UMMobClick/MobClick.h" not found错误
# 安装

运行 ```cordova plugin add https://github.com/shineabel/cordova-umeng-analytics``` 


# 使用方法

请务必在cordova ready中调用配置接口

配置API
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
开始记录页面停留
```$xslt
Umeng.Analytics.startPage('xxxPage', 
function () {
    alert("Success");
}, function (reason) {
    alert("Failed: " + reason);
});
```
结束记录页面停留
```$xslt
Umeng.Analytics.endPage('xxxPage', function () {
   alert("Success");
}, function (reason) {
   alert("Failed: " + reason);
});
```
自定义事件
```$xslt
Umeng.Analytics.logEvent({
    eventId: 'pay',
    attributes: {book:'Swfit Fundamentals'},
    num: 110
}, function () {
    alert("Success");
}, function (reason) {
alert("Failed: " + reason);
});
```
打开或关闭调试
```$xslt
Umeng.Analytics.setDebug(true, function () {
   alert("Success");
}, function (reason) {
   alert("Failed: " + reason);
});
```
