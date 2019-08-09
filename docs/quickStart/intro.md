# 初始化

## 步骤1：引入JS文件

在需要调用JS接口的页面引入如下JS文件，（支持https）:

http://domain/wlgamebridge.js

## 步骤2：通过config接口注入权限验证配置

```javascript
wlgame.config({
    debug: true, // 开启调试模式,调用的所有api的返回值会在客户端alert出来，若要查看传入的参数，可以在pc端打开，参数信息会通过log打出，仅在pc端时才会打印。
    appId: '', // 必填，app唯一标识
    timestamp: , // 必填，生成签名的时间戳
    nonceStr: '', // 必填，生成签名的随机串
    signature: '',// 必填，签名，见附录1
    jsApiList: [] // 必填，需要使用的JS接口列表，所有JS接口列表见附录2
});
```

## 步骤3：通过ready接口处理成功验证
```javascript
wlgame.ready(function({userInfo}){
    /* config信息验证后会执行ready方法，所有接口调用都必须在config接口获得结果之后，config是一个客户端的异步操作，所以如果需要在页面加载时就调用相关接口，则须把相关接口放在ready函数中调用来确保正确执行。对于用户触发时才调用的接口，则可以直接调用，不需要放在ready函数中。*/

    // userInfo 为用户相关信息

});
```

## 步骤4：通过error接口处理失败验证
```javascript
wlgame.error(function(res){
    // config信息验证失败会执行error函数，如签名过期导致验证失败，具体错误信息可以打开config的debug模式查看，也可以在返回的res参数中查看，对于SPA可以在这里更新签名。
});
```