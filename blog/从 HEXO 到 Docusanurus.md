---
slug: first
# title: 博客转移
author: 小哲
author_title: Executives @ Yespace
author_url: https://vxiaozhe1998.gitee.io
author_image_url: https://gitee.com/Vxiaozhe1998/Pic/raw/master/img/01.jpg
# image: https://gitee.com/Vxiaozhe1998/Pic/raw/master/img/01.jpg
tags: [博客, 编程, 文档, docusaurus]
---

# 从 HEXO 到 Docusanurus	

## 引言

作为一个很奇怪的人，在想要做一件事之前总要把能想到的准备工作都做好，现在，我想把读书笔记整理到一个博客中，我本身是有博客的，地址：https://vxiaozhe1998.gitee.io ,使用的是 `HEXO` 的框架和 ` NEXT` 的主题，不得不说，这个主题还是很简约好看的，但是写个博客记录生活还可以，用来记录读书笔记就多少有点儿力不从心了，但是作为一个编程小灰的我，在这个框架上进行魔改，多少有点儿难为情，我又不想使用 `语雀` 等别人的知识库平台，因为平台敏感词的限制，很多时候都会限制我语言组织，本来语文修养就不是很好，被限制了我可能会傻掉，因此，在经过多次挑选之后，最终选择了 `Docusanurus` , 因为本篇博文是在我初步了解了这个框架写的，所以在对于该框架的很多功能或者样式都不了解的前提下我暂时使用原始的 `Markdown` 进行先导的编写（其实我还想发布到其他平台，所以用最原始的 `Markdown`  写最保险)，对于该框架内置的一些功能与配置，我将在本文中进行详细的介绍，由于暂不了解 `Docusanurus` 的尾注功能，我将将参考的链接或者文本随附于引用处，下面，开始 `Docusanurus` 的搭建之路吧，哦，对了能找到这个框架多亏了一个网站：https://jamstack.org/ ，在这个网站里有很多静态页面生成的框架，他甚至还为此做了一个排行榜，愿意折腾的兄弟可以挨着评测评测。

<!--truncate-->

> 作为一个买(bu)不（xiang）起（mai）服务器的白嫖党，我将将 `Docusanrus` 存放在 `gitee` 或者 `github` 上，但是由于 `gitee` 近期正在进行改造，没法渲染页面，那就只能使用 `github` 进行托管了与渲染了，不过 `github` 也有他的好处，就是可以使用个人的域名，由于我的个人域名上已经搭建了我最老的博客： https://vxiaozhe1998.cn ，因此，我将尝试在二级域名上进行，由于是读书笔记，二级域名就定义为： https://note.vxiaozhe1998.cn ,对于 `github` 页面访问的速度问题，我可能会慢慢进行优化，因为虽然是整读书笔记的前期准备工作，但是我不希望影响我的阅读进度。

## 我用到的软件

+ `Vscode` ：yyds 的 `Vscode`  [下载地址](https://code.visualstudio.com/)
+ `git`：使用 `github` 不得不使用的软件 [下载地址](https://git-scm.com/downloads)
+ `node.js`：面向 `npm` 编程的工程师必备的 [下载地址](http://nodejs.cn/download/) （注：根据官网的要求 `node.js` 版本需要不低于 `12.13.0` , 这个下载时候注意一下，下载安装之后可以通过在 `CMD` 中输入 `node -v` 来查看版本）
+ `yarn` ：这个是一款性能强劲的 `Javascript` 包管理器，他可替代 `npm` 客户端，在安装了 `node.js` 之后，可以通过在 `CMD` 中输入 `npm install -g yarn` 进行安装，安装之后可以通过 `yarn -version` 进行查看版本，要求版本不低于 `1.5`

> 他们怎么使用，安装什么插件我在此就不再赘述了，因为这些东西的文档都比较完备，随便去 `百度一下` , `必应几下` 都能搜到一堆，软件篇到此结束。

## 开始使用 `Docusanurus`

> 官方文档在此：https://docusaurus.io/zh-CN/docs

:::info 那我为啥还要写？

虽然他有中文版本，但是我感觉很多都是机翻的并且还有很多没有进行翻译，并且不符合我的阅读习惯，很多东西我读的云里雾里的，~~可能是我水平不够~~，因此我希望将我部署的过程完完整整地记录下来，以便下次我一不小心把东西整丢了时的笔记恢复。

:::

### 0. 给他安个家

在任意一个想要给他安家的目录单击右键并选择 `Git Bash Here` 并按照个人的喜好输入下面的代码：

```node.js
npx @docusaurus/init@latest init [名称] [模板]
```

其中：

+ **名称**：是你家的名字，也就是内容存放所在的文件夹的名称
+ **模板**：官方只提供了两个模板 `@docusaurus/theme-classic` 和 `@docusaurus/theme-bootstrap` ，但是根据官方的意思`@docusaurus/theme-bootstrap` 模板不要考虑了，因为他们还没准备好，只有 `@docusaurus/theme-classic`  可用于生产环境，我为了少点儿麻烦事儿，我就选择经典主题了。

对于我来说，我想将框架放到一个名称为 `Note` 的文件夹并使用经典主题 `@docusaurus/theme-classic` ，我需要定位到某个目录，例如我定位到了我的 `H:` 盘，在 `H:` 盘中右键并选择 `Git Bash Here` ，在弹出的窗口中输入：

```node.js
npx @docusaurus/init@latest init Note classic
```

如下图所示：

![指令界面](https://gitee.com/Vxiaozhe1998/Pic/raw/master/img/image-20210717231626236.png)

### 1. 添置点儿家具

创建完了之后，右键单击创建的目录并选择 `通过code打开` ，如果右键菜单没有这个选项可以去百度一下 `为什么我安装了vscode之后右键没有通过code打开？` ，进入 `Vscode` 中之后点击菜单栏的 `终端` 并点击 `新终端` 在弹出的终端中输入下面的代码：

```yarn
yarn start
```

如下图所示：

![指令界面](https://gitee.com/Vxiaozhe1998/Pic/raw/master/img/image-20210717232439483.png)

运行完之后会在自动打开默认浏览器并跳转至 `http://localhost:3000/` 页面，在页面中会显示默认的内容。

**来了解一下添置了什么新家具吧！**

通过
