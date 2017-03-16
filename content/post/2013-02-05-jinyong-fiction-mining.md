---
title: 十八般武艺，谁主天下？
date: '2013-02-05T18:30:45+00:00'
author: Liyun
categories:
  - 数据挖掘与机器学习
tags:
  - pagerank
  - 小说
  - 文本挖掘
  - 网络图
  - 金庸
slug: jinyong-fiction-mining
---

十八般武艺各有神通之处，所谓“一弓、二弩、三枪、四刀、五剑、六矛、七盾、八斧、九钺、十戟、十一鞭、十二锏、十三挝、十四殳、十五叉、十六耙、十七绵绳套索、十八白打”，这让一个江湖新手一上来就学全十八般武艺，还真是有点为难人家呢。这在古代，天下可都是一群架一群架扎扎实实打出来的。指挥者可以运筹帷幄决胜于千里之外，但是真要上阵的小兵们可就惨多了——谁若是稍有走神，怕是小命就危在旦夕了。还有那血雨腥风却始终有无数人向往的江湖，或迷人或险恶，总得有一技傍身方觉得安心些。可是，这一技说来容易，到底学才可以雄霸天下呢？嗯，其实一般说来我们是不需要担心这个问题的，可是凡事总有例外——比如做梦的时候&#8230;

小编不幸的就在梦中穿越回了古代一回，然后面对着师傅一下子扔出来的一堆兵器傻了眼——这该如何下手呢？直到梦醒，耳边回荡的还是师傅那严厉的声音“给你一天时间考虑，明天来见我的时候告诉我你要学什么”。呃，为了明天做梦的时候不挨骂，还是老老实实的选一样东西吧。可是这也不能信手拈来就是嘛，总要有点科学依据，要不怎么能显得出来我这个辛辛苦苦梦中穿越回去的现代人的智商优越性呢？

于是开始狂翻枕边常备的武侠小说。“问世间情为何物，直叫人生死相许”——正沉浸在杨过和小龙女的离别悲伤之中，恍然觉悟，呃，貌似不对，看错章节了&#8230;师傅明天才不会管我怎么谈恋爱呢。可是这么多打打杀杀的，金庸老鬼的十四本巨著这到啥年啥月才能看完呀！晚上就得回师傅答案呢。算了，在这个信息时代，自然要倚仗科技的力量——比如，文本分析神马的应该可以搞定吧？先去百度一下，结果度娘说：

> 得人心者得天下&#8230;
  
> 得中原者得天下&#8230;
  
> 得此女者得天下&#8230;
  
> 得知识者得天下&#8230;
  
> 得青年者得天下&#8230;
  
> 得蜀者得天下&#8230;

这些怎么看起来这么不靠谱&#8230;算了，还是自己动手丰衣足食吧。眼看太阳就要下山了，小编赶紧打开电脑。噼里啪啦一阵键盘声响起，金庸大侠的十四本小说就乖乖的躺在那里了。稍待片刻，等我做好了分析，嘿嘿，晚上就不怕师傅拷问了。都说群众的智慧是无穷的，听说[一博彩公司预测大选什么的比那些专门的学者们还要准](http://www.npr.org/2012/11/29/166177281/y)&#8230;我还是先看看那些大侠们都用什么吧！都说剑品即人品，那我们就来看看这些武器的PR值吧（此处纯属开玩笑 :P，PageRank还是一个比较好用的计算网络权重的指标）。<figure id="attachment_6696" style="width: 665px" class="wp-caption aligncenter">

