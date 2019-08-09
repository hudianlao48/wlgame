# 媒体

## 获取摄像头和麦克风内容
```javascript
wlgame.getUserMedia({
	audio: true,
	video:{ 'facingMode': "user" },
	// 后置摄像头参数： video: { facingMode: { exact: "environment" } }
	success: function (steam) {
		// 成功获取摄像头和麦克风内容
	},
	error: function (error) {
		// 获取失败
	}
})
```