# WEB
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
<title>无标题文档</title>
<style type="text/css">
<!--
body {
	font: 100%/1.4 Verdana, Arial, Helvetica, sans-serif;
	background-color: #4E5869;
	margin: 0;
	padding: 0;
	color: #000;
}

/* ~~ 元素/标签选择器 ~~ */
ul, ol, dl { /* 由于浏览器之间的差异，最佳做法是在列表中将填充和边距都设置为零。为了保持一致，您可以在此处指定需要的数值，也可以在列表所包含的列表项（LI、DT 和 DD）中指定需要的数值。请注意，除非编写一个更为具体的选择器，否则您在此处进行的设置将会层叠到 .nav 列表。 */
	padding: 0;
	margin: 0;
}
h1, h2, h3, h4, h5, h6, p {
	margin-top: 0;	 /* 删除上边距可以解决边距会超出其包含的 div 的问题。剩余的下边距可以使 div 与后面的任何元素保持一定距离。 */
	padding-right: 15px;
	padding-left: 15px; /* 向 div 内的元素侧边（而不是 div 自身）添加填充可避免使用任何方框模型数学。此外，也可将具有侧边填充的嵌套 div 用作替代方法。 */
}
a img { /* 此选择器将删除某些浏览器中显示在图像周围的默认蓝色边框（当该图像包含在链接中时） */
	border: none;
}

/* ~~ 站点链接的样式必须保持此顺序，包括用于创建悬停效果的选择器组在内。 ~~ */
a:link {
	color:#414958;
	text-decoration: underline; /* 除非将链接设置成极为独特的外观样式，否则最好提供下划线，以便可从视觉上快速识别 */
}
a:visited {
	color: #4E5869;
	text-decoration: underline;
}
a:hover, a:active, a:focus { /* 此组选择器将为键盘导航者提供与鼠标使用者相同的悬停体验。 */
	text-decoration: none;
}

/* ~~ 此容器包含所有其它 div，并依百分比设定其宽度 ~~ */
.container {
	width: 80%;
	max-width: 1260px;/* 可能需要最大宽度，以防止此布局在大型显示器上过宽。这将使行长度更便于阅读。IE6 不遵循此声明。 */
	min-width: 780px;/* 可能需要最小宽度，以防止此布局过窄。这将使侧面列中的行长度更便于阅读。IE6 不遵循此声明。 */
	background-color: #FFF;
	margin: 0 auto; /* 侧边的自动值与宽度结合使用，可以将布局居中对齐。如果将 .container 宽度设置为 100%，则不需要此设置。 */
}

/* ~~ 标题未指定宽度。它将扩展到布局的完整宽度。标题包含一个图像占位符，该占位符应替换为您自己的链接徽标 ~~ */
.header {
	background-color: #6F7D94;
}

/* ~~ 以下是此布局的列。 ~~ 

1) 填充只会放置于 div 的顶部和/或底部。此 div 中的元素侧边会有填充。这样，您可以避免使用任何“方框模型数学”。请注意，如果向 div 自身添加任何侧边填充或边框，这些侧边填充或边框将与您定义的宽度相加，得出 *总计* 宽度。您也可以选择删除 div 中的元素的填充，并在该元素中另外放置一个没有任何宽度但具有设计所需填充的 div。

2) 由于这些列均为浮动列，因此未对其指定边距。如果必须添加边距，请避免在浮动方向一侧放置边距（例如：div 中的右边距设置为向右浮动）。在很多情况下，都可以改用填充。对于必须打破此规则的 div，应向该 div 的规则中添加“display:inline”声明，以控制某些版本的 Internet Explorer 会使边距翻倍的错误。

3) 由于可以在一个文档中多次使用类（并且一个元素可以应用多个类），因此已向这些列分配类名，而不是 ID。例如，必要时可堆叠两个侧栏 div。您可以根据个人偏好将这些名称轻松地改为 ID，前提是仅对每个文档使用一次。

4) 如果您更喜欢在右侧（而不是左侧）进行导航，只需使这些列向相反方向浮动（全部向右，而非全部向左），它们将按相反顺序显示。您无需在 HTML 源文件中移动 div。

*/
.sidebar1 {
	float: left;
	width: 20%;
	background-color: #93A5C4;
	padding-bottom: 10px;
}
.content {
	padding: 10px 0;
	width: 80%;
	float: left;
}