[<img class=" wp-image-6696 " title="金庸的武侠世界" alt="金庸的武侠世界" src="http://cos.name/wp-content/uploads/2012/11/the_world.png" width="665" height="595" srcset="http://cos.name/wp-content/uploads/2012/11/the_world.png 665w, http://cos.name/wp-content/uploads/2012/11/the_world-300x268.png 300w, http://cos.name/wp-content/uploads/2012/11/the_world-500x447.png 500w, http://cos.name/wp-content/uploads/2012/11/the_world-335x300.png 335w" sizes="(max-width: 665px) 100vw, 665px" />](http://cos.name/wp-content/uploads/2012/11/the_world.png)<figcaption class="wp-caption-text">金庸的武侠世界</figcaption></figure> 

然后看看排名，果然还是学剑最好哇！

`剑 0.018411053<br />
刀 0.017516021<br />
掌 0.017137869<br />
抓 0.011880115<br />
拳 0.011605281<br />
圈 0.007458074<br />
船 0.005805638<br />
镖 0.004840676<br />
枪 0.004806615<br />
弓 0.003935635<br />
钩 0.003358054<br />
棍 0.003121407<br />
叉 0.002733994<br />
拐 0.002570806<br />
锤 0.002392814<br />
斧 0.002056493<br />
戟 0.001731019<br />
铲 0.001521452<br />
戚 0.00148074`

嘻嘻，搞定了晚上梦会师傅的事情，就可以开始玩玩其他的了。顺便，好奇的心情发作&#8230;有没有发现，其实这朵花，真的是开了好多瓣呢？一瓣，怕就是一本书吧！<figure id="attachment_6697" style="width: 723px" class="wp-caption aligncenter">

[<img class=" wp-image-6697 " title="金庸一枝花" alt="金庸一枝花" src="http://cos.name/wp-content/uploads/2012/11/jinyong_flower.png" width="723" height="696" srcset="http://cos.name/wp-content/uploads/2012/11/jinyong_flower.png 723w, http://cos.name/wp-content/uploads/2012/11/jinyong_flower-300x288.png 300w, http://cos.name/wp-content/uploads/2012/11/jinyong_flower-500x481.png 500w, http://cos.name/wp-content/uploads/2012/11/jinyong_flower-311x300.png 311w" sizes="(max-width: 723px) 100vw, 723px" />](http://cos.name/wp-content/uploads/2012/11/jinyong_flower.png)<figcaption class="wp-caption-text">金庸：一枝花</figcaption></figure> 

好吧，继续过过瘾&#8230;既然都这样了，就开始八卦一下这些人物的关系吧！<figure id="attachment_6700" style="width: 690px" class="wp-caption aligncenter">

[<img class=" wp-image-6700 " title="金庸人物关系网" alt="金庸人物关系网" src="http://cos.name/wp-content/uploads/2012/11/characters_main.png" width="690" height="755" srcset="http://cos.name/wp-content/uploads/2012/11/characters_main.png 690w, http://cos.name/wp-content/uploads/2012/11/characters_main-274x300.png 274w, http://cos.name/wp-content/uploads/2012/11/characters_main-456x500.png 456w" sizes="(max-width: 690px) 100vw, 690px" />](http://cos.name/wp-content/uploads/2012/11/characters_main.png)<figcaption class="wp-caption-text">金庸人物关系网</figcaption></figure> 

等等，什么，射雕三部曲居然不在一块儿！这到底是什么个情况！！！<figure id="attachment_6702" style="width: 714px" class="wp-caption aligncenter">

[<img class=" wp-image-6702 " title="射雕三部曲关系网" alt="射雕三部曲关系网" src="http://cos.name/wp-content/uploads/2012/11/fiction_three_small.png" width="714" height="551" srcset="http://cos.name/wp-content/uploads/2012/11/fiction_three_small.png 714w, http://cos.name/wp-content/uploads/2012/11/fiction_three_small-300x231.png 300w, http://cos.name/wp-content/uploads/2012/11/fiction_three_small-500x385.png 500w, http://cos.name/wp-content/uploads/2012/11/fiction_three_small-388x300.png 388w" sizes="(max-width: 714px) 100vw, 714px" />](http://cos.name/wp-content/uploads/2012/11/fiction_three_small.png)<figcaption class="wp-caption-text">射雕三部曲关系网</figcaption></figure> 

哎，我的童年彻底毁掉了。什么黄衫姑娘啊，什么郭襄祖师爷啊，原来《倚天屠龙记》跟《神雕侠侣》和《射雕英雄传》根本没那么多血脉相亲&#8230;呜呜。

&#8212;&#8212;&#8212;&#8211;废话若干&#8212;&#8212;&#8212;&#8211;
  
1. 选择金庸的作品只是因为有现成的金庸词库，本来还想弄古龙的呢，结果古龙的没有现成的词库，伤心。
  
2. 明显的，字数少的作品占劣势，毕竟连接数要少很多呢。
  
3. “连接关系”的定义和[思喆的明朝那些事儿](http://www.bjt.name/2012/09/ming-dynasty/)一样，就是在同一个段落中出现。当然，也可以放宽到上下若干段落之内，不过现在已经够复杂的了，再放宽不见得多多少信息量。
  
4. 可视化部分由Gephi搞定，文本分析部分由R搞定，各取所长嘛。
  
5. 同义词替换。1.20的上海R沙龙上很多朋友提出来，应该有一些基本的同义词替换，比如“杨过”也可称为“过儿”，小龙女亦作“龙儿”和“姑姑”。这样的替换需要建立一个针对金庸的同义词词典，暂时还没有现成的资源。
  
6. 同样是沙龙的朋友提出来的，对于关系的定义应该更明确一点，不单单是出现在同一段落。金庸的还好，古龙的文风就更加飘逸，不适合这样定义。然而更细致的定义需要对金庸的文字进行更深入的理解，进行一些语义分析，还有待进一步对于语言理解的深入。