# ITCT Homework 2

* R07944007 網媒碩一 林良翰

## 1. [Prob. 3.1.]

### a. Markov's Inequality

* By the definition of probability

    $E\left[ X \right] =\int _{ -\infty  }^{ \infty  }{ xP\left( x \right) dx } $

* Since r.v. $X$ is non-negative

    $E\left[ X \right] =\int _{ 0 }^{ \infty  }{ xP\left( x \right) dx }$

* By the property of integrals

    $E\left[ X \right] =\int _{ 0 }^{ t }{ xP\left( x \right) dx } +\int _{ t }^{ \infty  }{ xP\left( x \right) dx } \ge \int _{ t }^{ \infty  }{ xP\left( x \right) dx } \ge \int _{ t }^{ \infty  }{ tP\left( x \right) dx } =tP\left( X\ge t \right) $

    Thus

    $P\left( X\ge t \right) \le \frac { E\left[ X \right]  }{ t }$

### b. Chebyshev's Inequality

* By the definition of mean and variance

    * Mean : $\mu =E\left[ Y \right] $
    * Variance : ${ \sigma  }^{ 2 }=E\left[ { \left( Y-E\left[ Y \right]  \right)  }^{ 2 } \right] =E\left[ { \left( Y-\mu  \right)  }^{ 2 } \right] =E\left[ X \right] $

* By Markov's enequality

    $P\left( X\ge { \epsilon  }^{ 2 } \right) \le \frac { E\left[ X \right]  }{ { \epsilon  }^{ 2 } } $

    Thus

    $P\left( { \left| Y-\mu  \right|  }\ge { \epsilon  } \right) =P\left( { \left( Y-\mu  \right)  }^{ 2 }\ge { \epsilon  }^{ 2 } \right) \le \frac { E\left[ { \left( Y-\mu  \right)  }^{ 2 } \right]  }{ { \epsilon  }^{ 2 } } =\frac { { \sigma  }^{ 2 } }{ { \epsilon  }^{ 2 } }$

### c. Weak Law of Large Numbers

* Chebyshev's inequality

    A r.v. $X$ with its mean $E\left(X\right)=\mu$ and variance $Var\left(X\right)=\sigma^2$, for any $\epsilon\ge0$

    $P\left( { \left| X-\mu  \right|  }\ge { \epsilon  } \right) \le \frac { { \sigma  }^{ 2 } }{ { \epsilon  }^{ 2 } }$

    which is same as

    $P\left( { \left| X-E\left( X \right)  \right|  }\ge { \epsilon  } \right) \le \frac { Var\left( X \right)  }{ { \epsilon  }^{ 2 } } ​$

* Find $E\left( { \bar { Z }  }_{ n } \right) $ and $Var\left( { \bar { Z }  }_{ n } \right) $

    * $E\left( { \bar { Z }  }_{ n } \right) =E\left( \frac { 1 }{ n } \sum\limits _{ i=1 }^{ n }{ { Z }_{ i } }  \right) =\frac { 1 }{ n } E\left( \sum\limits _{ i=1 }^{ n }{ { Z }_{ i } }  \right) =\frac { 1 }{ n } \sum\limits _{ i=1 }^{ n }{ E\left( { Z }_{ i } \right)  } =\frac { 1 }{ n } \left( n\mu  \right) =\mu$
    * $Var\left( { \bar { Z }  }_{ n } \right) =Var\left( \frac { 1 }{ n } \sum\limits _{ i=1 }^{ n }{ { Z }_{ i } }  \right) =\frac { 1 }{ { n }^{ 2 } } Var\left( \sum\limits _{ i=1 }^{ n }{ { Z }_{ i } }  \right) =\frac { 1 }{ { n }^{ 2 } } \sum\limits _{ i=1 }^{ n }{ Var\left( { Z }_{ i } \right)  } =\frac { 1 }{ { n }^{ 2 } } \left( n{ \sigma  }^{ 2 } \right) =\frac { { \sigma  }^{ 2 } }{ { n } }$

* Thus, by Chebyshev's inequality and the mean, variance of ${ \bar { Z }  }_{ n }$, for any $\epsilon\ge0$

    $P\left( { \left| { \bar { Z }  }_{ n }-E\left( { \bar { Z }  }_{ n } \right)  \right|  }\ge { \epsilon  } \right) \le \frac { Var\left( { \bar { Z }  }_{ n } \right)  }{ { \epsilon  }^{ 2 } } $

    $\Rightarrow P\left( { \left| { \bar { Z }  }_{ n }-\mu  \right|  }\ge { \epsilon  } \right) \le \frac { { \sigma  }^{ 2 } }{ { n\epsilon  }^{ 2 } }$

## 2. [Prob. 3.4.]

### a.

