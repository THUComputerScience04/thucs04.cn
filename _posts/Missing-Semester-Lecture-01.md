---
title: 如何使用MarkDown书写博客
date: 2021/05/02 21:29:00
tags:
- 知识分享
- Linux
author:
- QC
---



## Missing Semester Lecture 1

**linux系统简单命令操作**

<!--more-->

* echo + 内容：重复一遍
* date：输出当前时间

基本规则：空格代表命令的分割

* echo $PATH 可查看所有环境路径，即每一个指令可能存放的所有路径
* which + 指令可查看该指令的程序路径（如which echo）
* pwd：将输出现在所在路径（present working directory）
* cd /----：切换当前工作路径（change directory）
* .. ：可回到上一级文件夹
* ls：列出当前所有文件
* cd ~/---/---：~即代表 home/名字 这一目录，简略成这样写，相当于从头写路径，有时更方便
* cd -：表示返回上一个所在的文件夹路径中，相当于返回（但不是返回上一级）
* ls --help：可查看很多相关列出文件的方式与操作
  * 例如：ls -l 可以按行展开列出详细文件信息（longlisting format）

* -l打开的文件详细信息中会出现十位字母：
  * 第一位d代表是文件夹
  * 之后9位代表权限，三位一组，共三组
  * 第一组代表自己的权限，第二组是群组的权限，第三组是所有人的权限
  * r-read w-write x-execute
  * 注意：想要打开某文件夹，必须要对之前路径中的所有文件夹都有execute的权限
* mv：move，可以修改文件名与路径，需要mv+两个路径
* rm：只能remove文件
* rmdir：只能remove空文件夹
* mkdir：创建空文件夹
* contrl+l：清屏
* 大于与小于号分别可作为输入流与输出流；其个数代表循环输入、输出的个数
  * 例如：echo hello > hello.txt，那么后者文件中将写入hello
  * cat < hello.txt 将在terminal中输出hello

* | ：(pipe) 以左侧的输出，作为右侧的输入

* sudo (do as super user)：root一般拥有所有所有超级用户权限

* sudo su：让shell以超级用户的身份运行指令，从而可以做很多修改等；su + 原用户名可以切换回来。

  * 例如，修改屏幕亮度：可以sudo su直接以root身份进行调节

    即sudo su; echo 500 > brightness

  * 或者可以 echo 500 |  sudo tee brightness; 其中tee意思为既能通过pipe将左侧输出传给右侧作为输入，也能将该输出打在电脑上

=======
---
title: Missing Semester Lecture 1
date: 2021/05/02 21:29:00
tags:
- 知识分享
- Linux
author:
- QC
---

## Missing Semester Lecture 1

**linux系统简单命令操作**

* echo + 内容：重复一遍
* date：输出当前时间

基本规则：空格代表命令的分割

* echo $PATH 可查看所有环境路径，即每一个指令可能存放的所有路径
* which + 指令可查看该指令的程序路径（如which echo）
* pwd：将输出现在所在路径（present working directory）
* cd /----：切换当前工作路径（change directory）
* .. ：可回到上一级文件夹
* ls：列出当前所有文件
* cd ~/---/---：~即代表 home/名字 这一目录，简略成这样写，相当于从头写路径，有时更方便
* cd -：表示返回上一个所在的文件夹路径中，相当于返回（但不是返回上一级）
* ls --help：可查看很多相关列出文件的方式与操作
  * 例如：ls -l 可以按行展开列出详细文件信息（longlisting format）

* -l打开的文件详细信息中会出现十位字母：
  * 第一位d代表是文件夹
  * 之后9位代表权限，三位一组，共三组
  * 第一组代表自己的权限，第二组是群组的权限，第三组是所有人的权限
  * r-read w-write x-execute
  * 注意：想要打开某文件夹，必须要对之前路径中的所有文件夹都有execute的权限
* mv：move，可以修改文件名与路径，需要mv+两个路径
* rm：只能remove文件
* rmdir：只能remove空文件夹
* mkdir：创建空文件夹
* contrl+l：清屏
* 大于与小于号分别可作为输入流与输出流；其个数代表循环输入、输出的个数
  * 例如：echo hello > hello.txt，那么后者文件中将写入hello
  * cat < hello.txt 将在terminal中输出hello

* | ：(pipe) 以左侧的输出，作为右侧的输入

* sudo (do as super user)：root一般拥有所有所有超级用户权限

* sudo su：让shell以超级用户的身份运行指令，从而可以做很多修改等；su + 原用户名可以切换回来。

  * 例如，修改屏幕亮度：可以sudo su直接以root身份进行调节

    即sudo su; echo 500 > brightness

  * 或者可以 echo 500 |  sudo tee brightness; 其中tee意思为既能通过pipe将左侧输出传给右侧作为输入，也能将该输出打在电脑上

>>>>>>> a81e3dcec386f8ed8e866c8a67830062cb2ef870
* xdg-open：类似于查找，可以帮助你在正确的位置打开你想要的文件夹，更加快捷