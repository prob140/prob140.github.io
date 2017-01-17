---
layout: page
title: LaTeX Introduction
---

<a href="http://prob140.berkeley.edu/user-redirect/interact?repo=prob140&path=Latex.ipynb" class="button"> Click Here to Launch Interact </a>

# An Introduction to $\LaTeX$ (LaTeX)

Latex is a typesetting language used for formatting equations (and much more) in the scientific communities. LaTeX is used very commonly in higher mathematical and computer science classes and academia. In Stat 140, we'll be using LaTeX to "pretty print" equations and answers for homeworks and labs

## How To Follow This Introduction?

If you're viewing through Jupyter, then you're all set! Otherwise, go ahead and download this notebook [here](/latex.ipynb). This way, you'll be able to follow and modify the examples that we give, as well as test your own. To see the latex behind the math expressions, go ahead and edit that particular cell

## How Do We Use LaTeX?

For the purposes of this introduction, and for Prob 140, we shall use the "math mode" in Latex through markdown cells in Jupyter Notebook. Remember that in order to switch a cell to "markdown mode", simply change the option from "code" $\to$ "Markdown" on the above toolbar.


There are two main ways to enter math mode

    $ You're in Inline Math Mode $

    $$
You're in Centered Math Mode
$$

### Inline Math Mode

We use inline math when we want to put in equations and/or variables in sentences / the natural flow of text. Here's an example of inline math:

    Say you have $x$ cows and $y$ chickens on a farm, and you've counted $100$ legs amongst all the animals. What are $x$ and $y$?

This is what that'll look like:

Say you have $x$ cows and $y$ chickens on a farm, and you've counted $100$ legs amongst all the animals. What are $x$ and $y$?

*Note*: Notice that text while inside math mode are somewhat italicized; don't use math mode to write all your text, leave it just for variables

### Centered Math Mode

We use centered math mode, when there are particular equations that you'd like to highlight, or have stand out. Here's an example.

    $$
1 + 2 + \dots + n = 0.5n(n+1)
$$

This is what that'll look like:

$$
1 + 2 + \ldots + n = 0.5n(n+1)
$$

*Note*: Don't worry about `ldots` yet

## Superscripts and Subscripts

### Superscripts

In order to write superscripts, of the form $x^y$, simply write `$x^y$`


`$ 2^3 = 8$`:

$ 2^3 = 8$

`$ (x+y)^2 = x^2 + 2xy + y^2$`:

$ (x+y)^2 = x^2 + 2xy + y^2$

** Warning: ** Generally, the power can only be one character long; to write more, you must wrap it with braces { } . So for example:

If you forget braces, it'll look like this:

`$2^10 = 1024$`:

$2^10 = 1024$

To fix, simply add braces

`$2^{10} = 1024$`:

$2^{10} = 1024$

### Subscripts

In order to write subscripts, of the form $a_1$, simply use the *underscore character* `_` and write `$a_1$`


`$ 2^3 = 8$`:

$ 2^3 = 8$

`$ (x+y)^2 = x^2 + 2xy + y^2$`:

$ (x+y)^2 = x^2 + 2xy + y^2$

** Warning: ** Just as with the superscript, the subscript can only be one character long; to write more, you must wrap it with braces { }


## Expressions

LaTeX provides commands for writing symbols in your mathematical expressions. In the last example you saw the `\ldots` command; as you saw, this drew the dots like this: $\ldots$.

Here are some examples of such commands

1. `\sum` : $\sum$
2. `\prod` : $\prod$
3. `\infty` : $\infty$
4. `\log`  : $\log$
5. `\int` : $\int$
6. `\alpha` : $\alpha$
7. `\cup` : $\cup$
8. `\cap` : $\cap$
9. `\ldots` : $\ldots$
10. `\pm` : $\pm$
11. `n \choose k` : $n \choose k$

We can use the subscripting and superscripting from the last section with any of these commands as well; it all integrates well. Here's an example from the *Math Prerequisites* worksheet


**1.** Consider the sequence defined by $c_i = i$ for $i = 1, 2, \ldots 10$. What is $\sum_{i=1}^{10} c_i$?



Essentially, all the greek letters have such commands (simply go `\yourgreekletterhere`): These we use a lot; here are some of the common ones we use

