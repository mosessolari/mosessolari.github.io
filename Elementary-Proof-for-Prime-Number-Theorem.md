[March 23, 2024]

# An elementary proof for the prime number theorem (a Gödel numbering approach)

## Introduction
The "prime number theorem" is a mathematic statement on the distribution of prime numbers being logarithmic. It was pondered upon during the times of Gauss (https://archive.org/details/carlfriedrichgu00gausgoog/page/444/mode/2up) and can be stated as follows:

```math
\pi(x)\sim\frac{x}{\ln(x)}
```
```math
where\ \pi(x)\ is\ the\ number\ of\ primes\ from\ 0\to x
```

Using the "fundamental theorem of arithmetic" (which maybe should be more appropriately referred to by its other name - the prime factorization theorem), I will be proving the above statement. According to Wikipedia, the fundamental theorem of arithmetic was first posed by Kamāl al-Dīn al-Fārisī, and in brief terms, asserts that every composite number can be uniquely constructed by multiplying prime numbers together. The following proof relies on a similar thought process behind Kurt Gödel's "Gödel numbering".

<br></br>

## Motivation
It's not like I'm all day stalking everyones proofs or anything, but every proof I have seen for the prime number theorem is ugly as hell bruh. I have this weird notion in my mind that simple questions deserve simple answers, and since the pnt is one of those problems that has historically had some controversy in regards to having a "simple" answer, I decided to write my own proof. Also, hopefully, this can help people realise the some of the strengths behind a more "classical" approach/mindset towards mathmetics.

<br></br>

## Math

### Definitions
Before moving onto the proof, first a few definitions must be made. What even is a number? Intuitively we know what the number 12 is, but what really is 12? We know it symbollically as "12" because it is written in base 10, but if we were to write 12 in binary (base 2), then it would be written as "1100". This is the train of thought that provoked our initial question, and with a similar line of reasoning we imagine the following formalisation of some number, $N$:

```math
N(b,d)=\sum_{k=0}^\infty\left[d_{k}b^k\right]
```
```math
where\ b\ is\ the\ base\ that\ the\ number\ is\ being\ represented\ in\ and\ d\ is\ the\ set\ of\ digits\ associated\ with\ said\ representation\ (d_{k} < b)
```

For an example, the number 12 is written as such:

```math
N(10,d)=2*(10^0)+1*(10^1)=2+10=12\qquad where\ d=\left\{2,1,0,0,0,\ldots,0\right\}
```

Using the set of digits, $d$, we can assign a value to $N$ with the function:

```math
G(d)=\sum_{k=0}^\infty\left[p_{k}^{d_{k}}\right]
```
```math
where\ p_{k}\ is\ the\ kth\ prime\ starting\ from\ k=0\ (p_{0}=2,\ p_{1}=3,\ p_{2}=5\ etc)
```

By the fundamental theorem of arithemtic, we can observe that for each combination of values for $b$ and $d$, there are uniquely associated values of $N$ and $G$ (this is a form of Gödel numbering). 

<br></br>

### Proof
The core of this proof is based around the primality of a number's corresponding Gödel number (the $G$ function). Observe that:

```math
G(d)=p_{l}\ \iff \ d_{k}=0\quad\forall\quad k\neq l\ \ and\ \ d_{l}=1
```

This means if we are counting up to $x$ in base $b$, then for some positive integer, $n$, we will have $n$ prime Gödel numbers when $x=b^n$ (i.e. there are exactly $n$ prime Gödel numbers less than $b^n$ counted Gödel numbers). Letting this ratio be $R$, we can observe the prime number theorem: 

```math
R(x)=\frac{b^n}{n}=\frac{x}{\log_{b}(x)}=\frac{x}{\ln(x)}\ln(b)
```

Because every number, $N$, has an associated Gödel number, $G$, then as $x\to\infty$, all numbers will have been counted, creating a 1 to 1 corrolation between the size of the prime numbers and prime Gödel numbers. With this fact in mind, it can be said that the prime-counting function, $\pi(x)$, has the same limit as $R(x)$ when $x\to\infty$.

```math
\therefore R(x)\sim\pi(x)
```

This concludes the proof.
