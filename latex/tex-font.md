# Latex: Fonts



## Font Sizes

`\tiny`
$$\tiny\text{sample πρόγραμμα font size}$$

`\scriptsize`
$$\scriptsize\text{sample πρόγραμμα font size}$$

`\small`
$$\small\text{sample πρόγραμμα font size}$$

`\large`
$$\large\text{sample πρόγραμμα font size}$$

`\Large`
$$\Large\text{sample πρόγραμμα font size 0123456789}$$

`\LARGE`
$$\LARGE\text{sample πρόγραμμα font size 0123456789}$$

`\huge`
$$\huge\text{sample font size 0123456789}$$

`\Huge`
$$\Huge\text{sample font πρόγραμμα 0123456789}$$


## Font Styles

`\texttt`
$$\texttt{sample πρόγραμμα font in the πρόγραμμα 0123456789}$$

`\textrm`
$$\textrm{sample πρόγραμμα font in the πρόγραμμα 0123456789}$$

`\textsf`
$$\textsf{sample πρόγραμμα font in the πρόγραμμα 0123456789}$$

`\textbf`
$$\textbf{sample πρόγραμμα font in the πρόγραμμα 0123456789}$$

`\text`
$$\textit{sample πρόγραμμα font in the πρόγραμμα 0123456789}$$


## Alignment
For equations longer than a line use the multline environment. Insert a double backslash to set a point for the equation to be broken. The first part will be aligned to the left and the second part will be displayed in the next line and aligned to the right.

$$$
\begin{multline}
p(x) = 3x^6 + 14x^5y + 590x^4y^2 + 17x^5y + 19x^3y^3 - 14x^5y +\\
17x^5y + 3x^6 + 14x^5y + 590x^4y^2 + \\
17x^5y + 12x^2y^4 - 12xy^5 + 2y^6 - a^3b^3
\end{multline}
$$$

If there are several equations that you need to align vertically, the align environment will do it.

The ampersand character `&` determines where the equations align:

$$$
\begin{align}
2x - 5y & =  18 \\
3x + 9y & =  -12
\end{align}
$$$

below we arrange the equations in three columns. LaTeX assumes that each equation consists of two parts separated by a `&`; also that each equation is separated from the one before by an `&`.

use `*` to toggle the equation numbering. When numbering is allowed, you can label each row individually.

$$$
\begin{align*}
x&=y           &  w &=z              &  a&=b+c\\
2x&=-y         &  3w&=\frac{1}{2}z   &  a&=b\\
-4 + 5x&=2+y   &  w+2&=-1+w          &  ab&=cb
\end{align*}
$$$


## Fractions
The binomial coefficient is defined by the next expression:

$$$
\binom{n}{k} = \frac{n!}{k!(n-k)!}
$$$


Use `\displaystyle` to turn inline display style into block display style:

When displaying fractions in-line, $$\frac{3x}{2}$$,
you can set a block display style:
$$\displaystyle \frac{3x}{2}$$


Use `\textstyle` for the other way around:

$$$
\small\text{block display style:} \\
f(x)=\frac{P(x)}{Q(x)} \\
\small\text{inline display style:} \\
f(x)=\textstyle\frac{P(x)}{Q(x)}
$$$
