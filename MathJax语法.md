title: MathJax语法
date: 2019-09-02 08:27:06
tags: [笔记]
categories: [笔记]
---

## 摘要

记录一下MathJax显示数学公式的语法

<!--more-->

https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference
https://www.cnblogs.com/linxd/p/4955530.html


## 基础语法

### 公式标记与查看公式

用 `$...$` 表示行内公式。如$\sum_{i=0}^n i^2 = \frac{(n^2+n)(2n+1)}{6}$。
用 `$$...$$` 表示行间公式。如$$\sum_{i=0}^n i^2 = \frac{(n^2+n)(2n+1)}{6}$$

### 希腊字母

名称 | 大写 | Tex | 小写 | Tex
:-: | :-: | :-: | :-: | :-:
alpha | $A$ | `A` | $\alpha$ | `\alpha` | 
beta | $B$| `B` | $\beta$ | `\beta` |
gamma | $\Gamma$| `\Gamma` | $\gamma$ | `\gamma` |
delta | $\Delta$| `\Delta` | $\delta$ | `\delta` |
epsilon | $E$| `E` | $\epsilon$ | `\epsilon` |
zeta | $Z$ | `Z` | $\zeta$ | `\zeta` |
eta | $H$ | `H` | $\eta$ | `\eta` |
theta | $\Theta$ | `\Theta` | $\theta$ | `\theta` |
iota | $I$ | `I` | $\iota$ | `\iota` |
kappa | $K$ | `K` | $\kappa$ | `\kappa` |
lambda | $\Lambda$ | `\Lambda` | $\Lambda$ | `\lambda` |
mu | $M$ | `M` | $\mu$ | `\mu` |
nu | $N$ | `N` | $\nu$ | `\nu` |
xi | $\Xi$ | `\Xi` | $\xi$ | `\xi` |
omicron | $O$ | `O` | $\omicron$ | `\omicron` |
pi | $\Pi$ | `\Pi` | $\pi$ | `\pi` |
rho | $P$ | `P` | $\rho$ | `\rho` |
sigma | $\Sigma$ | `\Sigma` | $\sigma$ | `\sigma` |
tau | $T$ | `T` | $\tau$ | `\tau` |
upsilon | $\Upsilon$ | `\Upsilon` | $\upsilon$ | `\upsilon` |
phi | $\Phi$ | `\Phi` | $\phi$ | `\phi` |
chi | $X$ | `X` | $\chi$ | `\chi` |
psi | $\Psi$ | `\Psi` | $\psi$ | `\psi` |
omega | $\Omega$ | `\Omega` | $\omega$ | `\omega` |

### 上标与下标

上标和下标分别使用`^`与`_`，默认情况下，上下标仅对下一个组起作用。一个组即单个字符或者使用｛...｝包裹起来的内容。

也就是说如果使用`10^10`，会得到$10^10$，而`10^{10}`才是$10^{10}$。

同时大括号还能消除二义性，如`x^5^6`将得到一个错误的结果，必须使用大括号界定`^`的结合性。`{x^5}^6`：${x^5}^6$或者`x^{5^6}`：$x^{5^6}$。

### 括号

小括号和中括号用原始的即可。大括号因为用来分组，因此需要使用`\{`和`\}`表示大括号。也可以使用`\lbrace`和`\rbrace`。

尖括号使用`\langle`和`\rangle`表示，如`\langle x \rangle`：$\langle x \rangle$。

上取整：使用`\lceil`和`\rceil`表示。如`\lceil x \rceil`：$\lceil x \rceil$

下取整：使用`\lfloor`和`\rfloor`表示。如`\lfloor x \rfloor`：$\lfloor x \rfloor$

不可见括号：使用.表示

原始符号并不会随着公式大小缩放，可以使用`\left(...\right)`来自适应的调整括号大小。

比如`\lbrace\sum_{i=0}^0 i^2 = \frac{(n^2+n)(2n+2)}{6}\rbrace\tag{1.1}`，显示出来$$\lbrace\sum_{i=0}^0 i^2 = \frac{(n^2+n)(2n+2)}{6}\rbrace\tag{1.1}$$

