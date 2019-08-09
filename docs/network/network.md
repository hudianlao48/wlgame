# 网络

## wlgame.network.type

获取网络类型

```javascript
wlgame.network.type

// 返回值是wifi或者4G或者EDGE
```

## onPingChange

监听网络延迟

```javascript
const ad = wlgame.onPingChange(function (ping) {
		// 当前网络的延迟
	});
```