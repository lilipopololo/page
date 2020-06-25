---
layout: demo
title: demo
description: 最近查找关于cv库关于全景图生成的代码作为大作业，翻出一堆使用stitcher的，一查结果md全使用opencv2.xxx版本，我了个大草。仔细查看了后才发现
category: opencv
---
最近查找关于cv库关于全景图生成的代码作为大作业，翻出一堆使用stitcher的，一查结果md全使用opencv2.xxx版本，我了个大草。仔细查看了后才发现opencv2版本那些有版权的算法还集成在opencv里，从3.0版本开始出现了一个contrib库专门存放这些文件，不再提供这些算法了。也就是说使用contrib的算法不能为赚取利益，然后cmake处理一下，发现vs2015编译出现一堆错误。底下是错误解决方式还有文件说明。
偶，还有md按照教程编出来的带extra库的opencv debug版本13个G，release版本7个G我放弃治疗直接删了。md占我空间的恶人就是你！！！！！！！！！！！！！！！！！！！！！！！
\images\otherD:\boostdesc_bgm.i等.zip
见
https://blog.csdn.net/qq_31112205/article/details/105210496
https://blog.csdn.net/AlexWang30/article/details/99612188?locationNum=6&fps=1