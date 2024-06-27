#math #calculus 

In this chapter, we will describe the curves in $\mathbb{R}^2$ or $\mathbb{R}^{3}$ as the image of a function.

**Scaler function** *(shorten for function)*  
$$f: D \subseteq \mathbb{R} \to Y \subseteq \mathbb{R}, \quad \text{domain} \to \text{codomain}$$
**Vector-valued function**  
$$\vec{r}: D \subseteq \mathbb{R} \to Y \subseteq \mathbb{R}^{n},\;n=2, 3,\text{ usually}$$  
# Definition  

> **Vector-valued function** or **vector function** on an interval $I$ is a function mapping *number* to a *vector* in $\mathbb{R}^{n}$, denoted by  
> $$\vec{r}: I \to \mathbb{R}^{n},$$  
> where $I \in \mathbb{R}$ and $\mathbb{R}^{n}$ is viewed as *a set of vectors*.  

**Component-wise**  

> For the vector function $\vec{r}(t)$, it can be written component-wisely:  
> $$\vec{r}(t) = \big(r_{1}(t), r_{2}(t),\dots ,r_{n}(t)\big),\;t \in I.$$
> Here $r_{k}(t)$ in each component is a function.

## I. Physical Background  

The motion in space  

## II. Geometric Background  

3-D: $\vec{r}(t) = \big(r_{1}(t), r_{2}(t),r_{3}(t)\big) \implies \begin{cases} x=r_{1}(t) \\ y =r_{2}(t) \\ z = r_{3}(t) \end{cases}$,  a parametric equation set for a curve in $\mathbb{R}^{3}$.  

$\quad$  
eg:   

Sketch the curve parametrized by the function $\vec{r}(t):=(\cos t, \sin t, t),  \; t \in \mathbb{R}.$  

![[helix.png]]

# Calculus for $\vec{r}(t)$  

## 1. Limit  

### Definition  

> We say $\vec{r}$ has a limit $\vec{L}$ as $t$ approaches $t_{0}$, and write  
> $$\lim_{ t \to t_{0} } \vec{r}(t) = \vec{L},$$
> if $\forall\,\varepsilon > 0,$ $\exists\,\delta > 0,$ s.t.  $\forall\,t \in I,$
> $$0< |t-to| < \delta \implies |\vec{r}(t) - \vec{L}|<\varepsilon.$$  

*Remark:* $|(a, b, c)| = \sqrt{ a^{2}+b^{2}+c^{2} },$ the **Euclidean distance**.  

**Component-wise Limit**  

> $\vec{r}(t) = \big(r_{1}(t), r_{2}(t), \dots, r_{n}(t)\big),\quad \vec{L} = (L_{1}, L_{2}, \dots, L_{n})$.  
> $$\lim_{ t \to t_{0} } \vec{r}(t) = \vec{L} \iff \lim_{ t \to t_{0} } r_{k}(t) = L_{k},\;k=1, 2, \dots, n.$$  

## 2. Continuity  

> $\vec{r}$ is **continuous** at $t_{0} \in I,$ if 
> $$\lim_{ t \to t_{0} } \vec{r}(t) = \vec{r}(t_{0}).$$  

**Component-wise Continuity**  

> $\vec{r}(t) = \big(r_{1}(t), r_{2}(t), \dots, r_{n}(t)\big)$ is **continuous**  
> $\iff r_{i}(t)$ is **continuous** for $i=1, 2, \dots, n.$  

*Remark:* If there is **ANY** component function is NOT continuous, then the vector function is NOT continuous.  

$\quad$  
eg:   

Let $\vec{r} = (\cos t, \sin t, \lfloor t \rfloor)$, find its limit when $t \to \cfrac{\pi}{4}$. Is it continuous for $t \in \mathbb{R}$?  

$\underline{Sol}\;$  
