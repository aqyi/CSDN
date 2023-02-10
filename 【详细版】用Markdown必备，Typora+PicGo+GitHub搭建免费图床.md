# Typora+PicGo+GitHub搭建免费图床

# tips

写在最前面，如果赶时间搭建请直接跳转到[实操教程](#实操教程)

😀**知道大家长时间网上冲浪，为了劳逸结合的学习，该文章附有风景图片欣赏**:smile:

![余晖](https://img-blog.csdnimg.cn/fc0f9464f97b48888ea214ec46f606cc.jpeg#pic_center)~阿木又拍摄于云南省武定县~

![丁达尔美景](https://img-blog.csdnimg.cn/d1ab3183b02a41e7aeb6b3e138faa8b9.jpeg#pic_center)~图片来源：抖音某网友~

---
# 图床

## 什么是图床？
>:b:百度给的解释是：**储存图片的服务器**，***有国内和国外之分。***<p> 
>国外的图床由于有空间距离等因素决定访问速度很慢影响图片显示速度<br>
>**国内也分为单线空间、多线空间和cdn加速三种。** <p>
>就是专门用来存放图片，同时允许你把图片对外连接的网上空间，不少图床都是免费的。

图床说简单了就是互联网中存储图片的空间，举个例子：

	假设你在微信朋友圈分享一张图片，你的好友可以通过朋友圈看到你分享的图片。
🌆那么他是去访问你的手机的相册吗？<p>其实不是，你分享图片，也就是把图片上传到微信的服务器<br>微信为你生成一个独一无二的访问链接，这个链接指向的空间其实就是图床。

---

## 为什么需要图床？
:camping: 当大家使用轻量级标记语言写好了图文并茂的文字，当我们发布在博客网站的时候，发现大多图片都打不开，其实图片储存在你本地相册，发布博客后服务器访问不到地址路径，这个时候我们就需要借助到一个图床。

:camping: 会去接触图床的人通常都是一些喜欢在网上分享博客（编程经验）的人，使用图床的人通常采用Markdown的方式去编辑文字。我们都知道现在通常流行两种方式编辑文字：
* **富文本编辑**，Word就是其中非常具有代表性的，文字的各种格式都是通过交互按钮设置的，这时候需要频繁的鼠标配合操作（熟悉快捷键的大佬除外）。这种方式操作简单便捷，但是对于大量编辑工作的文字工作者，双手离开键盘使用鼠标往往容易打乱书写节奏和思路，效率低。

* **Markdown编辑**，是一种通过Markdown标记语言去规定格式的纯文本编辑方式。这种方式使得文字工作者专注于文字，而非格式，双手可以彻底的解放鼠标，大大提高了效率。Markdown比富文本编辑方式更加具有通用性，word的文字整篇复制到有道云笔记格式会出现差异，这也是富文本编辑的巨大缺陷，只能说轻量级标记语言的优点懂的人很爱。

**专门用来存放图片，同时允许你把图片对外连接的网上空间，它可以将照片转换成更容易分享的代码、链接等等，提高用户图片的使用效率。**

---
## 怎样获得图床？
获得图床的方式有很多，综合考虑过后我们使用Typora+PicGo+GitHub搭建,
图床使用流程

**目前有许多获得图床的途径非常多，通常分为收费的和免费的。**

* 收费图床：穷人一个，没钱用收费的，对于个人而言，免费的足够了

* 免费图床：(羊毛很多，拼命薅)​ 🐑七牛云、路过图床、聚合图床、有道云和微博。

**具体搭建操作后边会为你讲述，先带你补充基本知识，请跟随我的脚步往下走。**<p>为什么不选其他?
> 相关资料推荐给你：新浪[二思丶](https://zhongce.sina.com.cn/article/view/53974) 、稀土掘金[danielsk](https://juejin.cn/post/7084137919845236743) 、 知乎[Se.Jeong](https://zhuanlan.zhihu.com/p/58863378)

---
# Markdown是什么？
![官方](https://img-blog.csdnimg.cn/47b2258afd6e49c1a233fef88e3e66d8.png)

[Markdown官网介绍](https://markdown.com.cn/intro.html)
>Markdown是一种**轻量级标记语言**，排版语法简洁，让人们更多地关注内容本身而非排版。它使用易读易写的纯文本格式编写文档，可与HTML混编，可导出 HTML、PDF 以及本身的 .md 格式的文件。因简洁、高效、易读、易写，Markdown被大量使用，如Github、Wikipedia、简书等。

千万不要被「**标记**」、「**语言**」吓到，Markdown的语法十分简单，常用的标记符号不超过十个，用于日常写作记录绰绰有余，不到半小时就能完全掌握。

就是这十个不到的标记符号，却能让**人优雅地沉浸式记录，专注内容而不是纠结排版**，达到「心中无尘，码字入神」的境界。

* 在线体验一下[Markdown在线编辑器](https://markdown.com.cn/editor/)。
* 让我们从 [Markdown 标题语法](https://markdown.com.cn/basic-syntax/headings.html)开始学习吧。
---
# typora简介
![官网](https://img-blog.csdnimg.cn/876d85aff08c49a7b0e1260b88a7734e.png)

Typora是一款免费的轻量级Markdown编辑器，它没有Mou，Haroopad等Markdown编辑器那么大名鼎鼎，算是较为小众的一款产品。
>在文章开始使用[TOC] 将自动在文章生成目录
你还可以在侧栏查看自己的目录结构，十分方便。

凭良心说话，Typora有着诸多优秀的特性可参照知乎“老宋的茶书会”[Typora - 不要太棒的Markdown编辑器](https://zhuanlan.zhihu.com/p/44998516)

Typora提供了较为丰富的主题，并且Typora支持开发者开发主题。如果你对CSS有所涉及，你完全可以自己撸一个属于自己的主题出来，简直不要太任性。

Typora中文官网：[Typora](https://typoraio.cn/)

---
# PicGo介绍

![PicGo](https://img-blog.csdnimg.cn/24daafddf4534095a00ba5283940f6b1.png)
>一个用于快速上传图片并获取图片 URL 链接的工具
特色功能
支持拖拽图片上传
支持快捷键上传剪贴板里第一张图片
Windows 和 macOS 支持右键图片文件通过菜单上传 (v2.1.0+)
上传图片后自动复制链接到剪贴板
支持自定义复制到剪贴板的链接格式
支持修改快捷键，默认快速上传快捷键：command+shift+p（macOS）| control+shift+p（Windows\Linux)
支持插件系统，已有插件支持 Gitee、青云等第三方图床
更多第三方插件以及使用了 PicGo 底层的应用可以在 Awesome-PicGo 找到。欢迎贡献！
支持通过发送 HTTP 请求调用 PicGo 上传（v2.2.0+)
更多功能等你自己去发现.
---
写累了放个风景图片养养眼。🌹
![路灯](https://img-blog.csdnimg.cn/7cf90e95404e4c40bb295f88c4f83e7c.jpeg#pic_center)~图片来源：抖音某用户~

---
# Github必备知识
![GitHub](https://img-blog.csdnimg.cn/4d9bf71fa60648e991ee1c9fd750a3af.png)
## 1. GitHub的历史
GitHub历史参照csdn穆瑾轩[Git&GitHub就是这么简单](https://blog.csdn.net/xiaoxianer321/article/details/118713836?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522167530488716800188591323%2522%252C%2522scm%2522%253A%252220140713.130102334.pc%255Fblog.%2522%257D&request_id=167530488716800188591323&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~blog~first_rank_ecpm_v1~rank_v31_ecpm-1-118713836-null-null.blog_rank_default&utm_term=github&spm=1018.2226.3001.4450)而写。

可能大家都听过Git和GitHub，关于他们也有很多的描述，要说清楚他们之间的关系，故事还得从那一年说起。
### 1970-80年代初
最初美国贝尔实验室的 Ken Thompson，以BCPL语言为基础，设计出很简单接近硬件的B语言，并用B语言写了第UNⅨX操作系统；早期程序员可以用手工的方式进行备份，并以注释或者新建文本文件来记录变动，如使用cp命令备份，使用tar命令将一些文件归为一个.tar文件

后来 Walter f.Tchy使用C开发了RCS( Revision Control System)用于版本控制，RCS允许多个用户同时读取文件，但只允许一个用户锁定( locking）并写入文件(类似于多线程的 mutex)。RCS的互斥写入机制避免了多人同时修改同一个文件的可能，但代价是程序员长时间的等待,给团队合作带来不便。**(RCS本地版本控制系统)**
### 1986年
直到1986年，Dick Grune写了一系列的shell脚本用于版本管理，并最终以这些脚本为基础，构成了CVS( ConcurrenVersions System)版本控制系统，CVS后来用C语言重写，CVS是开源软件,CVS被包含在GNU的软件包中，并因此得泛的推广，CVS继承了RCS的集中管理的理念，CVS引进分支（branch）的概念，分支是主干文件在本地复制的副本，用户对本地副本进行修改，且可以在分支提交(commit)多次修改。用户在分支的工作结束之后，需要将分支合并到主干中,以便让其他人看到自己的改动。CVS也有许多被人诟病的地方，如两个用户同时合并,那么合并结果将是某种错乱的混合体。

后来 Karl Fogel和 Jim Blandy(是长期的CVS用户)开发了 Subversion，依赖类似于硬连接( hard link)的方式来提高郊率,避免过多的复制文件本身。

### 1991-2001
Linux之父 Linus Torvalds在1991年创建开源的 Linux操作系统与 Linux开源项目的代码是dir和 patch"命令来手动为别人整合代码的。 Linux开源的内核项目管理起来一直很麻烦实在是太发者花费过在版本管理上，社区的兄弟们也对这种方式表达了强烈不满。

### 2002
 到了2002年，一个叫Tim Kemp 的人发现 Subversion 是一个非常好的版本管理系统，但是缺乏一个好的图形界面客户端程序。做一个与 Windows 外壳整合的 Subversion 客户端程序的想法是受一个叫 TortoiseCVS 的 CVS 客户端程序所启发的。Tim 研究了 TortoiseCVS 的源码并以此为 TortoiseSVN 的基础，这也就是我们现在使用的SVN（是一种集中式的版本控制系统）。    Linus Torvald本人相当厌恶CVS以及Subversion，于是Linus选择了一个商业的版本控制系统BitKeeper（分布式VCS）BitKeeper的东家BitMover公司出于人道主义精神，授权Linux社区免费使用这个版本控制系统，但前提是Linux社区的用户不去破解BitKeeper。

### 2005
 一晃眼，到了2005年，Linux社区牛人聚集，由于社区开发Samba的Andrew好奇地破解了BitKeeper公司的分布式VCS产品然后被对方发现，导致Linux项目被BitMover公司回收了免费使用权。Linus向BitMover公司道个歉，于是Linus最终决定写一款开源的分布式VCS软件，花了两周时间自己用C写了一个分布式版本控制系统，这就是Git！一个月之内，Linux系统的源码已经由Git管理了！**（git分布式版本控制系统）**（分布式,当我们连接共享版本库时，可以先将服务器上的项目,克隆到本地，相当于每一台电脑上都有整个项目的文件备份，在没有网时也可以开发,完成开发后,可以先提交到本地仓库,当有网的时候,再提交到共享版本库，这样一来，如果我们的服务器或者我们自己的电脑出故障,我们也没有任何担心的）

### 2008
GitHub（**Git中心枢纽**），于2007年10月1日开始开发，由GitHub公司，的开发者Chris Wanstrath、PJ Hyett和Tom Preston-Werner使用Ruby on Rails编写而成，他的UI设计确实有点糟糕。网站于2008年2月以beta版本开始上线，4月份正式上线。2008年7月，发布了Gists功能，用于托管代码片段。2008年12月，发布了GitHub Pages功能，这样大家就可以基于这个的repo，创建网站了。
### 2011
到了2011年，GitHub公司启动GitHub Enterprise项目，探索盈利模式。也是在11月，Github拥有了100万用户。
### 2014
 2014年5月，Atom编辑器免费开源。现在大家常用的VSCode就是基于Atom。
### 2018
2018年6月,微软宣布收购 Github,耗资75亿美元。 Github上已经有了3000万开发者。
### 2019
1月份, Github宣布私有仓库全部免费,无限创建,但是最多只能有三个合作者。因为GHub上性别严重失衡,男性群体高达95%以所以 Github经常被大家戏称为 Gayhub,也是全球最大同性交友网站

>**总结**   
>Git 是由 Linux 之父 Linus Tovalds 为了更好地管理linux内核开发而创立的分布式版本控制系统。<p>
><b>GitHub 的核心是一个名为 Git 的开源版本控制系统，Git 负责在您的计算机上本地发生的所有与 GitHub 相关的事情，GitHub可以托管各种git库，并提供一个web界面。<p>
GitHub的独特卖点在于从另外一个项目进行分支的简易性。为一个项目贡献代码非常简单，首先点击项目站点的“fork”按钮，然后将代码检出并将修改加入到刚才分出的代码库中，最后通过内建的“pull request”机制向项目负责人申请代码合并。

---
# GitHub
## GitHub注册及教程
### 注册GitHub账号
首先去[GitHub官网](https://github.com/)注册一个属于你的账号，进入后点击`Sign Up`,后接着往下走，这里就不详细的描述注册的过程了，准备一个可以使用的邮箱账号就行。

注册好账号后：我们的Github主页就是这个样子的。下面会对主页一些内容进行简单的介绍。
>  tips:以下GitHub教程内容来自[穆瑾轩
](https://blog.csdn.net/xiaoxianer321/article/details/118713836?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522167530488716800188591323%2522%252C%2522scm%2522%253A%252220140713.130102334.pc%255Fblog.%2522%257D&request_id=167530488716800188591323&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~blog~first_rank_ecpm_v1~rank_v31_ecpm-1-118713836-null-null.blog_rank_default&utm_term=github&spm=1018.2226.3001.4450)
版权归原作者所有

![GitHub教程](https://img-blog.csdnimg.cn/42b5d020c4e74678a329156f2eb3876b.png)
![教程1](https://img-blog.csdnimg.cn/aed1456f662c414ca7ec34c08accd984.png)
![教程2](https://img-blog.csdnimg.cn/c52f23cb6a8a4cffbd276e7763546033.png)
![教程3](https://img-blog.csdnimg.cn/b841765a69374994858250bf21d08bdc.png)
![教程4](https://img-blog.csdnimg.cn/ebc01af0bfbe479aa28f6affc5be3dfc.png)
![教程5](https://img-blog.csdnimg.cn/aaa7dab59326431081d36cec8503fcb7.png)
![教程6](https://img-blog.csdnimg.cn/c236686a92ec4d96a6d37e316f8faf02.png)
![教程6](https://img-blog.csdnimg.cn/ff7945edad2143888cad1ccc2e8c6e0e.png)
![教程7](https://img-blog.csdnimg.cn/cf2d1885a11b49d0a914e6abcccce04e.png)

累了吧，看看风景吧。
![风景](https://img-blog.csdnimg.cn/52656aba5e3b4179b58bd9b880de7f85.jpeg#pic_center)~图片来源：抖音某网友~

---
# 实操教程
## 1.参照上述过程创建好GitHub仓库
## 2.下载PicGo
GithubPicGo项目地址：<https://github.com/Molunerfinn/PicGo>

下载地址：[PicGo](https://molunerfinn.com/PicGo/) （比较慢）

镜像下载地址：<https://github.com/Molunerfinn/picgo/releases>（比较快）

由于下载过程较慢，甚至会出现下载失败的情况，所以我为大家提供了一个云盘下载资源。为了方便维护，我把下载链接放在了公众号后台，关注我的公众号【ESRG技录橙】，回复 “图床” 即可获得下载链接。

下载完成，双击启动安装即可。

	如果安装成功，PicGo不能正常使用，则可以用兼容模式启动。
**此电脑--->右键属性--->兼容性--->以兼容模式运行这个程序**
下方**以管理员身份运行此程序**==（图中忘记标选）==

![属性](https://img-blog.csdnimg.cn/c86eb6a6e3ed44e7987b75aca99fab50.png)
## 3.运行`PicGo`

![PicGo的github设置](https://img-blog.csdnimg.cn/9696b61aa9ba42ebb64a6fe3c49eb040.png)

**仓库名：[`github`用户名]/[第一步新建的仓库名称]**

**分支：默认master，从2020.10.01开始，`github`的默认分支名变更为main**

**设定`token：token`创建跳转到[Token获取](#Token获取)**

> token的意思是“令牌”，是服务端生成的一串字符串，作为客户端进行请求的一个标识。

>当用户第一次登录后，服务器生成一个token并将此token返回给客户端，以后客户端只需带上这个token前来请求数据即可，无需再次带上用户名和密码。

>简单token的组成；`uid`(用户唯一的身份标识)、time(当前时间的时间戳)、sign（签名，token的前几位以哈希算法压缩成的一定长度的十六进制字符串。为防止token泄露）

>`github`在主页的头像下有个Settings选项，具体的地址是：<https://github.com/settings/tokens>

### Token获取
推荐选择创建稳定
![Token](https://img-blog.csdnimg.cn/5ded6ef420c144e094382a7a21bb561f.png)
![创建新的Token](https://img-blog.csdnimg.cn/e5f6004cfc6742e79b9e85703602b15b.png)
~点击Generate taken~
![note](https://img-blog.csdnimg.cn/d3a0a316080a4ca4ac23dfc87d2f590c.png)
**只显示一次，妥善保管**
![note2](https://img-blog.csdnimg.cn/57308546dd4842f687b31d2816300857.png)


指定存储路径：可填可不填，如果填写了，图片就会存储在`img`文件夹下

设定自定义域名：https://cdn.jsdelivr.net/gh/[`github`用户名]/[仓库名]@main，注意，此处的分支一定要填写@main，否则默认使用master分支。而现在`github`创建的默认分支名为main，如果不指定，则会出现图片不能上传的情况。
## 4.配置`typora`

在`typora`顶部菜单界面，选择“文件” - > “偏好设置”，设置图片存储方式。
![typora配置](https://img-blog.csdnimg.cn/705c443273c34cc99f248fab59bf1544.png)
配置好后直接拖拽上传
![picgo图床](https://img-blog.csdnimg.cn/34f121868cc148e1b2899f631b1101a2.png)
![配置成功](https://img-blog.csdnimg.cn/b26e606685504a56bf3c60db5e4e5cca.png)
仓库配置好后`GitHub`即可出现图片
![img](https://img-blog.csdnimg.cn/0d776176ef1146b8ab420473506a6e31.png)

---
