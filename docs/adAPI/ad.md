# 激励视频广告

激励视频广告组件是由客户端原生的图片、文本、视频控件组成的，层级最高，会覆盖在 Canvas 上。

```javascript
// 播放激励视频广告
wlGameBridge.playAd({
	customParams: '' // 游戏自主选择上报广告播放的参数，用于后台统计时候的筛选和分析，bridge不做处理，直接上报。
});

// 监听广告播放结果
window.addEventListener('adPlaySuccess', (e) => {
    if(e){
        // 广告成功播放，游戏内逻辑自选，可以解锁关卡，奖励生命，获得道具等等。
    }
});
window.addEventListener('adPlayError', (e) => {
    if(e){
        // 用户没有正常看完激励视频广告，游戏内逻辑自选
    }
});

```