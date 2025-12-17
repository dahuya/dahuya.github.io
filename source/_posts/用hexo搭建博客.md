---
title: 用hexo搭建博客
date: 2025-01-04 21:14:35
tags:
---

1准备工作

下载nodejs和git,vscode并安装



输入

```
ssh-keygen -t rsa -C "邮件地址"
```

敲4次Enter

然后进入C:\Users\用户名，在里面进入.ssh文件，用文本编辑器打开，复制ssh keys,打开github,粘贴，如图

![](https://s2.loli.net/2025/01/04/EO3JVsf2YQxrmjR.png)



**![](https://s2.loli.net/2025/01/04/Kq72YZkPXewLtUT.png)**

然后输入ssh -T git@github.com  如果显示不能连接就输入ssh -T -p 443 git@ssh.github.com

这是因为防火墙或网络设置可能会阻止 SSH 端口 22 的通信，后面一个是443端口，基本不会被封。

在喜欢位置新建文件Blog，然后进入文件夹

右键空白处然后点Git bash here，依次输入

```
hexo init
```

hexo install

hexo g  生成静态文件。
这个命令会将 Markdown 文件转化为 HTML 页面，
hexo **s**  启动本地服务器，预览博客效果。
在本地启动一个开发服务器，方便在发布前查看博客页面效果。



用记事本打开_config.yml

  type: git
  repository: 
  branch: main

npm install hexo-deployer-git --save



```
hexo g（生成）
hexo d（上传）  部署博客到远程服务器。
```