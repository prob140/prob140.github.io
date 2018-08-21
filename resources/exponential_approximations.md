---
layout: page
title: Exponential Approximations
---

![](/resources/exponential.png "Exp, Log, and Two Tangents")


### Exponential Function ###

For all $x$,
$$
e^x ~~ = ~~ \lim_{n \to \infty} \big{(} 1 + \frac{x}{n} \big{)}^n
~~ = ~~ \sum_{k = 0}^\infty \frac{x^k}{k!}
$$
The expansion as a sum implies that 
$$
e^x ~~ \sim ~~ 1 + x ~~~~~~~~ \text{for small } x
$$

You can see this in the figure. Around $x = 0$, the blue graph of $e^x$ and the red graph of $1+x$ are almost indistinguishable.


### Log Function ###
The figure also shows that 
$$
\log(x) ~~ \sim ~~ -1 + x ~~~~~~~~ \text{for } x \text{ near } 1
$$

This approximation is easier to understand if you write $x$ as 1 plus a small increment $w$. The approximation becomes

$$
\log(1 + w) ~~ \sim ~~ w ~~~~~~~~ \text{for small } w
$$

Now you can see the connection between this approximation and the one for the exponential function above. This one follows by taking logs on both sides of the approximation to $e^x$ for small $x$. It doesn't matter whether you refer to the small number as $x$ or $w$. But it does matter that it is small.