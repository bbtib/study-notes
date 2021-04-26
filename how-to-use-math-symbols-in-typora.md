This is copy and test page from [official typora doc](https://support.typora.io/Math/)



Typora supports rendering normal mathematics using `Tex/LaTeX` syntax. The rendering process is processed by [`MathJax`](https://www.mathjax.org/).

[TOC]

# Math Block (Display Math)
Math blocks are `LaTeX` expressions wrapped by `$$` mark and line break, for example:

```Markdown
$$
\begin{align*}
y = y(x,t) &= A e^{i\theta} \\
&= A (\cos \theta + i \sin \theta) \\
&= A (\cos(kx - \omega t) + i \sin(kx - \omega t)) \\
&= A\cos(kx - \omega t) + i A\sin(kx - \omega t)  \\
&= A\cos \Big(\frac{2\pi}{\lambda}x - \frac{2\pi v}{\lambda} t \Big) + i A\sin \Big(\frac{2\pi}{\lambda}x - \frac{2\pi v}{\lambda} t \Big)  \\
&= A\cos \frac{2\pi}{\lambda} (x - v t) + i A\sin \frac{2\pi}{\lambda} (x - v t)
\end{align*}
$$
```

will be rendered as
$$
\begin{align*}
y = y(x,t) &= A e^{i\theta} \\
&= A (\cos \theta + i \sin \theta) \\
&= A (\cos(kx - \omega t) + i \sin(kx - \omega t)) \\
&= A\cos(kx - \omega t) + i A\sin(kx - \omega t)  \\
&= A\cos \Big(\frac{2\pi}{\lambda}x - \frac{2\pi v}{\lambda} t \Big) + i A\sin \Big(\frac{2\pi}{\lambda}x - \frac{2\pi v}{\lambda} t \Big)  \\
&= A\cos \frac{2\pi}{\lambda} (x - v t) + i A\sin \frac{2\pi}{\lambda} (x - v t)
\end{align*}
$$


```
x^{2} + 5x + 8 = 0
```
will be rendered as 

$$
x^{2} + 5x + 8 = 0
$$

## Inline Math

First of all, please enable **inline math** feature from preferences panels -> *Markdown* section. Preferences panel can be opened From menu bar: `File` -> `Preferences...`, or use shortcut key — `command`/`ctrl` + `,`. This setting will be applied after Typora restarts.



Inline math use syntax like this `$<Math Expressions>$`, e.g: `$f = \frac{2 \pi}{T}$`.



This is some test $\frac{2 \pi}{T}$ math expression

## TeX Commands available in Typora

You could find the all supported TeX commands in http://docs.mathjax.org/en/v2.6-latest/tex.html#supported-latex-commands.

You could add new commands using `\def` or`\newcommand`. For example:

```
$$
\def\bold#1

\bold{this\ is\ now\ bold}
$$
```

Followings seems not working 
$$
\def\bold#1

\bold{this\ is\ now\ bold}
$$



## Chemistry Expressions

Typora has the built-in [mhchem](https://mhchem.github.io/MathJax-mhchem/) extension, which can be used to render Chemistry Expressions, you could use like this:

```Markdown
$\ce{CH4 + 2 $\left( \ce{O2 + 79/21 N2} \right)$}$
```

Which will be rendered as![img](how-to-use-math-symbols-in-typora.assets/Snip20180815_1.png)

For more details, please refer https://mhchem.github.io/MathJax-mhchem/.

## Auto Numbering

Typora supports auto-numbering math blocks. To turn on this feature, please open preferences panel, and enable “Auto Numbering Math Equations” under the “Markdown” section.

![img](how-to-use-math-symbols-in-typora.assets/Snip20180818_4.png)

## Troubleshooting

### Force Refresh

When Math rendering goes wrong, like output math too wild/narrow, or equation numbering becomes incorrect, you can trigger force refresh for all math from the `Edit` → `Math Tools` menu.

## Limitations

- MathJax supports a limited subsets of all LaTeX commands (references: http://docs.mathjax.org/en/latest/input/tex/macros/index.html).
- Not all export formats support math, and some commands/features of math/LaTeX would become unavailable after export.