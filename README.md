# getLocation

html5网页获取地理位置


HTML5 Geolocation API (地理位置应用程序接口)

## 目前PC浏览器支持情况：Location
Location
>Firefox 3.5+
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
if ( navigator.geolocation ) {
    console.log("浏览器支持");
}else{
    console.log("浏览器不支持");
}

```




## navigator.geolcation 对象下面 提供了三个方法

```
//获取用户当前位置
navigator.geolocation.getCurrentPosition(onSuccess,onError,option);

//监听用户位置  持续获取用户当前位置
navigator.geolocation.watchPosition(onSuccess,onError,option)

//取消监听
navigator.geolocation.clearWatch(watchID)

```

### onSuccess , onError , option  参数说明

```
//onSuccess方法成功时调用的(必选)，onError方法失败是调用的(可选)，options其他参数(可选)

//onSuccess 的 属性值有很多 ，常用的有获取坐标的经纬度

function onSuccess(positon){

    //返回用户位置
    //经度
    var longitude = position.coords.longitude;
    //纬度
    var latitude       = position.coords.latitude;

}

options = {
     enableHighAccuracy,　　　//boolean 是否要求高精度的地理信息
     timeout,　　　　　　　　　//表示等待响应的最大时间，默认是0毫秒，表示无穷时间
     maximumAge　　　　　　　　//应用程序的缓存时间
}

```

> 获取当前位置加上偏移量会准一点 <br>
> 经度+经度校正值： 0.008774687519; <br>
> 纬度+纬度校正值： 0.00374531687912;<br>
> doc  By DanceSmile<br>








