---
layout:     post
title:      "Bayes Decision Rule"
subtitle:   " \"First step into ML\""
date:       2024-06-23 11:00:00
author:     "Yz"
header-img: "img/home-bg-o.jpg"

tags:
    - Machine Learning
---
# 贝叶斯公式
对于一些点 $a_i$ 它们有某些特征 $x_i$ 在已知特征 $x_i$的情况下将 $a_i$ 归类进$\omega_i$ 的概率记作 $P(\omega_i | x_i )$ \
那么有 $P(\omega_i | x_i ) = \frac{P(x_i | \omega_i)}{P(x_i)} = \frac{P(x_i | \omega_i)P(\omega_i)}{P(x_i)}$ \
+ 先验概率      $P(\omega_i)$
+ 联合概率密度  $P(\omega_i , x_i)$
+ 总体密度     $P(x_i)$
+ 类条件密度    $P(x_i | \omega_i)$
+ 后验概率      $P(\omega_i | x_i)$
+ 总体密度      $P(x_i)$
# 最小错误率贝叶斯决策
## 错误
定义某个决策在样本 $a_i$ 上错误的概率是 $P(e|a_i)$ \
假设共有n类 \
那么
$P(e|a_i)=\sum_{i=1}^{n}P(\omega|a_i),a_i \notin \omega_i$ \
错误率定义为 $P(e)=\int{P(e|a_i)P(a_i)da_i}$
## 决策
> $min \quad P(e)=\int{P(e|a_i)P(a_i)da_i}$
