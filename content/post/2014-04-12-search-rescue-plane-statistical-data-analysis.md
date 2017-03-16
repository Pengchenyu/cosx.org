---
title: 失联搜救中的统计数据分析
date: '2014-04-12T13:48:15+00:00'
author: COS编辑部
categories:
  - 推荐文章
  - 统计之都
tags:
  - 众包
  - 可视化
  - 失联搜救
  - 统计数据分析
  - 群体智慧
  - 贝叶斯
slug: search-rescue-plane-statistical-data-analysis
---

> 大数据时代如何活用数据可视化、大数据与众包、群体智慧、贝叶斯方法等为失联搜救出谋献策？请看下文。

作者：统计之都创作小组（code99）

**引子**

“MH370”作为航班代码，是近日震惊世界的马来西亚航空公司客机失去联络事件（后简称“马航事件”）留给公众最深刻的数字印象。时至今日，有关马航事件的调查和搜救工作仍在继续。遗憾的是直到截稿时间，MH370航班的残骸仍未找到。

在历史上的多次飞机船只等交通工具出现失联情况的突发事件中，数据的收集、分析以及信息的及时发布都在搜寻中起到过关键的作用。比如在2009年，法国航空公司曾有一架民航客机失去联络和踪迹。当时，有不少基于数据分析的文献为失事飞机的搜寻提供了援助。前事不忘，后事之师。本文旨在基于统计学领域的相关知识结合大众可以获知的信息来对马航事件进行了解和分析。本文秉持科普视角，试图阐述在应对马航事件过程中数据收集和数据分析所起到的作用，继而为寻找失联飞机提供一些思路。我们将以寻找失事飞机和船只的事件为线索，来梳理其中涉及到的数据分析思路，以试图减少大家的猜疑和困惑。<!--more-->

**一、信息可视化助公众了解事件**

马航事件牵动全球关注。在马航事件发生之后，很多公众几乎每天第一时间关注媒体报道——看一看飞机找到了没有。回顾在马航事件发生后各界媒体发布的图表、报告和多媒体新闻，其信息之多和繁杂致使公众没有足够时间和精力去了解事件进展。这时如果能用几张简洁明了的图表把新闻内容展示出来，往往能对公众了解事件进展起到事半功倍的效果。这就是信息可视化，或称为数据可视化。我们根据信息的内容分三部分介绍数据可视化在马航事件信息传递过程中的作用。

**直观了解事件进展**

我们或许很难用三言两语把马航事件的来龙去脉描述清楚，如果把马航事件用文字表述出来亦须耗费不少篇章。单纯的描述有时候并不利于公众了解事件。相反地，信息可视化则可直观地刻画马航事件。图1-1为马来西亚最初发布的关于马航MH370航班失联的消息。图1-2为马来西亚其后发布的马航MH370航班被侦察到的地理坐标。图1-3为最终被搜救队伍估计的马航MH370航班最后一次向卫星传出信号的可能位置。三幅图通过把相关地理位置刻画在二维平面，并且把关键的时间、地点、区域在二维平面标明，使得公众可以很直观地了解马航事件，非常有效地、避免误导地传递了关键信息。公众甚至无需阅读图中注释即可了解马航事件梗概。