/* ~~ 此分组的选择器为 .content 区域中的列表提供了空间 ~~ */
.content ul, .content ol { 
	padding: 0 15px 15px 40px; /* 此填充反映上述标题和段落规则中的右填充。填充放置于下方可用于间隔列表中其它元素，置于左侧可用于创建缩进。您可以根据需要进行调整。 */
}

/* ~~ 导航列表样式（如果选择使用预先创建的 Spry 等弹出菜单，则可以删除此样式） ~~ */
ul.nav {
	list-style: none; /* 这将删除列表标记 */
	border-top: 1px solid #666; /* 这将为链接创建上边框 – 使用下边框将所有其它项放置在 LI 中 */
	margin-bottom: 15px; /* 这将在下面内容的导航之间创建间距 */
}
ul.nav li {
	border-bottom: 1px solid #666; /* 这将创建按钮间隔 */
}
ul.nav a, ul.nav a:visited { /* 对这些选择器进行分组可确保链接即使在访问之后也能保持其按钮外观 */
	padding: 5px 5px 5px 15px;
	display: block; /* 这将为链接赋予块属性，使其填满包含它的整个 LI。这样，整个区域都可以响应鼠标单击操作。 */
	text-decoration: none;
	background-color: #8090AB;
	color: #000;
}
ul.nav a:hover, ul.nav a:active, ul.nav a:focus { /* 这将更改鼠标和键盘导航的背景和文本颜色 */
	background-color: #6F7D94;
	color: #FFF;
}

/* ~~ 脚注 ~~ */
.footer {
	padding: 10px 0;
	background-color: #6F7D94;
	position: relative;/* 这可以使 IE6 hasLayout 以正确方式进行清除 */
	clear: both; /* 此清除属性强制 .container 了解列的结束位置以及包含列的位置 */
}

/* ~~ 其它浮动/清除类 ~~ */
.fltrt {  /* 此类可用于在页面中使元素向右浮动。浮动元素必须位于其在页面上的相邻元素之前。 */
	float: right;
	margin-left: 8px;
}
.fltlft { /* 此类可用于在页面中使元素向左浮动。浮动元素必须位于其在页面上的相邻元素之前。 */
	float: left;
	margin-right: 8px;
}
.clearfloat { /* 如果从 #container 中删除或移出了 #footer，则可以将此类放置在 <br /> 或空 div 中，作为 #container 内最后一个浮动 div 之后的最终元素 */
	clear:both;
	height:0;
	font-size: 1px;
	line-height: 0px;
}
-->
</style><!--[if lte IE 7]>
<style>
.content { margin-right: -1px; } /* 此 1px 负边距可以放置在此布局中的任何列中，且具有相同的校正效果。 */
ul.nav a { zoom: 1; }  /* 缩放属性将为 IE 提供其需要的 hasLayout 触发器，用于校正链接之间的额外空白 */
</style>
<![endif]--></head>

<body>