* By AEP and the property of typical set ${ { A }_{ \epsilon  } }^{ \left( n \right)  }$ with respect to $P\left(X\right)$ which is the set of sequence $\left( { X }_{ 1 },{ X }_{ 2 },\dots ,{ X }_{ n } \right) \in { X }^{ n }$

    ${ 2 }^{ -n\left( H\left( X \right) +\epsilon  \right)  }\le P\left( { X }_{ 1 },{ X }_{ 2 },\dots ,{ X }_{ n } \right) \le { 2 }^{ -n\left( H\left( X \right) -\epsilon  \right)  }​$

* Derive $A^n$
    $\begin{eqnarray} { A }^{ n } & = & \left\{ { x }^{ n }\in { X }^{ n }:\left| -\frac { 1 }{ n } \log { P\left( { x }^{ n } \right)  } -H\left( X \right)  \right| \le \epsilon  \right\}  \\  & = & \left\{ { x }^{ n }\in { X }^{ n }:-\epsilon \le -\frac { 1 }{ n } \log { P\left( { x }^{ n } \right)  } -H\left( X \right) \le \epsilon  \right\}  \\  & = & \left\{ { x }^{ n }\in { X }^{ n }:{ 2 }^{ -n\left( H\left( X \right) +\epsilon  \right)  }\le P\left( { x }^{ n } \right) \le { 2 }^{ -n\left( H\left( X \right) -\epsilon  \right)  } \right\}  \\  & = & { { A }_{ \epsilon  } }^{ \left( n \right)  } \end{eqnarray}$

    $A^n​$ is just the same as typical set

    $P\left\{ { X }^{ n }\in { A }^{ n } \right\} =P\left\{ { X }^{ n }\in { { A }_{ \epsilon  } }^{ \left( n \right)  } \right\} \rightarrow 1-\epsilon $, $\forall \epsilon >0$ as $n \rightarrow \infty$

    Thus, $P\left\{ { X }^{ n }\in { A }^{ n } \right\} \rightarrow 1​$

### b.

* By the strong law of large numbers

    $P\left( \lim\limits _{ n\rightarrow \infty  }{ \frac { 1 }{ n } \sum\limits _{ i=1 }^{ n }{ { X }_{ i } } =\mu  }  \right) =1$

    which can be rewrite as

    $\forall \epsilon >0$, $P\left( \left| \left( \frac { 1 }{ n } \sum\limits _{ i=1 }^{ n }{ { X }_{ i } }  \right) -\mu  \right| \le \epsilon  \right) \rightarrow 1$, as $n\rightarrow \infty $

* ${ B }^{ n }=\left\{ { x }^{ n }\in { X }^{ n }:\left| \left( \frac { 1 }{ n } \sum\limits _{ i=1 }^{ n }{ { X }_{ i } }  \right) -\mu  \right| \le \epsilon  \right\} $

    $P\left\{ { X }^{ n }\in B^{ n } \right\} \rightarrow 1$

* By $P\left\{ { X }^{ n }\in A^{ n } \right\} \rightarrow 1​$, there exists $\epsilon >0​$ and $N_1​$ such that $P\left\{ { X }^{ n }\in A^{ n } \right\} >1-\frac { \epsilon  }{ 2 } ​$ for all $n\gt N_1​$

    By $P\left\{ { X }^{ n }\in B^{ n } \right\} \rightarrow 1$, there exists $\epsilon >0$ and $N_2$ such that $P\left\{ { X }^{ n }\in B^{ n } \right\} >1-\frac { \epsilon  }{ 2 } $ for all $n\gt N_2$

* So, for all $n\gt N=\max\left(N_1,N_2\right)​$ and for any $\epsilon >0​$

    $\begin{eqnarray} P\left\{ { X }^{ n }\in A^{ n }\cap B^{ n } \right\}  & = & P\left\{ { X }^{ n }\in A^{ n } \right\} +P\left\{ { X }^{ n }\in B^{ n } \right\} -P\left\{ { X }^{ n }\in A^{ n }\cup B^{ n } \right\}  \\  & > & 1-\frac { \epsilon  }{ 2 } +1-\frac { \epsilon  }{ 2 } -1 \\  & = & 1-\epsilon  \end{eqnarray}$

    Thus

    $P\left\{ { X }^{ n }\in A^{ n }\cap B^{ n } \right\} \rightarrow 1-\epsilon $, for all $n\gt N$ and for any $\epsilon >0$

### c.

* By the property of probability

    $\sum\limits _{ { x }^{ n }\in A^{ n }\cap B^{ n } }^{  }{ P\left( { x }^{ n } \right)  } \le 1$

* By the property of typical set, for $x^n\in A^n$

    $P\left( { x }^{ n } \right) \ge { 2 }^{ -n\left( H\left( X \right) +\epsilon  \right)  }​$

* Combine above two inequations

    $1\ge \sum\limits _{ { x }^{ n }\in A^{ n }\cap B^{ n } }^{  }{ P\left( { x }^{ n } \right)  } \ge \sum\limits _{ { x }^{ n }\in A^{ n }\cap B^{ n } }^{  }{ { 2 }^{ -n\left( H\left( X \right) +\epsilon  \right)  } } \ge \left| A^{ n }\cap B^{ n } \right| { 2 }^{ -n\left( H\left( X \right) +\epsilon  \right)  }$

    Therefore

    $\left| A^{ n }\cap B^{ n } \right| \le { 2 }^{ n\left( H\left( X \right) +\epsilon  \right)  }$

