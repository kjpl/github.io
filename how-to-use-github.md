说明
作为一名开发者，Github上面有很多东西值得关注学习，可是刚刚接触github，怎样一步步学习使用Github？怎样更高效的利用Github？ 在这里搜集整理网络上面的资料，汇总成这么一篇repo 《Github使用指南》，供大家一起学习。 :octocat:

github 入门使用教程-图文并茂 很简洁的说明如何使用，看图即可明白。
github help Sometimes you just need a little help. 中文翻译版在此Github 帮助文档。
github 之 fork 简介指南 帮你理解清楚什么是fork，fork 的工作流有哪些。
github-cheat-sheet 关于使用 git 和 github 的一些技巧汇总，中文版在此GitHub秘籍
The GitHub Blog github 官方博客，关注最新动态。
How to Build a GitHub Github一名早期员工介绍Github的历史，5年108名员工无人离职。
阳志平：如何高效利用GitHub 介绍的挺全，以及一些用法，如怎样利用Github来学习、演讲找工作等。
github 支持的 emoji表情 :v: :clap:
github guides 从Contributing to Open Source on GitHub、Hello World、Forking Projects、Be Social、Making Your Code Citable、Mastering Issues、Mastering Markdown、Mastering Wikis、Getting Started with GitHub Pages 等9个方面图文详细讲解每一步如何使用，以及能做哪些功能。
fork-me-on-github 个人博客、技术博客等如果需要添加github 的彩带，可以使用此方法。
蒋鑫-GotGitHub 《Git权威指南》的作者，对Github有很深的了解。（由于首页打开太慢，放到了本文目录中，下面的文章既是）
原文地址：http://www.worldhello.net/gotgithub/index.html

GotGitHub¶
Author:	Jiang Xin
Version:	v0.9.1-13-g5075479
Copyright:	Creative Commons BY-NC-SA
前言¶

动笔写GitHub不是因为我对其了解，恰恰是对其太不了解。

在我的《Git权威指南》 [1] 一书中，涉及到GitHub的只有区区三页纸，这显然回答不了读者对于GitHub的诸多疑问。 记得在《Git权威指南》刚刚完稿之际，机械工业出版社华章公司的杨福川编辑就鼓动我写一本关于GitHub的书，我用了好多理由推辞了。 头条理由就是我真的累着了。在每一章节开始动笔之时，都好像是坐在了中学语文考试的考堂上写作文，时间快到了可仍然动不了笔， 再写一本书无疑要重复这一痛苦的经历。 第二个理由是我更喜欢编程，而不是写文档，尤其写GitHub会有大量截图、图像处理的琐碎工作。 第三个理由彻底让编辑投降，那就是GitHub是一个国外网站，也许书一出，【此句已被原作者删除】。

让我最终决定动笔，是源于CSDN蒋总在美国拜访GitHub总部后告诉我的一些见闻，我对GitHub如此成功运作产生了兴趣，于是开始研究GitHub的博客，愈发发现GitHub是一群有趣的人在做的有趣的事，如果只把GitHub当作一个Git服务器，实在是暴殄天物。GitHub已经并将继续获得成功，若真能凭借此书把GitHub尽量全面地展现，让每一个Git使用者用好GitHub也是一件幸事。

这本书将采用GitHub的方式进行撰写和发布 [2] ，任何人都可以看到本书（包括源码），更可以用GitHub的方法参与本书的撰写和纠错。网络出版对于我和杨福川编辑都是一个全新的体验。感谢Git，让我在一年内拥有了两种不同的出版体验。

– 蒋鑫, 2011.12

[1]	http://www.worldhello.net/gotgit/
[2]	https://github.com/gotgit/gotgithub
目录¶

1. 探索GitHub
1.1. 什么是GitHub
1.2. GitHub亮点
1.3. 探索GitHub
2. 加入GitHub
2.1. 创建GitHub账号
2.2. 浏览托管项目
2.3. 社交网络
3. 项目托管
3.1. 创建新项目
3.1.1. 新版本库即是新项目
3.1.2. 版本库初始化
3.1.3. 从已有版本库创建
3.2. 操作版本库
3.2.1. 强制推送
3.2.2. 新建分支
3.2.3. 设置默认分支
3.2.4. 删除分支
3.2.5. 里程碑管理
3.3. 公钥认证管理
3.3.1. 用户级公钥管理
3.3.2. 项目级公钥管理
3.4. 版本库钩子扩展
3.4.1. 邮件通知功能
3.4.2. 和Redmine整合
3.5. 建立主页
3.5.1. 创建个人主页
3.5.2. 创建项目主页
3.5.3. 使用专有域名
3.5.4. 使用Jekyll维护网站
4. 工作协同
4.1. Fork + Pull模式
4.1.1. 版本库派生
4.1.2. Pull Request
4.1.3. 手工合并
4.1.4. 在线编辑
4.1.5. 简化的 Fork + Pull Request
4.2. 共享版本库
4.2.1. 版本库授权
4.2.2. 与传统集中式工作模式的异同
4.2.3. 合并后推送
4.2.4. 合并还是变基
4.3. 组织和团队
4.3.1. 创建新组织
4.3.2. 组织管理
4.3.3. 版本库管理
4.3.4. 个人还是组织
4.4. 代码评注
4.4.1. 提交评注
4.4.2. 逐行评注
4.5. 缺陷跟踪
4.5.1. 标签
4.5.2. 里程碑
4.5.3. Issue的生命周期
4.5.4. Pull Requst也是Issue
4.6. 维基
4.6.1. 维基初始化
4.6.2. 使用维基
4.6.3. 维基与Git
5. 付费服务
5.1. GitHub收费方案
5.2. GitHub企业版
6. GitHub副产品
6.1. GitHub:Gist
6.1.1. 数据的粘贴和引用
6.1.2. Gist背后的Git库
6.1.3. Greasemonkey
6.1.4. 命令行操作Gist
6.2. 其他版本控制工具支持
6.2.1. 用SVN操作GitHub
6.2.2. 用Hg操作GitHub
6.3. 客户端工具
6.3.1. github:mac
6.3.2. hub
6.3.3. iOS应用
6.4. 其他
6.4.1. GitHub:Jobs
6.4.2. GitHub:Shop
6.4.3. GitHub短网址服务
6.4.4. GitHub Open Source
7. 附录：轻量级标记语言