[<img class="aligncenter size-full wp-image-9729" alt="clues1-clues1-0副本" src="http://cos.name/wp-content/uploads/2014/04/clues1-clues1-0副本.png" width="900" height="305" srcset="http://cos.name/wp-content/uploads/2014/04/clues1-clues1-0副本.png 900w, http://cos.name/wp-content/uploads/2014/04/clues1-clues1-0副本-300x101.png 300w, http://cos.name/wp-content/uploads/2014/04/clues1-clues1-0副本-500x169.png 500w" sizes="(max-width: 900px) 100vw, 900px" />](http://cos.name/wp-content/uploads/2014/04/clues1-clues1-0副本.png)

<p align="center">
  <strong>图1-1 马航MH370客机首次宣告失联</strong>
</p>

[<img class="aligncenter size-full wp-image-9730" alt="clues2-clues2-0副本" src="http://cos.name/wp-content/uploads/2014/04/clues2-clues2-0副本.png" width="900" height="305" srcset="http://cos.name/wp-content/uploads/2014/04/clues2-clues2-0副本.png 900w, http://cos.name/wp-content/uploads/2014/04/clues2-clues2-0副本-300x101.png 300w, http://cos.name/wp-content/uploads/2014/04/clues2-clues2-0副本-500x169.png 500w" sizes="(max-width: 900px) 100vw, 900px" />](http://cos.name/wp-content/uploads/2014/04/clues2-clues2-0副本.png)

<p align="center">
  <strong>图1-2 马航MH370客机关键坐标</strong>
</p>

[<img class="aligncenter size-full wp-image-9757" alt="clues3-clues3-0副本" src="http://cos.name/wp-content/uploads/2014/04/clues3-clues3-0副本1.png" width="900" height="644" srcset="http://cos.name/wp-content/uploads/2014/04/clues3-clues3-0副本1.png 900w, http://cos.name/wp-content/uploads/2014/04/clues3-clues3-0副本1-300x214.png 300w, http://cos.name/wp-content/uploads/2014/04/clues3-clues3-0副本1-500x357.png 500w" sizes="(max-width: 900px) 100vw, 900px" />](http://cos.name/wp-content/uploads/2014/04/clues3-clues3-0副本1.png)

<p align="center">
  <strong>图1-3 马航MH370客机最后一次向卫星传出信号的可能位置</strong>
</p>

**迅速了解搜救区域**

****目前，越来越多证据表明失联客机可能在印度洋中，因此，一个非常自然的疑问就是飞机残骸到底在哪里？卫星数据成为回答这个问题最受重视的信息来源。由于非专业人士很难读懂原始卫星数据，数据可视化可以帮助公众迅速了解搜救区域。图1-4展示了有关马航MH30航班的搜救区域。在图1-4中，圆点标记出疑似残骸所在的区域，圆点的颜色代表不同的发现日期。将有关疑似残骸的信息可视化到图表并配上适当的解释，可以帮助公众在短时间内了解正在被搜寻和将要被搜寻的区域以及已经搜寻到的疑似残骸。可视化方法显然比冗长的文字描述有效很多。此外，根据卫星对南印度洋上浮标的追踪数据，图1-5刻画了在3月8日至3月24日期间残骸的移动轨迹。由图1-5我们可以得到一些或能有助搜救的推测，譬如，不同区域疑似残骸的移动趋势截然不同，相比北端疑似残骸而言，南端疑似残骸向东运动的趋势更为明显等。

[<img class="aligncenter size-full wp-image-9732" alt="newdata-720-0副本" src="http://cos.name/wp-content/uploads/2014/04/newdata-720-0副本.png" width="900" height="594" srcset="http://cos.name/wp-content/uploads/2014/04/newdata-720-0副本.png 900w, http://cos.name/wp-content/uploads/2014/04/newdata-720-0副本-300x198.png 300w, http://cos.name/wp-content/uploads/2014/04/newdata-720-0副本-500x330.png 500w" sizes="(max-width: 900px) 100vw, 900px" />](http://cos.name/wp-content/uploads/2014/04/newdata-720-0副本.png)

<p align="center">
  <strong>图1-4 马航MH370客机搜救区域</strong>
</p>

[<img class="aligncenter size-full wp-image-9731" alt="buoys-720-0副本" src="http://cos.name/wp-content/uploads/2014/04/buoys-720-0副本.png" width="900" height="663" srcset="http://cos.name/wp-content/uploads/2014/04/buoys-720-0副本.png 900w, http://cos.name/wp-content/uploads/2014/04/buoys-720-0副本-300x221.png 300w, http://cos.name/wp-content/uploads/2014/04/buoys-720-0副本-500x368.png 500w" sizes="(max-width: 900px) 100vw, 900px" />](http://cos.name/wp-content/uploads/2014/04/buoys-720-0副本.png)

<p align="center">
  <strong>图1-5 疑似残骸标记物在三月八日至三月二十四日的移动轨迹</strong>
</p>

**了解搜救条件**

搜救条件，意为搜索救援行动的基础，包括搜救设备，搜救区域的气象情况等等。由于媒体报道较少，公众对搜救条件的了解相对少。事实上，大洋气象复杂，海洋的搜救条件往往比陆地的搜救条件要恶劣，因而此番搜救是一个巨大考验。图1-6的图（a）和图（b）分别描述了3月16日南印度洋的风速和浪高。在两幅图中，颜色越深的区域，风浪越小，颜色越接近白色的区域，风浪越大。综合图（a）和图（b），搜救海域位于南印度洋风浪最大区域的西北角，并且在图中部分搜救海域泛白，可见搜救条件恶劣。

[<img class="aligncenter size-full wp-image-9733" alt="sea-condition" src="http://cos.name/wp-content/uploads/2014/04/sea-condition.jpg" width="667" height="324" srcset="http://cos.name/wp-content/uploads/2014/04/sea-condition.jpg 667w, http://cos.name/wp-content/uploads/2014/04/sea-condition-300x145.jpg 300w, http://cos.name/wp-content/uploads/2014/04/sea-condition-500x242.jpg 500w" sizes="(max-width: 667px) 100vw, 667px" />](http://cos.name/wp-content/uploads/2014/04/sea-condition.jpg)

<p align="center">
  <strong>图1-6 三月十六日（a）相关搜救海域的风速；（b）相关搜救海域的浪高</strong>
</p>

**二、大数据和众包**

****当像飞机失联这样的突发事件发生时，搜索的第一步当然是要把它失联前所有的数据信息都收集在一起分析。航空公司，各国政府，各国军方的各种飞行数据，雷达数据，通讯数据都被用来帮忙。对这些数据的分析我们会在后面详细介绍。虽然，我们会理所当然地认为数据短缺似乎并不应当发生在这个大数据时代。但是，由于数据量大，数据源多，噪声大，从大数据中找到有价值的信息有可能变得更难。众包平台（Crowdsourcing）应运而生。

众包是什么呢？根据维基百科，“众包”这个概念最早出现于2005年。“外包”作为“众包”的姐妹词更为人熟知。“外包”指把工作任务交给非本公司的组织或者个人完成。“众包”，顾名思义，指把工作任务交给广大人民群众去完成。当今众包几乎都由网友完成。众包所交付的任务可以有任意的形式和内容。这些任务可以具体到找图片或编译代码，也可以是寻求一个答案或一个主意。例如，网友在知乎提问，世纪佳缘把其实际自动配对的难题放到网上作为建模竞赛，乃至有些人在微博上贴出失物照片以寻找失主，都属于广义上众包的范畴。

3月8日，DigitalGlobe公司在马航MH370航班离开马来西亚海岸几个小时后，调整了其高分辨率卫星群的位置，以获取尽可能多的图片数据。3月10日，DigitalGlobe公司把这些图片放到了众包平台Tomnod上，首个小时图片访问量达六万个。每当突发事件出现，众包平台就会推出活动专页，让热心网友在大量实时高分辨率卫星图片中寻找线索。在马航事件中，全民找飞机就是一次非常典型的众包案例。

DigitalGlobe公司卫星群中的5颗卫星，每天环绕地球75圈。这些卫星最初都用于与人道主义相关的目的。例如，如图2-1所示，这些卫星曾用于追踪上帝抵抗军在民主刚果共和国、苏丹南部以及中非共和国整个土地上的大规模动向，以预测和挫败上帝抵抗军的下一次攻击。后来这些卫星被越来越多地用于协助处理突发事件。去年，DigitalGlobe公司曾经提供覆盖了几千万平方公里的图片以寻找一架在美国爱达荷州坠毁的轻型飞机。如今，众包几乎成为了航空意外等意外事件的首要解决途径之一。一位前Tomnod员工曾表示，在马航事件发生伊始，Tomnod就收到来自美国政府的非官方请求，甚至收到来自保险公司的请求——各界都想知道关于马航事件的众包专页将何时上线。

在DigitalGlobe公司发布至Tomnod众包页面的卫星照片中，一个像素覆盖50厘米的土地空间或水域空间。 在NASA陆地卫星提供的卫星照片中，一个像素却要覆盖大约30米的土地空间或水域空间，即一架喷气机可能在图像中只占用一个像素。

[<img class="aligncenter size-full wp-image-9735" alt="zhongbao" src="http://cos.name/wp-content/uploads/2014/04/zhongbao.jpg" width="1432" height="955" srcset="http://cos.name/wp-content/uploads/2014/04/zhongbao.jpg 1432w, http://cos.name/wp-content/uploads/2014/04/zhongbao-300x200.jpg 300w, http://cos.name/wp-content/uploads/2014/04/zhongbao-500x333.jpg 500w" sizes="(max-width: 1432px) 100vw, 1432px" />](http://cos.name/wp-content/uploads/2014/04/zhongbao.jpg)

<p align="center">
  <strong>图2-1 苏丹国，苏丹港，2011年10月8号, <i>DigitalGlobe, satellite GeoEye-1</i></strong>
</p>

DigitalGlobe公司几乎在获知马航事件的第一时间就展开了他们的行动。他们专门设立一个首窥（First Look）小组负责随时随刻对推特和新闻进行实时监控，以应对马航事件以及类似事件。首窥小组成员首先要决定卫星该飞往何处，然后他们开始调整系统让卫星到位。像地震这类事件，需要灾难发生之前的数据以期在搜救中进行对比。像马航事件，则需要根据新闻对正确监测位置进行推测，以安排卫星。“他们像使用谷歌地图一样搜寻地图，查完一个，然后继续到下一个区域，并尝试检查尽可能多的图片。我们时刻都有几百几千人做这一切。但这项任务是非常困难的，你需要小心地区分云，波浪和残骸，以期找到一两个可能有价值的点。当你真的去找图片的时候，你会惊奇地发现许多云彩看起来有多像船。我们用一组算法来对人群意见进行排名，看看那些地方大家都同意有问题.例如，如果100人中99个人都点击了一个有趣的小像素，这个像素就是真正有价值的。在这里，该算法通过数据进行筛选，看看哪些图片是可靠的，哪些不可靠，所以也许不应该得到同样的重视。之后，这些筛选出来的图片再由我们的分析师进行细查，并派人去现场搜救。”

众包并非万能，却能体现“众人拾柴火焰高”、“一方有难八方支援”的人道主义精神。Tomnod社区，作为一个众包平台，被认为是一个高尚的社区，由于其习惯于在寻常的大片陆地、冰原或水域寻找不易被察觉的关键图片。DigitalGlobe公司方面曾表示：“就像爱达华州空难一样，今天我们正在大海捞针。检查所有像素是很困难的，更何况我们正在寻找的东西没有确定特征。我猜想在这个阶段——我也希望我们是错的 ——我们找的东西看起来不像普通飞机。就是为什么我们要请求公众的帮助。”

众包这么好，以后是不是啥人也不要请，薪水也不要付了呢？当然不是！网友参与，纯粹出于个人兴趣，干活的质量和耐心，纯靠个人责任心。诚然网友里面“油菜花”很多，可是活儿的质量不能保证。因此众包仅限于那种大量重复性劳动，并且不需要太多技能，一般有一台电脑一根网线就能干，比如这次全民找飞机。顺便说Tomnod上那个专页现在还在，感兴趣的网友可以加入进去，期望能找到飞机残骸或者燃油泄漏的痕迹，据悉直到现在还有几千全球网友在继续这项工作。同时，如何客观分析众包平台上得出结论和数据也是统计学家关心的问题。

&nbsp;

**三、群体智慧**

在寻找失事飞机、海底沉船、或珍珠宝藏过程中，当可用数据极其缺乏时，群体智慧（[The Wisdom of Crowds](http://wisdomofcrowds.blogspot.com/)）也可以派上用场。

1968年5月，美国潜艇蝎子号（Scorpion）在完成北大西洋参观后，在返回纽波特纽斯（Newport News）途中消失了。虽然海军知道蝎子号最后一次报告的位置，但是海军对蝎子号发生的事故一无所知，只能模糊得知在最后无线电联系后蝎子号前进的距离。为了寻找蝎子号，海军划定了一个半径32千米，数千英尺深的圆形海域。这几乎是一个不可能完成的任务。当时，人们想到的最可行方案是聘用三四个潜艇和海洋环流顶级专家来推断蝎子号的位置。但是，在雪莉·桑塔格（Sherry Sontag）和克里斯托弗·德鲁（Christopher Drew）的书《_Blind Man&#8217;s Bluff: The Untold Story of American Submarine Espionage_》中记载，一个叫约翰·克雷文（John Craven）的海军军官提出了一个不同的计划。

首先，克雷文列出一系列能够解释蝎子号事故的场景。接着，他组建了一个囊括各方面专家的团队。团队成员包括数学家、潜艇专家和救助人员等。有趣的是，他非但不是要求团队成员互相协商寻求一个答案，反而请每个成员提供自己对每个可能场景的发生概率的猜测。为了让事情变得更有趣，他把一瓶芝华士作为猜中的奖品。于是团队成员开始对潜艇可能遇到的麻烦、潜艇的下沉速度、下沉角度等因素下注。

可以预见，团队成员个人推测信息无法告诉克雷文蝎子号的具体位置，但克雷文认为，如果他能把所有答案加在一起，构建一个蝎子号出事全景的复合图像，他应该会得到对潜艇最终位置的很好估计。而这正是他所做的。他收集了所有的猜测，并使用贝叶斯方法来估计蝎子号的最终位置。当一切完成后，克雷文得到一个该团队对于潜艇位置的集体估计。

克雷文最后得到的位置和任何一个团队成员猜测的位置都不同。换句话说，没有一个成员规划的场景和克雷文使用所有收集到的信息构成的场景是重合的。克雷文最后的估计才是真正的集体判断，是该团队作为一个整体取得的，而不是团队中最聪明的人的判断。最后事实证明这个集体的判断非常精彩。在蝎子号消失后的第五个月，海军发现了它。它和克雷文最后得到的位置只差约200米。

这个故事的惊人之处在于是团队成员在几乎没有任何线索和证据的情况下做出的推断。真正的数据只是很小的碎片。没有人知道为什么潜艇沉没，没有人有任何行驶速度和下沉速度的信息。然而，即使在组里没有人知道任何这些事情的情况下，该团队作为一个整体表现得相当出色。

统计学家弗朗西斯·高尔顿（Francis Galton）在1906年最先提出群体智慧。在普利茅斯出席了一个农场活动时，他被一个重量猜测比赛所吸引。比赛目标是猜一头牛被屠宰后的重量。那次大约有800名男女老幼参加了比赛，每人写下自己的猜测。猜得最接近牛的屠宰后重量的人得奖。比赛结束后高尔顿拿着所有记录做统计分析。他发现，所有参赛者猜测的平均值1197磅和实际重量1198磅仅差一磅。集体的猜测不仅比比赛的实际赢家准确，而且也比养牛和宰牛专家所做的猜测准确。

有这个话题兴趣的读者可以参看詹姆斯·索罗维基（James Surowiecki）的书《群体的智慧》（_The Wisdom of Crowds: Why the Many Are Smarter Than the Few and How Collective Wisdom Shapes Business, Economies, Societies and Nations_）。在马航事件中，也有人提出是否可以用群体的智慧的方法来寻找它，但目前还没人实现这个想法。

&nbsp;

**四、贝叶斯与决策**

当我们在搜救过程中逐渐收集到更多更准确的数据，科学地结合现有数据、科学知识、以及主观经验无疑可为找寻失联客机带来一线曙光。在统计学领域，贝斯方法（Bayesian Methods）提供了一个可以将观测数据、科学知识以及各种经验结合在一起的应用框架。

我们用一个简单例子来说明一下这个框架。假设有一个布袋，装有10个黑球和5个白球，那么随机取出一个球是白色的概率是5/15，即1/3。生活中的情况要更复杂一些——有时我们根本不能事先知道在布袋里到底有几个黑色或者白色的球。这也正是我们有时会进行抽样调查的原因。在不清楚整体情况时，我们会随机抽取一些样本，通过对样本分析以了解整体的情况。若我们不断累积经验，我们的猜测将愈加接近真实情况。贝叶斯方法，作为一种科学的方法，其本质也正是通过不断积累经验，更新对整体的认识 ，从而对真实情形进行把握。

例如，在开始的时候，我们并不知道布袋中白球的比例，那这个比例对我们而言可能是0，也可能是1，或者是1/3，1/5等等。即所有这些比例对我们来说可能性都差不多。假定我们有放回地抽取了六次球，发现有两次抽到的是白球，有四次抽到的是黑球（记做事件A）。利用这六次抽取球的结果，我们大可猜测——在事件A发生的情况下，袋子中白球的比例是1/3的可能性就比较大了。如果加入一些更具体的概率模型和先验知识，用条件概率的计算来计算看到事件A以后我们对袋子内可能情况的描述，就是贝叶斯方法。

再比如说我们去一个陌生的餐馆吃饭。我们因为之前不了解这家餐厅，以至于我们似乎只能随机的做出一个判断。但是贝叶斯方法建议我们去利用可能积累的经验来提供判断的线索。比如，我们的经验是：通常那些坐满了客人的餐厅的食物要更美味些，而那些客人寥寥的餐厅的食物可能不那么可能。这样，我们可以观察餐厅的上座率，从而利用这一条件改变我们的判断：在坐满了客人的条件下，餐厅的食物可口的概率比较大。所以说，在我们认识事物不全面的情况下，贝叶斯方法是一种很好的利用经验帮助作出更合理判断的方法。

现在我们已经对贝叶斯方法有了一定了解，下面我们谈谈如何利用贝叶斯方法帮助寻找失事马航MH370客机呢？对于失事飞机，我们不仅需要找到它的三维坐标，同样需要找到它的失事原因。新线索的出现，帮助我们积累了经验，从而改变飞机是由于自然事故还是遭遇劫机等人为事故造成的概率。两者的概率大小分别由Pr（自然事故|找到的线索）和Pr（遭遇劫机等人为事故|找到的线索）描述。当然，我们还可以利用一些其他的线索帮助我们改变判断，比如飞机的原计划航线，风速，洋流，以及扫描过的海域的情况。法航事件的飞机残骸搜寻工作给我们提供了一个参考案例。

[<img class="aligncenter size-full wp-image-9736" alt="bayesian_plane" src="http://cos.name/wp-content/uploads/2014/04/bayesian_plane.jpg" width="576" height="484" srcset="http://cos.name/wp-content/uploads/2014/04/bayesian_plane.jpg 576w, http://cos.name/wp-content/uploads/2014/04/bayesian_plane-300x252.jpg 300w, http://cos.name/wp-content/uploads/2014/04/bayesian_plane-500x420.jpg 500w" sizes="(max-width: 576px) 100vw, 576px" />](http://cos.name/wp-content/uploads/2014/04/bayesian_plane.jpg)

<p align="center">
  <strong>图4-1 残骸可能地点后验概率分布图（概率由大到小顺序：红、橙、黄、绿、蓝）</strong>
</p>

接着，我们来回顾贝叶斯方法在法航事件搜救过程中的应用。在2009年6月1日早晨，法航447航班在暴风雨中失去了联系。2010年7月，法国航空事故调查处委任Metron负责重新检查分析已有的搜救信息以便绘制一副<a name="OLE_LINK7"></a><a name="OLE_LINK6"></a>飞机残骸可能地点的概率分布图，如图4-1所示，概率由大到小的顺序为：红、橙、黄、绿、蓝。2011年1月20日，法国航空事故调查处于其网站刊登了分析结果。直到2011年4月8日，法国航空事故调查处发言人表示2011年1月20日刊出分析结果暗示，在图2-1中的一个圆形范围内有很大可能性会发现飞机残骸；并且，在对该区域进行持续一周的搜寻之后，残骸被发现。随后<a name="OLE_LINK9"></a><a name="OLE_LINK8"></a>，飞行数据记录器和驾驶舱语音记录器被找到。最终确认残骸的位置离图4-1中的概率中心位置并不远，可见贝叶斯方法非常有效。

基于贝叶斯方法对整体概率进行计算所利用的信息来自四个阶段的搜寻工作。阶段一：利用被动声学技术搜寻水下定位信号器。法航447装备的飞行数据记录器和驾驶舱语音记录器可以帮助分析事故发生时的状况。同时，在飞机沉入水中时，飞机装配的水下定位信号器发出信号协助通讯。水下定位信号器的电池可以工作至少30天，平均可以工作40天。搜寻持续了31天并于2009年7月10日停止。两台搜救船——费尔蒙特冰川号和探险号，均装备了美国海军提供的声波定位装置——参与了搜救。阶段二：旁侧声呐搜寻。在声波搜寻结束后，BEA决定使用Pourquoi Pas 提供的IFREMER旁侧声呐技术继续搜寻。在本阶段，一些由于时间关系未能在第一阶段搜寻的海域也被搜寻。阶段三：旁侧扫描声呐搜寻。 阶段四：即我们在上一段提及的利用贝叶斯方法进行搜救，并最终找到了飞机残骸。图4-2展示了搜救过程。

[<img class="aligncenter size-full wp-image-9737" alt="bayesian_cal" src="http://cos.name/wp-content/uploads/2014/04/bayesian_cal.jpg" width="582" height="447" srcset="http://cos.name/wp-content/uploads/2014/04/bayesian_cal.jpg 582w, http://cos.name/wp-content/uploads/2014/04/bayesian_cal-300x230.jpg 300w, http://cos.name/wp-content/uploads/2014/04/bayesian_cal-500x384.jpg 500w" sizes="(max-width: 582px) 100vw, 582px" />](http://cos.name/wp-content/uploads/2014/04/bayesian_cal.jpg)

<p align="center">
  <strong>图4-2 飞机残骸地点的后验概率分布计算过程</strong>
</p>

由法航事件，我们可以看到贝叶斯方法确实可以为搜救飞机残骸提供理论依据。由于既得数据有时并不能为计算后验概率提供太多信息，我们需要纠集所有有用的信息，并使所有信息都可以转化为贝叶斯方法中的先验信息。诚如香港城市大学Nozer Singpurwalla教授所言，即使在数据量极为丰富的情况下，应用贝叶斯方法的时候都应考虑专家的主观判断、证据以及想象力。在搜寻飞机的过程中，搜寻队可以估算出已经搜寻过得海域中存在残骸但由于失误没有找到的概率、坏掉一个信号器与坏掉两个信号器是否是独立事件等等。

&nbsp;

**五、结束语**

除了数据分析与统计方法在上面几个方面的应用，其实我们可以看到整个搜寻过程就是一个通过数据收集，数据分析，统计推断，再收集，再分析，再推断，不断提高我们对事件的估计和把握的过程。从科学研究到日常决定，我们都是在不断重复类似这样的过程。多了解一些统计和分析的方法对我们做科学决策肯定会有帮助。

就在本文收稿的时候，搜寻前方传来消息：“在距离珀斯约1600公里处南印度洋水域负责搜寻失联航班的中国舰艇海巡01轮通过黑匣子搜寻仪，侦听到疑似马航失联航班的信号。”而后澳大利亚方面也几次探测到水下信号。希望这些发现和数据信息能够为我们找到马航370提供最新的强心剂。

<b style="line-height: 1.5;">参考资料</b>

<p align="left">
  <b>本文第一节图片来源：</b>
</p>

<p align="left">
  <span style="text-decoration: underline;"><a href="http://www.nytimes.com/interactive/2014/03/17/world/asia/search-for-flight-370.html">http://www.nytimes.com/interactive/2014/03/17/world/asia/search-for-flight-370.html</a></span>
</p>

<p align="left">
  <b>本文第二节图片及资料来源：</b><b></b>
</p>

<p align="left">
  <span style="text-decoration: underline;"><a href="http://www.wired.co.uk/news/archive/2014-03/11/digital-globe-hunts-for-malaysia-plane">http://www.wired.co.uk/news/archive/2014-03/11/digital-globe-hunts-for-malaysia-plane</a></span>
</p>

<p align="left">
  <b>本文第三节资料来源：</b><b></b>
</p>

<p align="left">
  <span style="text-decoration: underline;"><a href="http://leightonvw.com/2014/03/13/can-prediction-markets-help-find-a-missing-aircraft/">http://leightonvw.com/2014/03/13/can-prediction-markets-help-find-a-missing-aircraft/</a></span>
</p>

<p align="left">
  <b>本文第四节图片及资料来源：</b><b></b>
</p>

<p align="left">
  <span style="text-decoration: underline;"><a href="http://fivethirtyeight.com/features/how-statisticians-could-help-find-flight-370/">http://fivethirtyeight.com/features/how-statisticians-could-help-find-flight-370/</a></span>
</p>

<p align="left">
  <span style="text-decoration: underline;"><a href="https://www.informs.org/ORMS-Today/Public-Articles/August-Volume-38-Number-4/In-Search-of-Air-France-Flight-447">https://www.informs.org/ORMS-Today/Public-Articles/August-Volume-38-Number-4/In-Search-of-Air-France-Flight-447</a></span>
</p>

<p align="left">
  <b>马航事件脉络梳理：</b><b></b>
</p>

<p align="left">
  <a href="http://news.qq.com/zt2014/MH370/index.htm" target="_blank"><span style="text-decoration: underline;">http://news.qq.com/zt2014/MH370/index.htm</span></a>
</p>

&nbsp;

本文作者：统计之都创作小组（<a href="http://yishuo.org/" target="_blank">邓一硕</a>，<a href="http://blog.sina.com.cn/cattyguan" target="_blank">关菁菁</a>，<a href="http://chenangliu.info/" target="_blank">刘辰昂</a>，<a href="http://yixuan.cos.name/cn/" target="_blank">邱怡轩</a>，<a href="http://blog.cos.name/taoshi/" target="_blank">施涛</a>，<a href="http://weibo.com/u/1572842322" target="_blank">熊熹</a>，<a href="http://weibo.com/u/2296442893" target="_blank">周祺</a>）

感谢统计之都资深顾问谢益辉和香港浸会大学数学讲座教授汤涛在写作工程中提出的宝贵建议。