### d.

* From b.

    $P\left\{ { X }^{ n }\in A^{ n }\cap B^{ n } \right\} \rightarrow 1-\epsilon $, for all $n\gt\max\left(N_1,N_2\right)$ and for any $\epsilon >0$

    Thus, there exists a number $N$ such that $P\left\{ { X }^{ n }\in A^{ n }\cap B^{ n } \right\} \ge \frac { 1 }{ 2 }$, for all $n>N$

* By the property of typical set, for $x^n\in A^n$

    $P\left( { x }^{ n } \right) \le { 2 }^{ -n\left( H\left( X \right) -\epsilon  \right)  }$

* Combine above two inequations

    $\frac { 1 }{ 2 } \le P\left\{ { X }^{ n }\in A^{ n }\cap B^{ n } \right\} =\sum\limits _{ { x }^{ n }\in A^{ n }\cap B^{ n } }^{  }{ P\left( { x }^{ n } \right)  } \le \sum\limits _{ { x }^{ n }\in A^{ n }\cap B^{ n } }^{  }{ { 2 }^{ -n\left( H\left( X \right) -\epsilon  \right)  } } =\left| A^{ n }\cap B^{ n } \right| { 2 }^{ -n\left( H\left( X \right) -\epsilon  \right)  }$

    Therefore

    $\left| A^{ n }\cap B^{ n } \right| \ge \left( \frac { 1 }{ 2 }  \right) { 2 }^{ n\left( H\left( X \right) -\epsilon  \right)  }$

## 3. [Prob. 3.10.]

* Define the notataions

    $\log { x } =\log _{ 2 }{ x } $

    $\ln { x } =\log _{ e }{ x } $

* The volume ${ V }_{ n }=\prod\limits _{ i=1 }^{ n }{ { X }_{ i } } $

    We can derive

    $\log { { { \left( { V }_{ n } \right)  }^{ \frac { 1 }{ n }  } } } =\frac { 1 }{ n } \log { { { \left( { V }_{ n } \right)  } } } =\frac { 1 }{ n } \sum\limits _{ i=1 }^{ n }{ \log { { { \left( X_{ i } \right)  } } }  } $

* By the strong law of large numbers, and $X$ is uniform over $\left[ 0,1 \right] $

    $\frac { 1 }{ n } \sum\limits _{ i=1 }^{ n }{ \log { { { \left( X_{ i } \right)  } } }  } \rightarrow E\left[ \log { { { \left( X \right)  } } }  \right] =\int _{ 0 }^{ 1 }{ \log { { { \left( x \right) dx } } }  } =-\frac { 1 }{ \ln { 2 }  } $

* Finally we can derive $\lim\limits _{ n\rightarrow \infty  }{ { \left( { V }_{ n } \right)  }^{ \frac { 1 }{ n }  } } ​$

    $\lim\limits _{ n\rightarrow \infty  }{ { \left( { V }_{ n } \right)  }^{ \frac { 1 }{ n }  } } ={ e }^{ \lim\limits _{ n\rightarrow \infty  }{ \ln { { \left( { V }_{ n } \right)  }^{ \frac { 1 }{ n }  } }  }  }={ e }^{ \ln { 2 } \left( \lim\limits _{ n\rightarrow \infty  }{ \log { { { \left( { V }_{ n } \right)  }^{ \frac { 1 }{ n }  } } }  }  \right)  }={ e }^{ \ln { 2 } \left( -\frac { 1 }{ \ln { 2 }  }  \right)  }=\frac { 1 }{ e } $

* ${ \left( E\left[ { V }_{ n } \right]  \right)  }^{ \frac { 1 }{ n }  }={ \left( E\left[ \prod\limits _{ i=1 }^{ n }{ { X }_{ i } }  \right]  \right)  }^{ \frac { 1 }{ n }  }={ \left( \prod\limits _{ i=1 }^{ n }{ E\left[ { X }_{ i } \right]  }  \right)  }^{ \frac { 1 }{ n }  }={ \left( { \left( \frac { 1 }{ 2 }  \right)  }^{ n } \right)  }^{ \frac { 1 }{ n }  }=\frac { 1 }{ 2 } \neq \frac { 1 }{ e } ​$

    Thus, the expected edge length does not capture the idea of the volume of the box.

## 4. [Prob. 3.11.]

### a.

* By definition and the property of probability

    $P\left( A \right) >1-{ \epsilon  }_{ 1 }$

    $P\left( B \right) >1-{ \epsilon  }_{ 2 }$

    $P\left( A\cup B \right) \le 1\Rightarrow -P\left( A\cup B \right) \ge -1$

