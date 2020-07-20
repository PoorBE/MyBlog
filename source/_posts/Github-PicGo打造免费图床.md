---
title: Github+PicGo搭建免费图床
auther: 鄙人
summary: 本文讲解的图床是基于Github的，采用jsdelivr cdn进行加速，上传工具采用的是PicGo。
categories: 博客搭建
tags: Hexo
abbrlink: better01
date: 2020-07-10 09:51:57
img: 
top: true
cover:
coverImg:
password:
toc:
mathjax:
---

## 图床的搭建

> 图床：图床一般是指储存图片的服务器，有国内和国外之分。国外的图床由于有空间距离等因素决定访问速度很慢影响图片显示速度。国内也分为单线空间、多线空间和cdn加速三种。

### 1.创建仓库及生成token

​		**1. 新建一个github仓库，名称自定义即可**

![](https://cdn.jsdelivr.net/gh/PoorBE/images_b/img/Snipaste_2020-07-10_10-06-45.png)

 2. 生成token，PicGo需要填入token

    - 第一步：点击自己头像进入settings设置
    - 第二步：点击左侧菜单栏Developer settings
    - 第三步：点击左侧Personal access tokens
    - 第四步：点击右上角Generate new token
    - 第五步：为token起名，勾选权限，点击最下方绿色按钮即可
    - 第六步：复制保存生成的token（备用）

    ![](https://cdn.jsdelivr.net/gh/PoorBE/images_b/img/Snipaste_2020-07-10_10-12-51.png)

![](https://cdn.jsdelivr.net/gh/PoorBE/images_b/img/Snipaste_2020-07-10_10-17-24.png)

![](https://cdn.jsdelivr.net/gh/PoorBE/images_b/img/Snipaste_2020-07-10_10-21-42.png)

![](https://cdn.jsdelivr.net/gh/PoorBE/images_b/img/Snipaste_2020-07-10_10-24-41.png)

### 2.配置PicGo

  - 首先下载安装PicGo，图片上传工具PicGo下载地址：https://github.com/Molunerfinn/PicGo/releases

  - 配置GitHub图床，点击软件左侧图床设置选择GitHub图床

    ![](https://cdn.jsdelivr.net/gh/PoorBE/images_b/img/Snipaste_2020-07-10_10-36-30.png)

    - 设定仓库名：此处填写格式username/repo，username为你的github名字，repo为你刚才刚创建的图床仓库名
    - 设定分支名：master，采用默认分支即可
    - 设定Token：此处填写上一步得到的Token，添加到输入框即可。
    - 指定存储路径：自定义：例如img/ 。上传的图片会存入此路径
    - 设定自定义域名：格式：`https://cdn.jsdelivr.net/gh/username/repo`，`username`为GitHub用户名，`repo`为新建的仓库，用于存储图片

配置完成后点击确认即可

 - 上传图片 ，此处有好几种格式，可根据自己需要选择

   ![](https://cdn.jsdelivr.net/gh/PoorBE/images_b/img/Snipaste_2020-07-10_10-42-23.png)

- 上传成功后可到相册查看上传的图片![](https://cdn.jsdelivr.net/gh/PoorBE/images_b/img/Snipaste_2020-07-10_10-46-45.png)

- 注意：上传图片时有小几率失败，会出现短暂的上传条为红色的情况，可多试几次，如若不行则检查图床设置是否正确