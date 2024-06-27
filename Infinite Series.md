#math #calculus #series 

**(Infinite) Series:** Summation of *infinitely many* numbers (in order).  
$\quad$ $\{ a_{1},\;a_{2},\;\dots,\;a_{n},\;\dots \}$$\quad$   $\sum_{n=1}^{\infty}a_{n}:$ **infinite Sums**  
$\quad$ $S_{1}=a_{1}$  
$\quad$ $S_{2}=a_{1}+a_{2}$  
$\quad$ …  
$\quad$ $S_{n}=a_{1}+a_{2}+\dots+a_{n}$ $\quad$ $\sum_{k=1}^{n}a_{k}:$ **Partial Sums**  
$\{ S_{1},\;S_{2},\;\dots,\;S_{n},\;\dots \}$ is a new seq. of **Partial Sums** *recursively defined*.  
  
# Definition  
  
> Let $S=\displaystyle\lim_{ n \to \infty }S_{n}$ be the limit of this seq., we call $S$ to be the (*infinite) series* of the seq. $\{ a_{n} \}$.  
> $$S=\sum_{n=1}^{\infty}a_{n}=\lim_{ n \to \infty }S_{n}=\lim_{ n \to \infty } \sum_{k=1}^{n}a_{k}$$
> The series **converges** if $\displaystyle\lim_{ n \to \infty }S_{n}$ exists (as a finite number); otherwise it’s **divergent**.  
  
**Remark:**  
The summation can start *other index than* 1.  
**Note that** $a_{n}=S_{n}-S_{n-1}$, since $$\begin{cases}
S_{1}=a_{1} \\
S_{n}=S_{n-1}+a_{n}
\end{cases}$$recursion.  
$\quad$ 
  
eg 1:  
Consider $a_{n}=a$. If the series of $a_{n}$ converges or not?  
  
$\underline{Sol}$  By definition, we have $S_{n}=na$. Therefore,  
$$S=\lim_{ n \to \infty } S_{n}=\begin{cases}
\infty \quad &a>0 \\
0 \quad & a=0 \\
-\infty & a<0
\end{cases}$$
$\quad$ 

eg 2:  
**Geometric Series.**  
Consider $a_{n}=ar^{n-1}\;(a\neq 0)$, determine its convergency.  
  
$\underline{Sol}$  1) If $r=1$, we have $a_{n}=a$, like the example above;  
$\quad$ $\;$ 2) If $r \neq 1$, we have $$\begin{align}
S_{n} & =a(+r+\dots+r^{n-1})\cdot \frac{{1-r}}{{1-r}}=a \frac{{1-r^{n}}}{{1-r}} \\
\implies S & = \lim_{ n \to \infty } a \frac{{1-r^{n}}}{1-r}= \begin{cases}
\cfrac{a}{1-r},\quad & |r|<1 \\
\infty,\quad & |r|=1
\end{cases}
\end{align}$$  
$\quad$ 
  
eg 3:  
**Telescoping Series.**  
Consider $a_{n}= \cfrac{1}{n(n+1)}$, to determine its convergence.  
  
$\underline{Sol}$  Notice that $a_{n}= \cfrac{1}{n(n+1)}= \cfrac{{(n+1)-n}}{n(n+1)}= \cfrac{1}{n}- \cfrac{1}{n+1}$  
$\quad$ Thus, $$S_{n}= \left( 1- \frac{1}{2} \right)+ \left( \frac{1}{2} - \frac{1}{3} \right)+\dots+ \left(  \frac{1}{n}- \frac{1}{n+1} \right)= 1- \frac{1}{n+1}.$$$\quad$ *All intermediate terms are cancelled, which is why its called telescoping series.*  
$$S=\lim_{ n \to \infty } S_{n}=\lim_{ n \to \infty } \left( 1- \frac{1}{n+1} \right)=1.$$
$\quad$ 
  
# Properties  
  
## I. Linearility  
  
> Suppose $\sum a_{n}=A,\sum b_{n}=B$, then $\displaystyle\sum(ka_{n}+lb_{n})=kA+lB.$  
  