* We can obtain the probablility of the intersection of $A$ and $B$

    $P\left( A\cap B \right) =P\left( A \right) +P\left( B \right) -P\left( A\cup B \right) \ge 1-{ \epsilon  }_{ 1 }+1-{ \epsilon  }_{ 2 }-1=1-{ \epsilon  }_{ 1 }-{ \epsilon  }_{ 2 }$

### b.

* (a) from a.

    $1-\delta -\epsilon \le P\left( { A_{ \epsilon  } }^{ \left( n \right)  }\cap { { B }_{ \delta  } }^{ \left( n \right)  } \right) $

* (b) by the definition of probability of a set

    $P\left( { A_{ \epsilon  } }^{ \left( n \right)  }\cap { { B }_{ \delta  } }^{ \left( n \right)  } \right) =\sum\limits _{ { x }^{ n }\in { A_{ \epsilon  } }^{ \left( n \right)  }\cap { { B }_{ \delta  } }^{ \left( n \right)  } }^{  }{ P\left( { x }^{ n } \right)  } $

* (c) by the property of typical set that $x^n\in { A_{ \epsilon  } }^{ \left( n \right)  }$

    $P\left( { x }^{ n } \right) $ has upper bound ${ 2 }^{ -n\left( H-\epsilon  \right)  }$

    $\sum\limits _{ { x }^{ n }\in { A_{ \epsilon  } }^{ \left( n \right)  }\cap { { B }_{ \delta  } }^{ \left( n \right)  } }^{  }{ P\left( { x }^{ n } \right)  } \le \sum\limits _{ { x }^{ n }\in { A_{ \epsilon  } }^{ \left( n \right)  }\cap { { B }_{ \delta  } }^{ \left( n \right)  } }^{  }{ { 2 }^{ -n\left( H-\epsilon  \right)  } }$

* (d) by the definition of the cardinality of a set

    $\sum\limits _{ { x }^{ n }\in { A_{ \epsilon  } }^{ \left( n \right)  }\cap { { B }_{ \delta  } }^{ \left( n \right)  } }^{  }{ { 2 }^{ -n\left( H-\epsilon  \right)  } } =\left| { A_{ \epsilon  } }^{ \left( n \right)  }\cap { { B }_{ \delta  } }^{ \left( n \right)  } \right| { 2 }^{ -n\left( H-\epsilon  \right)  }$

* (e) by the property that ${ A_{ \epsilon  } }^{ \left( n \right)  }\cap { { B }_{ \delta  } }^{ \left( n \right)  }\subseteq { { B }_{ \delta  } }^{ \left( n \right)  }​$

    $\left| { A_{ \epsilon  } }^{ \left( n \right)  }\cap { { B }_{ \delta  } }^{ \left( n \right)  } \right| { 2 }^{ -n\left( H-\epsilon  \right)  }\le\left| { { B }_{ \delta  } }^{ \left( n \right)  } \right| { 2 }^{ -n\left( H-\epsilon  \right)  }$

### c.

* We apply similar steps in b.

    $\begin{eqnarray} 1-\delta  & \le  & P\left( { { B }_{ \delta  } }^{ \left( n \right)  } \right)  \\  & = & \sum _{ { x }^{ n }\in { { B }_{ \delta  } }^{ \left( n \right)  } }^{  }{ P\left( { x }^{ n } \right)  }  \\  & \le  & \sum _{ { x }^{ n }\in { { B }_{ \delta  } }^{ \left( n \right)  } }^{  }{ { 2 }^{ -n\left( H-\delta  \right)  } }  \\  & = & \left| { { B }_{ \delta  } }^{ \left( n \right)  } \right| { 2 }^{ -n\left( H-\delta  \right)  } \end{eqnarray}$

* Let $\delta^\prime =\delta -\frac { 1 }{ n } \log { \left( 1-\delta  \right)  } >0​$

    Finally we can get

    $\frac { 1 }{ n } \log { \left| { { B }_{ \delta  } }^{ \left( n \right)  } \right|  } \ge H-\delta^\prime ​$

## 5. [Prob. 4.6.]

### a.

* By the chain rule for entropy

    $\begin{eqnarray} \frac { 1 }{ n } H\left( { X }_{ 1 },{ X }_{ 2 },\dots ,{ X }_{ n } \right)  & = & \frac { 1 }{ n } \sum _{ i=1 }^{ n }{ H\left( { X }_{ i }|{ X }_{ i-1 },\dots ,{ X }_{ 1 } \right)  }  \\  & = & \frac { 1 }{ n } \left( H\left( { X }_{ n }|{ X }_{ n-1 },\dots ,{ X }_{ 1 } \right) +\sum _{ i=1 }^{ n-1 }{ H\left( { X }_{ i }|{ X }_{ i-1 },\dots ,{ X }_{ 1 } \right)  }  \right)  \\  & = & \frac { 1 }{ n } \left( H\left( { X }_{ n }|{ X }_{ n-1 },\dots ,{ X }_{ 1 } \right) +H\left( { X }_{ 1 },{ X }_{ 2 },\dots ,{ X }_{ n-1 } \right)  \right)  \end{eqnarray}$

