# ITCT Homework 1

* r07944007 網媒碩一 林良翰

## 1. [Prob. 2.1.]

### a.

* Let r.v. $X​$ be the number of flips required, thus we have $\left\{ x,p(x) \right\} ,\forall x\in X​$.

* Find the formula of $P\left(x\right)$, and let $r$ be the probability of flipping a head.
    $\begin{matrix} x=1 & , & P\left( x=1 \right)  & = & r \\ x=2 & , & P\left( x=2 \right)  & = & \left( 1-r \right) r \\ x=3 & , & P\left( x=3 \right)  & = & { \left( 1-r \right)  }^{ 2 }r \\ \vdots  &  &  & \vdots  &  \\ x=i & , & P\left( x=i \right)  & = & \left( 1-r \right) ^{ n-1 }r \end{matrix}$

* Find the entropy $H\left(X\right)$

    $\begin{matrix} H\left( X \right)  & = & -\sum\limits _{ x\in X }^{  }{ P\left( x \right) \log { P\left( x \right)  }  }  \end{matrix}\\ \begin{matrix} \quad  & = & -\sum\limits  _{ i=1 }^{ \infty  }{ { \left( 1-r \right)  }^{ i-1 }r\log { { \left( 1-r \right)  }^{ i-1 }r }  }  \end{matrix}\\ \begin{matrix} \quad  & = & -\sum\limits  _{ n=0 }^{ \infty  }{ { \left( 1-r \right)  }^{ n }r\log { { \left( 1-r \right)  }^{ n }r }  }  \end{matrix}\\ \begin{matrix} \quad  & = & -\left[ \sum\limits  _{ n=0 }^{ \infty  }{ { n\left( 1-r \right)  }^{ n }r\log { { \left( 1-r \right)  } }  } +\sum\limits   _{ n=0 }^{ \infty  }{ { \left( 1-r \right)  }^{ n }r\log { r }  }  \right]  \end{matrix}\\ \begin{matrix} \quad  & = & -\left[ \frac { 1-r }{ { \left[ 1-\left( 1-r \right)  \right]  }^{ 2 } } r\log { { \left( 1-r \right)  } } +\frac { 1 }{ 1-\left( 1-r \right)  } r\log { r }  \right]  \end{matrix}\\ \begin{matrix} \quad  & = & -\left[ \frac { 1-r }{ r } \log { { \left( 1-r \right)  } } +\log { r }  \right]  \end{matrix}​$

* $\because​$  it is a fair coin $\Rightarrow r=\frac{1}{2}​$

    $H\left(x\right)=-\left[ \log { { \left( \frac { 1 }{ 2 }  \right)  } } +\log { { \left( \frac { 1 }{ 2 }  \right)  } }  \right] =2​$

### b.

* Let r.v. $Y​$ be the number of questions required, thus we have $\left\{ y,p(y) \right\} ,\forall y\in Y​$.

* List the questions

    1st question ($y=1​$): Is $x = 1​$ ? 

    2nd question ($y=2$): If not, is $x=2$ ?

    3rd question ($y=3​$): If not, is $x=3​$ ?

    ...

    n-th question ($y=n$): If not, is $x=n$ ?

    $\Rightarrow p\left(y\right)=p\left(x\right)​$

* The entropy of $Y$ is same as $X$

    $H\left(Y\right)=H\left(X\right)=2$

## 2. [Prob. 2.3.]

* $H\left(p\right)​$ will reach its minimum when only one element of $p​$ is non-zero, with total $n​$ possible cases.

* All possible $p$ that make $H\left(p\right)​$ achieve minimum

    $p=\left[ { p }_{ 1 },\overbrace { 0,\dots ,0 }^{ n-1 }  \right] ,{ p }_{ 1 }>0\\ p=\left[ 0,{ p }_{ 2 },\overbrace { 0,\dots ,0 }^{ n-2 }  \right] ,{ p }_{ 2 }>0\\ \vdots \\ p=\left[ \overbrace { 0,\dots ,0 }^{ n-1 } ,{ p }_{ n } \right] ,{ p }_{ n }>0$

## 3. [Prob. 2.4.]

