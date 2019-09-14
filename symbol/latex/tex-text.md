# LATEX: Text

## Text rendering

$$
\begin{align}
\text{To prove it by contradiction try and assume}
\end{align}
$$


## Greek

$$
\varGamma\ \ \varDelta \ \ \varTheta \ \ \varLambda
$$



## Colours

`\color{colourspec}` changes the current foreground colour.

It is either:
- HTML named-colour: 
  + black, white
  + aqua, blue, navy, teal,
  + fuchsia, gray, green, lime, maroon,
  + olive, purple, red, silver, yellow
- RGB colour value:     
  + `#rgb` or `#rrggbb`    
  + where rgb or rrggbb is a 3-digit or 6-digit hexadecimal number    
  + `#000000` is black    
  + `#FFFFFF` is white     
  + `#1AC`=`#11AACC` (shorthand)

As an example, 
`$$a { b \color{red} c \color{#0F0} d } e$$` 
will render a, b and e in the default colour (usually black), c in red and d in green.

$$
4 + \color{fuchsia} x + y - \color{blue} z - y \\
a { b \color{red} c \color{#0F0} d } e \\
$$


$$
\color{fuchsia}{\{}
  \color{green}{\{}
    \color{blue}{\{}
      \color{#e5c07b}{\{}
        \color{#d19a66ff}{\{}
          \color{#61afefff}{\{}
            \color{#282c34ff}{\{}
              \color{#d55fdeff}{\{}
                \color{#89ca78ff}{\{}
                  a
                \color{#89ca78ff}{\}}
              \color{#d55fdeff}{\}}
            \color{#282c34ff}{\}}
          \color{#61afefff}{\}}
        \color{#d19a66ff}{\}}
      \color{#e5c07b}{\}}
    \color{blue}{\}}
  \color{green}{\}}
\color{fuchsia}{\}}
$$



$$
\color{fuchsia}{\{ \clubsuit}
  \color{green}{\{ \spadesuit}
    \color{blue}{\{ \clubsuit}
      \color{#e5c07b}{\{ \clubsuit}
        \color{#d19a66ff}{\{ \spadesuit}
          \color{#61afefff}{\{ \clubsuit}
            \color{#282c34ff}{\{ \spadesuit}
              \color{#d55fdeff}{\{ \clubsuit}
                \color{#89ca78ff}{\{ \clubsuit}
                  \quad \clubsuit
                  \spadesuit \quad 
                \color{#89ca78ff}{\}}
              \color{#d55fdeff}{\}}
            \color{#282c34ff}{\}}
          \color{#61afefff}{\}}
        \color{#d19a66ff}{\}}
      \color{#e5c07b}{\}}
    \color{blue}{\}}
  \color{green}{\}}
\color{fuchsia}{\}}
$$
