---
layout:     post
title:      一些数的整除性质、割尾法与截断法
subtitle:   
date:       2024-05-05
author:     VecantDK
header-img: img/post-bg-coffee.jpeg
catalog: 	 true
tags:

    - 数学
---

<head>
    <script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>
    <script type="text/x-mathjax-config">
        MathJax.Hub.Config({
            tex2jax: {
            skipTags: ['script', 'noscript', 'style', 'textarea', 'pre'],
            inlineMath: [['$','$']]
            }
        });
    </script>
</head>



## 前言 

在试除一些数时经常会用到它们的整除性质. 比如**若一个整数的末位是0或5，则这个数能被5整除**、**若一个整数的数字和能被3整除，则这个数能被3整除**等等. 本文重点研究3、9、7、11、13、17、19等数的整除性质. 

---

## 一、3，9的整除性质

**若一个整数的数字和能被 $3$ 整除，则这个数能被 $3$ 整除；**

**若一个整数的数字和能被 $9$ 整除，则这个数能被 $9$ 整除.**

3和9的整除性质比较常见. 先证明一个引理： 



**引理1**    $9\mid (10^k-1)(k\in\mathbb{N})$.

**证明**    $10^k-1=\overbrace{9\cdots9}^{k\text{个}9}=9\times \overbrace{1\cdots1}^{k\text{个}1}$.

易知 $9\mid 9\times \overbrace{1\cdots1}^{k\text{个}1}$.

所以 $9\mid (10^k-1)$. ■



下面给出原命题的证明. 

**证明**    对于任意整数 $\overline{a_na_{n-1}\cdots a_0}$，它都可以表示成 $\sum\limits_{i=0}^na_i\times10^i$​ 的形式.

则

（1）$3\mid \overline{a_na_{n-1}\cdots a_0}$

$\Leftrightarrow3\mid (a_0\times10^0+a_1\times10+\cdots+a_n\times10^n)$.

由**引理1**得知 $9\mid (10^n-1)$，

所以 $3\mid (10^n-1)$，即 $10^n\equiv1(\mod3)$

所以 $3\mid (a_0\times10^0+a_1\times10+\cdots+a_n\times10^n)$.

$\Leftrightarrow3\mid (a_0+a_1+\cdots+a_n)$.

即**若一个整数的数字和能被 $3$ 整除，则这个数能被 $3$ 整除.**

（2）$9\mid \overline{a_na_{n-1}\cdots a_0}$

$\Leftrightarrow9\mid (a_0\times10^0+a_1\times10+\cdots+a_n\times10^n)$.

由**引理1**得知 $9\mid (10^n-1)$，即 $10^n\equiv1(\mod9)$

所以 $9\mid (a_0\times10^0+a_1\times10+\cdots+a_n\times10^n)$.

$\Leftrightarrow9\mid (a_0+a_1+\cdots+a_n)$.

即**若一个整数的数字和能被 $9$ 整除，则这个数能被 $9$ 整除.** ■

## 二、7，11，13，17，19的整除性质（割尾法）

割尾法一般是指用数的高位数 $\pm$​ 低位数的倍数形成的数的整除性质来判断原数的整除性质. 

- $7$ 的整除性质：**若一个整数的个位数字截去，再从余下的数中减去个位数的 $2$ 倍，如果差是 $7$ 的倍数，则原数能被 $7$ 整除.**
- $11$ 的整除性质：**若一个整数的个位数字截去，再从余下的数中减去个位数，如果差是 $11$ 的倍数，则原数能被 $11$ 整除.**
- $13$ 的整除性质：**若一个整数的个位数字截去，再从余下的数中加上个位数的 $4$ 倍，如果和是 $13$ 的倍数，则原数能被 $13$ 整除.**
- $17$ 的整除性质：**若一个整数的个位数字截去，再从余下的数中减去个位数的 $5$ 倍，如果差是 $17$ 的倍数，则原数能被 $17$ 整除.**
- $19$ 的整除性质：**若一个整数的个位数字截去，再从余下的数中加上个位数的 $2$ 倍，如果和是 $19$ 的倍数，则原数能被 $19$ 整除.**

下面给出证明. 



**证明**    对于任意整数 $\overline{a_na_{n-1}\cdots a_0}$，它可以表示成 $\overline{xa_0}=10x+a_0$ 的形式，其中 $x=\overline{a_na_{n-1}\cdots a_1}$.

（1）$7\mid x-2a_0$

$\Leftrightarrow7\mid 10x-20a_0$

$\Leftrightarrow7\mid 10x-20a_0+21a_0$

$\Leftrightarrow7\mid 10x+a_0$

$\Leftrightarrow7\mid \overline{a_na_{n-1}\cdots a_0}$.

即**若一个整数的个位数字截去，再从余下的数中减去个位数的 $2$ 倍，如果差是 $7$ 的倍数，则原数能被 $7$ 整除.**

（2）$11\mid x-a_0$

$\Leftrightarrow11\mid 10x-10a_0$

$\Leftrightarrow11\mid 10x-10a_0+11a_0$

$\Leftrightarrow11\mid 10x+a_0$

$\Leftrightarrow11\mid \overline{a_na_{n-1}\cdots a_0}$.

即**若一个整数的个位数字截去，再从余下的数中减去个位数，如果差是 $11$ 的倍数，则原数能被 $11$ 整除.**

