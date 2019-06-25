# PhotoClip
移动端头像裁剪插件，图片裁剪后为base64编码

```
var boxClipHeadImg = document.getElementById('boxClipHeadImg');
var pc = new PhotoClip('#clipArea', {
	size: 260,
	outputSize: 640,
	// 分别占宽度和高度的大小
	//adaptive: ['60%', '80%'],
	file: '#file',
	view: '#view',
	ok: '#clipBtn',
	//img: 'img/mm.jpg',
	loadStart: function() {
		console.log('开始读取照片');
	},
	loadComplete: function() {
		console.log('照片读取完成');
		boxClipHeadImg.style.display = 'block';
	},
	done: function(dataURL) {
		console.log(dataURL);
	},
	fail: function(msg) {
		alert(msg);
	}
});

```