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