（3）$13\mid x+4a_0$

$\Leftrightarrow13\mid 10x+40a_0$

$\Leftrightarrow13\mid 10x+40a_0-13\times3a_0$

$\Leftrightarrow13\mid 10x+a_0$

$\Leftrightarrow13\mid \overline{a_na_{n-1}\cdots a_0}$.

即**若一个整数的个位数字截去，再从余下的数中加上个位数的 $4$ 倍，如果和是 $13$ 的倍数，则原数能被 $13$ 整除.**

（4）$17\mid x-5a_0$

$\Leftrightarrow17\mid 10x-50a_0$

$\Leftrightarrow17\mid 10x-50a_0+17\times3a_0$

$\Leftrightarrow17\mid 10x+a_0$

$\Leftrightarrow17\mid \overline{a_na_{n-1}\cdots a_0}$​.

即**若一个整数的个位数字截去，再从余下的数中减去个位数的 $5$ 倍，如果差是 $17$ 的倍数，则原数能被 $17$ 整除.**

（5）$19\mid x+2a_0$

$\Leftrightarrow19\mid 10x+20a_0$

$\Leftrightarrow19\mid 10x+20a_0-19a_0$

$\Leftrightarrow19\mid 10x+a_0$

$\Leftrightarrow19\mid \overline{a_na_{n-1}\cdots a_0}$.

即**若一个整数的个位数字截去，再从余下的数中加上个位数的 $2$ 倍，如果和是 $19$ 的倍数，则原数能被 $19$ 整除.** ■

## 三、7，11，13的整除性质（截断法）

**若一个整数的后三位截去，再从余下的数中减去后三位，如果差是 $7$，$11$，$13$ 的倍数，则原数能被  $7$，$11$，$13$ 整除.**

下面给出证明. 

**证明**    由 $7\times11\times13=1001$ 可得 $7\mid 1001,11\mid 1001,13\mid 1001$.

对于任意整数 $\overline{a_na_{n-1}\cdots a_2 a_1 a_0}$，它可以表示成 $\overline{xa_0}=1000x+\overline{a_2 a_1 a_0}$ 的形式，其中 $x=\overline{a_na_{n-1}\cdots a_3}$.

则  $7\mid \overline{a_na_{n-1}\cdots a_2 a_1 a_0}$

$\Leftrightarrow7\mid (1000x+\overline{a_2 a_1 a_0})$

$\Leftrightarrow7\mid (1001x-x+\overline{a_2 a_1 a_0})$

$\Leftrightarrow7\mid ({\overline{a_2 a_1 a_0}}-x)$.

即**若一个整数的后 $3$ 位截去，再从余下的数中减去后三位，如果差是 $7$ 的倍数，则原数能被  $7$​ 整除.**

同理，可证 $11$，$13$ 的整除性质. ■

## 四、11的整除性质（奇偶位差法）

**若一个整数的奇数位之和与偶数位之和的差能被 $11$ 整除，则这个数能被 $11$ 整除.**

先证明两个引理： 

**引理2**    $11\mid (10^{2k}-1)(k\in\mathbb{N})$.

**证明**    

$$
\begin{aligned}
{} & 10^{2k}-1 & \\
=  & \underbrace{\overline{9\cdots9}}_{2k\text{个}9} \\
=  & 9\times\underbrace{\overline{1\cdots1}}_{2k\text{个}1} & \\
=  & 9(11\cdot10^{2k-2}+11\cdot10^{2k-4}+\cdots+11) & \\
=  & 9\cdot11\cdot(10^{2k-2}+10^{2k-4}+\cdots+1).
\end{aligned}
$$


易知 $11\mid 9\cdot11\cdot(10^{2k-2}+10^{2k-4}+\cdots+1)$，

即 $11\mid (10^{2k}-1)$. ■



**引理3** $11\mid (10^{2k+1}+1)(k\in\mathbb{N})$.

**证明**    因式分解 $x^{2k+1}+1$ 可得

$x^{2k+1}+1=(x+1)(x^{2k}-x^{2k-1}+x^{2k-2}-\cdots+1)$​.

当 $x=10$ 时，$\text{原式}=10^{2k+1}+1=11(10^{2k}-10^{2k-1}+10^{2k-2}-\cdots+1)$.

易知 $11\mid 11(10^{2k}-10^{2k-1}+10^{2k-2}-\cdots+1)$，所以 $11\mid (10^{2k+1}+1)$. ■



下面给出原命题的证明.

**证明**    对于任意整数 $A=\overline{a_na_{n-1}\cdots a_0}$，

$$
\begin{aligned}
{A=} & a_0\times10^0+a_1\times10+\cdots+a_n\times10^n & \\
=  &   (a_0(10^0-1)+a_0)+(a_1(10+1)-a_1)+\cdots+(a_n(10^n\pm1)\mp a_n).& \\
\end{aligned}
$$

由**引理2**、**引理3**可得

$11\mid A$

$\Leftrightarrow11\mid ((a_0(10^0-1)+a_0)+(a_1(10+1)-a_1)+\cdots+(a_n(10^n\pm1)\mp a_n))$

$\Leftrightarrow11\mid (a_0-a_1+\cdots\mp a_n)$，

即**若一个整数的奇数位之和与偶数位之和的差能被 $11$ 整除，则这个数能被 $11$ 整除.** ■



