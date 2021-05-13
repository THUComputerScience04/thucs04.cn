<<<<<<< HEAD
---
title: 如何使用MarkDown书写博客
date: 2021/05/09 14:00:00
categories: Introduction
tags:
- introduction
- 教程
author:
- WXY
- QC
---

## 如何使用MarkDown书写博客

### 1. 引言

到目前为止，计04班的设备采购工作已经完成，基础的博客网页（ www.thucs04.cn ）也已经搭建完成，班级博客将是以后班级形象展示的重要阵地。

那班级博客上都有什么呢？这就需要大家来贡献自己的力量，书写一些博文，然后经过Github进行上传，充实我们的班级博客。

为了方便博客的维护，以及减少书写HTML的麻烦，经主要技术人员研究决定，让大家使用MarkDown来书写博文，主题、内容不限。

那么，什么是MarkDown呢？确切地来说，MarkDown是一种格式，就像是Word文档里可以调整字体的风格、字号，可以加粗文字等，Markdown也是用来进行这些操作的一种语言规范，例如本篇教程就是使用这种规范来书写的。但与Word不同的是，Markdown没有十分方便的GUI（图像界面），需要我们书写一些简单的代码来对这些文字进行格式的设定。

### 2. MarkDown的书写平台

就像是我们写C++的代码会放在VScode 上一样，书写Markdown也有这样的平台，在这种平台上书写，可以方便地让我们看到代码的效果。

下面推荐两种书写Markdown的平台

* VS code

* typora

#### 2.1 VS code 书写Markdown 方式

1.  安装vscode，这就足够了，不需要在vscode中安装其他插件
2. 在vscode新建一个文件，后缀为 .md  例如：test1.md
3. 右键点击上方 test1.md的标签，选择打开预览，就可以在预览当中看到自己书写的MarkDown代码的效果。
4. 完成上述工作之后，你就可以在test1.md文件中~~快乐地~~书写博文和代码了（如何书写见下方语法教程）

<img src="https://i.loli.net/2021/05/09/8TfaBZdCFWbkAcD.png" alt="操作图示"  />

#### 2.2 typora书写Markdown 方式

1. 安装typora，网址：https://typora.io/  ，往下翻，可以看到右上角Download选项，点击跳转到下载页面，根据电脑操作系统的版本下载对应的安装包
2. 安装typora（无需打开这个软件）
3. 在桌面（或其他位置）上新建一个文件，后缀为.md，以test.md为例
4. 打开这个文件（选择打开方式为typora），之后你就可以在test.md文件中~~快乐地~~书写博文和代码了

<img src="https://i.loli.net/2021/05/09/nCNAxTJZuqabl4V.png" alt="typora版.png"  />

### 3. Markdown基本使用

**在写博文时，你只需要正常地输入博客的内容，然后在需要的格式处加上MarkDown的语法即可**

如下例（左侧为代码和文本，右侧为效果图）

