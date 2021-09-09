---
index_img: /img/uploads/Deployment.png
title: 0.0 Deployment | 部署
date: 2021-08-22 23:59:43
updated: 2021-08-22 23:59:43
tags:
  - 备忘
  - 避坑
  - 部署
categories:
  - DEV
keywords:
  - 部署
---
> ## *工欲善其事，必先利其器                     ——《论语·卫灵公》*

大学三年加上近期的一段实习都令我发现一个不解的现象，开发技术熟练的人员却连书本技术篇第一章的开发环境部署都不熟悉甚至不会，大家似乎已然将环境部署和开发想当然的分开学习，我认为这是致命的。你或许会说我吃个饭还用想稻谷是怎么种出来的？我怎么可能啥都会？但这就好比当农民伯伯和你去执行节约粮食这个习惯一样，对你而言是行为约束，对他而言这是精神上的理所应当的，二者之间的执行力度将会截然不同。因此花了一周搭建起属于自己的博客，在此列出三个主流效率工作系统的开发环境配置胎教指北。为了给自己备忘学习，也为了在网络垃圾资源泛滥的当下给各位节省时间，从同一起点出发，要卷也能从同一起点开卷🤪

- - -

### 主流操作系统

### macOS Big Sur11.5.2

### Windows 10/11

### Manjaro-KDE-21.0.7-210614-linux510

## 1.macOS Big Sur11.5.2

Mac开发环境是大家公认较为优秀的，因此放在第一位讲，废话不多说直接开始

* 部署操作小到操作系统的安装，大到整个项目的开发部署调优维护，都在一开始操作系统的安装便要确定最终的方向和目的，因此在Big Sur 首次安装完毕运行向导时就要明确我们的方向和操作。

1. 硬盘加密选项，选择不加密
2. Apple ID注册登录(邮箱注册较好)
3. iCloud 文稿选择不同步

* Xcode安装

  * 两种方法：APP Store ｜ Apple Developer 支持

![APP Store](https://portal.qiniu.com/cdn/domain/qxk6l0b62.bkt.clouddn.com/https://portal.qiniu.com/cdn/domain/qxk6l0b62.bkt.clouddn.com/uPic/pOuehF.png)

    APP Store：[‎Xcode on the Mac App Store (apple.com)](https://apps.apple.com/us/app/xcode/id497799835?mt=12)

    Apple Developer：[More - Downloads - Apple Developer](https://developer.apple.com/download/all/)
  * Command Line Tools for Xcode 下载安装（请对应安装的Xcode版本）
  * 安装完后请Xcode打开一次，阅读并同意Xcode使用协议

* <details>
<summary>科学上网GitHub开源乐园，学生党避免资本压榨的学习天堂</summary>
<p><b>由于国内的网络安全问题，大家会发现GitHub或微软账号登陆时长出现无法链接或者链接缓慢，虽然现在已经有了许多替代方案，但依然会出现链接失效、资源维护老旧、盗版倒卖，甚至违法诈骗</b></p>
<p><b>因此在此建议大家依然是买一张飞机票，飞向开源天堂，如此井底之蛙也能突破水压，越过井壁，发现外面精彩的世界</b></p>
<p><b>在此便不便多言了，这里推荐Clash，也是一款免费的开源软件，覆盖我所介绍的三个操作系统，macOS推荐安装ClashXPro，设计了增强模式更加强大便利，使用起来如履平地，丝滑流畅</b></p>
<p><b>接下来便考验的是进入此行的最基础基本功，搜索引擎的使用和学习，你若成功GET了那么请继续看下去，若没有明白恭喜你可以打开WPS写转专业申请或者辞职报告转行了</b></p>

* 初次设定git

  * 开启你的小飞机登陆GitHub：[GitHub](https://github.com/)
  * 注册GitHub账号
  * global git config：这是你的身份凭证，此时请打开你的terminal终端.app，开启你今后职业生涯将做的最多的工作：⌘command + CV

    ```bash
    git config --global user.name "你的git用户名"
    git config --global user.email 你的GitHub账户绑定邮箱@example.com
    ```
* Homebrew🍺安装
  * 使用Mac的第一源动力：[Homebrew](https://brew.sh/)
  * 一键安装：
    ```bash
    /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
    ```
  * <details> 
<summary>什么是Homebrew？</summary>
<p><b>Homebrew是一个维护非常到位且非常强大的PackageManager包管理工具</p></b>
<p><b>什么是包管理工具？顾名思义可以理解为它就是一个软件管家，不过它没有图形界面，通过SHELL命令行进行交互。你或许会想没有界面是多么麻烦，然而在如今网络环境如垃圾场一样的今天，像RSS新闻订阅一样返璞归真真的会让生活更加淳朴而高效</p></b>
<p><b>如 $ brew install steam 这简单的一句命令意为 嘿brew给我装个steam我想玩游戏了，而完成这一切你不必再打开浏览器关掉弹出的弹窗，被八卦新闻和垃圾资本广告吸引走注意力或打扰，没有虚假的非官方网站链接，假的跳转链接和给你下载木马的高速下载器。下载下来也不必找到安装包点4次下一步再因为因为没去掉checkbox的✅而下一堆推广垃圾软件再去卸载，也不必再去 case(配置错误){default:打开百度;case1:*SDN ⌘CV;case2:飞天逼乎 ⌘CV;case3:过期简书 ⌘CV;case4:阿里云开发者 ⌘CV;case5:腾讯云开发者 ⌘CV;...}</p></b>
<p><b>brew会自动帮你更新所有Homebrew下已装软件,并且为你安装最纯净最新的软件版本，而这种一键帮你搜索安装配置听起来像“VIP“的服务是免费开源不收费的</p></b>

* gcc & cmake 安装

  ```bash
  brew install gcc cmake
  ```
  * 万恶起源的C造就了一切的快速而普及向的开发，因此配置C是难免的，Xcode虽然自带了gcc但我们依然需要Homebrew来安装配置一下，方便今后Homebrew的编译和安装
 
* pyenv & nvm 安装
  ```bash
  brew install pyenv nvm
  ```
  * Homebrew让我们体验到了包管理模式的方便快捷，因此同理，pyenv和nvm分别是python和node的包管理工具，可以在其包下安装多个版本的python和nvm，相当于打的包管理下有多个小的包管理工具。这样的模式就像系统中的多个账户一样，Homebrew相当于系统中的root，pyenv和nvm就是系统中的账户一样，嵌套管理着 

* iterm2 使用macOS的第二大动力源
  ```bash
  brew install iterm2
  ```
  * iterm 是专门面向 macOS 的终端补充软件，其在实现系统终端的功能上加入了大量用户可以自定义的功能，没有花里胡哨，只有更花里胡哨。人皆爱美，这点覆盖率还是蛮高的。
  * iterm 的配置

