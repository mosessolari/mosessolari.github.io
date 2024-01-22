[January 22, 2024]

# Analytic Continuation of the Sigma function (across its indices) from $\mathbb{Z}\rightarrow\mathbb{C}$

## Introduction:

The "Sigma" function in mathematics is a notation that is used as an analogue to the iterative operation of addition.
It is a fundamental construct of arithmatic mathematics, and has been studied extensively, however, only for summations up to some $`N:N\in\mathbb{Z}`$.
In this text I will be deriving the following expression for the Sigma function:
$$S(z)=\lim_{N\to\infty}\sum_{k=a}^z\left[f(k)-f(k+N)\right]=\lim_{N\to\infty}\sum_{k=a}^N\left[f(k)-f(k+z)\right]\quad\forall\ z:z\in\mathbb{C}$$
I also present cases where:
$$S(x):=\sum_{k=a}^x\left[f(k)\right]\quad\forall\ x:x\in\mathbb{R}$$

<br></br>
<br></br>

## Motivation:

In our ever bourgeoning world of experience, there is unending arms race associated with the war of discovery, so we must treat our prized armory that is mathematics with care, and ensure that the blades are perpetually sharpened – every idea is a whetstone. Simply put, this is my attempt at refurbishing/sharpening one of our oldest knives: the Sigma function. To narrow it down to direction application, I will be using this result to generalise the Polygamma function (in a future post), and in a similar vain, it can be recognised that these ideas crossover with statistical and quantum mechanics.

<br></br>
<br></br>

## Math:

First, observe the definition for the Sigma function that adds $f(k)$ and $xth$ number of times, with the introduction of some independent variable, $m$:
$$\sum_{k=a}^x\left[f(k)\right]=\sum_{k=a}^x\left[f(k)\right]+\sum_{k=x+1}^N\left[f(k)\right]-\sum_{k=x+1}^N\left[f(k)\right]\quad\forall\ N:N\in\mathbb{Z}$$


--------------------




$$S(x)=\lim_{N\to\infty}\sum_{k=a}^x\left[f(k)-f(k+N)\right]=\lim_{N\to\infty}\sum_{k=a}^N\left[f(k)-f(k+x)\right]\quad\forall\ x:x\in\mathbb{R}$$


$$\sum_{k=a}^N \left[ f(k, x) \right] = \sum_{k=a}^N \left[ f(k, x) \right]$$

$\sum_{k=a} ^{N} a_i x^i$

$`\sqrt{3x-1}+(1+x)^2\left( \sum_{k=1}^n a_k b_k \right)^2`$
