---
title: COS论坛精华帖系列——use R for fun系列之小应用制作篇
date: '2013-08-10T16:24:30+00:00'
author: COS编辑部
categories:
  - 推荐文章
  - 软件应用
tags:
  - fun包
  - R语言
  - 交互
  - 应用
  - 论坛
slug: cos-series-use-r-for-fun-application
---

系列以use R for fun为主题，以[COS论坛](http://cos.name/cn/)上的精华帖、相关的package以及自己的一些code为素材，结合自身的一些编程体会，从而整合成文。本文是第二篇小应用制作篇。

***本文素材出处均已在正文注明**

本文继续承接上一篇的话题([小游戏开发篇](http://cos.name/2013/08/cos-series-use-r-for-fun-game/))，继续在交互操作上做文章，不同的是这里引入了更丰富的操作和idea，仅仅做些小游戏还远远达不到我们的胃口，因此这里不妨再把思维拓宽些，让R来我们的生活服务(理论上)，于是小应用制作篇就此诞生，虽称不上游戏但同样可以给我们带来的快乐。由于面更广因此idea就更为关键了(在玩统计的过程中idea同样关键！)，上篇所讲的内容可以被完美继承到本篇中，至于其他内容很难明确说需要事先掌握R的某一块内容(少量增加了一些)，所以这里就直接上例子！

<!--more-->

**一、关机**

听起来似乎挺不错的，当你把代码码完想关电脑时，是不是觉得关个电脑都觉得麻烦，没错R可以帮你自动关机。提前加载fun包，想关机的时候

<pre>shutdown()</pre>

然后回车你就可以放心的去睡觉了(当然直接用shell(()或者system()装逼么也完全可以)，此外函数的wait参数，可以用于设置等待时间，也就是多少时间后再行关机(以秒为单位)，因此还可以用来设置定时关机(比方说写在程序最后，如果程序需要跑一晚上的话)。COS原帖在[这里](http://cos.name/cn/topic/15648#post-15648)，源代码在[这里](https://github.com/yihui/fun/blob/master/R/shutdown.R)，最后加一句：危险动作，谨慎模仿！

**二、新年快乐**

曾经也想过做一些类似用于新年祝福的东西，怎奈每次新年不是这事就是那事，等到真的有空了，一看早被人抢了先了(而且新年早过了)，那也没有办法，继续引用呗！COS前辈们创作的关于新年快乐的一些作品大部分已经收录在fun包的demo中，有空的时候可以一一demo之，里面有音乐也有动画，考虑到关于音乐和动画的文章排在后面，所以这里先不细说，但是可以先跑为快！不妨试一试

<pre>demo(HappyNewYear2010Yixuan)</pre>

就能看到炫酷的动画

[<img class="alignnone size-medium wp-image-116 aligncenter" alt="happynewyear2010" src="http://chenangliu.info/cn/wp-content/uploads/2013/08/happynewyear2010-300x121.jpg" width="300" height="121" />](http://chenangliu.info/cn/wp-content/uploads/2013/08/happynewyear2010.jpg)

再来看看happy new year的滚动字幕，原来demo中并没有把坐标去掉，若想要更好的效果，可以先

<pre>par(bty="n",xaxt="n", yaxt="n",mar=c(0,0,0,0));</pre>

把坐标去掉，同时拓宽作图面积(再多嘴一句，要想画出自己满意的图，par一定要掌握好)，当然同时也可以自己再加一个喜庆一点的背景什么的，截取某一个瞬间

[<img class="alignnone size-medium wp-image-117 aligncenter" alt="happynewyear2009" src="http://chenangliu.info/cn/wp-content/uploads/2013/08/happynewyear2009-300x84.jpg" width="300" height="84" />](http://chenangliu.info/cn/wp-content/uploads/2013/08/happynewyear2009.jpg)

此外

<pre>demo(HappyNewYear2009Music);</pre>

就可以听到纯正的新年快乐歌了(这里需要加载tuneR包或者sound包，关于音乐制作方面敬请期待之后的文章)。关于COS原帖暂时没有考证，读者可以自行进[论坛](http://cos.name/cn/)搜索之。

**三、放大镜**

放大镜的idea来源于谢大在它的《现代统计图形》中给的一个例子，但是感觉这幅图实在说不出什么现实一点的描述，于是灵机一动对主体部分稍作修缮，就改造成了一个比较挫的放大镜。因此只是在某一幅特定的图中具有放大效果，所以也不能算纯粹的放大镜，不过娱乐效果好歹是有了那么一点。主要是对mousemove这一块的改动，改成下面的代码

<pre>mousemove&lt;-function(buttons, x, y) {
r&lt;-0.2;
idx=(xx-x)^2+(yy-y)^2&lt;r^2
plot(xx, yy, type="n")
rect(-1, -1, 2, 2, col="gray")
points(xx[idx], yy[idx], col="green", cex = 2)
points(xx[!idx], yy[!idx], col="green")
t&lt;-seq(0,2*pi,0.01);
lines(r*sin(t)+x,r*cos(t)+y,col="blue",lwd=5);
lines(1.1*r*sin(t)+x,1.1*r*cos(t)+y,col="blue",lwd=5);
}</pre>

然后随机点的设置的多一点(改成200个点或许效果更好点)，就有种放大镜(显微镜)下看细菌(点的形状可变，例如变成杆菌之类的)的感觉了！当然其实也有很多可以进一步改进的地方，例如对某几个点特殊处理一下，就可以改成照妖镜了。当然也可以再往镜子上加根棍子之类的，不怕做不到就怕想不到！

[<img class="alignnone size-medium wp-image-118 aligncenter" alt="fangdajing" src="http://chenangliu.info/cn/wp-content/uploads/2013/08/fangdajing-300x300.jpeg" width="300" height="300" />](http://chenangliu.info/cn/wp-content/uploads/2013/08/fangdajing.jpeg)

**四、计算器——DIY**

前面的示例大多比较随意，于是这里挑一个写这篇文章时临时起兴而写的程序作为详解的示例——计算器，制作计算器可以通过两种途径，一种是制作GUI，效果会比较装逼，如果做得仔细的话完全可以做得跟微软自带的计算器一模一样甚至完爆它，但是这会用到tcltk或者GTK+之类的，不符合本文一切从简的原则，不过这里还是多嘴提一句如果对做GUI感兴趣的话可以采用gWidgets系列的几个package，关于这方面的内容没记错的话谢大曾经在某界China-R上做个一个报告，此外还可以参考其自带的小品文，毫不夸张的说用它来山寨个统计软件界面那是不再话下。回到主题，第二种就是依然借助于R强大的作图设备，再次利用给力的交互式作图来完成，事实也说明，掌握的不在多而在于精，如果能够对几个重要的函数有着深刻的理解并且能够灵活的运用胜过只是听说一堆函数却不去实际操作。

计算器的制作分为三步，一是计算机界面，关于界面参考最老式的就行了，输出框+数字键+运算符，ok搞定，用一下segments和text足矣，当然为了不瞎了别人的眼，配色什么的也需要调一下，考虑到笔者审美观非常拙计，已遭n多人吐槽，故无奈只得通过随机数的方法进行配色，还请广大读者谅解。第二步是键盘与图形的交互，这里与图片中的按键无关，但需要制定键盘上某些需要的按键的具体功能，而重点又在于运算符，这里为了能和后面的鼠标结合操作，需要用到双箭头赋值，即&#8221;<<-&#8220;，它的意思是向上一层环境中的对象赋值，如果找不到，就再往上一层，如果一直往上都找不到，就到最顶层的环境即全局环境中赋值，具体可以参考[这里](http://cos.name/cn/topic/106805#post-231488)。也就是第三步就是鼠标和数字键的对应啦，这一步并不繁琐因为具体的操作都可以直接copy第二步的代码，唯独需要改动的就是把坐标信息和图中的数字键对应起来。

[<img class="alignnone size-medium wp-image-119 aligncenter" alt="jisuanqi" src="http://chenangliu.info/cn/wp-content/uploads/2013/08/jisuanqi-300x300.jpeg" width="300" height="300" />](http://chenangliu.info/cn/wp-content/uploads/2013/08/jisuanqi.jpeg)

这里只是开发了部分最基本的四则运算功能，剩下的就留给大家发挥自己的想象来填补这些空缺了，具体的方法完全可以依葫芦画瓢，但更提倡另辟蹊径开拓创新。

注：代码由于是即兴而作，因此不堪入目，目测可以精简，若实在想毁一毁三观的，可以前往[本人blog中同名文章](http://chenangliu.info/cn/use-r-for-fun-application/)的附录中查看。

**五、闹钟**

之前可以说是一个半成品，那么最后给一个成品——闹钟来收官，这其实是闹钟兼时钟，最初想法的来源是某处programming的时候用到了系统时间的获取，于是想到了把他可视化(勉强称之为可视化吧，各位看官给我留点面子)出来， 闹钟其实本质上是一个动画，其中融合了简单音乐的制作。之前我把只完成了一部分的代码传在了人大经济论坛上(bug比较多，忽略为好)，后经过了修缮，大致做出了点样子，具体的过程我就不说了，关于最终的代码方便起见我做成了一个小的package，可以在[我的blog上同名文章](http://chenangliu.info/cn/use-r-for-fun-application/)的附录中下载。

[<img class="alignnone size-medium wp-image-120 aligncenter" alt="clock" src="http://chenangliu.info/cn/wp-content/uploads/2013/08/clock-277x300.jpg" width="277" height="300" />](http://chenangliu.info/cn/wp-content/uploads/2013/08/clock.jpg)

**六、关于一些用到函数的解释**

示例中用到了一些或许做普通statistical computation时不太常用的函数，这里有必要简单解释一下它们的用法仅供参考。

**（1）winDialog()：**该函数的功能怕是看了名字就能猜到一二了，它可以在windows系统下弹出一个对话框，也可以算是一种交互吧，在需要设置一些提示手段之类的情况下该函数具有不错的效果，例如在闹钟就是在时间到了的时候弹出了时间到的窗口。该函数的usage的如下：

<pre>winDialog(type = c("ok", "okcancel", "yesno", "yesnocancel"),
message)</pre>

tag共有两个，type指的是窗口的类型。如果选择的是&#8221;ok&#8221;则弹出的窗口中会有&#8221;确定&#8221;按钮，同理&#8221;okcancel&#8221;则是&#8221;确定&#8221;和&#8221;取消&#8221;，&#8221;yes&#8221;和&#8221;no&#8221;为&#8221;是&#8221;和&#8221;否&#8221;，而message则是弹出的窗口需要表达的信息，例如&#8221;Hello World&#8221;。winDialog函数的效果可以参考下图：

[<img class="alignnone size-full wp-image-121 aligncenter" alt="question" src="http://chenangliu.info/cn/wp-content/uploads/2013/08/question.jpg" width="266" height="121" />](http://chenangliu.info/cn/wp-content/uploads/2013/08/question.jpg)

另外与winDialog有关的还有一个非常有意思的函数，就是winMenus系列function，它可以用来修改windows窗口菜单，具体可以参考?winMenus

（2）Sys.sleep()：这个函数其实还挺常用的，同样可以顾名思义，其用途就是让程序暂停运行一段时间，因为唯一的参数就是时间，以秒为单位。

这篇可以看做是小游戏篇的续集，另外这里的“应用”也并非真正意义上的应用，如果让有的朋友失望了那我只能说声抱歉，如果有更好的示例或者idea欢迎和我或者COS的几位前辈联系，会及时更新，当然如果很棒的话目测就果断收录fun包了。关于基于交互式操作部分就先行告一段落，当然之后肯定还会提及，下篇预告——玩转图像篇，惊喜更多，不要错过！

**关于作者**

  * 刘辰昂，浙大准大四本科，统计之都主站编辑
  * weibo：[求证1加1](http://weibo.com/2011764505/profile?topnav=1&wvr=5)
  * blog: <http://chenangliu.info/cn/>
  * email: liuchenang@gmail.com