# 激励视频广告

激励视频广告组件是由客户端原生的图片、文本、视频控件组成的，层级最高，会覆盖在 Canvas 上。

```javascript
const ad = wlgame.createRewardedVideoAd({
	success: function () {
		// 播放完成的回调
	},
	error: function (err) {
		// 未加载成功的回调
	}
});
```