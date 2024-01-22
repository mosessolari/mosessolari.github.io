[January 22, 2024]

# Analytic Continuation of the Sigma notation (across its indices) from $\mathbb{Z}\to\mathbb{C}$

## Introduction
The Sigma notation in mathematics is a notation that is used as an analogue to the iterative operation of addition.
It is a fundamental construct of arithmatic mathematics, and has been studied extensively, however, only for summations up to some $`N:N\in\mathbb{Z}`$.
In this text I will be deriving the following expression for a "smooth" summation function, S
```math
S(x,f,N)=\sum_{k=a}^x\left[f(k)-f(k+N)\right]=\sum_{k=a}^N\left[f(k)-f(k+x)\right]
```
that is an analogue to a standard useage of the Sigma notation by
```math
lim_{N\to\pm\infty}S(x,f,N):=\sum_{k=a}^x\left[f(k)\right]\ \ \forall\ \left\{x\in\mathbb{R}\right\}\ \ when\ \ \lim_{N\to\pm\infty}\sum_{k=a}^{t}\left[f(k+N)\right]=0\ \ \forall\ \left\{|t|\in\mathbb{N}\right\}
```
$S$ is also analytically extended such that
```math
\lim_{M\to0}S(\frac{1}{z},f,\frac{1}{M})=\lim_{M\to0}\sum_{k=a}^{\frac{1}{z}}\left[f(k)-f(k+\frac{1}{M})\right]=\lim_{M\to0}\sum_{k=a}^\frac{1}{M}\left[f(k)-f(k+\frac{1}{z})\right]\ \ \forall\ \left\{z\in\mathbb{C}:z\neq 0\right\}
```

<br></br>

### Motivation

In our ever bourgeoning world of experience, there is a perpetual arms race that is associated with the war of discovery, and in good favour, we must treat our prized armory with respect and care, ensuring that we always strive to have our blades sharpened and throats polished. Simply put, this is my attempt at refurbishing one of mathematics best weapons: the Sigma notation. Narrowing the scope down to direction application; I will be using the aforementioned analogue expression for $S$ to generalise the Polygamma function in a future post, and in a similar vein, implications in statistical and quantum mechanic can be recognised.

<br></br>

## Math

First, observe the following expression of the Sigma notation from some point $a\in\mathbb{R}$ that sums $f(k)$ an $xth$ number of times; introducing an independent variable, $N$, we see
```math
\sum_{k=a}^x\left[f(k)\right]=\sum_{k=a}^N\left[f(k)\right]-\sum_{k=x+1}^N\left[f(k)\right]\ \ \forall\ \left\{N\in\mathbb{Z}:N > x > a\ \ or\ \ a > x > N\right\}\ \ and\ \ f(q)\in\mathbb{C}\ \ \forall\ \left\{q\in\mathbb{C}\right\}
```

On the RHS we can move the $x$ term from $k=x+1$ into $f(k)$ by subtracting $x$ from the index start and finish
```math
\sum_{k=a}^x\left[f(k)\right]=\sum_{k=a}^N\left[f(k)\right]-\sum_{k=1}^{N-x}\left[f(k+x)\right]
```

Following a similar line of reasoning from the first step, we see
```math
\sum_{k=a}^x\left[f(k)\right]=\sum_{k=a}^N\left[f(k)\right]-\sum_{k=1}^N\left[f(k+x)\right]+\sum_{k=N-x+1}^N\left[f(k+x)\right]
```

Subtracting the Sigma terms that start at $k=N-x+1$ from both sides, then applying similar reason from the second step gives the afformentioned smooth summation function, $S$
```math
S(x,f,N)=\sum_{k=a}^x\left[f(k)\right]-\sum_{k=N+1}^{N+x}\left[f(k)\right]=\sum_{k=a}^N\left[f(k)-f(k+x)\right]
```
```math
\sum_{k=a}^x\left[f(k)\right]-\sum_{k=1}^x\left[f(k+N)\right]=\sum_{k=a}^N\left[f(k)-f(k+x)\right]
```
```math
\sum_{k=a}^x\left[f(k)-f(k+N)\right]=\sum_{k=a}^N\left[f(k)-f(k+x)\right]\qquad(1)
```

Note that $(1)$ is in $\mathbb{Z}$ if both $x$ and $N$ are also in $\mathbb{Z}$. By letting $|N|\to\infty$ we find a calculatable expression for $lim_{|N|\to\infty}S(x,f,N)$ in a larger domain for $x$. It can be seen that
```math
lim_{N\to\pm\infty}S(x,f,N):=\sum_{k=a}^x\left[f(k)\right]\ \ \forall\ \left\{x\in\mathbb{R}\right\}\ \ when\ \ \lim_{N\to\pm\infty}\sum_{k=a}^{t}\left[f(k+N)\right]=0\ \ \forall\ \left\{|t|\in\mathbb{N}\right\}
```
which is a more well defined analogue to the Sigma notation for $x$.

This is the part where you may have to suspend your disbelief for a moment, lol. Letting $N=\frac{1}{M},\ x=\frac{1}{z}$ where $`\left\{M\in\mathbb{C}\right\}`$, $`\left\{z\in\mathbb{C}:z\neq 0\right\}`$ and $|\frac{1}{M}|>|\frac{1}{z}|$, we can rewrite $S$ in terms of complex indices
```math
\lim_{M\to0}S(\frac{1}{z},f,\frac{1}{M})=\lim_{M\to0}\sum_{k=a}^{\frac{1}{z}}\left[f(k)-f(k+\frac{1}{M})\right]=\lim_{M\to0}\sum_{k=a}^\frac{1}{M}\left[f(k)-f(k+\frac{1}{z})\right]\ \ \forall\ \left\{z\in\mathbb{C}:z\neq 0\right\}
```

<br></br>

## Concluding Statements
Get good, kid. (I will be back to for that Polygamma generalisation, so until then LOVE YOU IF YOU ARE READING THIS)
