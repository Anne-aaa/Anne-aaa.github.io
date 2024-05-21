---
title: blog
date: 2024-05-21 15:18:47
tags: 日常记录
---
### 一. 搭建流程

详情见：https://www.zhihu.com/question/21193762 关于搭建的流程。再参考一些别的综合一下。

具体原理是，可以建立master和hexo两个分支，hexo分支用来存放hexo init出来的服务器，master是hexo的静态文件生成后部署到的分支。这样，即使换电脑，也可以继续把代码拉下来，继续用hexo写博客。

### 二. 过程中遇到的问题

电脑是mac 系统是zshrc，环境变量文件是.zshrc

环境变量最后一行写的是pnpm 所以我得用pnpm安装，才能识别到这个command

### 三. 日常改动：

1. 直接把.md文件复制到source/_post文件夹中，复制完之后然后使用文本编辑器打开它，在第一行加上title。 也可以直接 hexo new 一篇博客
2. 在.git目录下，依次执行git add .、git commit -m "..."、git push origin hexo指令将改动推送到GitHub（此时当前分支应为hexo
3. 要进入hexo跟目录（和_config.yml同一目录下），删除旧的静态文件，即 public 文件
   hexo clean。 然后才执行 hexo d -g 生成静态文件并部署到远程服务器,到master分支上。 需要等待一会才能见到。

hexo s可以先在本地预览。

注意问题1.

如果你在运行`hexo`命令时出现了`Usage`提示而无法执行后面的子命令, 很可能是因为你当前所在的目录不是 Hexo 站点的根目录。Hexo 需要在站点根目录下才能正确执行命令。
