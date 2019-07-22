# LATEX


## align and box

$$
\begin{align}
1 \quad
  & p \to q
  & premise\\
2 \quad
  & \bbox[5px,border:1px solid black]{\lnot q}
  & {assumption}\\
3 \quad
  & p\lor q
  & \text{assumption}\\
4 \quad
  & \lnot q \to \lnot p
  & {MT \ 1,2}\\
\end{align}
$$


## array align

$$
\begin{array}{lll}
   1 & R &Premise 1 \\
   2 & S &Premise 2 \\
   \hline
   . & . &.\\
   . & . &.\\
   \hline
   n & Conclusion & Justification \\
\end{array}
$$
