---
layout:     post                                    # 使用的布局（不需要改）
title:      优雅的建立天文学术文献库         # 标题
subtitle:   下载paper，管理paper，阅读paper            #副标题
date:       2017-10-06                              # 时间
author:     Chaoli Zhang                            # 作者
header-img: img/Tag-bg-hacker.jpg                  #这篇文章标题背景图片
catalog: true                                       # 是否归档
published: true
tags:                                               #标签
    - Academic
    - Astro
---

如果你也被底下的问题所困惑，那么这篇文章正好适合你😏：

1. 怎么大量下载天文paper？
2. 你觉得一篇文献里面的reference paper很好，怎么全部下载？
3. 当你需要读一篇paper的时候，怎么样在堆积如海的PDF里面立马找到自己需要的paper？

<span style="color:green"> 事先声明: 我下面介绍的方法不一定是最优雅的，我相信在藏龙卧虎的天文界一定有更赞的方法。如果您有更好的方法，还请不吝赐教。</span>

好，废话少说，进入主题！

---
### 工具

你需要下载/安装以下的工具 （具体怎么安装很简单，参考下面链接。相信这绝对难不倒学天文的小伙伴 😉）：

1. [Python Anaconda](https://www.anaconda.com/download/#download)
2. [adsbibdesk](http://blog.jonathansick.ca/)
3. [Bibdesk](http://bibdesk.sourceforge.net/)
4. [SAO/NASA ADS ](http://adsabs.harvard.edu/abstract_service.html)

### 方法

### 【步骤1】 收集paper里面所有reference的DOI号



现在假设你想下载这张paper里面136篇reference paper [Planck intermediate results. XXXIX. The Planck list of high-redshift source candidates](http://adsabs.harvard.edu/abs/2016A%26A...596A.100P)， 照片如下：

![Planck_paper_ref.png](/img/paper_downld/paper_ref.png "Planck_paper_ref.png")



【步骤1-1】 点击上面的链接，打开Planck intermediate results. XXXIX.的ads界面, 然后点击References in the article：

![ads_page1.png](/img/paper_downld/ads_page1.png "ads_page1.png")

【步骤1-2】根据下面图示输入相应参数：

![ads_page2.png](/img/paper_downld/ads_page2.png "ads_page2.png")

【步骤1-3】 得到相应所有paper的DOI号码，如下图所示：

![ads_page3.png](/img/paper_downld/ads_page3.png "ads_page3.png")

【步骤1-4】 复制所有的adsbibdesk *** 到你喜爱的text editor （我使用sublime text 3）, 然后存储为paper.sh, 如下图：

![ads_page4.png](/img/paper_downld/ads_page4.png "ads_page4.png")

【步骤1-5】 然后把paper.sh弄成可执行的文件，比如，在iTerm2里面输入：chmod +x paper.sh

![ads_page5.png](/img/paper_downld/ads_page5.png "ads_page5.png")

### 【步骤2】 利用adsbibdesk下载

【步骤2-1】接下来就可以打开bibdesk了，如下 (这一步很重要，如果没打开bibdesk，可能会出现bug )：

![bibdesk_1.png](/img/paper_downld/bibdesk_1.png "bibdesk_1.png")

【步骤2-2】iterm2执行paper.sh文件，然后就可以自动下载136篇paper，然后归档到planck.bib文件里面：

![bibdesk_2.png](/img/paper_downld/bibdesk_2.png "bibdesk_2.png")

---

### 总结

- 当你第一次使用adsbibdesk的时候，它会自动在你的Documents文件夹创建一个Papers文件夹，你下载所有PDFs都将被存储在/Documents/Papers里面。
- adsbibdesk下载下来的paper名字都是tmp******.pdf, 但这丝毫不影响你在planck.bib搜寻到你要的paper.

![bibdesk_3.png](/img/paper_downld/bibdesk_3.png "bibdesk_3.png")


至于怎么样在堆积如海的PDFs里面立马找到自己需要的paper，很简单，只需要在planck.bib里面搜寻paper的名字，或者一作的名字：

![bibdesk_4.png](/img/paper_downld/bibdesk_4.png "bibdesk_4.png")

### 建议

如果你开始一个天文新领域，那可以找那个领域<span style="color: purple"> 最出名</span>和<span style="color: purple"> 应用最多</span>的几篇paper，然后把这里面的所有reference paper都下载下来。我个人感觉，一个领域里只要下载个600-800篇文章，那以后基本上你想看什么文章，都不用去ads去找，直接到你的私人文献库去找，80-90%会在那里。而且，你写paper的时候就再也不用担心做bibliography.










