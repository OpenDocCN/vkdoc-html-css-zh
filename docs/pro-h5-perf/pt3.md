# 第三部分：建立一个网站

<!-- ch 6~18 -->

在本节中，我们将在第二章到第五章中给出的所有性能建议应用到一个实际的网站(`[`clikz.us`](http://clikz.us)`)。因为电子商务网站通常比博客或新闻列表需要更复杂的布局，所以我们以电子商务网站为例。此外，当我们构思这本书时，我们正在为一家非常大的电子商务公司工作，这就是我们心中的问题。

本节由两个小节组成。第一个是第六章到第九章，处理出现在每个页面上的元素:HTML 样板文件、导航元素、标题和页脚。

首先，我们展示如何创建页面模板。我们使用`[`www.html5boilerplate.com`](http://www.html5boilerplate.com)`来获得一个包含许多有用选项的基础页面。然后，我们通过条件语句让事情在各种版本的 Internet Explorer 上正常工作。我们还处理其他细节，比如处理兼容模式、加载 jQuery 和添加 Google Analytics。最后，我们设置了站点的网格，用来控制页面各个部分的位置。

然后我们讨论为什么一个网站应该为不同议程的访问者提供不同种类的导航。然后我们展示如何创建两种不同的导航。我们从菜单开始，为那些喜欢浏览他们想要的东西的访问者。然后，我们在菜单上添加一个搜索框，供那些喜欢搜索而不是浏览的人使用。我们还讨论了如何让我们的导航在不支持 CSS3 甚至不支持 JavaScript 的浏览器上工作。

接下来是为每一页的顶部创建一个报头。在冒险之前，我们先处理一个常见的问题:国家选择器。虽然我们自己的站点没有使用国家选择器，但是我们展示了如何让国家选择器尽可能好地运行。我们使用一个绝对定位元素的列表来创建我们的报头，并讨论如何使用 CSS 剪辑来处理部分图像。最后，我们给出关于报头的基本建议:保持简洁。

然后我们处理如何为我们的网站制作页脚。重用我们菜单中的内容(第七章)，我们把它变成一个位于页面底部的站点地图。然后我们添加法律块。在这个过程中，我们讨论了为什么 SVG 是其他图像格式的一个很好的替代品。然后，我们演示如何用 SVG 创建一个图像(我们将在本书的剩余部分使用它),以及如何通过 JavaScript 与 SVG 图像进行交互。

第二小节处理构建我们在整个示例站点中重用的控件。我们引入了“分形”设计模式的概念——在这种模式中，复杂的控件由简单的控件组成。每个控件实际上都是一个带有样式表的 PHP 函数，每个控件都需要特定的 HTML 结构。通过研究每个控件，我们添加了一些您可能会发现在使用控件和进行其他 web 开发时有用的细节。

这本书的一个关键概念是分形(或嵌套)控件。我们首先讨论模式的一般特征。在讨论该模式时，我们展示了 label 控件——我们的第一个也是最简单的控件。然后是一个基于我们之前工作的案例研究(我们是在做那份工作时认识的，那份工作让我们有了写一本书的想法)。我们还将讨论何时将 CSS 与 JavaScript 分离，何时将它们结合起来(以及如何结合)。

我们接下来讨论为什么我们开发链接控件，然后展示我们是如何做的。我们详细介绍了构成控件的功能和样式。(我们添加了一个 JavaScript 组件，为不能通过 CSS 显示工具提示的浏览器提供故障转移能力。)

接下来，我们讨论为什么以及如何创建一个包含链接的盒子。我们认为边栏对于提供关于产品的补充信息是有用的，这些信息在页面的主要部分是不合适的。组成 sidebox 控件内容的链接实际上是链接控件。还记得嵌套控件的分形概念吗？sidebox 控件的链接提供了一个例子。

接下来，我们将详细解释我们的按钮控件，并包括七种不同的处理方法。正如我们在详述我们的 web 重用模式时所讨论的，我们通过从一个处理到下一个处理重用 HTML 来实践我们所宣扬的。通过改变风格，我们得到了七种不同的治疗方法。

然后我们详细介绍价格控制，这是我们最复杂的控制之一。首先，它实际上是两个控制:价格控制和运输控制。另一方面，价格控制意味着重复，以创造我们所说的“价格栈”。在描述价格和运输控制时，我们解决了一个经常被忽视的问题:如何让一行点——一个点前导——从商品的末尾到价格的开头。

然后，我们展示如何创建产品列表。同样，这个想法是通过调用一个相当简单的函数来创建一个复杂的页面组件。与任何其他控件相比，产品控件更多地使用控件中控件的范例。产品控件包含价格、运输、链接和按钮控件。此外，产品控件是第一个使用数据对象的控件，我们将其构造为 JSON 对象。

接下来，我们将介绍创建表格的控件。我们提供了两种处理方式:一种是带有标题行的表格，另一种是左侧带有标题内容的表格(可以说是标题列)。我们还创建了不使用 table、tr 和 td 元素以及使用这些元素的表。大多数浏览器可以正确显示不使用传统表格元素的表格。对于那些不能处理现代表格呈现的浏览器，我们提供了传统元素。

然后，我们继续讨论如何创建一组选项卡。我们再次提供两种处理方式，水平(浅色)和垂直(深色)。为了克服我们在许多网站上发现的选项卡的一些恼人之处，我们制作了选项卡，以便每个选项卡都可以是一个唯一的地址。这样，用户可以链接到一个单独的选项卡，并通过浏览器历史记录返回。我们还确保我们的选项卡内容正确居中，即使一个选项卡有单行标签，另一个有多行标签。最后，我们通过动画显示从一个选项卡到另一个选项卡的转换，增加了一点视觉趣味。

我们通过描述两个让我们更容易制作表单的控件来结束本书。我们定义了一个字段集控件和一个输入控件。顾名思义，fieldset 控件创建一个 fieldset 元素及其子元素(输入元素和其他内容)。输入控件创建一个支持所有可能类型(复选框、单选按钮等)的单一输入元素。).作为我们分形范例的一个例子，字段集控件使用输入控件。在这个过程中，我们展示了如何用`:before`和`:after`伪选择器创建有趣的视觉效果。最后，我们展示了一种适用于所有控件的技术:制作快捷控件。