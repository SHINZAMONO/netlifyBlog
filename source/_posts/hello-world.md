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

```bash
$ hexo new "My New Post"
```

More info: [Writing](https://hexo.io/docs/writing.html)

### Run server

```bash
$ hexo server
```

More info: [Server](https://hexo.io/docs/server.html)

### Generate static files

```bash
$ hexo generate
```

More info: [Generating](https://hexo.io/docs/generating.html)

### Deploy to remote sites

```bash
$ hexo deploy
```

More info: [Deployment](https://hexo.io/docs/one-command-deployment.html)