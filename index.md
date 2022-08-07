---
title: Mathematical Methods for Signal Analysis
layout: default
---
<script src='https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.4/MathJax.js?config=default'></script>

# Table of Contents (in progress..)
* [Chapter 1: Linear Algebra](#chapter-1)
* [Chapter 2: Least Square](#chapter-1)
* [Chapter 3: Principle Compononent Ananlysis](#chapter-1)
* [Chapter 4: Independent Compononent Ananlysis](#chapter-1)

<hr>
# Chapter 1
## Linear Algebra


## Covariance Matrix
Consider a matrix $$X \in R^{n\times m}$$, where $$X$$ has $$n$$ samples of $$m$$-different measuresments, i.e. $$m$$-channels signals. Typically, $$n>m$$. In other domain, $$m$$ is typically known as features, sources, independent variables etc. So, X is an Matrix with m features (measurements).

Then Covariance Matrix $$C_x$$ is computed as:
$$C_x =  X^TX$$

which will be a $$m \times m$$ matrix

Now the question is, what it is, and what does it tell us. To understand, this let's take a small example and go thorugh it. Let's consider a $$X$$ as

$$X = 
  \left[\begin{array}{cc} 
  -2& 2& -4& 1&  \\
  -1& 1& -4& -1&  \\
  0& 0& 1& 2&  \\
  1& -1& 3& -2&  \\
 2& -2& 4& 0&  \\
  \end{array}\right]
$$ which leads to  $$X = 
  \left[\begin{array}{cc} 
  10 & -10 & 23 & -3 &  \\
  -10 & 10 & -23 & 3 &  \\
  23 & -23 & 58 & -4 &  \\
  -3 & 3 & -4 & 10 &  \\
  \end{array}\right]
$$



<!--
<hr>
# Chapter 2
-->
