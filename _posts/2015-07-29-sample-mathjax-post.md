---
layout: post
author: 红阳
title: "Mathjax test"
description: 
modified: 2015-07-29
mathjax: true
---
模板采用MathJax支持数学公式，只要在使用公式文章的头信息加入`mathjax: true`就可以使用。
markdown和mathjax有少许冲突，所以在使用时常常遇到一些问题，下面就把常见的问题列出来，以作参考。


由于这两者的语法有少许冲突，所以在使用时常常遇到一些问题，下面就把常见的问题列出来，以作参考。

<span class="more"></span>

backslash的问题。Markdown中，backslash是用作转义字符的，虽然MathJax(LaTeX)中也会用作转义，但也使用两个backslash作为"\\\\"作为换行符。因此，如果在输入数学公式的时候，如果仅仅输入两条backslash，那么会导致Markdown将这个识别成backslash的转义，即仅仅输入一条backslash。因此，在数学公式中的换行，应该使用四条backslash，即输入"\\\\\\\\"。

在Markdown中，"\\{"是用来表示一个花括号的，也就是说这里的backslash是用来转义的，因此，如果在输入数学公式的时候，仅仅输入一条backslash加上{，那么Markdown就先把他们识别成一个花括号，然后MathJax仅仅看到一个花括号，也就是说，类似"\left\\{"就变成了"\left{"。

**The Lorenz Equations**

$$
\begin{aligned}
  \dot{x} & = \sigma(y-x) \\\\
  \dot{y} & = \rho x - y - xz \\\\
  \dot{z} & = -\beta z + xy
\end{aligned}
$$

**The Cauchy-Schwarz Inequality**

$$
( \sum\_{k=1}^n a\_k b\_k )^2 \leq
 ( \sum\_{k=1}^n a\_k^2 ) ( \sum\_{k=1}^n b_k^2 )
$$

**A Cross Product Formula**

$$
  \mathbf{V}\_1 \times \mathbf{V}\_2 =
  \begin{vmatrix}
    \mathbf{i} & \mathbf{j} & \mathbf{k} \\\\
    \frac{\partial X}{\partial u} & \frac{\partial Y}{\partial u} & 0 \\\\
    \frac{\partial X}{\partial v} & \frac{\partial Y}{\partial v} & 0 \\\\
  \end{vmatrix}
$$

**The probability of getting \(k\) heads when flipping \(n\) coins is:**

$$P(E) = {n \choose k} p^k (1-p)^{ n-k} $$

**An Identity of Ramanujan**

$$
   \frac{1}{(\sqrt{\phi \sqrt{5}}-\phi) e^{\frac25 \pi}} =
     1+\frac{e^{-2\pi}} {1+\frac{e^{-4\pi}} {1+\frac{e^{-6\pi}}
      {1+\frac{e^{-8\pi}} {1+\ldots} } } }
$$

**Maxwell's Equations**


$$\begin{align}
  \nabla \times \vec{\mathbf{B}} -\, \frac1c\, \frac{\partial\vec{\mathbf{E}}}{\partial t} & = \frac{4\pi}{c}\vec{\mathbf{j}} \\\\
  \nabla \cdot \vec{\mathbf{E}} & = 4 \pi \rho \\\\
  \nabla \times \vec{\mathbf{E}}\, +\, \frac1c\, \frac{\partial\vec{\mathbf{B}}}{\partial t} & = \vec{\mathbf{0}} \\\\
  \nabla \cdot \vec{\mathbf{B}} & = 0
\end{align}$$