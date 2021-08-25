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

部署环境小到安装操作系统，大到部署一个工作项目并调优

## 1.macOS Big Sur11.5.2

Mac开发环境是大家公认较为优秀的，因此放在第一位讲，废话不多说直接开始

* 部署操作小到操作系统的安装，大到整个项目的开发部署调优维护，都在一开始操作系统的安装便要确定最终的方向和目的，因此在Big Sur 首次安装完毕运行向导时就要明确我们的方向和操作。

1. 硬盘加密选项，选择不加密
2. Apple ID注册登录(邮箱注册较好)
3. iCloud 文稿选择不同步

* Xcode安装

  * 两种方法：APP Store ｜ Apple Developer 支持

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
* Homebrew🍺
  * 使用Mac的第一源动力：[Homebrew](https://brew.sh/)
  * 一键安装：
    ```bash
    /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
    ```

### Generate static files

```bash
$ hexo generate
```

More info: [Generating](https://hexo.io/docs/generating.html)

### Deploy to remote sites

```bash
$ hexo deploy
```