**Remark:**  
We don’t have product or quotient rule, as $\sum a_{n}b_{n}$ or $\sum \cfrac{a_{n}}{b_{n}}$ may not converge.  
Let $\sum a_{n}=S_{n},\;\sum b_{n}=T_{n}$, i.e., $S_{n}\to A,\;T_{n}\to B$, then $kS_{n}+lT_{n}\to kA+lB.$  
  
## II. Divergence Extension  
  
> Suppose $\sum a_{n}=A,\;\sum b_{n}$ diverges, then $\displaystyle\sum (a_{n}+b_{n})$ diverges.  
  
$\underline{Pf}$  *Contradiction*.  
$\quad$ Suppose $\displaystyle\sum(a_{n}+b_{n})$ converges, and we have $\sum a_{n}$ convergent, therefore  
	$$\sum b_{n}=\displaystyle \Big((a_{n}+b_{n})-a_{n}\Big)$$
$\quad$ should converge. (conv. - conv.)  $\implies \impliedby$  
  
## III. Multiplication  
  
> If $\sum a_{n}$ diverges and $k\neq 0$, then $\sum(ka_{n})$ also diverges.  
  
$\underline{Pf}$  *Contradiction.*  
$\quad$ Assume that $\sum(ka_{n})$ converges, and we have $\sum a_{n}$ diverges, then $$\sum a_{n}=\sum\left( \frac{1}{k}\cdot k a_{n} \right)=\frac{1}{k}\sum(ka_{n})$$$\quad$ should converges.  $\implies \impliedby$  
  
## IV. Divergence Addition  
  
> Suppose $\sum a_{n}$ and $\sum b_{n}$ diverges, $\displaystyle\sum(a_{n}+b_{n})$ is inconclusive.  
  
eg:  
$\{ a_{n} \}=(-1)^{n},\;\{ b_{n} \}=(-1)^{n-1},$ then $(a_{n}+b_{n})$ always gives 0. So $\displaystyle\lim_{ n \to \infty }\left( \displaystyle\sum_{k}^{n}(a_{k}+b_{k}) \right)=0.$  
$\quad$ 
  
**Question:** For $\displaystyle\sum_{n}^{\infty} \frac{1}{n^{2}}$, now to test its convergence without computing its limit out?  
*Let’s leave it [[#^integralTest|later]].*  
  
# Convergence Test  
  
## I. The n-th Term Test  
  
> If $\sum a_{n}$ **converges**, then $\displaystyle\lim_{ n \to \infty }a_{n}$ **exists** AND **equal to 0**.  
  
**Remark:**  
extremely useful when test **if a series converges.** If $\displaystyle\lim_{ n \to \infty }a_{n}$ D.N.E. *or* $\neq 0$; then the series **diverges.**  
  
Equivalently,  
> If $\displaystyle\lim_{ n \to \infty }a_{n}$ D.N.E. *or* $\displaystyle\lim_{ n \to \infty }a_{n}\neq 0$, the series diverges.  
  
*But the **converse** is **NOT** true.* So **DO NOT** use this to argue a series **converges**.  
  
$\underline{Pf}$  By definition, we have $a_{n}=S_{n}-S_{n-1}$. Since the series converges, we have  $$\lim_{ n \to \infty } a_{n}=\lim_{ n \to \infty } (S_{n}-S_{n-1})=S-S=0.$$
$\quad$ 
  
eg 1:  
Test the convergence:  $a_{n}=(-1)^{n};\;b_{n}= \frac{{e^{ n }-2}}{4e^{ n }+4}$.  
  
$\underline{Sol}$  1) $\displaystyle\lim_{ n \to \infty }(-1)^{n}$ D.N.E., thus the series diverges.  
$\quad\;$ 2) $\displaystyle\lim_{ n \to \infty }b_{n}= \frac{1}{4}\neq 0$, thus the series diverges.  
$\quad$ 
  
[[MAT1002 Calculus II|Back to Menu]]  
  