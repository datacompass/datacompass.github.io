---
layout: post
use_math: true
---

Regression is fitting a bunch of data points with a curve.

The data are $xy$-coordinate pairs:

![Data Dample]({{ site.url }}/images/data-sample-notional.jpg){:height="500px"}

The two steps of regression are:
<OL>

<LI>  Choose the type of curve we want to fit the data with.

<LI>  Choose a curve of that type that is a closest fit.

</OL>
We will explain these below.


As you might have guessed, there are different types of curves.  Two examples are:


![{\bf Linear.} $y_{\mbox{\small LIN}} = mx + b$ ]({{ site.url }}/images/data-sample-linear-fit-notional.jpg){:height="400px"}


\begin{tabular}{cc}
{\bf Linear.} $y_{\mbox{\small LIN}} = mx + b$ & {\bf Quadratic.} $y_{\mbox{\small QUAD}} = ax^2 + bx + c$ \\
{\includegraphics[scale = 0.35]{data-sample-linear-fit-notional.pdf}} &
{\includegraphics[scale = 0.35]{data-sample-quadratic-fit-notional.pdf}} \\
\end{tabular}

There are also other types, but we won't need to go into them here.  Choosing the type of curve to fit the data is something of an art that one gets better at with experience.

Each type of curve is defined by the parameters in its formula. The parameters of a linear curve $y_{\mbox{\small LIN}}$ are its slope, $m$, and its $y$-intercept, $b$.  The parameters, of a quadratic curve $y_{\mbox{\small QUAD}}$ are the coefficients $a, b, c$, with $a$ being nonzero.

Say in Step 1 above, we chose the linear type.  To do Step 2, we would first write the sum
$$title: "misc"
4
permalink: "/mathjax_test.html"
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