* (a) uses the chain rule of entropy.
* (b) $\because$ the relation of $x$ and $g\left(x\right)$ is clearly defined by function $g$ $\Rightarrow$ $p\left(g\left(x\right)|x\right)=1$

    $H\left( g\left( X \right) |X \right) =\sum\limits _{ x\in X }^{  }{ \sum\limits _{ g\left( x \right) \in g\left( X \right)  }^{  }{ p\left( g\left( x \right) ,x \right) \log { p\left( g\left( x \right) |x \right)  }  }  } =\sum\limits _{ x\in X }^{  }{ \sum\limits _{ g\left( x \right) \in g\left( X \right)  }^{  }{ p\left( g\left( x \right) ,x \right) \log { 1 }  }  } =0$
* (c) also uses the chain rule of entropy.
* (d) $\because$ entropy always larger or equals to zero: $H\left( X|g\left( X \right)  \right) \ge 0$

## 4. [Prob. 2.5.]

* Assume $p\left( x \right) >0,\forall x\in X​$

* $H\left( { Y }|{ X } \right) =\sum\limits _{ y\in Y }^{  }{ \sum\limits _{ x\in X }^{  }{ p\left( y,x \right) \log { p\left( { y }|{ x } \right)  }  }  } =0​$
    We have two cases

    * Case 1 : $p\left( y,x \right) =0,\forall x\in X,\forall y\in Y$

        $\because p\left( x \right) >0$, we could only assure that $p\left( y,x \right) \ge 0$, so this case couldn't work.

    * Case 2 : $\log { p\left( { y }|{ x } \right)  } =0,\forall x\in X,\forall y\in Y$

        $\forall x\in X,\forall y\in Y,\because \log { p\left( { y }|{ x } \right)  } =0$

        $\Rightarrow p\left( { y }|{ x } \right) =1$

        $ \Rightarrow p\left( { y },{ x } \right) =p\left( { x } \right)$

        $ \Rightarrow y$ is a function of $x$

        $\Rightarrow$ r.v. $Y$ is a function of r.v. ​$X$

* So if $H\left( { Y }|{ X } \right)=0​$, then $Y​$ is a function of $X​$

## 5. [Prob. 2.10.]

### a.

* By the definition of entropy

    $H\left( { X }_{ 1 } \right) =-\sum\limits _{ x\in { X }_{ 1 } }^{  }{ { p }_{ 1 }\left( x \right) \log { { p }_{ 1 }\left( x \right)  }  } ​$
    $H\left( { X }_{ 2 } \right) =-\sum\limits_{ x\in { X }_{ 2 } }^{  }{ { p }_{ 2 }\left( x \right) \log { { p }_{ 2 }\left( x \right)  }  } ​$

* Let $p( \cdot )$ be the probability mass function of r.v. $X$

    $p\left( x \right) =\begin{cases} \alpha p_{ 1 }\left( x \right) , & \forall x\in X_{ 1 } \\ \left( 1-\alpha  \right) p_{ 2 }\left( x \right) , & \forall x\in X_{ 2 } \end{cases}$

* Again, by the definition of entropy

    $H\left( { X } \right) =-\sum\limits _{ x\in { X }_{ 1 }\cup { X }_{ 2 } }^{  }{ { p }\left( x \right) \log { { p }\left( x \right)  }  } ​$
    $\because { X }_{ 1 }\cap { X }_{ 2 }=\phi ​$

    $\Rightarrow -\sum\limits  _{ x\in { X }_{ 1 }\cup { X }_{ 2 } }^{  }{ { p }\left( x \right) \log { { p }\left( x \right)  }  } =-\sum\limits  _{ x\in { X }_{ 1 } }^{  }{ { p }\left( x \right) \log { { p }\left( x \right)  }  } -\sum\limits  _{ x\in { X }_{ 2 } }^{  }{ { p }\left( x \right) \log { { p }\left( x \right)  }  } ​$

    $=-\sum\limits  _{ x\in { X }_{ 1 } }^{  }{ \alpha p_{ 1 }\left( x \right) \log { \alpha p_{ 1 }\left( x \right)  }  } -\sum\limits  _{ x\in { X }_{ 2 } }^{  }{ \left( 1-\alpha  \right) p_{ 2 }\left( x \right) \log { \left( 1-\alpha  \right) p_{ 2 }\left( x \right)  }  } ​$

    $=\alpha H\left( { X }_{ 1 } \right) +\left( 1-\alpha  \right) H\left( { X }_{ 2 } \right) -\log { { \alpha  }^{ \alpha  }{ \left( 1-\alpha  \right)  }^{ \left( 1-\alpha  \right)  } }​$

