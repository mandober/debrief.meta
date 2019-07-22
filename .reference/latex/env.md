# Latex: Environments
https://golem.ph.utexas.edu/~distler/blog/itex2MMLcommands.html


## Array env

`\begin{env}…\end{env}`
* where `env` is: `matrix, pmatrix, bmatrix, Bmatrix, vmatrix, Vmatrix, smallmatrix, cases, aligned, gathered, split, array, svg`

Produces an array with 4 columns:

$$
\begin{array}[t]{clrc}
  1 & 2 & 3 & 4 \\
  5 & 6 & 7 & 8 \\
  9 & 10& 11& 12
\end{array}
$$

- col 1: `c`entered
- col 2: `l`eft-aligned
- col 3: `r`ight-aligned
- col 4: `c`entered
- The top line of the array is aligned with the equation axis


As in AMSLaTeX, 
- `\begin{matrix} ... \end{matrix}` is equivalent to
- `\begin{array}{cc...c}...\end{array}`
- except that you don't have to explicitly state the number of columns.


## SVG

`\begin{svg}...\end{svg}` allows you to embed snippets of SVG in itex equations. To assist in Instiki's LaTeX export feature, you can also include a graphicx command:

`\begin{svg} ... \end{svg}`
`\includegraphics[width=...]{foo}`
where foo.pdf is a file containing a PDF version of the graphic. In itex, the `\includegraphics` command is defined as a NOOP, and the SVG is embedded in the MathML output. In Instiki's LaTeX export, the opposite is true: the svg environment is a NOOP, and the `\includegraphics` command is included in the output.


## Array Options

The `\array{}` command allows much finer control over the layout of arrays.

```
\array
\arrayopts
\collayout (=\colalign), \rowalign, \align, \equalcols, \equalrows, \collines, \rowlines, \frame, \padding
\rowopts
\colalign, \rowalign
\cellopts
\colalign, \rowalign, \rowspan, \colspan
```

## Greek Letters

$$
\alpha, \beta, \gamma, \delta, \\
\epsilon, \backepsilon, \varepsilon, \\
\zeta, \eta, \theta, \vartheta, \iota, \kappa, \varkappa, \lambda, \\
\mu, \nu, \xi, \omicron, \pi, \varpi, \rho, \varrho, \sigma, \\
\varsigma, \tau, \upsilon, \phi, \varphi, \chi, \psi, \omega, \\
\Gamma, \Delta, \Theta, \Lambda, \Xi, \Pi, \Sigma, \Upsilon, \Phi, \Psi, \Omega, \\
\digamma, \mho
$$


## Log-like Symbols

$$
\arccos, \arcsin, \arctan, \arg, \cos, \cosh, \cot, \coth, \\
\csc, \deg, \det, \dim, \exp, \gcd, \inf, \hom, \ker, \lg, \\
\lim, \liminf, \limsup, \ln, \log, \max, \min, \\
212 \mod 5 \\
13 \pmod 1 \\
\Pr, \sec, \sin, \sinh, \sup, \tan, \tanh
$$


## Delimiters

$$
(, ), [, ], 
\langle, 
\rangle, 
\lbrace = \{, 
\rbrace = \} \\
\lceil \rceil \\
\lmoustache \rmoustache \\
\lfloor \rfloor \\
\ \\
\uparrow \downarrow \updownarrow \\
\vert = |\\
\Vert = \|\\
/
$$

In TeX, delimiters are non-stretchy, by default. Stretchy delimiters are obtained with `\left<delim>` and `\right<delim>`. Each `\left<delim>` must be matched with a corresponding `\right<delim>`. If you don't want a visible matching delimiter, you can match with the invisible delimiters, `\left.` and `\right.` .

Fixed-size large delimiters are generated with the modifiers:
`\big,\Big,\bigg,\Bigg, \bigl,\Bigl,\biggl,\Biggl`, and 
`\bigr,\Bigr,\biggr,\Biggr`.

For example,
`\Biggr)` generates a very large (3×natural size) right parenthesis;
`\bigl\vert` generates a large (1.2×natural size) left vertical bar.



## Operators

$$
1 \cong 2 \ncong 2 \\
A \dashv C \vdash A \\
M \Vdash C \\
C \vDash D \\
S \nvDash S \\
S \nVDash F \\
D \nvdash D\\
E \Vvdash D
$$


