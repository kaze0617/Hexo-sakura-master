---
title: 黑苹果AMD cpu支持列表
author: KAZE
avatar: 'https://cdn.jsdelivr.net/gh/kaze0617/cdn@2.3/images/custom/avatar.jpg'
authorLink: kaze0617.gitee.io
comments: true
date: 2020-03-29 12:21:36
authorAbout: 爱折腾
authorDesc: 爱折腾，热爱二次元。
categories: 支持
tags:
keywords:
description:
photos: https://cdn.jsdelivr.net/gh/kaze0617/cdn@2.3/images/article/AMD.jpg
---
转载自[Hac的小窝](http://hac.fangf.cc/archives/349)
## 目前，支持黑苹果的AMD CPU主要是以下几种

+ 核心架构：Bulldozer 如FX系列
+ 核心架构：Jaguar 如A系列
+ 核心架构：Zen 如Ryzen, Threadripper, Athlon 2xxGE系列

### 支持的macOS版本

+ High Sierra 10.13.6 (17G65, 17G66, 17G8030, 17G8037)
+ Mojave 10.14.6 (18G84, 18G87, 18G95, 18G103)
+ Catalina 10.15.0 (19A583, 19A602), 10.15.1 (19B88)

常见的有：1700x，AMD Ryzen 5 2600，AMD FX6300，AMD Ryzen 3600g，AMD Ryzen 7 2700X，AMD Ryzen 5 1400，AMD X4-760K,AMD RYZEN 3700x等。

## 完全支持

### Ryzen:

+ Zen:

  + Ryzen 3 1200 至 Ryzen 7 1800X, 所有X系列
  + Threadripper 1900X, 1920X, 1950X

### Zen+:

  + Ryzen 3 2300X 至 Ryzen 7 2700X 所有X和MAX系列，G系列除外。
  + Threadripper 2920X, 2950x, 2970WX, 2990WX

### Zen2:

+ Ryzen 5 3500 至 Ryzen 9 3950X, 所有X和MAX系列，G系列除外。

### 15/16h:

  + Bulldozer
  + Piledriver
  + Steamroller
  + Excavator
  + Trinity
  + Richland
  + Kaveri
  + Carrizo
  + Bristol Ridge

### Zen (Raven Ridge):

  + Athlon 200 GE 至 Athlon 240 GE
  + Athlon 3000G
  + Ryzen 3 2200GE 至 Ryzen 5 Pro 2400G

### Zen+ (Picasso):

  + Athlon Pro 300GE
  + Ryzen 3 3200G 至 Ryzen 5 Pro 3400G

### TX40 3000-系 Threadripper

  + Threadripper 3960X
  + Threadripper 3970X
  + Threadripper 3990X

## 注意事项
+ 任何AMD CPU的笔记本均不支持黑苹果，不用考虑！

+ 所有核显均不支持黑苹果！必须使用独立显卡

+ Opteron和EPYC处理都没有经过测试，不确定能否使用。

+ 15/16的CPU可能存在一定的问题，不建议再使用。

+ 请注意的是，AMD 黑苹果为适合于生产环境，可能存在一定的软件和系统兼容性问题，适合一般家用。