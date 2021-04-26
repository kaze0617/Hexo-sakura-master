---
title: 黑苹果必备:Intel核显platform ID整理及smbios速查表
author: KAZE
avatar: 'https://cdn.jsdelivr.net/gh/kaze0617/cdn@2.3/images/custom/avatar.jpg'
authorLink: /about/
authorAbout: 爱折腾
authorDesc: 爱折腾，热爱二次元。
comments: true
date: 2020-03-31 17:11:50
categories: 支持
tags:
keywords:
description: 驱动你的核心显卡。
photos: https://cdn.jsdelivr.net/gh/kaze0617/cdn@2.3/images/article/intelgraphics.jpg
---
转载自[Hac的小窝](http://hac.fangf.cc/archives/349)
# <center>smbios速查表</center>
| SMBIOS ID      | CPU Family   | GPUs \(S = Switchable\)                          | Year and size   |
|----------------|--------------|--------------------------------------------------|-----------------|
| MacBook1,1     | Yonah        | GMA 950                                          | 13" 2006        |
| MacBook2,1     | Merom        | GMA 950                                          | 13" 2006/07"    |
| MacBook3,1     | Merom        | GMA X3100                                        | 13" 2007        |
| MacBook4,1     | Penryn       | GMA X3100                                        | 13" 2008        |
| MacBook4,2     | Penryn       | GMA X3100                                        | 13" 2008        |
| MacBook5,1     | Penryn       | GeForce 9400M                                    | 13" 2008        |
| MacBook5,2     | Penryn       | GeForce 9400M                                    | 13" 2009        |
| MacBook6,1     | Penryn       | GeForce 9400M                                    | 13" 2009        |
| MacBook7,1     | Penryn       | GeForce 320M                                     | 13" 2010        |
| MacBook8,1     | Broadwell m  | HD 5300                                          | 12" 2015        |
| MacBook9,1     | Skylake m    | HD 515                                           | 12" 2016        |
| MacBook10,1    | Kaby Lake m  | HD 615                                           | 12" 2017        |
| —              | —            | —                                                | —               |
| MacBookAir1,1  | Merom        | GMA X3100                                        | 13" 2008        |
| MacBookAir2,1  | Penryn       | GeForce 9400M                                    | 13" 2008/09"    |
| MacBookAir3,1  | Penryn       | GeForce 320M                                     | 11" 2010        |
| MacBookAir3,2  | Penryn       | GeForce 320M                                     | 13" 2010        |
| MacBookAir4,1  | Sandy Bridge | HD 3000                                          | 11" 2011        |
| MacBookAir4,2  | Sandy Bridge | HD 3000                                          | 13" 2011        |
| MacBookAir5,1  | Ivy Bridge   | HD 4000                                          | 11" 2012        |
| MacBookAir5,2  | Ivy Bridge   | HD 4000                                          | 13" 2012        |
| MacBookAir6,1  | Haswell      | HD 5000                                          | 11" 2013        |
| MacBookAir6,2  | Haswell      | HD 5000                                          | 13" 2013        |
| MacBookAir7,1  | Broadwell    | HD 6000                                          | 11" 2015        |
| MacBookAir7,2  | Broadwell    | HD 6000                                          | 13" 2015        |
| MacBookAir8,1  | Kaby Lake    | Intel UHD Graphics 617                           | 13" 2018        |
| MacBookAir8,2  | Kaby Lake    | Intel UHD Graphics 617                           | 13" 2019        |
| —              | —            | —                                                | —               |
| MacBookPro1,1  | Yonah        | Radeon X1600                                     | 15" 2006        |
| MacBookPro1,2  | Yonah        | Radeon X1600                                     | 17" 2006        |
| MacBookPro2,1  | Merom        | Radeon X1600                                     | 15" 2006        |
| MacBookPro2,2  | Merom        | Radeon X1600                                     | 17" 2006        |
| MacBookPro3,1  | Merom        | GeForce 8600M GT                                 | 15"/17" 2007    |
| MacBookPro4,1  | Penryn       | GeForce 8600MG GT                                | 17" 2008        |
| MacBookPro5,1  | Penryn       | GeForce 9400M/9600M GT                           | S, 15" 2008/09" |
| MacBookPro5,2  | Penryn       | GeForce 9400M/9600M GT                           | S, 17" 2009     |
| MacBookPro5,3  | Penryn       | GeForce 9400M/9600M GT                           | S, 15" 2009     |
| MacBookPro5,4  | Penryn       | GeForce 9400M/9600M GT                           | S, 15" 2009     |
| MacBookPro5,5  | Penryn       | GeForce 9400M/9600M GT                           | S, 13" 2009     |
| MacBookPro7,1  | Penryn       | GeForce 320M                                     | 13" 2010        |
| MacBookPro6,1  | Arrandale    | HD Graphics/GeForce GT 330M                      | S, 17" 2010     |
| MacBookPro6,2  | Arrandale    | HD Graphics/GeForce GT 330M                      | S, 15" 2010     |
| MacBookPro8,1  | Sandy Bridge | HD 3000                                          | 13" 2011        |
| MacBookPro8,2  | Sandy Bridge | HD 3000/Radeon HD 6490M                          | S, 15" 2011     |
| MacBookPro8,3  | Sandy Bridge | HD 3000/Radeon HD 6750M                          | S, 17" 2011     |
| MacBookPro9,1  | Ivy Bridge   | HD 4000/GeForce GT 650M                          | S, 15" 2012     |
| MacBookPro9,2  | Ivy Bridge   | HD 4000                                          | 13" 2012        |
| MacBookPro10,1 | Ivy Bridge   | HD 4000/GeForce GT 650M                          | S, 15" 2012/13" |
| MacBookPro10,2 | Ivy Bridge   | HD 4000                                          | 13" 2012/13"    |
| MacBookPro11,1 | Haswell      | Iris 5100                                        | 13" 2013/14"    |
| MacBookPro11,2 | Haswell      | Iris Pro 5200                                    | 15" 2013/14"    |
| MacBookPro11,3 | Haswell      | Iris Pro 5200/GeForce GT 750M                    | S, 15" 2013/14" |
| MacBookPro11,4 | Haswell      | Iris Pro 5200                                    | 15" 2015        |
| MacBookPro11,5 | Haswell      | Iris Pro 5200/Radeon R9 M370X                    | 15" 2015        |
| MacBookPro12,1 | Broadwell    | Iris 6100                                        | 13" 2015        |
| MacBookPro13,1 | Skylake      | Iris 540                                         | 13" 2016        |
| MacBookPro13,2 | Skylake      | Iris 550                                         | 13" 2016        |
| MacBookPro13,3 | Skylake      | HD 530/Radeon Pro 450                            | 15" 2016        |
| MacBookPro14,1 | Kaby Lake    | Iris Plus 640                                    | 13" 2017        |
| MacBookPro14,2 | Kaby Lake    | Iris Plus 650                                    | 13" 2017        |
| MacBookPro14,3 | Kaby Lake    | HDs 630/Radeon Pro 555                           | 15" 2017        |
| MacBookPro15,1 | Caffee Lake  | Intel UHD Graphics 630                           | 15" 2018        |
| MacBookPro15,2 | Caffee Lake  | Intel Iris Plus Graphics 655                     | 13" 2018        |
| MacBookPro15,3 | Caffee Lake  | UHD630/Radeon Pro555X/560XRadeon Pro Vega 16/20  | 15" 2019        |
| MacBookPro15,4 | Caffee Lake  | Intel Iris Plus Graphics 645                     | 13" 2019        |
| MacBookPro16,1 | Caffee Lake  | Intel UHD Graphics 630AMD Radeon Pro 5300M/5500M | 16" 2019        |
| —              | —            | —                                                | —               |
| iMac4,1        | Yonah        | Radeon X1600                                     | 17"/20" 2006    |
| iMac4,2        | Yonah        | GMA 950                                          | 17" 2006        |
| iMac5,1        | Merom        | Radeon X1600                                     | 17"/20" 2006    |
| iMac5,2        | Merom        | GMA 950                                          | 17" 2006        |
| iMac6,1        | Merom        | GeForce 7300GT                                   | 24" 2006        |
| iMac7,1        | Merom        | Radeon HD 2400 XT                                | 20"/24" 2007    |
| iMac8,1        | Penryn       | Radeon HD 2400 XT                                | 20"/24" 2008    |
| iMac9,1        | Penryn       | GeForce 9400M                                    | 20"/24" 2009    |
| iMac10,1       | Wolfdale     | GeForce 9400M                                    | 21\.5"/27" 2009 |
| iMac10,1       | Wolfdale     | Radeon HD 4670                                   | 21\.5"/27" 2009 |
| iMac11,1       | Lynnfield    | Radeon HD 4850                                   | 27" 2009        |
| iMac11,2       | Clarkdale    | Radeon HD 4670                                   | 21\.5" 2010     |
| iMac11,3       | Clarkdale    | Radeon HD 5670                                   | 27" 2010        |
| iMac12,1       | Sandy Bridge | Radeon HD 6750M                                  | 21\.5" 2011     |
| iMac12,2       | Sandy Bridge | Radeon HD 6770M                                  | 27" 2011        |
| iMac13,1       | Ivy Bridge   | GeForce GT 640M                                  | 21\.5" 2012     |
| iMac13,2       | Ivy Bridge   | GeForce GTX 660M                                 | 27" 2012        |
| iMac13,1       | Ivy Bridge   | HD 4000                                          | 21\.5" 2013     |
| iMac14,1       | Haswell      | Iris Pro 5200                                    | 21\.5" 2013     |
| iMac14,1       | Haswell      | GeForce GT 750M                                  | 21\.5" 2013     |
| iMac14,2       | Haswell      | GeForce GT 755M                                  | 27" 2013        |
| iMac14,4       | Haswell      | HD 5000                                          | 21\.5" 2014     |
| iMac15,1       | Haswell      | Radeon R9 M290X                                  | 27" 2014/15"    |
| iMac16,1       | Broadwell    | HD 6000 or Iris Pro 6200                         | 21\.5" 2015     |
| iMac16,2       | Broadwell    | Iris Pro 6200                                    | 21\.5" 2015     |
| iMac17,1       | Skylake      | Radeon R9 M380                                   | 27" 2015        |
| iMac18,1       | Kaby Lake    | Iris Plus 640                                    | 21\.5" 2017     |
| iMac18,2       | Kaby Lake    | Radeon Pro 555                                   | 21\.5" 2017     |
| iMac18,3       | Kaby Lake    | Radeon Pro 570                                   | 27" 2017        |
| iMac19,1       | Coffee Lake  | Radeon Pro 580                                   | 2017            |
| iMac19,2       | Coffee Lake  | Radeon Pro 580X/Radeon Pro Vega 48               | 2019            |
| —              | —            | —                                                | —               |
| iMacPro1,1     |              | Radeon Pro Vega 56/64/64X                        | 2017            |
| —              | —            | —                                                | —               |
| Macmini1,1     | Yonah        | GMA 950                                          | 2006            |
| Macmini2,1     | Merom        | GMA 950                                          | 2007            |
| Macmini3,1     | Penryn       | GeForce 9400M                                    | 2009            |
| Macmini4,1     | Penryn       | GeForce 320M                                     | 2010            |
| Macmini5,1     | Sandy Bridge | HD 3000                                          | 2011            |
| Macmini5,2     | Sandy Bridge | Radeon HD 6630M                                  | 2011            |
| Macmini5,3     | Sandy Bridge | HD 3000                                          | 2011            |
| Macmini6,1     | Ivy Bridge   | HD 4000                                          | 2012            |
| Macmini6,2     | Ivy Bridge   | HD 4000                                          | 2012            |
| Macmini7,1     | Haswell      | HD 5000 or Iris 5100                             | 2014            |
| Macmini8,1     | Coffee Lake  | UHD Graphics 630                                 | 2018            |
| —              | —            | —                                                | —               |
| MacPro1,1      | Woodcrest    | GeForce 7300 GT                                  | 2006            |
| MacPro2,1      | Clovertown   | GeForce 7300 GT                                  | 2006            |
| MacPro3,1      | Harpertown   | Radeon HD 2600 XT                                | 2008            |
| MacPro4,1      | Nehalem      | GeForce GT 120                                   | 2009            |
| MacPro5,1      | Nehalem      | Radeon HD 5770                                   | 2010            |
| MacPro5,1      | Westmere     | Radeon HD 5770                                   | 2012            |
| MacPro6,1      | Ivy BridgeEP | FirePro D300                                     | 2013            |
| MacPro7,1      | Cascade Lake | Radeon Pro 580X/Radeon Pro Vega II               | 2019            |
| —              | —            | —                                                | —               |
| Xserve1,1      | Woodcrest    | Radeon X1300                                     | 2006            |
| Xserve2,1      | Harpertown   | Radeon X1300                                     | 2008            |
| Xserve3,1      | Nehalem      | GeForce GT 120                                   | 2009            |

# <center>intel核显平台</center>
## <center>sandy-bridge平台</center>
| 显卡型号                   | platform\-id | 机型                                      | 接口 | LVDS | DP | HDMI |
|------------------------|--------------|-----------------------------------------|----|------|----|------|
| Intel HD Graphics 3000 | 0x00010000   | MacBookPro8,1MacBookPro8,2MacBookPro8,3 | 4  | 1    | 3  |      |
| Intel HD Graphics 3000 | 0x00020000   |                                         | 1  | 1    |    |      |
| Intel HD Graphics 3000 | 0x00030010   | Macmini5,1Macmini5,3                    | 3  |      | 2  | 1    |
| Intel HD Graphics 3000 | 0x00030020   | Macmini5,1Macmini5,3                    | 3  |      | 2  | 1    |
| Intel HD Graphics 3000 | 0x00030030   | Macmini5,2                              | 0  |      |    |      |
| Intel HD Graphics 3000 | 0x00040000   | MacBookAir4,1MacBookAir4,2              | 3  | 1    | 2  |      |
| Intel HD Graphics 3000 | 0x00050000   | iMac12,1/iMac12,2                       | 0  |      |    |      |

## <center>ivy-bridge平台</center>
| 型号                     | platform\-id | 机型             | 接口 | LVDS | DP | HDMI |
|------------------------|--------------|----------------|----|------|----|------|
| Intel HD Graphics 4000 | 0x01660000   |                | 4  | 1    | 3  |      |
| Intel HD Graphics 4000 | 0x01660001   | MacBookPro10,2 | 4  | 1    | 2  | 1    |
| Intel HD Graphics 4000 | 0x01660002   | MacBookPro10,1 | 1  | 1    |    |      |
| Intel HD Graphics 4000 | 0x01660003   | MacBookPro9,2  | 4  | 1    | 3  |      |
| Intel HD Graphics 4000 | 0x01660004   | MacBookPro9,1  | 1  | 1    |    |      |
| Intel HD Graphics 4000 | 0x01660005   |                | 3  |      | 3  |      |
| Intel HD Graphics 4000 | 0x01660006   | iMac13,1       | 0  |      |    |      |
| Intel HD Graphics 4000 | 0x01660007   | iMac13,2       | 0  |      |    |      |
| Intel HD Graphics 4000 | 0x01660008   | MacBookAir5,1  | 3  | 1    | 2  |      |
| Intel HD Graphics 4000 | 0x01660009   | MacBookAir5,2  | 3  | 1    | 2  |      |
| Intel HD Graphics 4000 | 0x0166000a   | Macmini6,1     | 3  |      | 2  | 1    |
| Intel HD Graphics 4000 | 0x0166000b   | Macmini6,2     | 3  |      | 2  | 1    |

## <center>haswell平台</center>
| 显卡型号                         | platform\-id | 机型                                   | 接口 | LVDS | DP | eDP | HDMI |
|------------------------------|--------------|--------------------------------------|----|------|----|-----|------|
|                              | 0x04060000   |                                      | 3  | 1    |    | 1   | 1    |
|                              | 0x0c060000   |                                      | 3  | 1    |    | 1   | 1    |
| Intel HD Graphics 4600       | 0x04160000   |                                      | 3  | 1    |    | 1   | 1    |
| Intel HD Graphics 4400       | 0x0a160000   |                                      | 3  | 1    |    | 1   | 1    |
|                              | 0x0c160000   |                                      | 3  | 1    |    | 1   | 1    |
| Intel HD Graphics 5000       | 0x04260000   |                                      | 3  | 1    |    | 1   | 1    |
| Intel HD Graphics 5000       | 0x0a260000   |                                      | 3  | 1    |    | 1   | 1    |
|                              | 0x0c260000   |                                      | 3  | 1    |    | 1   | 1    |
| Intel Iris Pro Graphics 5200 | 0x0d260000   |                                      | 3  | 1    |    | 1   | 1    |
|                              | 0x0d220003   | iMac14,1iMac14,4                     | 3  | 1    | 2  |     |      |
| Intel HD Graphics 4600       | 0x04120004   |                                      |    |      |    |     |      |
| Intel HD Graphics 5000       | 0x0a260005   |                                      | 3  | 1    | 2  |     |      |
| Intel HD Graphics 5000       | 0x0a260006   | MacBookAir6,1MacBookAir6,2Macmini7,1 | 3  | 1    | 2  |     |      |
| Intel Iris Pro Graphics 5200 | 0x0d260007   | MacBookPro11,2MacBookPro11,3         | 4  | 1    | 2  |     | 1    |
| Intel Iris Graphics 5100     | 0x0a2e0008   | MacBookPro11,1                       | 3  | 1    | 2  |     |      |
| Intel HD Graphics 4600       | 0x0412000b   | iMac15,1                             | 0  |      |    |     |      |

## <center>broadwell平台</center>
| 显卡型号                         | platform\-id | 机型                                 | 接口 | LVDS | DP | eDP | HDMI |
|------------------------------|--------------|------------------------------------|----|------|----|-----|------|
|                              | 0x16060000   |                                    | 3  | 1    |    | 1   | 1    |
|                              | 0x160e0001   |                                    | 3  | 1    | 2  |     |      |
| Intel HD Graphics 5500       | 0x16160000   |                                    | 3  | 1    |    | 1   | 1    |
| Intel HD Graphics 5300       | 0x161e0000   |                                    | 3  | 1    |    | 1   | 1    |
| Intel Iris Pro Graphics 6200 | 0x16220000   |                                    | 3  | 1    |    | 1   | 1    |
| Intel HD Graphics 6000       | 0x16260000   |                                    | 3  | 1    |    | 1   | 1    |
| Intel Iris Graphics 6100     | 0x162b0000   |                                    | 3  | 1    |    | 1   | 1    |
| Intel HD Graphics 5300       | 0x161e0001   | MacBook8,1                         | 3  | 1    | 2  |     |      |
|                              | 0x16060002   |                                    | 3  | 1    | 2  |     |      |
| Intel HD Graphics 5500       | 0x16160002   |                                    | 3  | 1    | 2  |     |      |
| Intel Iris Pro Graphics 6200 | 0x16220002   |                                    | 3  | 1    | 2  |     |      |
| Intel HD Graphics 6000       | 0x16260002   |                                    | 3  | 1    | 2  |     |      |
| Intel Iris Graphics 6100     | 0x162b0002   | MacBookPro12,1                     | 3  | 1    | 2  |     |      |
| Intel HD Graphics 5600       | 0x16120003   |                                    | 3  | 1    | 2  |     |      |
| Intel HD Graphics 6000       | 0x16260004   |                                    | 3  | 1    | 2  |     |      |
| Intel Iris Graphics 6100     | 0x162b0004   |                                    | 3  | 1    | 2  |     |      |
| Intel HD Graphics 6000       | 0x16260005   |                                    | 3  | 1    | 2  |     |      |
| Intel HD Graphics 6000       | 0x16260006   | iMac16,1MacBookAir7,1MacBookAir7,2 | 3  | 1    | 2  |     |      |
| Intel Iris Pro Graphics6200  | 0x16220007   | iMac16,2                           | 3  | 1    | 2  |     |      |
| Intel HD Graphics 6000       | 0x16200008   |                                    | 2  | 1    | 1  |     |      |
| Intel Iris Graphics 6100     | 0x162b0008   |                                    | 3  | 1    | 2  |     |      |

## <center>skylake平台</center>
| 显卡型号                        | platform\-id | 机型             | 接口 | LVDS | DP | HDMI |
|-----------------------------|--------------|----------------|----|------|----|------|
| Intel HD Graphics 530       | 0x19120000   |                | 3  |      | 3  |      |
| Intel HD Graphics 520       | 0x19160000   |                | 3  | 1    | 2  |      |
| Intel Iris Graphics 540     | 0x19260000   |                | 3  | 1    | 2  |      |
| Intel Iris Graphics 550     | 0x19270000   |                | 3  | 1    | 2  |      |
| Intel HD Graphics 530       | 0x191b0000   | MacBookPro13,3 | 3  | 1    | 2  |      |
| Intel HD Graphics 515       | 0x191e0000   |                | 3  | 1    | 2  |      |
| Intel Iris Pro Graphics 580 | 0x193b0000   |                | 3  | 1    | 1  | 1    |
| Intel HD Graphics 530/4K\*  | 0x193b0005   | MacBookPro13,1 | 4  | 1    | 3  |      |
| Intel HD Graphics 510       | 0x19020001   |                | 0  |      |    |      |
| Intel HD Graphics 530       | 0x19120001   |                | 0  |      |    |      |
|                             | 0x19170001   |                | 0  |      |    |      |
| Intel Iris Pro Graphics 580 | 0x19320001   |                | 0  |      |    |      |
| Intel HD Graphics 520       | 0x19160002   |                | 3  | 1    | 2  |      |
| Intel Iris Graphics 540     | 0x19260002   | MacBookPro13,1 | 3  | 1    | 2  |      |
| Intel HD Graphics 515       | 0x191e0003   | MacBook9,1     | 3  | 1    | 2  |      |
| Intel Iris Graphics 540     | 0x19260004   |                | 3  | 1    | 2  |      |
| Intel Iris Graphics 550     | 0x19270004   | MacBookPro13,2 | 3  | 1    | 2  |      |
| Intel HD Graphics 530       | 0x191b0006   |                | 1  |      |    |      |
| Intel Iris Graphics 540     | 0x19260007   |                | 3  | 1    | 2  |      |

## <center>kabylake平台</center>
| 显卡型号                         | platform\-id | 机型                     | 接口 | LVDS | DP | HDMI |
|------------------------------|--------------|------------------------|----|------|----|------|
| Intel HD Graphics 630        | 0x59120000   | iMac18,2iMac18,3       | 3  |      | 3  |      |
| Intel HD Graphics 630        | 0x59120003   | FCPX加速用                | 0  |      |    |      |
| Intel HD Graphics 620        | 0x59160000   | MacBookPro14,2         | 3  | 1    | 2  |      |
| Intel HD Graphics 620        | 0x59160009   |                        | 3  | 1    | 2  |      |
|                              | 0x59180002   |                        |    |      |    |      |
| Intel HD Graphics 630        | 0x591b0000   | MacBookPro14,3         | 3  | 1    | 2  |      |
| Intel HD Graphics 630        | 0x591b0006   |                        | 1  | 1    |    |      |
|                              | 0x591c0005   |                        | 3  | 1    | 2  |      |
| Intel HD Graphics 615        | 0x591e0000   |                        | 3  | 1    | 2  |      |
| Intel HD Graphics 615        | 0x591e0001   | MacBook10,1            | 3  | 1    | 2  |      |
| Intel HD Graphics 635        | 0x59230000   |                        | 3  | 1    | 2  |      |
| Intel Iris Plus Graphics 640 | 0x59260000   |                        | 3  | 1    | 2  |      |
| Intel Iris Plus Graphics 640 | 0x59260002   | MacBookPro14,1iMac18,1 | 3  | 1    | 2  |      |
| Intel Iris Plus Graphics 640 | 0x59260007   |                        | 3  | 1    | 2  |      |
| Intel Iris Plus Graphics 650 | 0x59270000   |                        | 3  | 1    | 2  |      |
| Intel Iris Plus Graphics 650 | 0x59270004   | MacBookPro14,2         | 3  | 1    | 2  |      |
| Intel Iris Plus Graphics 650 | 0x59270009   |                        | 3  | 1    | 2  |      |
| Intel UHD Graphics 617       | 0x87c00000   |                        | 3  | 1    | 2  |      |
| Intel UHD Graphics 617       | 0x87c00005   | MacBookAir8,1          | 3  | 1    | 2  |      |

## <center>caffeelake平台</center>
| 显卡型号                         | platform\-id | 机型             | 接口 | LVDS | DP | STOLEN |
|------------------------------|--------------|----------------|----|------|----|--------|
|                              | 0x3E000000   |                | 3  | 1    | 2  | 57mb   |
| Intel UHD Graphics 630       | 3E910003     | FCPX加速用        |    |      |    |        |
| Intel UHD Graphics 630       | 3E920000     |                | 3  | 1    | 2  | 57mb   |
| Intel UHD Graphics 630       | 3E920003     | FCPX加速用        |    |      |    |        |
| Intel UHD Graphics 630       | 3E920009     |                | 1  | 1    |    | 57mb   |
| Intel UHD Graphics 630       | 3E9B0000     | MacBookPro15,1 | 3  | 1    | 2  | 57mb   |
| Intel UHD Graphics 630       | 3E980003     | FCPX加速用        |    |      |    |        |
| Intel UHD Graphics 630       | 3E9B0006     |                | 1  | 1    |    | 38mb   |
| Intel UHD Graphics 630       | 3E9B0007     | Macmini8,1     | 3  |      | 3  | 57mb   |
| Intel UHD Graphics 630       | 3E9B0008     |                | 1  |      |    | 57mb   |
| Intel UHD Graphics 630       | 3E9B0009     |                | 3  | 1    | 2  | 57mb   |
| Intel Iris Plus Graphics 655 | 3EA50000     |                | 3  | 1    | 2  | 57mb   |
| Intel Iris Plus Graphics 655 | 3EA50004     | MacBookPro15,2 | 3  | 1    | 2  | 57mb   |
| Intel Iris Plus Graphics 655 | 3EA50005     |                | 3  | 1    | 2  | 57mb   |
| Intel Iris Plus Graphics 655 | 3EA50006     |                | 3  | 1    | 2  | 57mb   |
| Intel Iris Plus Graphics 655 | 3EA50009     |                | 3  | 1    | 2  | 57mb   |

## <center>新增平台</center>
| 显卡型号                   | platform\-id | 机型                       | 接口 | LVDS | DP | HDMI |
|------------------------|--------------|--------------------------|----|------|----|------|
| Intel UHD Graphics 620 | 0x3ea00000   | 仿冒3e9b0007               |    |      |    |      |
| Intel UHD Graphics 617 | 0x87c00000   | MacBookAir8,1            |    |      |    |      |
| Intel UHD Graphics 630 | 0x3e9b0007   | MacBookPro15,1Macmini8,1 |    |      | 3  |      |

<style>
    table th {
    font-weight: bold; /*加粗*/
    text-align: center !important; /*内容居中，加上 !important 避免被 Markdown 样式覆盖*/
    background: #FE9600; /*背景色*/
}
    table tbody tr:nth-child(2n) {
    background: #eee; 
}
    table {
    width: 100%; /*表格宽度*/
    max-width: 65em; /*表格最大宽度，避免表格过宽*/
    border: 1px solid #dedede; /*表格外边框设置*/
    margin: 15px auto; /*外边距*/
    border-collapse: collapse; /*使用单一线条的边框*/
    empty-cells: show; /*单元格无内容依旧绘制边框*/
}
table th,
table td {
  height: 35px; /*统一每一行的默认高度*/
  border: 1px solid #dedede; /*内部边框样式*/
  padding: 0 10px; /*内边距*/
}
table td {
    font-weight: bold
}
</style>