### b.

* Let $H\left( X \right) =h,\ H\left( { X }_{ 1 } \right) ={ h }_{ 1 },\ H\left( { X }_{ 2 } \right) ={ h }_{ 2 },\ H\left(A\right)=\log { { \alpha  }^{ \alpha  }{ \left( 1-\alpha  \right)  }^{ \left( 1-\alpha  \right)  } } ={ h }_{ \alpha  }$

* $\because h​$ is a concave function, thus it has maximum value. We conduct first derivative test to find it

    $\begin{matrix} \frac { dh }{ d\alpha  }  & = & \frac { d\left( \alpha { h }_{ 1 }+\left( 1-\alpha  \right) { h }_{ 2 }+{ h }_{ \alpha  } \right)  }{ d\alpha  }  \end{matrix}\\ \begin{matrix} \quad  & = & { h }_{ 1 }-{ h }_{ 2 }+\frac { d\log { { \alpha  }^{ \alpha  }{ \left( 1-\alpha  \right)  }^{ \left( 1-\alpha  \right)  } }  }{ d\alpha  }  \end{matrix}\\ \begin{matrix} \quad  & = & { h }_{ 1 }-{ h }_{ 2 }+\log { \frac { 1-\alpha  }{ \alpha  }  } \overset { set }{ = } 0 \end{matrix}$

    Let ${ \alpha  }^{ \ast  }=\frac { 1 }{ 1+{ 2 }^{ -{ h }_{ 1 }+{ h }_{ 2 } } }$ such that $h$ reaches its maximum value

* Now we have the upper bound of $h$

    $\begin{matrix} h & \le  & { \alpha  }^{ \ast  }{ h }_{ 1 }+\left( 1-{ \alpha  }^{ \ast  } \right) { h }_{ 2 }-\log { { { \alpha  }^{ \ast  } }^{ { \alpha  }^{ \ast  } }{ \left( 1-{ \alpha  }^{ \ast  } \right)  }^{ \left( 1-{ \alpha  }^{ \ast  } \right)  } }  \end{matrix}$

    $\begin{matrix} \quad  & = & { \alpha  }^{ \ast  }{ h }_{ 1 }+\left( 1-{ \alpha  }^{ \ast  } \right) { h }_{ 2 }-{ \alpha  }^{ \ast  }\log { { { \alpha  }^{ \ast  } } } -{ \left( 1-{ \alpha  }^{ \ast  } \right)  }\log { { \left( 1-{ \alpha  }^{ \ast  } \right)  } }  \end{matrix}$

    Let $\beta ={ 2 }^{ -{ h }_{ 1 }+{ h }_{ 2 } }$

    $\Rightarrow{ \alpha  }^{ \ast  }=\frac { 1 }{ 1+{ 2 }^{ -{ h }_{ 1 }+{ h }_{ 2 } } } =\frac { 1 }{ 1+\beta  } $

    $\begin{matrix} h & \le  & \frac { 1 }{ 1+\beta  } { h }_{ 1 }+\left( 1-\frac { 1 }{ 1+\beta  }  \right) { h }_{ 2 }-\frac { 1 }{ 1+\beta  } \log { { \frac { 1 }{ 1+\beta  }  } } -{ \left( 1-\frac { 1 }{ 1+\beta  }  \right)  }\log { { \left( 1-\frac { 1 }{ 1+\beta  }  \right)  } }  \end{matrix}$

    $\begin{matrix} \quad  & = & \frac { 1 }{ 1+\beta  } \left( { h }_{ 1 }-{ h }_{ 2 } \right) +{ h }_{ 2 }+\log { \left( 1+\beta  \right)  } -\frac { \beta  }{ 1+\beta  } \left( { -h }_{ 1 }+{ h }_{ 2 } \right)  \end{matrix}$

    $\begin{matrix} \quad  & = & { h }_{ 1 }+\log { \left( 1+\beta  \right)  }  \end{matrix}​$

