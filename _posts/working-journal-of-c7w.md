---
title: 某 c7w 的工作报告
date: 2021-5-9 17:53:20
---

这里面是一只勤勉的鸽子的工作报告。

<!--more-->

## 工作报告（5.9）

没错，这一条是测试，如果测好了就把这个补全。

没错，测好啦！

+ sync.py

```python
import os
import re
import sys
import shutil
import subprocess

blog_dir = '''/Project/thucs04.cn/'''
blog_process = ''''''

def pull():
    os.chdir(blog_dir+"blog_raw")
    try:
        pull_output = subprocess.check_output(['git', 'pull', 'origin', 'master']).decode('utf-8')
    except:
        pull_output = ""
    return pull_output

def hexo():
    print("Start Moving files and generating HTML.")
    try:
        shutil.rmtree(blog_dir+"blog_new/source")
    except:
        pass
    copy_result = subprocess.check_output(['cp', '-r', blog_dir+"blog_raw", blog_dir+"blog_new/source"]).decode('utf-8')
    shutil.rmtree(blog_dir+"blog_new/source/.git")
    os.chdir(blog_dir+"blog_new")
    copy_result = subprocess.check_output(['hexo', 'clean'])
    copy_result = subprocess.check_output(['hexo', 'g'])
    try:
        shutil.rmtree(blog_dir+"www/blog")
    except:
        pass
    copy_result = subprocess.check_output(['cp', '-r', blog_dir+"blog_new/public", blog_dir+"www/blog"]).decode('utf-8')
    
    

if __name__ == "__main__":
    if(len(sys.argv)>=2):
        if sys.argv[1] == "g":
            hexo()
            exit(0)
    pull_output = pull()
    # Check if pull_output contains "Already up to date."
    if re.search("Already up to date.", pull_output):
        print("Already Up To Date.")
    else:
        sel = '''Updating (.*?)\.\.(.*?)\n'''
        pattern = re.compile(sel)
        resultGroup = pattern.findall(pull_output)
        if len(resultGroup) == 0:
            exit(0)
        hexo()

```

+ /usr/lib/systemd/system/blog-sync.service
+ /usr/lib/systemd/system/blog-sync.timer

To-Do List:

+ 发现 GoAuthing 还是有问题
+ 博客端口要加一波反向代理，不然链接有问题
+ 换主题，Customize

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

