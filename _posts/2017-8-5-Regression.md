---
layout: post
use_math: true
---

Regression is fitting a bunch of data points with a curve.

The data are $xy$-coordinate pairs:

![Data Sample]({{ site.url }}/images/data-sample-notional.jpg){:height="400px" width = "450px"}

The two steps of regression are:
<ol>

<li>  <b>Choose the type of curve</b> we want to fit the data with. </li>

<li>  <b>Find a particular curve</b> of that type that is a closest fit. </li>

</ol>
We will explain these below.

As you might have guessed, there are different types of curves.  Two examples are:

| <b>Linear:</b> $ y_{LIN} = {\bf m} x + {\bf b} $ | <b>Quadratic:</b> $ y_{QUAD} = {\bf a} x^2 + {\bf b} x + {\bf c} $  |
|:---|---:|
|![linear fit]({{ site.url }}/images/data-sample-linear-fit-notional.jpg){:height="300px" width = "400px"} | ![quadratic fit]({{ site.url }}/images/data-sample-quadratic-fit-notional.jpg){:height="300px width = "400px"}|



There are also other types, but we won't need to go into them here.  Choosing the type of curve to fit the data is something of an art that one gets better at with experience.

Each type of curve is defined by the parameters in its formula.  Here are the parameters for linear and quadratic types:

| Curve type | : | Parameters|
|:---|----|:---|
| Linear  | : | slope ${\bf m}$ and $y$-intercept ${\bf b}$ |
| Quadratic: | : | coefficients ${\bf a}, {\bf b}, {\bf c}$, with ${\bf a} \neq 0$ |

Say in Step 1 above, we chose the linear type.  To do Step 2 for this choice, we first write the sum

$$
S({\bf m}, {\bf b}) = 
\big[
({\bf m} \: x_{1} + {\bf b}) - y_{1}
\big]^2 + 
\big[
({\bf m} \: x_{2} + {\bf b}) - y_{2}
\big]^2 + 
\ldots +
\big[
({\bf m} \: x_{n} + {\bf b}) - y_{n}
\big]^2
$$

(This sum measures "how off" the linear fit is for the particular values ${\bf m}, {\bf b}$.) For Step 2, we would then find the line that is a "closest fit."  This means that we would find the values ${\bf m}, {\bf b}$ that minimize the sum $S({\bf m}, {\bf b})$.  The formula for these values is already known and is already programmed into Excel and other software.


If instead of the linear type we chose the quadratic type, we would be minimizing the sum

$$
\begin{array}{lll}
S({\bf a}, {\bf b}, {\bf c}) & = & 
\big[
({\bf a} \: x_{1}^2 + {\bf b}  \: x_{1} + {\bf c}) - y_{1}
\big]^2 \\  
& + &
\big[
({\bf a} \: x_{2}^2 + {\bf b} \: x_{2} + {\bf c}) - y_{2}
\big]^2 \\
& + &
\ldots \\ 
& + &
\big[
({\bf a} \: x_{n}^2 + {\bf b} \: x_{n} + {\bf c}) - y_{n}
\big]^2 \\
\end{array}
$$

with respect to ${\bf a}, {\bf b}, {\bf c}$.  This minimization is also already programmed into Excel and other standard software.
