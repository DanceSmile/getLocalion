# getLocalion
html5网页获取地理位置

HTML5 Geolocation API (地理位置应用程序接口)

目前PC浏览器支持情况：

Firefox 3.5+
Chrome 5.0+
Safari 5.0+
Opera 10.60+
Internet Explorer 9.0+

手机支持情况：

>Android 2.0+
iPhone 3.0+
Opera Mobile 10.1+
Symbian (S60 3rd & 5th generation)
Blackberry OS 6
Maemo

## 检测浏览器是否支持

```
if(navigator.geolocation){
    console.log("浏览器支持");
}else{
    console.log("浏览器不支持");
}
```
## navigator.geolcation 对象下面 提供了三个方法

```
//获取用户当前位置
navigator.geolocation.getCurrentPosition(onsuccess,onerror,option);

//监听用户位置  持续获取用户当前位置
navigator.geolocation.watchCurrentPosition(onsuccess,onerror,option)


//取消监听
navigator.geolocation.clearWatch(watchID)

```



