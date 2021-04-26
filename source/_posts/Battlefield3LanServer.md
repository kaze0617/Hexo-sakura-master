---
title: Battlefield3LanServer
author: KAZE
avatar: 'https://cdn.jsdelivr.net/gh/kaze0617/cdn@2.3/images/custom/avatar.jpg'
authorLink: /about/
authorAbout: 爱折腾
authorDesc: 爱折腾，热爱二次元。
comments: true
date: 2020-12-16 17:49:23
categories: 技术
tags:
keywords:
description: 战地3局域网服务器开服教程
photos: https://cdn.jsdelivr.net/gh/kaze0617/image-hosting@master/20210425/BF3.jpg
---
声明：本教程请勿商用，仅供学习和交流。
## 文件准备
- BF3_PC_Server_R38_1149977_Binaries.7z
- bf3emu.7z
- XAMPP（版本尽量在2015年左右，PHP版本必须在7.0以下）
- 网页源码（修改版和非修改版自己选）
- BF3 Server bat设置文件（随便选一个）
- 联机补丁（最新版网页模板有下载链接）

## 安装XAMPP并配置
1. 安装 一直点继续就行了
2. 设置 Apache和Mysql点start，如果出现红字说明端口被占用，所以点右边的Netstat来检查80和443是否占用，如果占用，点击config
打开httpd.conf 将Listen后面的值改为8080（或其他没被使用的端口号），打开httpd-ssl.conf，将里面所有443修改为446（或其他没被使用的端口号），保存关闭。然后点右上角那个config，点击Service and Port Settings，将Main Port改为8080（和Listen的值一样），SSL Port改为446，然后点save。

![Inkedxampp_LI.jpg](https://i.loli.net/2020/12/20/t2qXjdFZsHpvElA.jpg)

3. 点击Mysql那一行的Admin，点击用户账户，点击新建账户，用户名bf3，选择本地账户，密码bf3，往下滑，勾选新建与账户名同名的数据库，权限全选。点击执行。

4. 点开新创建的bf3数据库，点击导入，选择bf3emu（先解压该文件）里面的bf3.sql（如果用的是新版网页，就用那个压缩包里面的bf3.sql不要搞混）

5. 建立管理员用户确保数据库与服务端连接，loginpersona中没有数据，需要自己选上面一排的 Insert （插入）数据 email填test@test.com，password填test,保存并关闭。

## 网页配置（Lan-Battlelog）
1. 复制bf3emu\htdocs文件夹下的所有文件到C:\xampp\htdocs里（记得先备份原htdocs。
2. 修改 htdocs 文件夹下 config.cfg 的 hostIP-localPlayer （填ipconfig查到的ipv4地址）， user, password, database都为bf3，保存并关闭。

## BlazerServer配置
1. 解压BF3_PC_Server_R38_1149977_Binaries.7z（简称R38）文件，然后打开bf3emu文件夹下Bf3 Server files文件夹下ServerPassBF3.exe，输入刚刚在数据库里填写的email和password，填完后回车。然后复制bf3.exe到刚刚解压的R38文件夹下。

2. 解压BF3 Server bat设置文件到R38文件夹，然后打开bf3emu\BlazeServer\conf\conf.txt。为保险期间先建立LAN服务器。所以WanIpForLocalServer=这一项后面地址删除，然后Redihost =填写你的IPV4地址或者127.0.0.1，dbname=bf3,dbuser=bf3,dbpass=bf3，保存并关闭。

## 上述完成后退出并关闭上述提到过的所有程序。

## 服务器开启
1. 全部程序应以管理员身份运行。
2. 先开启xampp，运行Apache和Mysql，然后打开bf3emu\BlazeServer\BlazeServer.exe,再去解压后的R38文件夹打开__Start_Server-XXXX.bat文件等待服务器开启。
3. 开启成功后会显示IN_GAME
