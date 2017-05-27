# Day01-初识Git和Github

tag ： git
date : 2017-5-27
auther : itgoyo

---

## Git
说到Git你或许不是了解，但是Linux系统你一定听过，Git就是Linux系统创始人林纳斯·托瓦兹一手创造出来的，奠定了他在编程界大神的地位。

#### Git的诞生
这是一个传奇故事，时间定格到2005年，当时linux再使用一个叫做BitKeeper的版本控制工具，BitKeeper开发商在这一年决定不再免费提供给linux社区使用，linus当即伸出了中指，于是两周后Git诞生了，一个月之内Linux的源码已经由Git托管。

<div align=center>
![](http://omvbl46i3.bkt.clouddn.com/17-5-27/59474026.jpg)
</div>

#### Git的优点
git是国外开源版本库，不需要自己搭建服务器，你在上面搭建上传的工程代码都是公开的，谁都可以访问，可以设置团队成员分配修改的权限。如果要像SVN一样指定的人可以访问Git就需要收费了，SVN需要你有一台服务器，上面安装SVN Server实现版本控制

* 快速

如果你每移动一下鼠标都要等待五秒，是不是很受不了？版本控制也是一样的，每一个命令多那么几秒钟，一天下来也会浪费你不少时间。Git的操作非常快速，你可以把时间用在别的更有意义的地方。

* 离线工作

在没有网络的情况下如何工作？如果你用SVN或者CVS的话就很麻烦。而Git可以让你在本地做所有操作，提交代码，查看历史，合并，创建分支等等。

* 回退

人难免犯错。我很喜欢Git的一点就是你可以“undo”几乎所有的命令。你可以用这个功能来修正你刚刚提交的代码中的一个问题或者回滚整个代码提交操作。你甚至可以恢复一个被删除的提交，因为在后端，Git几乎不做任何删除操作。

* 省心

你有没有丢失过版本库？我有，而那种头疼的感觉现在还记忆犹新。而用Git的话，我就不必担心这个问题，因为任何一个人机器上的版本都是一个完整的备份。

* 选择有用的代码提交

当你把纽带，冰块还有西红柿一起扔进搅拌机的时候至少有两个问题。第一，搅拌过后，没有人知道之前扔进去了些什么东西。第二，你不能回退，重新把西红柿拿出来。同样的，当你提交了一堆无关的更改，例如功能A加强，新增功能B，功能C修复，想要理清这一堆代码到底干了什么是很困难的。当然，当发现功能A出问题的时候，你无法单独回滚功能A。Git可以通过创建“颗粒提交”，帮你解决这个问题。“staging area”的概念可以让你决定到底那些东西需要提交，或者更新，精确到行。

* 自由选择工作方式

使用Git，你可以同时和多个远程代码库连接，“rebase”而不是"merge"甚至只连接某个模块。但是你也可以选择一个中央版本库，就像SVN那样。你依然可以利用Git的其他优点。

* 保持工作独立

把不同的问题分开处理将有助于跟踪问题的进度。当你在为功能A工作的时候，其他人不应该被你还没有完成的代码所影响。分支是解决这个问题的办法。虽然其他的版本控制软件业有分支系统，但是Git是第一个把这个系统变得简单而快速的系统。

* 随大流

虽然只有死于才随着波浪前进，但是很多时候聪明的程序员也是随大流的。越来越多的公司，开源项目使用Git，包括Ruby On Rails，jQuery，Perl，Debian，Linux Kernel等等。拥有一个强大的社区是很大的优势，有很多教程、工具。随着开源的热潮越来越汹涌，使得类似于Github这样子的开源网站，受到更多更多程序员的喜爱与青睐，Git是时代选择的必然结果。

## Github
GitHub 是一个面向开源及私有软件项目的托管平台，因为只支持 Git 作为唯一的版本库格式进行托管，故名 GitHub。GitHub 于 2008 年 4 月 10 日正式上线，除了 Git 代码仓库托管及基本的 Web 管理界面以外，还提供了订阅、讨论组、文本渲染、在线文件编辑器、协作图谱（报表）、代码片段分享（Gist）等功能。目前，其注册用户已经超过350万，托管版本数量也是非常之多，其中不乏知名开源项目 Ruby on Rails、jQuery、python 等。

#### Github趣事
2013年1月15日晚间，全球最大的社交编程及代码托管网站GitHub突然疑似遭遇DDOS攻击，访问大幅放缓，该网站管理员经过日志查询，发现是来自12306的抢票插件用户洪水般的访问导致GitHub出现问题。该事件加上当初知乎吵架事件，使得Github在国内的发展像炸开的锅一样，拦都拦不住。

## Git的安装

- Window

下载Git

[https://git-scm.com/downloads](https://git-scm.com/downloads)

配置ssh key

```Java
ssh-keygen -t rsa -C "yourid@xxmail.com"
```
![](http://omvbl46i3.bkt.clouddn.com/17-5-27/96538348.jpg)

然后连续按回车键3次

![](http://omvbl46i3.bkt.clouddn.com/17-5-27/74500875.jpg)


出现以上图片说明已经在本地创建好ssh key了
路径在C:\Users\admin\.ssh
![](http://omvbl46i3.bkt.clouddn.com/17-5-27/44708043.jpg)

然后使用文本编辑器打开id_rsa.pub，然后把里边的内容完全复制

然后登陆[Github官网](https://github.com)

[https://github.com](https://github.com)

点击设置选项

![](http://omvbl46i3.bkt.clouddn.com/17-5-27/28296803.jpg)

然后把刚刚复制的ssh key复制进去

![](http://omvbl46i3.bkt.clouddn.com/17-5-27/32336481.jpg)

完成了以上步骤检测一下是否已经成功链接上Github

```
$ ssh -T git@github.com
```

```
admin@iTgoyo-PC MINGW32 ~/Desktop
$  ssh -T git@github.com
The authenticity of host 'github.com (192.30.255.112)' can't be established.
RSA key fingerprint is SHA256:nThbg6kXUpJWGl7E1IGOCspRomTxdCARLviKw6E5SY8.
Are you sure you want to continue connecting (yes/no)?
```

输入yes

![](http://omvbl46i3.bkt.clouddn.com/17-5-27/58239146.jpg)
出现上面信息即本地连接Github已经成功

- Mac OS
基本和上面没差
打开终端，输入
```
cd ～/.ssh
```

```
如果存在，先将已有的ssh备份，或者将新建的ssh生成到另外的目录下
如果不存在，通过默认的参数直接生成ssh:
ssh-keygen -t rsa -C xxxxx@gmail.com（注册github时的email）
(输入完成后，按enter健即可，命令行会自动提示下面这一行👇，接下来的命令行一路按enter健即可)
Generating public/private rsa key pair.
Enter file in which to save the key (/Users/twer/.ssh/id_rsa):
Created directory '/Users/twer/.ssh'.
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in /Users/twer/.ssh/id_rsa.
Your public key has been saved in /Users/twer/.ssh/id_rsa.pub.
The key fingerprint is:
18:16:11:c9:01:6c:48:09:7f:27:66:43:0d:7f:3f:84 xxxxx@gmail.com
The key's randomart image is:
+--[ RSA 2048]----+
|.o.++=== |
|.ooo.+. . |
| ..* = E . |
| o = + o |
| . S o |
| . |
| |
| |
| |
+-----------------+
```

此时会在你的电脑里生成一个.ssh的文件，里面有你的ssh key的信息，如果需要复制这个信息，可以在命令行里输入 pbcopy < ~/.ssh/id_rsa.pub，这个是复制的命令，然后打开一个文本文件，粘贴即可

过程参考Windows

#### 对于Github的初学者的建议

推荐两本Github入门

[GitHub入门与实践](https://github.com/itgoyo/500Days-Of-Github/PDF/GitHub入门与实践.pdf)

[github-beginners](https://github.com/itgoyo/500Days-Of-Github/PDF/github-beginners 1.0.pdf)

自我感觉刚入门Github的时候没必要逼着自已一定要使用命令行敲完代码，然后创建仓库，提交信息，上传代码。

因为图形化界面的Git工具很多

个人推荐官方的[Github For Desktop](https://desktop.github.com/)

当然也有其他童鞋觉得[SourceTree](https://www.sourcetreeapp.com/)也是不错的选择，看自己爱好吧，工具而已，自己喜欢就好。

有童鞋反馈说Github For Desktop安装比较慢的问题，可以使用[Lantern](https://github.com/getlantern/forum)翻墙,如果你觉得速度不错，想办理会员版的话可以使用我的推荐码**2CR4W2**进行购买专业版，这样子我们都彼此会多获得三个月的会员时间

#### 提交代码到Github仓库

- 先在Github官网上创建自己的仓库

![](http://omvbl46i3.bkt.clouddn.com/17-5-27/76224850.jpg)

![](http://omvbl46i3.bkt.clouddn.com/17-5-27/33695609.jpg)

以下我拿桌面版的Github来进行演示

![](http://omvbl46i3.bkt.clouddn.com/17-5-27/95435534.jpg)

即可下载到本地

![](http://omvbl46i3.bkt.clouddn.com/17-5-27/28740787.jpg)

即可打开到本地Github项目的仓库

我们随意改变一下工程的内容，例如以下，我新增了一个txt文本文件

再点开客户端

![](http://omvbl46i3.bkt.clouddn.com/17-5-27/62240631.jpg)

此时客户端已经检测到内容的改变，当你想把本地的资源提交到远程的仓库时

![](http://omvbl46i3.bkt.clouddn.com/17-5-27/56382664.jpg)

同步完成了之后你就会发现Github仓库上面已经有你刚刚提交的信息了

![](http://omvbl46i3.bkt.clouddn.com/17-5-27/75169227.jpg)

谢谢你的浏览，如果你觉得这篇文章对你有帮助或者想收藏的话，不妨点一点上面的star或者watch。

如果文中有什么错误或者似乎错别字的话，也可以指出来，届时会修改好，再重新发布一次，如果你有什么好的建议和想法的话，欢迎邮件联系我。

E-mail：itgoyo@gmail.com