* From stationarity, for all $1\le i\le n​$

    $H\left( { X }_{ n }|{ X }_{ n-1 },\dots ,{ X }_{ 1 } \right) \le H\left( { X }_{ i }|{ X }_{ i-1 },\dots ,{ X }_{ 1 } \right) $

    We can derive

    $H\left( { X }_{ n }|{ X }_{ n-1 },\dots ,{ X }_{ 1 } \right) \le \frac { 1 }{ n-1 } \sum\limits _{ i=1 }^{ n-1 }{ H\left( { X }_{ i }|{ X }_{ i-1 },\dots ,{ X }_{ 1 } \right)  } =\frac { 1 }{ n-1 } H\left( { X }_{ 1 },{ X }_{ 2 },\dots ,{ X }_{ n-1 } \right) $

* Finally we can get

    $\frac { 1 }{ n } H\left( { X }_{ 1 },{ X }_{ 2 },\dots ,{ X }_{ n } \right) \le \frac { 1 }{ n } \left( \frac { 1 }{ n-1 } H\left( { X }_{ 1 },{ X }_{ 2 },\dots ,{ X }_{ n-1 } \right) +H\left( { X }_{ 1 },{ X }_{ 2 },\dots ,{ X }_{ n-1 } \right)  \right) =\frac { 1 }{ n-1 } H\left( { X }_{ 1 },{ X }_{ 2 },\dots ,{ X }_{ n-1 } \right) $

### b.

* By the stationarity, for all $1\le i\le n$

    $H\left( { X }_{ n }|{ X }_{ n-1 },\dots ,{ X }_{ 1 } \right) \le H\left( { X }_{ i }|{ X }_{ i-1 },\dots ,{ X }_{ 1 } \right) $

* Thus we can derive

    $\begin{eqnarray} H\left( { X }_{ n }|{ X }_{ n-1 },\dots ,{ X }_{ 1 } \right)  & = & \frac { 1 }{ n } \sum _{ i=1 }^{ n }{ H\left( { X }_{ n }|{ X }_{ n-1 },\dots ,{ X }_{ 1 } \right)  }  \\  & \le  & \frac { 1 }{ n } \sum _{ i=1 }^{ n }{ H\left( { X }_{ i }|{ X }_{ i-1 },\dots ,{ X }_{ 1 } \right)  }  \\  & = & \frac { 1 }{ n } H\left( { X }_{ 1 },{ X }_{ 2 },\dots ,{ X }_{ n } \right)  \end{eqnarray}$

## 6. [Prob. 4.8.]

* By the definition of entropy and ${ p }_{ 1 }+{ p }_{ 2 }=1$

    $H\left( X \right) =-{ p }_{ 1 }\log { { p }_{ 1 } } -{ p }_{ 2 }\log { { p }_{ 2 } } =-{ p }_{ 1 }\log { { p }_{ 1 } } -\left( 1-{ p }_{ 1 } \right) \log { \left( 1-{ p }_{ 1 } \right)  }$

* Define r.v. $T=\left\{ { t }_{ 1 },{ t }_{ 2 } \right\}$ is the symbol duration of r.v. $X$

    $E\left[ T \right] ={ p }_{ 1 }{ t }_{ 1 }+{ p }_{ 2 }{ t }_{ 2 }={ p }_{ 1 }+2{ p }_{ 2 }=2-{ p }_{ 1 }$

* Define $f\left( { p }_{ 1 } \right)$ is the source entropy per unit time controled by $p_1$

    $f\left( { p }_{ 1 } \right) =\frac { H\left( X \right)  }{ E\left[ T \right]  } =\frac { -{ p }_{ 1 }\log { { p }_{ 1 } } -\left( 1-{ p }_{ 1 } \right) \log { \left( 1-{ p }_{ 1 } \right)  }  }{ 2-{ p }_{ 1 } } $

* Since $f\left(0\right)=f\left(1\right)=0​$, the maximum point occurs between $0<{ p }_{ 1 }<1​$, thus we take 1st derivative of $f​$ and set it to 0 to find optimal $p_1^\star​$ such that $f\left(p_1^\star\right)​$ has maximum

    $\frac { d }{ d{ p }_{ 1 } } \left( \frac { -{ p }_{ 1 }\log { { p }_{ 1 } } -\left( 1-{ p }_{ 1 } \right) \log { \left( 1-{ p }_{ 1 } \right)  }  }{ 2-{ p }_{ 1 } }  \right) =\frac { 1 }{ { \left( 2-{ p }_{ 1 } \right)  }^{ 2 } } \left[ \ln { \left( 1-{ p }_{ 1 } \right) - } 2\ln { { p }_{ 1 } }  \right] =0$

    We can get

    $1-{ p }_{ 1 }={ \left( { p }_{ 1 } \right)  }^{ 2}\Rightarrow{ p }_{ 1 }^\star=-\frac { 1 }{ 2 } \pm \frac { \sqrt { 5 }  }{ 2 } ​$ 

    Since $0<{ p }_{ 1 }<1​$

    ${ p }_{ 1 }^\star=-\frac { 1 }{ 2 } +\frac { \sqrt { 5 }  }{ 2 } $