* Since $n^x$ is strictly increasing when $n\gt 1,\ \forall x \in \R$

    $\begin{matrix} { { 2 }^{ h } } & \le  & { 2 }^{ { h }_{ 1 }+\log { \left( 1+\beta  \right)  }  } \end{matrix}$

    $\begin{matrix} { \quad  } & = & { 2 }^{ { h }_{ 1 } }\times { 2 }^{ \log { \left( 1+\beta  \right)  }  } \end{matrix}$

    $\begin{matrix} { \quad  } & = & { 2 }^{ { h }_{ 1 } }\left( 1+\beta  \right) ={ 2 }^{ { h }_{ 1 } }+\beta { 2 }^{ { h }_{ 1 } } \end{matrix}$

    $\begin{matrix} { \quad  } & = & { 2 }^{ { h }_{ 1 } }+{ 2 }^{ -{ h }_{ 1 }+{ h }_{ 2 }+{ h }_{ 1 } } \end{matrix}$

    $\begin{matrix} { \quad  } & = & { 2 }^{ { h }_{ 1 } }+{ 2 }^{ { h }_{ 2 } } \end{matrix}$

* Finally,

    $\begin{matrix} { { 2 }^{ H\left( X \right)  } } & \le & { 2 }^{ H\left( { X }_{ 1 } \right)  }+{ 2 }^{ H\left( { X }_{ 2 } \right)  } \end{matrix}$

## 6. [Prob. 2.12.]

### a. 

- $H\left( X \right) =-\sum\limits _{ x\in X }^{  }{ p\left( x \right) \log { p\left( x \right)  }  } =-p\left( X=0 \right) \log { p\left( X=0 \right)  } -p\left( X=1 \right) \log { p\left( X=1 \right)  } =-\frac { 2 }{ 3 } +\log { 3 }​$
- $H\left( Y \right) =-\sum\limits_{ y\in Y }^{  }{ p\left( y \right) \log { p\left( y \right)  }  } =-p\left( Y=0 \right) \log { p\left( Y=0 \right)  } -p\left( Y=1 \right) \log { p\left( Y=1 \right)  } =-\frac { 2 }{ 3 } +\log { 3 }​$

### b.

- $H\left( { X }|{ Y } \right) =-\sum\limits  _{ x\in X }^{  }{ \sum\limits  _{ y\in Y }^{  }{ p\left( x,y \right) \log { p\left( x|y \right)  }  }  } =\frac { 2 }{ 3 } ​$
- $H\left( Y|{ X } \right) =-\sum\limits _{ x\in Y }^{  }{ \sum\limits _{ y\in X }^{  }{ p\left( y,x \right) \log { p\left( y|x \right)  }  }  } =\frac { 2 }{ 3 } $

### c.

- $H\left( X,Y \right) =H\left( X \right) +H\left( { Y }|{ X } \right) =-\frac { 2 }{ 3 } +\log { 3 } +\frac { 2 }{ 3 } =\log { 3 } $

### d.

- $H\left( Y \right) -H\left( Y|{ X } \right) =-\frac { 2 }{ 3 } +\log { 3 } -\frac { 2 }{ 3 } =-\frac { 4 }{ 3 } +\log { 3 } $

### e.

- $I\left( X;Y \right) =H\left( X \right) -H\left( X|{ Y } \right) =H\left( Y \right) -H\left( Y|{ X } \right) =-\frac { 4 }{ 3 } +\log { 3 } $

### f.

<img src="../Information%20Theory%20&%20Coding%20Techniques/imgs/venn.png" width="50%">

## 7. [Prob. 2.16.]

### a.

* By data process inequality

    If $X\rightarrow Y\rightarrow Z$, then $I\left( X;Z \right) \le I\left( X;Y \right) $

    Thus,

    $\begin{matrix} I\left( { X }_{ 1 };{ X }_{ 3 } \right)  & \le  & \left( { X }_{ 1 };{ X }_{ 2 } \right)  \end{matrix}\\ \begin{matrix}  & = & H\left( { X }_{ 2 } \right) -H\left( { X }_{ 2 }|{ X }_{ 1 } \right)  \end{matrix}\\ \begin{matrix}  & \le  & H\left( { X }_{ 2 } \right)  \end{matrix}\\ \begin{matrix}  & \le  & \log { \left| { X }_{ 2 } \right|  }  \end{matrix}\\ \begin{matrix}  & = & \log { k }  \end{matrix}\\ $

