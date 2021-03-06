### 说明  
  
#### `rem.html`：手机版响应式网页文件结构(采用相对单位rem)  
* 说明：rem是相对单位，相对于根元素html，root em。  
* 页面基于750px设计稿，但兼容多种尺寸移动设备。  
* html{font-size:100px;}为参照，方便计算rem值，如body的width为：7.5rem，设计稿的横向分辨率/`100`。  
* `除了html根节点的font-size使用px单位外，其他css尺寸尽量使用rem单位`思想(如果确实要用px单位，可以跟媒介查询挂钩)。  
* 屏幕旋转或屏幕大小发生变化后会自动调整  
* device-width的计算公式为：设备的物理分辨率/(devicePixelRatio * scale)，设备像素比devicePixelRatio高清屏一般都是2。  
  
#### `web.html`：电脑常用网页文件结构  
  
#### `mob.html`：手机常用网页文件结构  
  
#### `head.md`：网页head(含常用meta标签)  
  
本项目Sublime Text代码编辑器snippet已完成 [https://github.com/wuyumin/SublimeText3/tree/master/UserSnippet](https://github.com/wuyumin/SublimeText3/tree/master/UserSnippet)  
  
#### 链接建议使用“相对协议”  
相对协议，也就是链接以`//`开头，前面去掉了`http:`或`https:`字样，这样做的好处是浏览器能够根据你的网站当前所采用的协议来加载服务器上的文件，这样无论今后是采用 http 还是 https 协议，都不用再次修改文件的链接地址了。
	
#### `微信分享显示缩略图`：非采用JS-SD形式  
图片的尺寸是有要求的，长和宽都要300px及以上。  
```html
<div style="display:none;">
	<img src="/wechat_share.png" alt="">
</div>
```
另外，微信获取缩略图是按代码的顺序来的，获取到第一张符合要求的图片后就调用了，所以微信分享这段代码置放的顺序会影响缩略图效果。我一般做法是首页放在body标签段最前面，列表页和详情页放在body标签段结束前(这样方便微信先拿其他符合要求的图片，这个图当作备用) 。  
  
如果出现什么问题或有什么建议，欢迎你在GitHub里Pull Requests或Issues一下，方便进行改进。  
