<p>效果图这样子的</p>
<img src="http://images.cnblogs.com/cnblogs_com/ihqn19/856534/o_QQ%e6%88%aa%e5%9b%be20160722115754.jpg" width="450" />

<p>点击小图，则切换大图的地址。小图配有左右切换的按钮。并且单击右边的小图会自己滚动。</p>

<p>使用方法</p>
<p>new Silde( {'wrap': $('.j-slide-box') } )</p>

<p>参数说明：</p>
 <p> option为对象。</p>
 <p> option.wrap 为整个运行都包含的大容器，避免跟其它混淆 为jQ节点$()</p>
 <p> option.box 滚动小图的容器 为jQ节点$(),不设置则使用默认.j-small-box'</p>
 <p> option.arrow 前一张后一张的指针元素 为jQ节点$(),不设置则使用默认'.j-arrow'</p>
<p>  option.class 小图交互类 为'string',不设置则使用默认'active-img'</p>
 <p> option.img   切换时需要更换src的图片元素img  为jQ节点$(),不设置则使用默认'.j-big-img'</p>
<p>其中option.wrap 为必填，其它如果不填的话会使用默认</p>



<br/>
<p>原理：</p>
<p>点击小图，则切换大图的地址  同时，当点击超容器能容纳的个数的一半时，向右滚动把后面的小图显示出来</p>
<img src="http://images.cnblogs.com/cnblogs_com/ihqn19/856534/o_QQ%E6%88%AA%E5%9B%BE20160722114738.jpg" width="450" />
<p>但这样，会有一个问题，比如当单击最后一个元素时，容器右侧会留白。所以如果滚得太远则直接使用小图总个数-容器能容纳的个数为滚动距离</p>
<img src="http://images.cnblogs.com/cnblogs_com/ihqn19/856534/o_QQ%E6%88%AA%E5%9B%BE20160722114334.jpg" width=450"" />