### b.

* By a., if $k = 1$, then

    $I\left( { X }_{ 1 };{ X }_{ 3 } \right) \le \log { 1 } =0$

    Because mutual information between two r.v. is always non-negative, therefore

    $I\left( { X }_{ 1 };{ X }_{ 3 } \right) =0 \Rightarrow X_1$ and $X_3$ are independent.

## 8. [Prob. 2.18.]

* List all possibilities of $X$ and $Y$

    * If $y=4$, $x$ has 2 possible cases with probablility ${ \left( \frac { 1 }{ 2 }  \right)  }^{ 4 }$, $P\left(Y=4\right)=\frac{1}{8}$
    * If $y=5$, $x$ has 8 possible cases with probablility ${ \left( \frac { 1 }{ 2 }  \right)  }^{ 5 }$, $P\left(Y=5\right)=\frac{1}{4}$
    * If $y=6$, $x$ has 20 possible cases with probablility ${ \left( \frac { 1 }{ 2 }  \right)  }^{ 6 }$, $P\left(Y=6\right)=\frac{5}{16}$
    * If $y=7$, $x$ has 40 possible cases with probablility ${ \left( \frac { 1 }{ 2 }  \right)  }^{ 7 }$, $P\left(Y=7\right)=\frac{5}{16}$

* $H\left( X \right) =-\sum\limits _{ x\in X }^{  }{ P\left( x \right) \log { P\left( x \right)  }  } =-\left( \frac { 2 }{ { 2 }^{ 4 } } \log { \frac { 1 }{ { 2 }^{ 4 } }  } +\frac { 8 }{ { 2 }^{ 5 } } \log { \frac { 1 }{ { 2 }^{ 5 } }  } +\frac { 20 }{ { 2 }^{ 6 } } \log { \frac { 1 }{ { 2 }^{ 6 } }  } +\frac { 40 }{ { 2 }^{ 7 } } \log { \frac { 1 }{ { 2 }^{ 7 } }  }  \right) =5.8125$

* $H\left( Y \right) =-\sum\limits _{ y\in Y }^{  }{ P\left( y \right) \log { P\left( y \right)  }  } =-\left( \frac { 1 }{ 8 } \log { \frac { 1 }{ 8 }  } +\frac { 1 }{ 4 } \log { \frac { 1 }{ 4 }  } +\frac { 5 }{ 16 } \log { \frac { 5 }{ 16 }  } +\frac { 5 }{ 16 } \log { \frac { 5 }{ 16 }  }  \right) \approx 1.924$

* $\because Y$ is a deterministic function of $X$, $H\left(Y|X\right)=0$

* $\because H\left( X \right) +H\left( Y|X \right) =H\left( X,Y \right) =H\left( Y \right) +H\left( X|Y \right) $

    $\Rightarrow H\left( X|Y \right) =H\left( X \right) +H\left( Y|X \right) -H\left( Y \right) =3.889$

## 9. [Prob. 2.25.]

### a.

* Using definition and venn diagram

    $\begin{matrix}  & I\left( X;Y;Z \right)  \end{matrix}\\ \begin{matrix} \overset { def. }{ = }  & I\left( X;Y \right) -I\left( X;Y|Z \right)  \end{matrix}\\ \begin{matrix} \overset { chain\ rule }{ = }  & I\left( X;Y \right) -\left[ I\left( X;Y,Z \right) -I\left( X;Z \right)  \right]  \end{matrix}\\ \begin{matrix} \overset { venn. }{ = }  & I\left( X;Y \right) +I\left( X;Z \right) -\left[ H\left( X \right) +H\left( Y,Z \right) -H\left( X,Y,Z \right)  \right]  \end{matrix}\\ \begin{matrix} \overset { def. }{ = }  & I\left( X;Y \right) +I\left( X;Z \right) -\left[ H\left( X \right) +H\left( Y,Z \right) -H\left( X,Y,Z \right)  \right]  \end{matrix}\\ \begin{matrix} \overset { def. }{ = }  & I\left( X;Y \right) +I\left( X;Z \right) -\left[ H\left( X \right) +H\left( Y \right) +H\left( Z \right) -I\left( Y;Z \right) -H\left( X,Y,Z \right)  \right]  \end{matrix}\\ \begin{matrix} = & I\left( X;Y \right) +I\left( X;Z \right) +I\left( Y;Z \right) -H\left( X \right) -H\left( Y \right) -H\left( Z \right) +H\left( X,Y,Z \right)  \end{matrix}$

