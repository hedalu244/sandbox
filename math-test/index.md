## インライン数式

```
インライン数式 $E=mc^2$

インライン数式 \\\left(E=mc^2\\\right)
```

インライン数式 $E=mc^2$

インライン数式 \\\\left(E=mc^2\\\\right)

## ブロック数式

```
$$E=mc^2$$

\[E=mc^2\]
```

$$E=mc^2$$

\\[E=mc^2\\]


## 形式意味論

レミウェイの解釈は、レミウェイ文集合から意味集合への全射である。つまり、一つのレミウェイ文が複数の意味に解釈されることはなく、また、レミウェイ文で表せない意味は存在しない。ここで意味とは以下のように構成される集合である。これは単純化した一階述語論理である。

ある集合を$V$とし、$V$の元を **変数記号** と呼ぶ。ある集合を$P$とし、$P$の元を **述語記号** と呼ぶ。$V$や$P$は無限集合でも有限集合でもよい。

$P$を添字集合とする集合族$C$がある。この要素を **格集合** と呼び、格集合の元を **格記号** と呼ぶ。格集合はすべて有限集合である。

述語記号$p$と、$C_p$から変数記号$V$への写像$A$の組$\\left(p, A\\right)$を原子論理式と呼ぶ。原子論理式は`述語記号(格記号:変数記号, 格記号:変数記号...)`という形式で表記する。

**論理式** は以下のように再帰的に定義される。また、各論理式$\\phi$について **自由変数** $F\\left(\\phi\\right) \\left(F\\left(\\phi\\right)\\subset V\\right)$を以下のように定義する。

+ 任意の原子論理式$\\left(p, A\\right)$は論理式であり、$F\\left(\\left(p, A\\right)\\right)$は$A$の値域である。
+ $\\phi$が論理式ならば、$\\left(\\lnot \\phi\\right)$ は論理式であり、$F\\left(\\left(\\lnot \\phi\\right)\\right)=f\\left(\\phi\\right)$である。
+ $\\phi_0$～$\\phi_n$が論理式ならば、$\\left(\\phi_0 \\land \\phi_1 \\land ... \\land \\phi_n\\right)$は論理式であり、$F\\left(\\left(\\phi_0 \\land \\phi_1 \\land ... \\land \\phi_n\\right)\\right)=f\\left(\\phi_0\\right) \\cup f\\left(\\phi_1\\right) \\cup ... \\cup f\\left(\\phi_n\\right)$である。
+ $\\phi$が論理式で $x∈F\\left(\\phi\\right)$ならば、$\\left(\\exists x \\phi\\right)$は論理式であり、$F\\left(\\left(\\exists x \\phi\\right)\\right)$は$f\\left(\\phi\\right)$から$x$を除いた集合 \\left(${v∈f\\left(\\phi\\right)|v≠x}$\\right) である。

論理式$\\phi$のうち、$F\\left(\\phi\\right)$が空集合であるものを、ここでの **意味** とする。

こうして定義した論理式には $\\lor$、$\\Rightarrow$、$\\forall$ などがないが、これらは以下のような同一視をすれば表現できる。

\\[\\left(\\phi \\lor \\psi\\right) → \\lnot\\left(\\lnot\\phi \\land \\lnot\\psi\\right)\\]

\\[\\left(\\phi \\Rightarrow \\psi\\right) → \\lnot\\left(\\phi \\land \\lnot\\psi\\right)\\]

\\[\\left(\\forall x \\phi\\right) → \\left(\\lnot\\left(\\exists x \\lnot\\phi\\right)\\right)\\]

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