1. `\alpha` : $\alpha$
1. `\beta` : $\beta$
1. `\lambda` : $\lambda$
1. `\mu` : $\mu$
1. `\sigma` : $\sigma$
1. `\pi` : $\pi$

Some commands can take arguments (just like in Python). The way you pass in arguments into a command is by using the braces `{}` syntax

    \command{Arg 1}{Arg 2}...

The most common such command you'll use is the `\frac` command, which creates fractions. `\frac` takes in two arguments, the first the numerator, and the second the denominator (`\frac{Numerator}{Denominator}`). Here are some examples

1.
    \frac{10}{4} = \frac{5}{2}

$\frac{10}{4} = \frac{5}{2}$

2.
    \frac{x^2}{x} = x

$\frac{x^2}{x} = x$

Another common command you'll use is the `\sqrt` command, which takes in one argument- the operand. Here's an example

1.
    \sqrt{9} = 3

$\sqrt{9} = 3$


### Example Combining Everything Together

**Question:** Consider a polynomial $ax^2 + bx + c$. For what values of $x$ does this polynomial equal $0$?

**Answer**

`$$x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$`

$$x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$

### Bounds for summations, products, and integrals

For summations, products, and integrals, we often want to define the bounds or limits. In LaTeX, the syntax for the bounds are the same symbols as subscript and superscript.

    \sum_{lower}^{upper}
    \prod_{lower}^{upper}
    \int_{lower}^{upper}

Note that the bounds will appear next to the symbol in inline math mode and around the symbol in centered math mode

    \sum_{i=1}^\infty a_i
Inline:
$\sum_{i=1}^\infty a_i$

Centered:
$$\sum_{i=1}^\infty a_i$$

    \prod_{i=a}^{b} f(i)
$$\prod_{i=1}^{\infty} f(i)$$

    \int_{0}^{1}\frac{1}{x^2}dx
$$\int_{0}^{1}\frac{1}{x^2}dx$$

    \int_{0}^{1}\int_{0}^{1}(x+y)dxdy
$$\int_{0}^{1}\int_{0}^{1}(x+y)dxdy$$

    \lim_{x\to\infty} f(x)
$$\lim_{x\to\infty} f(x)$$


### Align

When manipulating long equations, it is often useful to show the steps in between. The ``align*`` environment provides easy vertical alignment of equations.Let's see an example

    \begin{align*}
        2x + 10 &= -4\\
        2x &= -14\\
        x &= -7
\end{align*}

$$
\begin{align*}
        2x + 10 &= -4\\
        2x &= -14\\
        x &= -7
\end{align*}
$$


    \begin{align*}
    f(x) &= \int_0^1 g(x)dx = \int_0^1 x^2dx\\
    &= \left[x^3\right]_0^1\\
    &= 1^3 - 0^3\\
    &= \boxed{1}
\end{align*}

$$
\begin{align*}
f(x) &= \int_0^1 g(x)dx = \int_0^1 x^2dx\\
&= \left[x^3\right]_0^1\\
&= 1^3 - 0^3\\
&= \boxed{1}
\end{align*}
$$

Note that the block starts with `\begin{align*} and ends with \end{align*}`. Each line ends with `\\` for new line. The character that we want to align is denoted with `&`

    \begin{align*}
    x&=y           &  w &=z              &  a&=b+c\\
    2x&=-y         &  3w&=\frac{1}{2}z   &  a&=b\\
    -4 + 5x&=2+y   &  w+2&=-1+w          &  ab&=cb
\end{align*}

$$\begin{align*}
x&=y           &  w &=z              &  a&=b+c\\
2x&=-y         &  3w&=\frac{1}{2}z   &  a&=b\\
-4 + 5x&=2+y   &  w+2&=-1+w          &  ab&=cb
\end{align*}$$

### Normal Text in Latex

Notice that any normal text is automatically italicized in LaTeX because it usually represents variables. To make text display normally, we can use `\text{}`

For example, `$P(\text{the coin lands heads}) = \frac{1}{2}`$ shows up as

$P(\text{the coin lands heads}) = \frac{1}{2}$

The ability to embed normal text in LaTeX is particularly useful when there are conditions:

    \frac{x^2}{x} = x \text{ if } x \ne 0