* Organize the equation

    $\begin{eqnarray} f\left( { p }_{ 1 } \right)  & = & \frac { -{ p }_{ 1 }\log { { p }_{ 1 } } -\left( 1-{ p }_{ 1 } \right) \log { \left( 1-{ p }_{ 1 } \right)  }  }{ 2-{ p }_{ 1 } }  \\  & = & \frac { -{ p }_{ 1 }\log { { p }_{ 1 } } -\left( 1-{ p }_{ 1 } \right) \log { \left( 1-{ p }_{ 1 } \right)  }  }{ 1+\left( 1-{ p }_{ 1 } \right)  }  \\  & = & \frac { -{ p }_{ 1 }\log { { p }_{ 1 } } -{ \left( { p }_{ 1 } \right)  }^{ 2 }\log { { \left( { p }_{ 1 } \right)  }^{ 2 } }  }{ 1+{ \left( { p }_{ 1 } \right)  }^{ 2 } }  \\  & = & \frac { -\left( 1-{ \left( { p }_{ 1 } \right)  }^{ 2 } \right) \log { { p }_{ 1 } } -{ 2\left( { p }_{ 1 } \right)  }^{ 2 }\log { { { p }_{ 1 } } }  }{ 1+{ \left( { p }_{ 1 } \right)  }^{ 2 } }  \\  & = & \frac { -\left( 1+{ \left( { p }_{ 1 } \right)  }^{ 2 } \right) \log { { p }_{ 1 } }  }{ 1+{ \left( { p }_{ 1 } \right)  }^{ 2 } }  \\  & = & -\log { { p }_{ 1 } }  \end{eqnarray}$

    Finally we can get

    $-\log { { p }_{ 1 }^{ \ast  } } =-\log { \left( -\frac { 1 }{ 2 } +\frac { \sqrt { 5 }  }{ 2 }  \right)  } \approx 0.6942$

## 7. [Prob. 4.12.]

### a.

* The dog's walk is 2nd order Markov, because we need the previous 2 position to know the previous position and direction.

* By the chain rule of entropy

    $H\left( { X }_{ 0 },{ X }_{ 1 },\dots ,{ X }_{ n } \right) =\sum\limits _{ i=0 }^{ n }{ H\left( { X }_{ i }|{ X }_{ i-1 },...,{ X }_{ 0 } \right)  } =H\left( { X }_{ 0 } \right) +H\left( { X }_{ 1 }|{ X }_{ 0 } \right) +\sum\limits _{ i=2 }^{ n }{ H\left( { X }_{ i }|{ X }_{ i-1 },...,{ X }_{ 0 } \right)  }$

* The initial position is deterministic $\Rightarrow H\left( { X }_{ 0 } \right) =0$

    The first move is equally likely to positive or negative $\Rightarrow H\left( { X }_{ 1 }|{ X }_{ 0 } \right) =H\left( \frac { 1 }{ 2 } ,\frac { 1 }{ 2 }  \right) =1$

    The rest of the move follow the rule defined by the problem

    $\sum\limits _{ i=2 }^{ n }{ H\left( { X }_{ i }|{ X }_{ i-1 },...,{ X }_{ 0 } \right)  } =\sum\limits _{ i=2 }^{ n }{ H\left( \frac { 1 }{ 10 } ,\frac { 9 }{ 10 }  \right)  } =\left( n-1 \right) H\left( \frac { 1 }{ 10 } ,\frac { 9 }{ 10 }  \right)$

* Thus we have

    $H\left( { X }_{ 0 },{ X }_{ 1 },\dots ,{ X }_{ n } \right) =1+\left( n-1 \right) H\left( \frac { 1 }{ 10 } ,\frac { 9 }{ 10 }  \right)$

### b.

* The entropy rate

    $\frac { H\left( { X }_{ 0 },{ X }_{ 1 },\dots ,{ X }_{ n } \right)  }{ n+1 } =\frac { 1+\left( n-1 \right) H\left( \frac { 1 }{ 10 } ,\frac { 9 }{ 10 }  \right)  }{ n+1 } \rightarrow H\left( \frac { 1 }{ 10 } ,\frac { 9 }{ 10 }  \right)$ as $n\rightarrow \infty $

### c. ?

* Let r.v. $S​$ be the number of steps taken between reversals, we have

    $E\left( S \right) =\sum\limits _{ s=1 }^{ \infty  }{ s{ \left( \frac { 9 }{ 10 }  \right)  }^{ s-1 }\frac { 1 }{ 10 }  } =10$

* Thus the expected number of steps the dog takes before reversing direction is

    $10+1=11$

## 8. [Prob. 4.19.]

* Define r.v. ${ V }_{ n }\in \left\{ 1,2,3,4,5 \right\} ​$ is the vertex position at time $n​$

