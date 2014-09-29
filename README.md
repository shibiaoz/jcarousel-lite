###demo地址
 [demo地址](http://www.gmarwaha.com/jquery/jcarousellite/demo.php#demo1)
 *http://www.gmarwaha.com/jquery/jcarousellite/demo.php#demo1*
###config
```step 1 you need to import the necessary js lib jquery && jcarousellite
    <script type="text/javascript" src="../jquery.js"></script>
	<script type="text/javascript" src="jquery.jcarousellite.js"></script>
```
```html layout
<div class="slide_wraper">
		<div class="jcarousel carousel_wraper">
			<ul>
				<li><img src="img1.jpg" width="300" height="200" ></li>
				<li><img src="img2.jpg" width="300" height="200"></li>
				<li><img src="img3.jpg" width="300" height="200"></li>
				<li><img src="img4.jpg" width="300" height="200"></li>
			</ul>
		</div>
		<span class="one">1</span>
		<span  class="two">2</span>
		<span class="three">3</span>
		<button class="prev j_prev">	&laquo;</button>
		<button class="next j_next">	&raquo;</button>	
	</div>
```
```you can set html some css style ,but not necessary
    .slide_wraper{
			width: 1200px;
			height: 400px;
			overflow: hidden; 
			position: relative;
		}
		.slide_wraper button{
			position: absolute;
			z-index: 2;
			top: 20%;
		}
		.slide_wraper span{
			cursor:pointer;
		}
		.slide_wraper .prev{
			left: 0;
		}
		.slide_wraper .next{
			right: 0;
		}
```
``` the last step is run config and run the jcarousellite
$(function  () {
			 $(".jcarousel").jCarouselLite({
		        btnNext: ".j_next",//上一个
		        btnPrev: ".j_prev",//下一个
				btnGo: ['.one','.two','.three'],//切换到第多少个itme
		       // auto:2000,//每隔1000ms自动切换
		        speed:500,//动画的效果	
				circular:true,//上一个、下一个是否是可循环的 ，默认是true
				visible:2,//显示几个item，默认是3个
				scroll:2,//切换的个数默认是1
				vertical:false,//是水平切花还是上下切换，默认好似false
		    });
		});
```