<div class="container">
  <div class="header"><a href="#"><img src="" alt="在此处插入徽标" name="Insert_logo" width="20%" height="90" id="Insert_logo" style="background-color: #8090AB; display:block;" /></a> 
    <!-- end .header --></div>
  <div class="sidebar1">
    <ul class="nav">
      <li><a href="#">链接一</a></li>
      <li><a href="#">链接二</a></li>
      <li><a href="#">链接三</a></li>
      <li><a href="#">链接四</a></li>
    </ul>
    <p> 以上链接说明了一种基本导航结构，该结构使用以 CSS 设置样式的无序列表。请以此作为起点修改属性，以生成您自己的独特外观。如果需要弹出菜单，请使用 Spry 菜单、Adobe Exchange 中的菜单构件 或其它各种 javascript 或 CSS 解决方案创建您自己的菜单。</p>
    <p>如果您想要在顶部进行导航，只需将 ul.nav 移到页面顶部并重新创建样式即可。</p>
    <!-- end .sidebar1 --></div>
  <div class="content">
    <h1>说明</h1>
    <p>请注意，这些布局的 CSS 带有大量注释。如果您的大部分工作都在设计视图中进行，请快速浏览一下代码，获取有关如何使用液态布局 CSS 的提示。您可以先删除这些注释，然后启动您的站点。要了解有关这些 CSS 布局中使用的方法的更多信息，请阅读 Adobe 开发人员中心上的以下文章：<a href=http://www.adobe.com/go/adc_css_layouts">http://www.adobe.com/go/adc_css_layouts</a>。</p>
    <h2>清除方法</h2>
    <p>由于所有列都是浮动的，因此，此布局在 .footer 规则中采用 clear:both 声明。此清除方法强制使 .container 了解列的结束位置，以便显示在 .container 中放置的任何边框或背景颜色。如果您的设计要求您从 .container 中删除 .footer，则需要采用其它清除方法。最可靠的方法是在最后一个浮动列之后（但在 .container 结束之前）添加 &lt;br class="clearfloat" /&gt; or &lt;div class="clearfloat"&gt;&lt;/div&gt;。这具有相同的清除效果。</p>
    <h3>徽标替换</h3>
    <p>此布局的 .header 中使用了图像占位符，您可能希望在其中放置徽标。建议您删除此占位符，并将其替换为您自己的链接徽标。 </p>
    <p> 请注意，如果您使用属性检查器导航到使用 SRC 字段的徽标图像（而不是删除并替换占位符），则应删除内嵌背景和显示属性。这些内嵌样式仅用于在浏览器中出于演示目的而显示徽标占位符。 </p>
    <p>要删除内嵌样式，请确保将 CSS 样式面板设置为“当前”。选择图像，然后在“CSS 样式”面板的“属性”窗格中右键单击并删除显示和背景属性。（当然，您始终可以直接访问代码，并在其中删除图像或占位符的内嵌样式。）</p>
    <h4>Internet Explorer 条件注释</h4>
    <p>这些液态布局包含 Internet Explorer 条件注释 (IECC)，用于更正两个问题。 </p>
    <ol>
      <li>在基于百分比的布局中，浏览器在舍入 div 大小方面不一致。如果浏览器必须呈现诸如 144.5px 或 564.5px 之类的数字，则必须将这些数字舍入到最接近的整数。Safari 和 Opera 向下舍入，Internet Explorer 向上舍入，而 Firefox 向上舍入一列，然后再向下舍入一列，以便完全填充容器。这些舍入问题可能导致某些布局出现不一致。此 IECC 提供了用于修复 IE 的 1px 负边距。您可以将其移至任何列（以及左侧或右侧），以满足您的布局需求。</li>
      <li>由于在某些情况下 IE6 和 IE7 中会呈现额外的空白，因此已向导航列表中的锚记添加缩放属性。缩放将为 IE 提供其专用的 hasLayout 属性来修复此问题。</li>
    </ol>
    <h4>背景</h4>
    <p>本质上，任何 div 中的背景颜色将仅显示与内容一样的长度。这意味着，如果要使用背景颜色或边框创建侧面列的外观，将不会一直扩展到脚注，而是在内容结束时停止。如果 .content div 将始终包含更多内容，则可以在 .content div 中放置一个边框将其与列分开。</p>
    <!-- end .content --></div>
  <div class="footer">
    <p>此 .footer 包含 position:relative 声明，以便为 .footer 指定 Internet Explorer 6 hasLayout，并使其以正确方式清除。如果您不需要支持 IE6，则可以将其删除。</p>
    <!-- end .footer --></div>
  <!-- end .container --></div>
</body>
</html>