* Define r.v. ${ X }_{ n }=\begin{bmatrix} P\left( { V }_{ n }=1 \right)  \\ P\left( { V }_{ n }=2 \right)  \\ P\left( { V }_{ n }=3 \right)  \\ P\left( { V }_{ n }=4 \right)  \\ P\left( { V }_{ n }=5 \right)  \end{bmatrix}$ is the vertex position distribution at time $n$

* The state transition matrix $p$

    ${ P }_{ ij }=P\left( { V }_{ n+1 }=j|{ V }_{ n }=i \right) =\begin{bmatrix} 0 & \frac { 1 }{ 3 }  & 0 & \frac { 1 }{ 3 }  & \frac { 1 }{ 3 }  \\ \frac { 1 }{ 3 }  & 0 & \frac { 1 }{ 3 }  & 0 & \frac { 1 }{ 3 }  \\ 0 & \frac { 1 }{ 3 }  & 0 & \frac { 1 }{ 3 }  & \frac { 1 }{ 3 }  \\ \frac { 1 }{ 3 }  & 0 & \frac { 1 }{ 3 }  & 0 & \frac { 1 }{ 3 }  \\ \frac { 1 }{ 4 }  & \frac { 1 }{ 4 }  & \frac { 1 }{ 4 }  & \frac { 1 }{ 4 }  & 0 \end{bmatrix}$

### a.

* The stationary distribution of vertex position ${ X }_{ n }^{ * }$

    ${ X }_{ n }^{ * }=\lim\limits _{ n\rightarrow \infty  }{ { X }_{ n } } ={ \begin{bmatrix} \frac { 3 }{ 16 }  & \frac { 3 }{ 16 }  & \frac { 3 }{ 16 }  & \frac { 3 }{ 16 }  & \frac { 4 }{ 16 }  \end{bmatrix} }^{ T }$ such that ${ X }_{ n }^{ * }={ P }_{ ij }\cdot { X }_{ n }^{ * }$

### b.

* By the definition of entropy rate

    $H\left( X \right) =\lim\limits _{ n\rightarrow \infty  }{ \frac { 1 }{ n } H\left( { X }_{ 1 },{ X }_{ 2 },\dots ,{ X }_{ n } \right)  } $

* Since $X_n​$ is a stationary process and it's also a Markov chain

    $H\left( X \right) =H^\prime \left( X \right) =\lim\limits _{ n\rightarrow \infty  }{ H\left( { X }_{ n }|{ X }_{ n-1 },\dots ,{ X }_{ 0 } \right)  } =H\left( { X }_{ 1 }|{ X }_{ 0 } \right) $

    $H\left( { X }_{ 1 }|{ X }_{ 0 } \right) =-\sum\limits _{ i=1 }^{ 5 }{ \left( P\left( { V }_{ 0 }=i \right) \sum\limits _{ j=1 }^{ 5 }{ P\left( { V }_{ 1 }=j|{ V }_{ 0 }=i \right) \log { P\left( { V }_{ 1 }=j|{ V }_{ 0 }=i \right)  }  }  \right)  } =4\cdot \frac { 3 }{ 16 } \log { 3 } +\frac { 4 }{ 16 } \log { 4 }$

### c.

* By the definition of mutual information

    $\begin{eqnarray} I\left( { X }_{ n+1 };{ X }_{ n } \right)  & = & H\left( { X }_{ n+1 } \right) -H\left( { X }_{ n+1 }|{ X }_{ n } \right)  \\  & = & H\left( { X }_{ n+1 } \right) -H\left( { X }_{ 1 }|{ X }_{ 0 } \right)  \\  & = & \left[ 4\cdot \frac { 3 }{ 16 } \log { \frac { 16 }{ 3 }  } +\frac { 4 }{ 16 } \log { \frac { 16 }{ 4 }  }  \right] -\left[ 4\cdot \frac { 3 }{ 16 } \log { 3 } +\frac { 4 }{ 16 } \log { 4 }  \right]  \\  & = & \frac { 3 }{ 4 } \log { \frac { 16 }{ 9 }  }  \end{eqnarray}$

## 9.

* Define the notation

    $X\in \left\{ a,b,c \right\} $

    $Y\in \left\{ { a }^{ \prime  },{ b }^{ \prime  },{ c }^{ \prime  } \right\} $

    and we have the following equation

    $\bar { P } +2\bar { Q } =1$

* By the definition of channel capacity

    $C=\max\limits _{ { P }_{ X } }{ I\left( X;Y \right)  } $

