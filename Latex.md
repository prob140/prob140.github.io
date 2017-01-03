---
layout: page
title: LaTeX Introduction
---

# An Introduction to $\LaTeX$ (LaTeX)

Latex is a typesetting language used for formatting equations (and much more) in the scientific communities. LaTeX is used very commonly in higher mathematical and computer science classes and academia. In Stat 140, we'll be using LaTeX to "pretty print" equations and answers for homeworks and labs

## How To Follow This Introduction?

If you're viewing through Jupyter, then you're all set! Otherwise, go ahead and download this notebook [here](#). This way, you'll be able to follow and modify the examples that we give, as well as test your own. To see the latex behind the math expressions, go ahead and edit that particular cell

## How Do We Use LaTeX?

For the purposes of this introduction, and for Prob 140, we shall use the "math mode" in Latex through markdown cells in Jupyter Notebook. Remember that in order to switch a cell to "markdown mode", simply change the option from "code" $\to$ "Markdown" on the above toolbar.


There are two main ways to enter math mode

    $ You're in Inline Math Mode $
    $$ You're in Centered Math Mode $$

### Inline Math Mode

We use inline math when we want to put in equations and/or variables in sentences / the natural flow of text. Here's an example of inline math:

    Say you have $x$ cows and $y$ chickens on a farm, and you've counted $100$ legs amongst all the animals. What are $x$ and $y$?

This is what that'll look like: 

Say you have $x$ cows and $y$ chickens on a farm, and you've counted $100$ legs amongst all the animals. What are $x$ and $y$?

*Note*: Notice that text while inside math mode are somewhat italicized; don't use math mode to write all your text, leave it just for variables

### Centered Math Mode

We use centered math mode, when there are particular equations that you'd like to highlight, or have stand out. Here's an example.

    $$ 1 + 2 + \dots + n = 0.5n(n+1)$$

This is what that'll look like: 

   $$ 1 + 2 + \ldots + n = 0.5n(n+1)$$

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


## Exploration

The best way to learn and absorb LaTeX is to look at examples and code it yourself. Once you have the above guiding principles down, the rest of LaTeX distills into simply finding the symbol that you were trying to find. In that spirit of exploration, we've given you the source for the *Mathematical Prerequisites* worksheet. Try to understand what each of the symbols are doing, and try writing your solutions and explanations in LaTeX below

#### Question 1: 
Consider the sequence defined by $c_i =i$, for $i=1, 2, \ldots , 10$.

1. Find $\sum_{i=1}^{10} c_i$.
2. If possible, find $\sum_{k=1}^{10} c_k$.  If this is not possible,explain why not.

#### Solution

*Your Answer Here*