### b.

- Using the properties

    $\begin{cases} I\left( X;Y \right) =H\left( X \right) +H\left( Y \right) -H\left( X,Y \right)  \\ I\left( Y;Z \right) =H\left( Y \right) +H\left( Z \right) -H\left( Y,Z \right)  \\ I\left( Z;X \right) =H\left( Z \right) +H\left( X \right) -H\left( Z,X \right)  \end{cases}$

    We can get

    $\begin{matrix}  & I\left( X;Y \right) +I\left( X;Z \right) +I\left( Y;Z \right) -H\left( X \right) -H\left( Y \right) -H\left( Z \right) +H\left( X,Y,Z \right)  \end{matrix}\\ \begin{matrix} = & H\left( X \right) +H\left( Y \right) +H\left( Z \right) -H\left( X,Y \right) -H\left( Y,Z \right) -H\left( Z,X \right) +H\left( X,Y,Z \right)  \end{matrix}$

- By a. and b., we can find that $I\left(X,Y,Z\right)​$ is symmetric and not necessary nonnegative.

## 10. [Prob. 2.29.]

### a.

* By the definition of probability

    $p\left( x|z \right) =\frac { p\left( x,z \right)  }{ p\left( z \right)  } \Rightarrow p\left( z \right) =\frac { p\left( x,z \right)  }{ p\left( x|z \right)  } $

    $p\left( x,y|z \right) =\frac { p\left( x,y,z \right)  }{ p\left( z \right)  } =\frac { p\left( x,y,z \right)  }{ p\left( x,z \right)  } p\left( x|z \right) =p\left( y|x,z \right) p\left( x|z \right) $

* By the definition of conditional entropy

    $\begin{matrix} H\left( X,Y|Z \right)  & = & -\sum\limits  _{ x\in X }^{  }{ \sum\limits  _{ y\in Y }^{  }{ \sum\limits  _{ z\in Z }^{  }{ p\left( x,y,z \right) \log { p\left( x,y|z \right)  }  }  }  }  \end{matrix}\\ \begin{matrix}  & = & -\sum\limits  _{ x\in X }^{  }{ \sum\limits  _{ y\in Y }^{  }{ \sum\limits  _{ z\in Z }^{  }{ p\left( x,y,z \right) \log { p\left( y|x,z \right) p\left( x|z \right)  }  }  }  }  \end{matrix}\\ \begin{matrix}  & = & -\sum\limits  _{ x\in X }^{  }{ \sum\limits  _{ y\in Y }^{  }{ \sum\limits  _{ z\in Z }^{  }{ p\left( x,y,z \right) \log { p\left( y|x,z \right)  }  }  }  } -\sum\limits  _{ x\in X }^{  }{ \sum\limits  _{ y\in Y }^{  }{ \sum\limits  _{ z\in Z }^{  }{ p\left( x,y,z \right) \log { p\left( x|z \right)  }  }  }  }  \end{matrix}\\ \begin{matrix}  & = & -\sum\limits  _{ x\in X }^{  }{ \sum\limits  _{ y\in Y }^{  }{ \sum\limits  _{ z\in Z }^{  }{ p\left( x,y,z \right) \log { p\left( y|x,z \right)  }  }  }  } -\sum\limits  _{ x\in X }^{  }{ \sum\limits  _{ z\in Z }^{  }{ p\left( x,z \right) \log { p\left( x|z \right)  }  }  }  \end{matrix}\\ \begin{matrix}  & = & H\left( Y|X,Z \right) +H\left( X|Z \right)  \end{matrix}\ge H\left( X|Z \right)​$

