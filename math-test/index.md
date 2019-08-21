## インライン数式

```
インライン数式 $E=mc^2$

インライン数式 \\\left(E=mc^2 \\\right)
```

インライン数式 $E=mc^2$

インライン数式 \\ \\left(E=mc^2 \\ \\right)

## ブロック数式

```
$$E=mc^2$$

\[E=mc^2\]
```

$$E=mc^2$$

\\[E=mc^2\\]


\\begin{align}
f(x) &= x^2+3x+2 \\\\
&= (x+1)(x+2)
\\end{align}


<script type="text/x-mathjax-config">
MathJax.Hub.Config({
  // Latexみたいに$...$で囲めばインラインになるようにする
  tex2jax: {
    inlineMath: [['$', '$'], ["\\(", "\\)"]],
    displayMath: [['$$', '$$'], ["\\[", "\\]"]],
    processEscapes: true
  }
});
</script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.2/MathJax.js?config=TeX-AMS_SVG" async></script>