$$
\frac{x^2}{x} = x \text{ if } x \ne 0
$$

    f(x)=\begin{cases}
    \lambda e^{-\lambda x} \text{, if }x>0\\
    0 \text{, else}
\end{cases}

$$
f(x)=\begin{cases}
    \lambda e^{-\lambda x} \text{, if }x>0\\
    0 \text{, else}
\end{cases}
$$


### Example (3c)

Let $\{c\}$ and $\{d\}$ be sequences of real numbers such that
$$\sum_{i=1}^{100} c_i = 10$$
$$\sum_{i=1}^{100} d_i = 20$$

What is $\sum_{i=1}^{100} (4c_i - d_i + 5)$?


### Solution



    \begin{align*}
    \sum_{i=1}^{100} (4c_i - d_i + 5) &= \sum_{i=1}^{100} 4c_i + \sum_{i=1}^{100} - d_i + \sum_{i=1}^{100} 5\\
    &= 4 \sum_{i=1}^{100} c_i - \sum_{i=1}^{100}  d_i + \sum_{i=1}^{100} 5\\
    &= 4 (10) - (20) + 5(100)\\
    &= 520
    \end{align*}

$$
\begin{align*}
    \sum_{i=1}^{100} (4c_i - d_i + 5) &= \sum_{i=1}^{100} 4c_i + \sum_{i=1}^{100} - d_i + \sum_{i=1}^{100} 5\\
    &= 4 \sum_{i=1}^{100} c_i - \sum_{i=1}^{100}  d_i + \sum_{i=1}^{100} 5\\
    &= 4 (10) - (20) + 5(100)\\
    &= 520
\end{align*}
$$

## Further Resources

You've made it! These steps outlined above should cover all the LaTeX you need to write solutions. Sometime in your pursuit, you may need some commands or symbols that haven't been listed here. When so, the following resources are here to help

- [Google](https://www.google.com/): This site lets you search for anything, including any LaTeX symbols that you might forget
- [DeTexify](http://detexify.kirelabs.org/classify.html): This site lets you draw a symbol, and will immediately find the corresponding Latex command. Similar apps for iPhone and Android also exist
- [ShareLatex Tutorial](https://www.sharelatex.com/learn/Mathematical_expressions) ShareLaTeX is one of the main online work environments; they have a very simple yet comprehensive tutorial about LaTex. If you'd like to learn more about LaTeX, this is your gateway


## Exploration

The best way to learn and absorb LaTeX is to look at examples and code it yourself. Once you have the above guiding principles down, the rest of LaTeX distills into simply finding the symbol that you were trying to find. In that spirit of exploration, we've given you the source for the *Mathematical Prerequisites* worksheet. Try to understand what each of the symbols are doing, and try writing your solutions and explanations in LaTeX below.

Don't worry about the `underline` command in the later questions: we only use it to print the blank spaces

#### Question 1:
Consider the sequence defined by $c_i =i$, for $i=1, 2, \ldots , 10$.

1. Find $\sum_{i=1}^{10} c_i$.

`\sum_{i=1}^{10} c_i`
2. If possible, find $\sum_{k=1}^{10} c_k$.  If this is not possible,explain why not.

`\sum_{k=1}^{10} c_k`

#### Solution

*Your Answer Here*

#### Question 2

Does the expression
$$
\sum_{n=1}^{10} 2
$$

`\sum_{n=1}^{10} 2`


make sense?  If it does, what is its value?

#### Solution

*Your Answer Here*

#### Question 3

Let $\{c\}$ and $\{d\}$ be sequences of real numbers so
that
$$
\sum_{i=1}^{100} c_i ~=~ 10$$
$$\sum_{j=1}^{100} d_j ~=~ 20
$$
In parts 1-3 find the value of the expression.


1) $\sum_{i=1}^{100} (4c_i + 5)$

2) $\sum_{i=1}^{100} 4c_i ~+~ 5$

3) $\sum_{i=1}^{100} (4c_i - d_i + 5)$

`\sum_{i=1}^{100} (4c_i - d_i + 5)`


4) True or false:
$$
\sum_{i=1}^{100} \sum_{j=1}^{100} (c_i + d_j) ~~=~~
\sum_{i=1}^{100} (c_i + d_i)
$$

`\sum_{i=1}^{100} \sum_{j=1}^{100} (c_i + d_j)  = \sum_{i=1}^{100} (c_i + d_i)`