![书写演示.png](https://i.loli.net/2021/05/09/6ypgriUdthWH7Nq.png)

这里强烈推荐使用typora，它可以即时地看到效果，不需要打开预览图

Markdown的具体语法可以在网上查到，推荐一个网站：[Markdown基本语法 - 简书 (jianshu.com)](https://www.jianshu.com/p/191d1e21f7ed/)

### 4. Markdown的基本语法教程

1. n个#加上一个空格代表一个n级标题

   ![基本使用1.png](https://i.loli.net/2021/05/09/GqoRmiFEkDnfl3C.png)

   ![基本使用2.png](https://i.loli.net/2021/05/09/y7QZD42mA1tHcKn.png)

2. 一对*括起来表示斜体；两对表示加粗；三对表示斜体加加粗

   ![基本使用3.png](https://i.loli.net/2021/05/09/vagwUxXlNIO49Dr.png)

   ![基本使用4.png](https://i.loli.net/2021/05/09/HLy5mDAivb7jtRO.png)

3. 1、2、3、4等编号会自动延续，生成有序列表

   ![基本使用5.png](https://i.loli.net/2021/05/09/wybZBPEjp1o5SVR.png)

   ![基本使用6.png](https://i.loli.net/2021/05/09/gbEdm3RhncS5jMo.png)

4. 三个或以上小短线 --- 在单行输入将会作为分割线

   ![基本使用7.png](https://i.loli.net/2021/05/09/16VqZWt7DSLgdOK.png)

   ![基本使用8.png](https://i.loli.net/2021/05/09/m1juBy7MObsXo42.png)

5. +，-，*加上空格将会生成无序列表；其可进行分级；在无序列表中shift+tab可回退至无序表的上一级

   ![基本使用9.png](https://i.loli.net/2021/05/09/GYwbNknClS9UKJa.png)

   ![基本使用10.png](https://i.loli.net/2021/05/09/7HGn21NarhXBUAR.png)

6. 用n个>符号之后加空格可以表示n级引用，可无限嵌套

   ![基本使用11.png](https://i.loli.net/2021/05/09/ZB8YjtXrCwLFyzM.png)

   ![基本使用12.png](https://i.loli.net/2021/05/09/bBwpkNqtL7fiuZD.png)

7. 连续输入三个`可调用代码块

   ![基本使用13.png](https://i.loli.net/2021/05/09/hawdrX9oUBEqJDT.png)

   ![基本使用14.png](https://i.loli.net/2021/05/09/tz53jiuWyhDg7vc.png)

8. 两对~中内容表示加上删除线

   ![基本使用15.png](https://i.loli.net/2021/05/09/agUVmMuLK4dHntp.png)

   ![基本使用16.png](https://i.loli.net/2021/05/09/wOu4AWe6a2ojULY.png)

9. 用短竖线 |内容|内容| 的方式可以创建表格，创建完后可自行调整大小

   ![基本使用17.png](https://i.loli.net/2021/05/09/vNkcCuhEUHWFqf2.png)

   ![基本使用18.png](https://i.loli.net/2021/05/09/PHJcvCAizxfEugS.png)

10. [内容]：(网址) 的形式可以实现参数式超链接，不加：也有其他方式

    ![基本使用19.png](https://i.loli.net/2021/05/09/XDMStH8uwE7PICR.png)

    ![基本使用20.png](https://i.loli.net/2021/05/09/QbXC5w9UoaFre6p.png)

    ![基本使用21.png](https://i.loli.net/2021/05/09/phgSi54vzPGD7b1.png)

    ![基本使用22.png](https://i.loli.net/2021/05/09/ZuYolXvWhUJgK16.png)

    ![基本使用23.png](https://i.loli.net/2021/05/09/O7DUpFEMuJseNmL.png)

    ![基本使用24.png](https://i.loli.net/2021/05/09/uUrsjwNIqiR4Vap.png)

11. 用！[名字]（路径）的方式可以插入图片（或大部分情况下直接复制即可）

    ![基本使用25.png](https://i.loli.net/2021/05/09/296sI1LpbTBRioa.png)

    

### 5. Markdown书写博客的其他要求

上面的教程已经教会了大家如何书写Markdown语言规范，而在书写博客时有一个额外的要求：在整篇文档的最上方添加Front-matter

如何添加Front-matter？

如图所示，只需在前面添加几行代码：

![title演示.png](https://i.loli.net/2021/05/09/MvAgdCxeQEnoj3S.png)

如果是typora，输入前面的三个短横线后会自动识别，此时不需要书写最后三个短横线

```markdown
---
title: 这是标题
date: 2021/05/08 12:00:00
author: 
- 作者名称1（建议使用GitHub用户名）
- 作者名称2（建议使用GitHub用户名）
categories: 这是分类
tag:
- demo
- test
---
```

从三条短横线开始，到三条短横线结束，需要填写title、date、author、categories、tag

* title 填写博客的标题，可以中文可以英文
* date 填写博客的建立日期 格式为 YYYY/MM/DD hh:mm:ss
* author 填写作者名称
* categories 这一篇博客的分类，（为了方便管理，目前大家从这四个英文标题当中选填，首字母大写）
  * Introduction  (各类教程、简介)
  * Diary （个人生活记录、推送）
  * Note （课堂、讲座笔记）
  * Discussion （有感而发的讨论）
* tag 博客希望的标签，可以添加多个，但是每个短横线之后一定要有**空格**

注意： 每一个参数的冒号后一定要有**空格**

### 6. 关于博客图片的要求

大家在书写博客时可能会有要用到图片的地方，但与基础的图片语法不同的是，博客的图片需要经过处理：

1. 将所用图片储存在本地（你的电脑里）

2. 打开网址 www.sm.ms

3. 将图片拖入框内，选择upload

4. 复制下方markdown的语句，粘贴到博客当中即可在博客中插入图片，此外不需要做任何操作

   ![空图.png](https://i.loli.net/2021/05/09/PCbwsqE2VS8Hv1K.png)

   ![空图2.png](https://i.loli.net/2021/05/09/UjuxBOtd8wKPim5.png)

   ![空图3.png](https://i.loli.net/2021/05/09/3doiDKBtmanGelJ.png)



=======
---
title: 如何使用MarkDown书写博客
date: 2021/05/09 14:00:00
categories: Introduction
tags:
- introduction
- 教程
author:
- WXY
- QC
---

如何使用MarkDown书写博客

<!--more-->

## 如何使用MarkDown书写博客

### 1. 引言

到目前为止，计04班的设备采购工作已经完成，基础的博客网页（ www.thucs04.cn ）也已经搭建完成，班级博客将是以后班级形象展示的重要阵地。

那班级博客上都有什么呢？这就需要大家来贡献自己的力量，书写一些博文，然后经过Github进行上传，充实我们的班级博客。

为了方便博客的维护，以及减少书写HTML的麻烦，经主要技术人员研究决定，让大家使用MarkDown来书写博文，主题、内容不限。

那么，什么是MarkDown呢？确切地来说，MarkDown是一种格式，就像是Word文档里可以调整字体的风格、字号，可以加粗文字等，Markdown也是用来进行这些操作的一种语言规范，例如本篇教程就是使用这种规范来书写的。但与Word不同的是，Markdown没有十分方便的GUI（图像界面），需要我们书写一些简单的代码来对这些文字进行格式的设定。

### 2. MarkDown的书写平台

就像是我们写C++的代码会放在VScode 上一样，书写Markdown也有这样的平台，在这种平台上书写，可以方便地让我们看到代码的效果。

下面推荐两种书写Markdown的平台

* VS code

* typora

#### 2.1 VS code 书写Markdown 方式

1.  安装vscode，这就足够了，不需要在vscode中安装其他插件
2. 在vscode新建一个文件，后缀为 .md  例如：test1.md
3. 右键点击上方 test1.md的标签，选择打开预览，就可以在预览当中看到自己书写的MarkDown代码的效果。
4. 完成上述工作之后，你就可以在test1.md文件中~~快乐地~~书写博文和代码了（如何书写见下方语法教程）

<img src="https://i.loli.net/2021/05/09/8TfaBZdCFWbkAcD.png" alt="操作图示"  />

#### 2.2 typora书写Markdown 方式

1. 安装typora，网址：https://typora.io/  ，往下翻，可以看到右上角Download选项，点击跳转到下载页面，根据电脑操作系统的版本下载对应的安装包
2. 安装typora（无需打开这个软件）
3. 在桌面（或其他位置）上新建一个文件，后缀为.md，以test.md为例
4. 打开这个文件（选择打开方式为typora），之后你就可以在test.md文件中~~快乐地~~书写博文和代码了

<img src="https://i.loli.net/2021/05/09/nCNAxTJZuqabl4V.png" alt="typora版.png"  />

### 3. Markdown基本使用

**在写博文时，你只需要正常地输入博客的内容，然后在需要的格式处加上MarkDown的语法即可**

如下例（左侧为代码和文本，右侧为效果图）

![书写演示.png](https://i.loli.net/2021/05/09/6ypgriUdthWH7Nq.png)

这里强烈推荐使用typora，它可以即时地看到效果，不需要打开预览图

Markdown的具体语法可以在网上查到，推荐一个网站：[Markdown基本语法 - 简书 (jianshu.com)](https://www.jianshu.com/p/191d1e21f7ed/)

### 4. Markdown的基本语法教程

1. n个#加上一个空格代表一个n级标题

   ![基本使用1.png](https://i.loli.net/2021/05/09/GqoRmiFEkDnfl3C.png)

   ![基本使用2.png](https://i.loli.net/2021/05/09/y7QZD42mA1tHcKn.png)

2. 一对*括起来表示斜体；两对表示加粗；三对表示斜体加加粗

   ![基本使用3.png](https://i.loli.net/2021/05/09/vagwUxXlNIO49Dr.png)

   ![基本使用4.png](https://i.loli.net/2021/05/09/HLy5mDAivb7jtRO.png)

3. 1、2、3、4等编号会自动延续，生成有序列表

   ![基本使用5.png](https://i.loli.net/2021/05/09/wybZBPEjp1o5SVR.png)

   ![基本使用6.png](https://i.loli.net/2021/05/09/gbEdm3RhncS5jMo.png)

4. 三个或以上小短线 --- 在单行输入将会作为分割线

   ![基本使用7.png](https://i.loli.net/2021/05/09/16VqZWt7DSLgdOK.png)

   ![基本使用8.png](https://i.loli.net/2021/05/09/m1juBy7MObsXo42.png)

5. +，-，*加上空格将会生成无序列表；其可进行分级；在无序列表中shift+tab可回退至无序表的上一级

   ![基本使用9.png](https://i.loli.net/2021/05/09/GYwbNknClS9UKJa.png)

   ![基本使用10.png](https://i.loli.net/2021/05/09/7HGn21NarhXBUAR.png)

6. 用n个>符号之后加空格可以表示n级引用，可无限嵌套

   ![基本使用11.png](https://i.loli.net/2021/05/09/ZB8YjtXrCwLFyzM.png)

   ![基本使用12.png](https://i.loli.net/2021/05/09/bBwpkNqtL7fiuZD.png)

7. 连续输入三个`可调用代码块

   ![基本使用13.png](https://i.loli.net/2021/05/09/hawdrX9oUBEqJDT.png)

   ![基本使用14.png](https://i.loli.net/2021/05/09/tz53jiuWyhDg7vc.png)

8. 两对~中内容表示加上删除线

   ![基本使用15.png](https://i.loli.net/2021/05/09/agUVmMuLK4dHntp.png)

   ![基本使用16.png](https://i.loli.net/2021/05/09/wOu4AWe6a2ojULY.png)

9. 用短竖线 |内容|内容| 的方式可以创建表格，创建完后可自行调整大小

   ![基本使用17.png](https://i.loli.net/2021/05/09/vNkcCuhEUHWFqf2.png)

   ![基本使用18.png](https://i.loli.net/2021/05/09/PHJcvCAizxfEugS.png)

10. [内容]：(网址) 的形式可以实现参数式超链接，不加：也有其他方式

    ![基本使用19.png](https://i.loli.net/2021/05/09/XDMStH8uwE7PICR.png)

    ![基本使用20.png](https://i.loli.net/2021/05/09/QbXC5w9UoaFre6p.png)

    ![基本使用21.png](https://i.loli.net/2021/05/09/phgSi54vzPGD7b1.png)

    ![基本使用22.png](https://i.loli.net/2021/05/09/ZuYolXvWhUJgK16.png)

    ![基本使用23.png](https://i.loli.net/2021/05/09/O7DUpFEMuJseNmL.png)

    ![基本使用24.png](https://i.loli.net/2021/05/09/uUrsjwNIqiR4Vap.png)

11. 用！[名字]（路径）的方式可以插入图片（或大部分情况下直接复制即可）

    ![基本使用25.png](https://i.loli.net/2021/05/09/296sI1LpbTBRioa.png)

    

### 5. Markdown书写博客的其他要求

上面的教程已经教会了大家如何书写Markdown语言规范，而在书写博客时有一个额外的要求：在整篇文档的最上方添加Front-matter

如何添加Front-matter？

如图所示，只需在前面添加几行代码：

![title演示.png](https://i.loli.net/2021/05/09/MvAgdCxeQEnoj3S.png)

如果是typora，输入前面的三个短横线后会自动识别，此时不需要书写最后三个短横线

```markdown
---
title: 这是标题
date: 2021/05/08 12:00:00
author: 
- 作者名称1（建议使用GitHub用户名）
- 作者名称2（建议使用GitHub用户名）
categories: 这是分类
tag:
- demo
- test
---
```

从三条短横线开始，到三条短横线结束，需要填写title、date、author、categories、tag

* title 填写博客的标题，可以中文可以英文
* date 填写博客的建立日期 格式为 YYYY/MM/DD hh:mm:ss
* author 填写作者名称
* categories 这一篇博客的分类，（为了方便管理，目前大家从这四个英文标题当中选填，首字母大写）
  * Introduction  (各类教程、简介)
  * Diary （个人生活记录、推送）
  * Note （课堂、讲座笔记）
  * Discussion （有感而发的讨论）
* tag 博客希望的标签，可以添加多个，但是每个短横线之后一定要有**空格**

注意： 每一个参数的冒号后一定要有**空格**

### 6. 关于博客图片的要求

大家在书写博客时可能会有要用到图片的地方，但与基础的图片语法不同的是，博客的图片需要经过处理：

1. 将所用图片储存在本地（你的电脑里）

2. 打开网址 www.sm.ms

3. 将图片拖入框内，选择upload

4. 复制下方markdown的语句，粘贴到博客当中即可在博客中插入图片，此外不需要做任何操作

   ![空图.png](https://i.loli.net/2021/05/09/PCbwsqE2VS8Hv1K.png)

   ![空图2.png](https://i.loli.net/2021/05/09/UjuxBOtd8wKPim5.png)

   ![空图3.png](https://i.loli.net/2021/05/09/3doiDKBtmanGelJ.png)



>>>>>>> a81e3dcec386f8ed8e866c8a67830062cb2ef870
