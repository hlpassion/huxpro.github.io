---
layout:    post
title:    "Machine Learning Yearning 翻译，动手写起来!"
subtitle:    "chapter10"
date:    2017-06-06 21:15:00
author:    "Heron"
header-img:    "img/post-bg-mly.webp"
header-mask:    0.3
catalog:    true
tags:
    - 博客
    - 翻译
    - 机器学习
---
## 10. Having a dev set and metric speeds up iterations

对于一个新的问题很难预先知道什么方法会work的最好。即使是经验丰富的机器学习研究者在发现满意的方法前也会尝试各种各样的想法。在构建一个机器学习系统时，我通常：

1. 首先构建一些如何建立系统的想法。
2. 编程实现这些想法。
3. 用实验来告诉我这些想法work的怎么样。(通常我开始的一些想法是不work的！)基于这些知识，返回生成更多的想法，不断的迭代这个过程。

![iteration](/img/in-post/mly-10-iteration.png)

这是一个迭代的过程。你循环的越快，你的进展就越快。这就是为什么开发/测试集和评价指标很重要：每次你尝试一个想法，在开发集上衡量你的想法的表现可以让你快速决定你的前进方向是不是正确。

相反，如果你没有特定的开发集和评价指标。每次你的团队开发一个猫分类器，你不得不把它移植到你的app中，然后亲身体验几个小时来感受这个新的分类器性能是否有提升。这将极其缓慢。并且，如果你的团队奖分类器精度从95%提升到95.1%，你通过亲身试用app可能无法检测到这0.1%的提升。然而通过这0.1%不断的改进，你的系统将取得很大的进步。使用开发集和评价指标可以让你快速检测哪个想法成功的给你的系统带来小(或大)的提升，让你快速决定在哪个方法上继续努力，哪个方法需要舍弃。