以及`\left\lbrace\sum_{i=0}^0 i^2 = \frac{(n^2+n)(2n+2)}{6}\right\rbrace\tag{1.2}`，显示出来$$\left\lbrace\sum_{i=0}^0 i^2 = \frac{(n^2+n)(2n+2)}{6}\right\rbrace\tag{1.2}$$

可以看到第二个公式中的括号是经过缩放的。

### 求和与积分

`\sum`用来表示求和符号，其下标表示求和下限，上标表示上限。如`\sum_1^n`: $\sum_1^n$。

`\int`用来表示积分符号，同样地，其上下标表示积分的上下限。如`\int_1^\infty`: $\int_1^\infty$。

与此类似的符号还有：`\prod`：$\prod$, `\bigcup`：$\bigcup$, `\bigcap`：$\bigcap$, `\iint`：$\iint$。

### 分式和根式

分式的表示：

* 第一种，使用`\frac ab`，`\frac`作用于其后的两个组a，b，结果为$\frac ab$。如果你的分子或分母不是单个字符，请使用{...}来分组。
* 第二种，使用`\over`来分隔一个组的前后两部分，如`{a+1 \over b+1}`：${a+1 \over b+1}$

根式使用`\sqrt`表示，如：`\sqrt[4]{\frac xy}`：$\sqrt[4]{\frac xy}$

### 字体

使用`\mathbb`或`\Bbb`显示黑板粗体字，此字体经常用来表示实数、整数、有理数、复数。如`\mathbb{CHNQRZ}`：$\mathbb{CHNQRZ}$

使用`\mathbf`显示黑体字，使用`\mathtt`显示打印机字体，使用`\mathrm`显示罗马字体，使用`\mathscr`显示手写体，使用`\mathfrak`显示Fraktur字母（一种德国字体）。

### 特殊函数和符号

1. 常见的三角函数，如`\sin x`：$\sin x$，`\arctan_x`：$\arctan_x$，`\lim_{1\to\infty}`：$\lim_{1\to\infty}$。
2. 比较运算符：`\lt`、`\gt`、`\le`、`\ge`、`\neq`：$\lt$ $\gt$ $\le$ $\ge$ $\neq$。可以在这些运算符前面加上`\not`，如`\not\lt`：$\not\lt$。
3. `\times` `\div` `\pm` `\mp`表示：$\times$ $\div$ $\pm$ $\mp$，`\cdot`表示居中的点，`x \cdot y` ：$x \cdot y$
4. 集合关系与运算：\cup \cap \setminus \subset \subseteq \subsetneq \supset \in \notin \emptyset \varnothing : \cup \cap \setminus \subset \subseteq \subsetneq \supset \in \notin \emptyset \varnothing
5. 表示排列使用`\binom{n+1}{2k}`：$\binom{n+1}{2k}$或`{n+1 \choose 2k}`：${n+1 \choose 2k}$
6. 箭头：`\to` `\rightarrow` `\leftarrow` `\Rightarrow` `\Leftarrow` `\mapsto:\to \rightarrow \leftarrow \Rightarrow \Leftarrow \mapsto
7. 逻辑运算符：\land \lor \lnot \forall \exists \top \bot \vdash \vDash：\land \lor \lnot \forall \exists \top \bot \vdash \vDash
8. \star \ast \oplus \circ \bullet : \star \ast \oplus \circ \bullet
9. \approx \sim \cong \equiv \prec : \approx \sim \cong \equiv \prec
10. \infty \aleph_o \nabla \partial \Im \Re : \infty \aleph_o \nabla \partial \Im \Re
11. 模运算 \pmode , 如 a \equiv b \pmod n : a≡b(modn)
12. \ldots与\cdots，其区别是dots的位置不同，ldots位置稍低，cdots位置居中。
a1+a2+⋯+an,a1,a2,…,an
13. 一些希腊字母具有变体形式，如\epsilon \varepsilon : ϵ ε , \phi \varphi : ϕ φ