If you think the identity is true, find the common value of the two
sides. If the identity is false,
can you find the value of either of the sides?


#### Solution

*Your Answer Here*

#### Question 4

Let $0 < p < 1$.  Find simple expressions for

1. $ \sum_{i=0}^{100} p^i $

2. $ \sum_{i=0}^{\infty} p^i $

3. $ \sum_{i=100}^{\infty} p^i $


#### Solution

*Your Answer Here*

#### Question 5

The sum $ \sum_{n=0}^{\infty} \frac{1}{n!} $ can be expressed very
simply.  Find that simple expression and a numerical value.

`\sum_{n=0}^{\infty} \frac{1}{n!}`


#### Solution

*Your Answer Here*

#### Question 6

Repeat the previous exercise for each of the sums

1. $$ \sum_{i=0}^{\infty} \frac{2^i}{i!} $$

` \sum_{i=0}^{\infty} \frac{2^i}{i!} `
2. $$ \sum_{i=0}^{\infty} \frac{2^{3i}}{i!} $$.

`\sum_{i=0}^{\infty} \frac{2^{3i}}{i!}`


If you had trouble with the previous exercise, this one might help.


#### Solution

*Your Answer Here*

#### Question 7

You know that $e^0 = 1$. What we're going
to need, quite often, is an approximation to $e^x$ for a small non-zero number $x$.
A crude approximation is 1 because $x$ is tiny. But you can get a finer approximation
by writing the first two terms in the expansion for $e^x$ and remembering that Taylor
says the rest is small compared to $x$.


1.  Explain why $e^{0.01}$ is roughly $1.01$ and $e^{-0.01}$ is roughly $0.99$.

2. Use your reasoning in part (a) to explain why $\log (1+x)$ is roughly $x$ for small $x$.
In this class, as in much of math, $\log$ is taken to the base $e$.


#### Solution

*Your Answer Here*

#### Question 8

How many different ways are there to arrange six people in a row?

#### Solution

*Your Answer Here*

#### Question 9

A committee consists of 6 women and 4 men.
How many different choices can be made if you want to select

- a Chairperson and an Assistant Chairperson?
- a subcommittee of two people?
- a committee of two men and two women?


#### Solution

*Your Answer Here*

#### Question 10

Let $a$ and $b$ be any two real numbers.
You know that $(a + b)^2 = a^2 + 2ab + b^2$.

1. Analogously, write the following as a sum of four terms: $(a + b)^3$

2. Let $n$ be a non-negative integer. Fill in the blanks:
$$
(a + b)^n ~=~ \sum_{k=\underline{~~}}^{\underline{~~}} \underline{~~~~~} a^k b^{n-k}
$$


`(a + b)^n ~=~ \sum_{k=\underline{~~}}^{\underline{~~}} \underline{~~~~~} a^k b^{n-k}`

#### Solution

*Your Answer Here*

#### Question 11

Calculate the following.

1. $\frac{d}{dx} \log (x^2)$

2. $\frac{d}{dx} xe^{-cx}$ where $c > 0$ is a constant

3. $\int xe^{-cx} dx$ where $c > 0$ is a constant (use part (b) or methods of integration)

4. $\int_0^{\infty} ce^{-cx} dx$ where $c > 0$ is a constant




#### Solution

*Your Answer Here*

#### Question 12

Let $c > 0$ be a constant. $\int_0^x ce^{-cx} dx$ doesn't make sense. Why not?

`\int_0^x ce^{-cx} dx`


#### Solution

*Your Answer Here*

#### Question 13

Calculate $ \int_0^1 \int_0^1 (x+xy+y) dx dy $.

`\int_0^1 \int_0^1 (x+xy+y) dx dy `


#### Solution

*Your Answer Here*

#### Question 14

 Fill in the blanks (it really helps to draw the region of integration):

`\int_0^1 \int_y^1 (x+xy+y) dx dy ~=~ \int_0^1 \int_{\underline{~~}}^{\underline{~~}} (x+xy+y) dy dx`


$$
\int_0^1 \int_y^1 (x+xy+y) dx dy ~=~ \int_0^1 \int_{\underline{~~}}^{\underline{~~}} (x+xy+y) dy dx
$$




#### Solution

*Your Answer Here*