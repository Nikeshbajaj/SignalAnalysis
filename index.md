---
title: Mathematical Methods for Signal Analysis
layout: default
---
<!--<script src='https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.4/MathJax.js?config=default'></script> -->

# Table of Contents (in progress...)
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

$$C_x =  \frac{1}{n} X^TX$$

which will be a $$m \times m$$ matrix. In estimation theory, $$n-1$$ is used i.e. $$C_x =  \frac{1}{n-1} X^TX$$, as to estimate statistics from sample, rather than from population.

Now the question is, what it is, and what does it tell us. To understand, this let's take a small example and go thorugh it. Let's consider a $$X$$ as
The choice of X is very specific at this time (i.e. mean of each coumun is zero), which will be clear in short.

$$X = 
  \left[\begin{array}{rrrr} 
  -2&  2& -4&  1 \\
  -1&  1& -4& -1 \\
   0&  0&  1&  2 \\
   1& -1&  3& -2 \\
   2& -2&  4&  0 \\
  \end{array}\right]
$$
which leads to  $$C_x = 
  \left[\begin{array}{rrrr} 
2.0 & -2.0 & 4.6 & -0.6 \\
-2.0 & 2.0 & -4.6 & 0.6 \\
4.6 & -4.6 & 11.6 & -0.8\\
-0.6 & 0.6 & -0.8 & 2.0 \\
  \end{array}\right]
$$

In python it is super easy to compute, assuming X is a numpy array ::: ```Cx = X.T@X/X.shape[0]``` :::

If look into details, what is happining is, we are computing dot product of every coulumn of $$X$$ with every row of $$X^T$$ (which is actually the column of $$X$$).
So, we have dot-product of each column with each other column, including it self. Lets name each column of $$X$$ as $$x_i$$ then

<!--
$$\begin{centre}
$$X^T = \left[\begin{array}{r}x_1^T\\
                            x_2^T\\
                            x_3^T\\
                            x_4^T\\ \end{array}\right]$$  and $$X = \left[x_1, x_2, x_3, x_4\right]$$
\end{centre}$$
-->

<p style="text-align:center">...</p>


$$X^T = \left[\begin{array}{r}x_1^T\\
                            x_2^T\\
                            x_3^T\\
                            x_4^T\\ \end{array}\right]$$  and $$X = \left[x_1, x_2, x_3, x_4\right]$$
  
  
$$X^T = \left[\begin{array}{crc}
                        - & x_1^T & -\\
                        - & x_2^T & -\\
                        - & x_3^T & -\\
                        - & x_4^T & -\\ \end{array}\right]$$ and $$X = \left[\begin{array}{cccc}
                        |   & |   &  |   &  |\\
                        x_1 & x_2 & x_3  & x_4\\
                        |   & |   &  |   &  |\\  \end{array}\right]$$



 $$C_x = 
    \frac{1}{n} X^TX = \frac{1}{n} \left[\begin{array}{rrrr} 
 x_1^Tx_1 & x_1^Tx_2 & x_1^Tx_3 & x_1^Tx_4  \\
 x_2^Tx_1 & x_2^Tx_2 & x_2^Tx_3 & x_2^Tx_4  \\
 x_3^Tx_1 & x_3^Tx_2 & x_3^Tx_3 & x_3^Tx_4  \\
 x_4^Tx_1 & x_4^Tx_2 & x_4^Tx_3 & x_4^Tx_4  \\
  \end{array}\right]
$$


<p style="border:2px; border-style:solid; border-color:#3377FF; padding: 1em;">  

<b>Theorem</b>: <i>Covariance matrix is always symmetric</i>
<br>
<b>Proof</b>: lets ignore <b>n</b>

$$C_x^T = (X^TX)^T = X^T(X^{T})^T = X^TX = C_x$$

<i>QED</i>
</p>

<!--
<p style="border:2px; border-style:solid; border-color:#3377FF; padding: 1em;">
<table>
<tr>
<td>
<p>
<b>Theorem</b>: <i>Covariance matrix is always symmetric</i>
<br>
<b>Proof</b>: lets ignore <b>n</b>
  
$$C_x^T = (X^TX)^T = X^T(X^{T})^T = X^TX = C_x$$

<i>QED</i>
</p>
</td
<td>
$$(AB)^T = B^TA^T$$
</td>
</tr>
</table>
</p>
-->


<table>
<tr>
<td>
<b>Theorem</b>: <i>Covariance matrix is always symmetric</i>
<br>
<b>Proof</b>: lets ignore <b>n</b>
  
$$C_x^T = (X^TX)^T = X^T(X^{T})^T = X^TX = C_x$$

<i>QED</i>
</td
<td>
$$(AB)^T = B^TA^T$$
</td>
</tr>
</table>





<!--
<hr>
# Chapter 2
-->
