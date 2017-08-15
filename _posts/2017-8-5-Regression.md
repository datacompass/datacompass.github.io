---
layout: post
use_math: true
---

Regression is fitting a bunch of data points with a curve.

The data are $xy$-coordinate pairs:

![Data Sample]({{ site.url }}/images/data-sample-notional.jpg){:height="400px"}

The two steps of regression are:
<ol>

<li>  Choose the type of curve we want to fit the data with. </li>

<li>  Choose a curve of that type that is a closest fit. </li>

</ol>
We will explain these below.

As you might have guessed, there are different types of curves.  Two examples are:

<b>Linear.</b> $ y_{LIN} = mx + b $    ![linear fit]({{ site.url }}/images/data-sample-linear-fit-notional.jpg){:height="300px"}

<b>Quadratic.</b> $ y_{QUAD} = a x^2 + b x + c $     ![quadratic fit]({{ site.url }}/images/data-sample-quadratic-fit-notional.jpg){:height="300px"}



There are also other types, but we won't need to go into them here.  Choosing the type of curve to fit the data is something of an art that one gets better at with experience.

Each type of curve is defined by the parameters in its formula. The parameters of a linear curve $y_{LIN}$ are its slope, $m$, and its $y$-intercept, $b$.  The parameters, of a quadratic curve $y_{QUAD}$ are the coefficients $a, b, c$, with $a$ being nonzero.

Say in Step 1 above, we chose the linear type.  To do Step 2, we would first write the sum

$$
S(m, b) = 
\big[
(m x_{1} + b) - y_{1}
\big]^2 + 
\big[
(m x_{2} + b) - y_{2}
\big]^2 + 
\ldots +
\big[
(m x_{n} + b) - y_{n}
\big]^2
$$

(This sum measures ``how off'' the linear fit is for the particular values $m, b$.) We would find the values $m, b$ that minimize the sum $S(m, b)$.  The formula for these values is already known and is already programmed into Excel and other software.


If, instead of the linear type we chose the quadratic type, we would be minimizing the sum
$$
S(a, b, c) = 
\big[
(a x_{1}^2 + bx_{1} + c) - y_{1}
\big]^2 + 
\big[
(a x_{2}^2 + bx_{2} + c) - y_{2}
\big]^2 + 
\ldots +
\big[
(a x_{n}^2 + bx_{n} + c) - y_{n}
\big]^2
$$
with respect to $a, b, c$.  This minimization is also already programmed into Excel and other standard programs.
