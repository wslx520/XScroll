## XScroll.js，图片切换

支持5种基本切换效果，但后4种效果分别有上下左右4个方向

[在线示例页](http://jo2.org/htmls/XScroll/XScroll.htm)

### 使用方法：

**html结构**

	<div class="container" id="idContainer2">

		<ul id="idSlider2">
			<li><a href="http://jo2.org/"><img src="images/s1.jpg"/></a></li>
			<li><a href="http://jo2.org/"><img src="images/s2.jpg"/></a></li>
			<li><a href="http://jo2.org/"><img src="images/s3.jpg"/></a></li>
			<li><a href="http://jo2.org/"><img src="images/s4.jpg"/></a></li>
		</ul>
		<ul id="slider2p" class="num">
			<li class="on">1</li>
			<li>2</li>
			<li>3</li>
			<li>4</li>
		</ul>
	</div>
**JS代码**：

	var xscroll = XScroll('idSlider2',{auto:3000,how:4, direct:1,Tween:Tween.CircOut,pager:'slider2p'});

第一个参数是id，第二个参数是选项设置

### 参数说明：

**how**:切换效果

0淡入淡出，

1两张图片同时滚动，

2当前图片不动，下一张图片覆盖上来，

3当前图片飞走，显示出下一张；

4当前图片与下一张图片反向拉伸，然后回切，完成切换.

**direct**:方向，

值为0123，分别表示左上右下，默认为0.在**how参数不为0时**有效

**delay**:自动滚动间隔时间。默认为4000

**step**:滚动步长。当滚动方向是水平时，step会默认为slider元素的offsetWidth；当滚动方向是垂直时，则默认为offsetHeight。当然，也可以自己设置

**pager**:

值应该是一个元素的id,指定slider的页码翻页元素。指定后XScroll会为此标签的第一层子元素添加跳转函数

**Tween**:

缓动公式，如easeIn,easeInOut之类的，具体参考Tween.js里的写法