$$
\amalg, \angle, \measuredangle, \sphericalangle, \\
\approx, \approxeq, \thickapprox, \\
\ast, \asymp, \backslash, \because, \between, \bot \\
\boxminus, \boxplus, \boxtimes, \boxdot, \bowtie
\bullet, \cap, \cup, \Cap, \Cup, \cdot, \\
\circledast, \circledcirc, \clubsuit, \curlyvee, \curlywedge, \\
\diamondsuit, \divideontimes, \dotplus, \heartsuit, \spadesuit, \\
\circ, \bigcirc, \\
\ \\
\dagger, \ddagger
\Diamond, \diamond, \div, \equiv, \\
\eqcirc, \neq ( = \ne), \Bumpeq, \bumpeq, \\
\circeq, \doteq, \doteqdot, \fallingdotseq, \risingdotseq, \\
\exists, \nexists, \flat, \forall, \frown, \smallfrown, \\
\ \\
\gt, \ngtr, \gg, \ggg, \geq ( = \ge), \ngeq, \geqq, \ngeqq, \\
\geqslant, \ngeqslant, \eqslantgtr, \gneq, \gneqq, \gnapprox, \\
\ \\
\gnsim, \gtrapprox, \gtrsim, \gtrdot, \gtreqless, \gtreqqless, \\
\gtrless, \gvertneqq, \in, \notin, \ni, \not\ni, \intercal, \\
\ \\
\lhd, \unlhd, \leftthreetimes, \\
\rightthreetimes, \lt, \nless, \ll, \lll, \leq ( = \le), \\
\nleq, \leqq, \nleqq, \leqslant, \nleqslant, \eqslantless, \\
\ \\
\lessapprox, \lessdot, \lesseqgtr, \lesseqqgtr, \lessgtr, \\
\lesssim, \lnapprox, \lneq, \lneqq \\
\ \\
\lnsim, \ltimes, \lvertneqq, \lozenge, \blacklozenge, \\
\mid ( = \shortmid), \nmid, \nshortmid, \models, \multimap, \\
\quad \nabla, \natural, \not, \neg, \odot, \circleddash, \\
\otimes, \oplus, \ominus, \oslash, \parallel, \nparallel, \\
\shortparallel, \nshortparallel, \partial, \\
\perp, \pitchfork, \pm, \mp, \\
prec: \\ 
\prec, \nprec, \precapprox, \\
\precnapprox, \preceq, \npreceq, \preccurlyeq, \curlyeqprec,\\
\precsim, \precnsim, \prime, \backprime, \propto, \varpropto, \\
\ \\
\rhd, \unrhd, \rtimes, \setminus, \smallsetminus, \sharp, \\
\sim, \nsim, \backsim, \simeq, \backsimeq, \thicksim, \\
\smile, \smallsmile, \subset, \subseteq, \\
\nsubseteq, \subseteqq, \nsubseteqq, \subsetneq, \subsetneqq, \\
\varsubsetneq, \varsubsetneqq, \Subset, \succ, \nsucc, \succeq, \\
\nsucceq, \succapprox, \succnapprox, \succcurlyeq, \curlyeqsucc, \\
\succsim, \succnsim, \supset, \supseteq, \nsupseteq, \\
\supseteqq, \supsetneq, \supsetneqq, \varsupsetneq, \\
\varsupsetneqq, \Supset, \square ( = \Box), \blacksquare, \\
\sqcup, \sqcap, \sqsubset, \sqsubseteq, \sqsupset, \sqsupseteq,\\
\star, \bigstar, \therefore, \times, \top, \triangle, \\
\triangledown, \triangleleft, \triangleright, \blacktriangle, \\
\blacktriangledown, \bigtriangleup, \bigtriangledown, \\
\blacktriangleleft, \blacktriangleright, \ntriangleleft, \\
\ntriangleright, \ntrianglelefteq, \ntrianglerighteq, \\
\trianglelefteq, \trianglerighteq, \triangleq, \\
\veebar, \wedge, \barwedge, \doublebarwedge, \wr \\
\vartriangleleft, \vartriangleright, \uplus, \vee \\
\smallsetminus \\
\backslash \\
\setminus
$$


## Symbols
$$
\aleph, \beth, \ell, \hbar, \Im, \imath, \jmath, \\
\eth, \Re, \wp, \infty, \emptyset, \varnothing
$$


## Dots
$$
a \dots b \\
b \cdots c \\
c \ddots d \\
g\ \vdots \ e \\
h \colon d \\
g \ldots f
$$

While ":" is allowed, it doesn't have enough spacing, use \colon


## Large Operators

\bigcup ( = \Union), \bigcap ( = \Intersection), \bigodot, \bigoplus ( = \Oplus), \bigotimes ( = \Otimes), \bigsqcup, \bigsqcap, \biginterleave, \biguplus, \bigwedge ( = \Wedge), \bigvee ( = \Vee), \coprod ( = \coproduct), \prod ( = \product), \sum, \int ( = \integral), \iint ( = \doubleintegral), \iiint ( = \tripleintegral), \iiiint ( = \quadrupleintegral), \oint ( = \conint = \contourintegral)


## Sizes and Styles

```
\displaystyle, 
\textstyle, 
\textsize, 
\scriptsize, 
\scriptscriptsize, 
\mathit, 
\mathbf ( = \boldsymbol), 
\mathrm, 
\mathbb, 
\mathfrak ( = \mathfr), 
\mathcal, 
\mathscr, 
\mathsf, 
\mathtt, 
\text
```

