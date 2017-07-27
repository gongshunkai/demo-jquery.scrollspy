<h2># demo-jquery.scrollspy v1.0</h2>
<p>jquery插件 ( 滚动监听  ) - jquery.scrollspy v1.0</p>
<p><b>演示地址：</b><a href="https://gongshunkai.github.io/demo/%E9%94%9A%E7%82%B9%E5%AE%9A%E4%BD%8D%E5%9E%82%E7%9B%B4%E6%BB%9A%E5%8A%A8/demo-scrollspy.html">https://gongshunkai.github.io/demo/%E9%94%9A%E7%82%B9%E5%AE%9A%E4%BD%8D%E5%9E%82%E7%9B%B4%E6%BB%9A%E5%8A%A8/demo-scrollspy.html</a></p>
<p><b>使用方法：</b></p>
<p><strong>一、监听浏览器窗口的滚动条就把配置参数写在body标签上</strong></p>
<p>&#60;body data-spy="scroll" data-target="#navbar-example" data-offset="0"&#62;</p>
<p>&#60;div id="navbar-example"&#62;<br>
  &#60;ul class="nav nav-tabs"&#62;<br>
  &#60;li&#62;&#60;a href="#a1"&#62;标题1&#60;/a&#62;&#60;/li&#62;<br>
  &#60;li&#62;&#60;a href="#a2"&#62;标题2&#60;/a&#62;&#60;/li&#62;<br>
  &#60;li&#62;&#60;a href="#a3"&#62;标题3&#60;/a&#62;&#60;/li&#62;
  <br>
  &#60;li&#62;&#60;a href="#a4"&#62;标题4&#60;/a&#62;&#60;/li&#62;
  <br>
  &#60;li&#62;&#60;a href="#a5"&#62;标题5&#60;/a&#62;&#60;/li&#62;<br>
  &#60;/ul&#62;
  <br>
  &#60;/div&#62;</p>
<p> &#60;div class="content"&#62;
  <br>
  &#60;div id="a1"&#62;
  &#60;h2&#62;标题1&#60;/h2&#62;
  &#60;/div&#62;<br>
  &#60;div id="a2"&#62;
  &#60;h2&#62;标题2&#60;/h2&#62;
  &#60;img src="http://www.lens-me.com/lensme/cl/cl-265s1.jpg"&#62;
  &#60;/div&#62;<br>
  &#60;div id="a3"&#62;
  &#60;h2&#62;标题3&#60;/h2&#62;
  &#60;/div&#62;<br>
  &#60;div id="a4"&#62;
  &#60;h2&#62;标题4&#60;/h2&#62;
  &#60;/div&#62;<br>
  &#60;div id="a5"&#62;
  &#60;h2&#62;标题5&#60;/h2&#62;
  &#60;/div&#62;<br>
  &#60;/div&#62;</p>
<p>//初始化<br>
$('body').scrollspy();</p>
<p>//每当一个新条目被激活后都将由滚动监听插件触发此事件。<br>
  $('#a1').on('activate.scrollspy',function(){<br>
console.log('#a1');<br>
});<br>
$('#a2').on('activate.scrollspy',function(){<br>
console.log('#a2');<br>
});<br>
$('#a3').on('activate.scrollspy',function(){<br>
console.log('#a3');<br>
});<br>
$('#a4').on('activate.scrollspy',function(){<br>
console.log('#a4');<br>
});<br>
$('#a5').on('activate.scrollspy',function(){<br>
console.log('#a5');<br>
});</p>
<p>&nbsp;</p>
<p>//当使用滚动监听插件的同时在 DOM 中添加或删除元素后，你需要像下面这样调用此刷新方法：<br>
$('[data-spy=&quot;scroll&quot;]').each(function () {<br>
var $spy = $(this).scrollspy('refresh');<br>
});</p>
<p>&nbsp;</p>
<p><strong>二、监听元素的滚动条就把配置参数写在元素标签上</strong></p>
<p>&lt;div id=&quot;navbar-example2&quot;&gt;<br>
&lt;ul class=&quot;nav nav-tabs&quot;&gt;<br>
&lt;li&gt;&lt;a href=&quot;#b1&quot;&gt;标题1&lt;/a&gt;&lt;/li&gt;<br>
&lt;li&gt;&lt;a href=&quot;#b2&quot;&gt;标题2&lt;/a&gt;&lt;/li&gt;<br>
&lt;li&gt;&lt;a href=&quot;#b3&quot;&gt;标题3&lt;/a&gt;&lt;/li&gt;<br>
&lt;li&gt;&lt;a href=&quot;#b4&quot;&gt;标题4&lt;/a&gt;&lt;/li&gt;<br>
&lt;li&gt;&lt;a href=&quot;#b5&quot;&gt;标题5&lt;/a&gt;&lt;/li&gt;<br>
&lt;/ul&gt;<br>
&lt;/div&gt;</p>
<p><br>
  &lt;div id=&quot;content2&quot; class=&quot;content&quot; data-spy=&quot;scroll&quot; data-target=&quot;#navbar-example2&quot;&gt;<br>
  &lt;div id=&quot;b1&quot;&gt;&lt;h2&gt;标题1&lt;/h2&gt;&lt;/div&gt;<br>
  &lt;div id=&quot;b2&quot;&gt;&lt;h2&gt;标题2&lt;/h2&gt;&lt;img src=&quot;http://www.lens-me.com/lensme/cl/cl-267s1.jpg&quot;&gt;&lt;/div&gt;<br>
  &lt;div id=&quot;b3&quot;&gt;&lt;h2&gt;标题3&lt;/h2&gt;&lt;/div&gt;<br>
  &lt;div id=&quot;b4&quot;&gt;&lt;h2&gt;标题4&lt;/h2&gt;&lt;/div&gt;<br>
  &lt;div id=&quot;b5&quot;&gt;&lt;h2&gt;标题5&lt;/h2&gt;&lt;/div&gt;<br>
  &lt;/div&gt;</p>
<p>//初始化<br>
  $('#content2').scrollspy();</p>