* Find the formula of mutual information

    $\begin{eqnarray} I\left( X;Y \right)  & = & H\left( X \right) -H\left( Y|X \right)  \\  & = & -\bar { P } \ln { \bar { P }  } -2\bar { Q } \ln { \bar { Q }  } -\left[ -\sum _{ x\in X }^{  }{ \sum _{ y\in Y }^{  }{ P\left( X=x,Y=y \right) \ln { P\left( X=x|Y=y \right)  }  }  }  \right]  \\  & = & -\bar { P } \ln { \bar { P }  } -2\bar { Q } \ln { \bar { Q }  } +2\bar { Q } q\ln { q } +2\bar { Q } \left( 1-q \right) \ln { \left( 1-q \right)  }  \\  & = & -\left( 1-2\bar { Q }  \right) \ln { \left( 1-2\bar { Q }  \right)  } -2\bar { Q } \ln { \bar { Q }  } +2\bar { Q } q\ln { q } +2\bar { Q } \left( 1-q \right) \ln { \left( 1-q \right)  }  \end{eqnarray}$

* To find the maximum value, we take 1st derivative of mutual information with $\bar{Q}$ and set it to 0

    $\begin{eqnarray} \frac { dI\left( X;Y \right)  }{ d\bar { Q }  }  & = & \frac { d\left[ -\left( 1-2\bar { Q }  \right) \ln { \left( 1-2\bar { Q }  \right)  } -2\bar { Q } \ln { \bar { Q }  } +2\bar { Q } q\ln { q } +2\bar { Q } \left( 1-q \right) \ln { \left( 1-q \right)  }  \right]  }{ d\bar { Q }  }  \\  & = & 2\ln { \left( 1-2\bar { Q }  \right)  } -2\ln { \bar { Q }  } +2\left[ q\ln { q } +\left( 1-q \right) \ln { \left( 1-q \right)  }  \right] =0 \end{eqnarray}$

    Let $\alpha ={ q }^{ q }{ \left( 1-q \right)  }^{ \left( 1-q \right)  }$

    The optimal ${ \bar { Q }  }^{ * }=\frac { \alpha  }{ 1+2\alpha  } ​$

* Set $\bar{Q}={ \bar { Q }  }^{ * }$

    $\begin{eqnarray} { I }_{ { \bar { Q }  }^{ * } }\left( X;Y \right)  & = & -\left( 1-2{ \bar { Q }  }^{ * } \right) \ln { \left( 1-2{ \bar { Q }  }^{ * } \right)  } -2{ \bar { Q }  }^{ * }\ln { { \bar { Q }  }^{ * } } +2{ \bar { Q }  }^{ * }q\ln { q } +2{ \bar { Q }  }^{ * }\left( 1-q \right) \ln { \left( 1-q \right)  }  \\  & = & -\left( 1-2\frac { \alpha  }{ 1+2\alpha  }  \right) \ln { \left( 1-2\frac { \alpha  }{ 1+2\alpha  }  \right)  } -2\frac { \alpha  }{ 1+2\alpha  } \ln { \frac { \alpha  }{ 1+2\alpha  }  } +2\frac { \alpha  }{ 1+2\alpha  } q\ln { q } +2\frac { \alpha  }{ 1+2\alpha  } \left( 1-q \right) \ln { \left( 1-q \right)  }  \\  & = & \ln { \left( 1+2\alpha  \right)  }  \\  & = & \ln { \left( 1+2{ q }^{ q }{ \left( 1-q \right)  }^{ \left( 1-q \right)  } \right)  }  \end{eqnarray}​$

## 10.

### a.

* $P\left( { y }_{ 0 } \right) =P\left( { x }_{ 0 },{ y }_{ 0 } \right) +P\left( { x }_{ 1 },{ y }_{ 0 } \right) =\frac { 1 }{ 2 } \frac { 99 }{ 100 } +\frac { 1 }{ 2 } \frac { 1 }{ 100 } =\frac { 1 }{ 2 } $
* $P\left( { y }_{ 1 } \right) =P\left( { x }_{ 0 },{ y }_{ 1 } \right) +P\left( { x }_{ 1 },{ y }_{ 1 } \right) =\frac { 1 }{ 2 } \frac { 1 }{ 100 } +\frac { 1 }{ 2 } \frac { 99 }{ 100 } =\frac { 1 }{ 2 } $

### b.

* $H\left( Y \right) =\frac { 1 }{ 2 } \log { 2 } +\frac { 1 }{ 2 } \log { 2 } =1$

### c.

* By the definition of mutual information

    $\begin{eqnarray} I\left( X;Y \right)  & = & H\left( X \right) -H\left( Y|X \right)  \\  & = & 1-\left[ \frac { 1 }{ 2 } \frac { 99 }{ 100 } \log { \frac { 100 }{ 99 }  } +\frac { 1 }{ 2 } \frac { 1 }{ 100 } \log { \frac { 100 }{ 1 }  } +\frac { 1 }{ 2 } \frac { 99 }{ 100 } \log { \frac { 100 }{ 99 }  } +\frac { 1 }{ 2 } \frac { 1 }{ 100 } \log { \frac { 100 }{ 1 }  }  \right]  \\  & = & 1-\frac { 99 }{ 100 } \log { \frac { 100 }{ 99 }  } -\frac { 1 }{ 100 } \log { \frac { 100 }{ 1 }  }  \\  & \approx  & 0.9192 \end{eqnarray}$