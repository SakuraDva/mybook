###video标签

|属性|说明|
|:-  |:-  |
|autopaly|加载完后自动播放|
|heigth|设置视频的高度|
|width|设置视频的宽度|
|controls|浏览器显示播放控件（控制台）|
|poster|用户点击播放前显示的图片|
|loop|视频播放完后再次播放|
|src|要播放的视频的地址|
|preload|如果出现该属性，则视频在页面加载时进行加载，并预备播放。如果使用 "autoplay"，则忽略该属性。|
|muted|规定视频的音频输出应该被静音。|

#支持的格式分析
|类型|说明|
|:-  |:-   |
|mp4|MPEG-4/H.264   必须要注意视频编码为H264，否则浏览器会不识别|
|flv|原生不支持|
|webm|网络视频格式(只有谷歌和火狐和Edge支持)|
|ogg|只有谷歌和火狐支持|


```html
<video controls>
	 <source  src="media/music.mp3" type="audio/mp3"/>
	 <source  src="media/video.mp4" type="video/mp4"/>
</video>
```

#例子
<video src="../../media/video.mp4" type="video/mp4" controls />
#心得
1.它是一个用来装影视的一个元素