* The equality holds when $H\left(Y|X,Z\right)=0$

    (When $Y$ is the function of $X$ and $Z$)

### b.

* By the chain rule of mutual information

    $I\left( X,Y;Z \right) =I\left( X;Z \right) +I\left( Y;Z|X \right) \ge I\left( X;Z \right)$

* The equality holds when $I\left( Y;Z|X \right) =0$

    (When $Y$ and $Z$ are conditionally independent given $X$)

### c.

* By the chain rule for entropy and definition of conditional mutual information

    $H\left( X,Y,Z \right) −H\left( X,Y \right) =H\left( Z|X,Y \right) \\ \begin{matrix} = & H\left( Z|X \right) -I\left( Z;Y|X \right)  \end{matrix}\\ \begin{matrix} \ge  & H\left( Z|X \right)  \end{matrix}\\ \begin{matrix} = & H\left( Z,X \right) -H\left( X \right)  \end{matrix}$

* The equality holds when $I\left( Z;Y|X \right) =0$

    (When $Z$ and $Y$ are conditionally independent given $X$)

### d.

* By the chain rule of mutual information

    $I\left( { X }_{ 1 },\dots { X }_{ n };Y \right) =\sum _{ i=1 }^{ n }{ I\left( { X }_{ i };Y|{ X }_{ i-1 },\dots ,{ X }_{ 1 } \right)  } $

    $\Rightarrow I\left( X,Y;Z \right) =I\left( X;Z \right) +I\left( Y;Z|X \right) =I\left( Y;Z \right) +I\left( X;Z|Y \right) $

    $\Rightarrow I\left( X;Z|Y \right) =I\left( X;Z \right) +I\left( Y;Z|X \right) -I\left( Y;Z \right) $ 

* The equality always hold.

## 11. [Prob. 2.32.]

### a.

* The minimum probability of error estimator

    $\hat { X } \left( y \right) =\begin{cases} \begin{matrix} 1, & y=a \end{matrix} \\ \begin{matrix} 2, & y=b \end{matrix} \\ \begin{matrix} 3, & y=c \end{matrix} \end{cases}$

* The associated $P_e$

    $\begin{matrix}  & { P }_{ e } \end{matrix}\\ \begin{matrix} = & { P\left( \hat { X } \left( Y \right) \neq X \right)  } \end{matrix}\\ \begin{matrix} = & { P\left( \hat { X } \left( Y=a \right) \neq X \right) +P\left( \hat { X } \left( Y=b \right) \neq X \right) +P\left( \hat { X } \left( Y=c \right) \neq X \right)  } \end{matrix}\\ \begin{matrix} = & \frac { 1 }{ 6 } +\frac { 1 }{ 6 } +\frac { 1 }{ 6 }  \end{matrix}\\ \begin{matrix} = & \frac { 1 }{ 2 }  \end{matrix}$

### b.

* Fano's inequality

    $H\left( { P }_{ e } \right) +{ P }_{ e }\log { \left( \left| X \right| -1 \right)  } \ge H\left( X|Y \right) $

* By weakened Fano's inequality

    ${ P }_{ e }\ge \frac { H\left( X|Y \right) -1 }{ \log { \left( \left| X \right|  \right)  }  }​$

    $\begin{matrix}  & H\left( X|Y \right)  \end{matrix}\\ \begin{matrix} = & \sum\limits _{ y=Y }^{  }{ P\left( Y=y \right) H\left( X|Y=y \right)  }  \end{matrix}\\ \begin{matrix} = & -\sum\limits _{ y\in Y }^{  }{ P\left( Y=y \right) \sum\limits _{ x\in X }^{  }{ P\left( X=x|Y=y \right) \log { P\left( X=x|Y=y \right)  }  }  }  \end{matrix}\\ \begin{matrix} = & -\frac { 1 }{ 3 } \left( \frac { 1 }{ 2 } \log { \frac { 1 }{ 2 }  } +\frac { 1 }{ 4 } \log { \frac { 1 }{ 4 }  } +\frac { 1 }{ 4 } \log { \frac { 1 }{ 4 }  }  \right)  \end{matrix}\\ \begin{matrix}  & -\frac { 1 }{ 3 } \left( \frac { 1 }{ 4 } \log { \frac { 1 }{ 4 }  } +\frac { 1 }{ 2 } \log { \frac { 1 }{ 2 }  } +\frac { 1 }{ 4 } \log { \frac { 1 }{ 4 }  }  \right)  \end{matrix}\\ \begin{matrix}  & -\frac { 1 }{ 3 } \left( \frac { 1 }{ 4 } \log { \frac { 1 }{ 4 }  } +\frac { 1 }{ 4 } \log { \frac { 1 }{ 4 }  } +\frac { 1 }{ 2 } \log { \frac { 1 }{ 2 }  }  \right)  \end{matrix}\\ \begin{matrix} = & \frac { 3 }{ 2 }  \end{matrix}$

    $\log { \left| X \right| =\log { 3 }  } $

    ${ P }_{ e }\ge \frac { 1.5-1 }{ \log { 3 }  } \approx 0.316$