## Spaces

`\ , \, \:`
`\; ( = \thickspace), \quad, \qquad`
`\! ( = \negthinspace), \negmedspace, \negthickspace`
`\phantom, \mathrlap, \mathllap, \mathclap, \space`


$$
space space \\
space \  space\\
space \, space \\
space \: space \\
space \; space \\
space \! space \\
space \thinspace space \\
space \negthinspace space \\
space \negmedspace space \\
space \quad space \\
space \qquad space \\
space \negthickspace space \\
space \phantom 1 space \\
space \space space \\
space space
$$


## Accents

$$
a \bar{A} + \overline B + \underline C + \vec D \\
A \overrightarrow B \overleftarrow C \overleftrightarrow D \\
\underrightarrow E \underleftarrow F \\
\underleftrightarrow E \dot F \\
\ddot E \dddot F A \ddddot B \\
\tilde C \widetilde D \\
A \check B \hat C \widehat D \\
AB \hat C \\
\boxed D \\
$$

## brace

$$
\displaystyle
1 + \overbrace{4+3+5}^{a-ha!} \\
1 + \underbrace{4+3+5}_{a-ha!}
$$


$$
\displaystyle{
  1 + \overbrace{4+3+5}^{a-ha!} \\
  1 + \underbrace{4+3+5}_{a-ha!}
}
$$


## ops

$$
4 \operatorname{plus}{4+3+5}  \\
4 \mathop{exp}{4,3,5}  \\
4 \mathbin {2} {4+3+5}  \\
4 \mathrel {2} {4+3+5}  \\
$$


As in LaTeX, `\sqrt` accepts an optional argument, so that `\sqrt[3]{n+1}` is equivalent to `\root{3}{n+1}`.


## Numbers

In MathML, numbers are represented as, e.g., <mn>127.3</mn>. itex2MML does its best to intelligently parse what's a number and what's not. Unfortunately, conventions for things like decimal markers are very culture-dependent, and incompatibly-so. If you don't like the way itex2MML parses the would-be numbers in your input, you can force it to interpret a certain string as a number, using the `\itexnum{}` command.


## Colours

`\color{colourspec}` changes the current foreground colour. 

colourspec is either
- HTML named-colour:   
aqua, black, blue, fuchsia, gray, green, lime, maroon, navy, olive, purple, red, silver, teal, white, or yellow
- RGB colour value:   
`#rgb` or `#rrggbb`, where rgb or rrggbb is a 3- or 6-digit hexadecimal number. `#000000` is black, `#FFFFFF` is white, and `#1AC`=`#11AACC`.

As an example, `$a { b \color{red} c \color{#0F0} d } e$` will render a, b and e in the default colour (usually black), c in red and d in green.

$$
4 + \color{fuchsia} x + y - \color{blue} z - y \\
a { b \color{red} c \color{#0F0} d } e \\
$$



## Interactivity

`\href{url}{expression}`
Turns a mathematical expression into a clickable link. This makes use of Xlink.

$$
\href{https://en.wikipedia.org/wiki/Radix}{Radix} 
$$

`\statusline{message}{expression}`
Displays the message text in the browser's status-line, when the user hovers his mouse over the mathematical expression. Works in current (but not older versions of) Mozilla/Firefox, or is easily implemented with a touch of Javascript.

`\tooltip{message}{expression}`
Displays the message text as a tooltip, when the user hovers his mouse over the mathematical expression. Also does not work natively in Mozilla/Firefox. Instead, Mozilla/Firefox supports the (nonexistent) title attribute. So, the same Javascript, below, works around the problem.

`\fghilight{colourspec}{expression} ( = \fghighlight)`
`\bghilight{colourspec}{expression} ( = \bghighlight)`
Change the foreground/background colour of an expression when the user hovers over it. Not supported by current browsers, but can be worked-around with little Javascript.

`\toggle{expression1}{expression2}`
Toggle between these two expressions when the user clicks on them.

`\begintoggle{expression1}{expression2}...{expressionN}\endtoggle`
Toggle between these n expressions when the user clicks on them.



## Equation Numbering
While itex2MML, the stream filter, does not provide such facilities, various tools built around it, like the itex2MML MovableType plugin and Maruku provide enhanced features, such as equation-numbering and cross-referencing. $$...$$ produces an unnumbered equation. \[...\] produces a numbered equation.

Optionally, `\[...\]` can contain a label
`\[...\label{foo}...\]`
You can then refer back to this equation by `(eq:foo)` or `\eqref{foo}`.
These are automatically turned into hyperlinks.






$$
x = 
\begin{cases}
  x > 0 : & 4 \\
  x = 0 : & 2 \\
  x < 0 : & 5
\end{cases}
$$


$$
\begin{split}
  1 & 2 & 3 & 4 \\
  5 & 6 & 7 & 8 \\
  9 & 10& 11& 12
\end{split}
$$