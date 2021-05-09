---
title: 某 c7w 的工作报告
date: 2021-5-9 17:53:20
---



## 工作报告（5.9）

没错，这一条是测试，如果测好了就把这个补全。

## 工作报告（5.8）

+ 博客相关
  + 为 thucs04.cn 添加了域名邮箱支持
  + <s>[*] 使用 admin@thucs04.cn 注册 gitlab 账号，并创立 private repo</s>
  + <s> username: admin@thucs04.cn psk: qianc20yyds</s>
  + <s>[*] 该 private repo 将用来存储博客文章的所有 raw markdown 版本</s>
  + 我们放弃了 gitlab，因为我发现 github 的 organization 也是可以创建 private 仓库的
  + 我们将所有的博客 source 文件夹下的内容，使用 thucs04/blog-raw 来存储
  + https://github.com/THUComputerScience04/blog-raw
+ 网络相关
  + 清华网络自动认证
    + 我们使用 thu.services 中提供的 GoAuthing 登入系统
    + https://github.com/z4yx/GoAuthing
    + **问题：密码的明文存储？如何能够切换？**