## 12. [Prob. 2.35.]

* Calculate $H\left(p\right)​$ and $H\left(q\right)​$

    $\begin{matrix} H\left( p \right)  & = & -\sum\limits _{ x\in X }^{  }{ p\left( x \right) \log { p\left( x \right)  }  }  \end{matrix}\\ \begin{matrix} \quad  & = & -\frac { 1 }{ 2 } \log { \frac { 1 }{ 2 }  } -\frac { 1 }{ 4 } \log { \frac { 1 }{ 4 }  } -\frac { 1 }{ 4 } \log { \frac { 1 }{ 4 }  }  \end{matrix}\\ \begin{matrix} \quad  & = & \frac { 3 }{ 2 }  \end{matrix}$

    $\begin{matrix} H\left( q \right)  & = & -\sum\limits _{ x\in X }^{  }{ q\left( x \right) \log { q\left( x \right)  }  }  \end{matrix}\\ \begin{matrix} \quad  & = & -\frac { 1 }{ 3 } \log { \frac { 1 }{ 3 }  } -\frac { 1 }{ 3 } \log { \frac { 1 }{ 3 }  } -\frac { 1 }{ 3 } \log { \frac { 1 }{ 3 }  }  \end{matrix}\\ \begin{matrix} \quad  & = & \log { 3 }  \end{matrix}​$

* Calculate $D\left( { p }\parallel { q } \right) ​$ and $D\left( { q }\parallel { p } \right) ​$

    $\begin{matrix} D\left( { p }\parallel { q } \right)  & = & \sum _{ x\in X }^{  }{ p\left( x \right) \log { \frac { p\left( x \right)  }{ q\left( x \right)  }  }  }  \end{matrix}\\ \begin{matrix} \quad  & = & \frac { 1 }{ 2 } \log { \frac { \frac { 1 }{ 2 }  }{ \frac { 1 }{ 3 }  }  } +\frac { 1 }{ 4 } \log { \frac { \frac { 1 }{ 4 }  }{ \frac { 1 }{ 3 }  }  } +\frac { 1 }{ 4 } \log { \frac { \frac { 1 }{ 4 }  }{ \frac { 1 }{ 3 }  }  }  \end{matrix}\\ \begin{matrix} \quad  & = & -\frac { 3 }{ 2 } +\log { 3 }  \end{matrix}$

    $\begin{matrix} D\left( { q }\parallel { p } \right)  & = & \sum _{ x\in X }^{  }{ q\left( x \right) \log { \frac { q\left( x \right)  }{ p\left( x \right)  }  }  }  \end{matrix}\\ \begin{matrix} \quad  & = & \frac { 1 }{ 3 } \log { \frac { \frac { 1 }{ 3 }  }{ \frac { 1 }{ 2 }  }  } +\frac { 1 }{ 3 } \log { \frac { \frac { 1 }{ 3 }  }{ \frac { 1 }{ 4 }  }  } +\frac { 1 }{ 3 } \log { \frac { \frac { 1 }{ 3 }  }{ \frac { 1 }{ 4 }  }  }  \end{matrix}\\ \begin{matrix} \quad  & = & \frac { 5 }{ 3 } -\log { 3 }  \end{matrix}$

* Thus,

    $D\left( { p }\parallel { q } \right) \neq D\left( { q }\parallel { p } \right) $