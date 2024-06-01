# Math Typesetting


Stack has built-in support for math typesetting using [KaTeX](https://katex.org/).

**It&#39;s not enabled by default side-wide,** but you can enable it for individual posts by adding `math: true` to the front matter. Or you can enable it side-wide by adding `math = true` to the `params.article` section in `config.toml`.

## Inline math

This is an inline mathematical expression: $\varphi = \dfrac{1&#43;\sqrt5}{2}= 1.6180339887…$

```markdown
$\varphi = \dfrac{1&#43;\sqrt5}{2}= 1.6180339887…$
```

## Block math

$$
    \varphi = 1&#43;\frac{1} {1&#43;\frac{1} {1&#43;\frac{1} {1&#43;\cdots} } } 
$$

```markdown
$$
    \varphi = 1&#43;\frac{1} {1&#43;\frac{1} {1&#43;\frac{1} {1&#43;\cdots} } } 
$$
```

$$
    f(x) = \int_{-\infty}^\infty\hat f(\xi)\,e^{2 \pi i \xi x}\,d\xi
$$

```markdown
$$
    f(x) = \int_{-\infty}^\infty\hat f(\xi)\,e^{2 \pi i \xi x}\,d\xi
$$
```

---

> 作者: [liyuhang](https://github.com/yuhanglee)  
> URL: https://yuhanglee.github.io/posts/math-typesetting/  

