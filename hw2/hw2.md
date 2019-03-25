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

## 2.





