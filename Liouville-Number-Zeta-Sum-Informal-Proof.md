[January 26, 2024]

# An informal proof that $\zeta(2n-1)\ \ \forall\ \ n\in\mathbb{N}$ are Liouville numbers (and some possible followup results on the matter regarding infinite sums of monotonic functions)

## Opening Notes
The "smooth" summation function that I discussed in my other post is a generalised equivalent (conceptually) to Euler's product definition for $\Gamma(x)$, but the names "Euler sum" and "Euler product" are already in use, so from here on out I will be referring to this function as a "Liouville sum". Why? Because the first time I saw this mathematics get used was by Liouville... Ironically to show the existence of Liouville numbers.

## Introduction
This is a draft proof to show that $\zeta(2n-1)\ \ \forall\ \ n\in\mathbb{N}$ are Liouville numbers. To do that I am going to present some identities. First, the Liouville sum (from my other post):
```math
S(f(t),x,N,a)=\sum_{k=a}^x\left[f(k)-f(k+N)\right]=\sum_{k=a}^N\left[f(k)-f(k+x)\right]\ \ (1)
```
and for monotonic f
```math
\lim_{N\to\infty}S(f(t),x,N,a):=\sum_{k=a}^x\left[f(k)\right]\ \ (2)
```
I would also like to give a functional relation; let $f(t,c)=\frac{1}{t^c}\ \ \forall\ \ t\in\mathbb{Q}$. If we have some $p$ and $q$ such that $p,q\in\mathbb{N}$ then we can let $t=k+\frac{p}{q}$ and see
```math
f(k+\frac{p}{q},c)=\frac{1}{(k+\frac{p}{q})^c}=\frac{q^c}{(kq+p)^c}=q^c f(kq+p,c)\ \ (3)
```
The following identity for inifinite summation will also make things easier to read
```math
L=\lim_{N\to\infty}\sum_{k=a}^N\left[f(k)\right]\ \ (4)
```

Now we can begin with the interesting results. 


## Math
Let some $p$ and $q$ exist such that $p,q\in\mathbb{N}$. From $(1)$, let $a=1$ and $x=\frac{p}{q}$, to see
```math
S(f(t,c),\frac{p}{q},N,1)=\sum_{k=1}^N\left[f(k,c)-f(k+\frac{p}{q},c)\right]
```

Introducing a new variable $M$ and subtracting the following expression
```math
\sum_{k=1}^{N}\left[f(k+M,c)\right]
```
and from from both sides gives
```math
S(f(t,c),N,M,1)-\sum_{k=1}^N\left[f(k+\frac{p}{q},c)\right]=S(f(t,c),\frac{p}{q},N,1)-\sum_{k=1}^{N}\left[f(k+M,c)\right]
```
Letting $M\to\infty$ and applying $(2)$ we see
```math
\lim_{M\to\infty}\left\{\sum_{k=1}^M\left[f(k,c)-f(k+N,c)\right]\right\}-\sum_{k=1}^N\left[f(k+\frac{p}{q},c)\right]:=S(f(t,c),\frac{p}{q},N,1)
```
Since the RHS and 
```math
\sum_{k=1}^N\left[f(k+\frac{p}{q},c)\right]
```
are in $\mathbb{Q}$, then 
```math
\lim_{M\to\infty}\left\{\sum_{k=1}^M\left[f(k,c)-f(k+N,c)\right]\right\}
```
must also be in $\mathbb{Q}$, which implies that
```math
\lim_{M\to\infty}\sum_{k=1}^M\left[f(k,c)\right]
```
and
```math
\lim_{M\to\infty}\sum_{k=1}^M\left[f(k+N,c)\right]
```
are algebraically dependent on each other. Continuing on, we can rearrange and write our previous equation in terms of $L$
```math
\lim_{M\to\infty}\sum_{k=1}^M\left[f(k,c),c)\right]-\sum_{k=1}^N\left[f(k+\frac{p}{q},c)\right]=S(f(t,c),\frac{p}{q},N,1)-\lim_{M\to\infty}\sum_{k=1}^M\left[f(k+N,c)\right]
```
```math
L-\sum_{k=1}^N\left[f(k+\frac{p}{q},c)\right]=S(f(t,c),\frac{p}{q},N,1)-\lim_{M\to\infty}\sum_{k=1}^M\left[f(k+N,c)\right]
```
From $(3)$ we can rewrite the LHS sum in terms of some functions $`P(N),Q(N)\in\mathbb{N}`$
```math
\sum_{k=1}^N\left[f(k+\frac{p}{q},c)\right]=q^c\sum_{k=1}^N\left[f(kq+p,c)\right]=\frac{P(N)}{Q(N)}
```
Here we can create a solution for $Q(N)$ by multiplying all the terms of $f(kq+p,c)$ together
```math
\therefore\ \ Q(N)=\Pi_{k=1}^N\left[(kq+p)^c\right]
```
This gives
```math
L-\frac{P(N)}{Q(N)}=S(f(t,c),\frac{p}{q},N,1)-\lim_{M\to\infty}\sum_{k=1}^M\left[f(k+N,c)\right]\ \ (5)
```
Recall Liouville number identity
```math
L-\frac{P(N)}{Q(N)}<\frac{1}{Q(N)^r}
```
From $(5)$ we get the expression
```math
S(f(t,c),\frac{p}{q},N,1)<\frac{1}{Q(N)^r}+\lim_{M\to\infty}\sum_{k=1}^M\left[f(k+N,c)\right]
```
Introducing some variable $W$ that is less than $M$ (it is not infinite) gives
```math
S(f(t,c),\frac{p}{q},N,1)<\frac{1}{Q(N)^r}+\sum_{k=1}^W\left[f(k+N,c)\right]<\frac{1}{Q(N)^r}+\lim_{M\to\infty}\sum_{k=1}^M\left[f(k+N,c)\right]
```
Here we can see a contradiction if we observe the behaviour of this expression as $N\to\infty$; taking the limit of $N\to\infty$ gives
```math
\lim_{N\to\infty}S(f(t,c),\frac{p}{q},N,1)<\lim_{N\to\infty}\frac{1}{Q(N)^r}+\lim_{N\to\infty}\sum_{k=1}^W\left[f(k+N,c)\right]<\lim_{N\to\infty}\frac{1}{Q(N)^r}+\lim_{N\to\infty}\lim_{M\to\infty}\sum_{k=1}^M\left[f(k+N,c)\right]
```
Which reduces to
```math
\sum_{k=1}^N\left[f(k,c)-f(k+\frac{p}{q},c)\right]:=\sum_{k=1}^{\frac{p}{q}}\left[f(k,c)\right]<0<0
```
This implies that, regardless of $p$, $q$ and $r$, if we select a sufficiently large $N$, then there must come a point where the Liouville number identity does not hold (which shows that $L$ is transcendental by Thue–Siegel–Roth theorem). Another result is that the irrationality measure of $L$ must be $\infty$, implying that it is a Liouville number. This concludes the proof.

## Final Statements
I believe that this idea can be used as a basis to show that any infinite sum of a monotonic function is a transcendental/Liouville number (you just have to have a construction for $`Q(N)`$ that grows quickly enough for $`\frac{1}{Q(N)^r}`$ to become negligble). Be safe cuties <3
