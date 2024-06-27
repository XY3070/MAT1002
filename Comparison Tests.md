#math #calculus #sequence

# Comparison Tests  
  
## I. Direct Comparison Test  
  
> $\sum a_{n},\;\sum b_{n},\;\forall,n\geq N$ *(arbitrary, usually choose to be 1)*,  
> $$0\leq a_{n}\leq b_{n}\to \begin{cases}
\sum b_{n} \;converges \implies &\sum a_{n}\;converges \\
\sum a_{n}\; diverges \implies &\sum b_{n}\;diverges
\end{cases}$$
  
$\underline{Pf}$  1) *Show the boundedness to get convergence.*  
$\quad$ WLOG *(without loss of generality)*, assume $N=1.$  
$\quad$ Denote $\displaystyle\sum_{k=1}^{n}a_{k}=S_{n},\;\sum_{n=1}^{\infty}b_{n}=B,$ we have  
$$0\leq S_{n}\leq \sum_{k=1}^{n}b_{k}\leq \sum_{n=1}^{\infty}b_{n}=B$$
$\quad$ Thus, $S_{n}$ is bounded $\implies$ $\sum a_{n}$ converges.  
$\quad$   
$\quad$ 2) Assume $\sum b_{n}$ converges. By the process of (1), $\sum a_{n}$ converges.  $\implies \impliedby$, thus $\sum b_{n}$ diverges.  
  
**Remark:**  
In general, if $k>0$, $0\leq \sum a_{n}\leq \sum kb_{n}$ still holds.  
$\quad$ 
  
eg 1:  
Show that $\displaystyle\sum \frac{1}{3^{n}+{n^{1/3}}}$ converges.  
  
$\underline{Pf}$  Notice that $3^{n}+ n^{1/3} >3^{n}>0,$  
$\quad$ So $0<a_{n}:= \frac{1}{3^{n}+{n^{1/3}}} < \frac{1}{3^n}=:b_{n}.$  
$\quad$ Consider **Geometric Series** $\sum \cfrac{1}{3^{n}}$ converges, by **Comparison Test**, it converges.  
$\quad$ 
  
eg 2:  
Show $\displaystyle\sum \frac{1}{3^{n}-n^{1/3}}$ converges.  
  
$\underline{Pf}$  Because $3^{n}-n^{1/3} <3^{n},$  
$\quad$ we can NOT utilize $\cfrac{1}{3^{n}}$ directly.  
$\quad$ Consider $\forall\,n>10$ *(just roughly)*, $3^{n}-n^{1/3}> \cfrac{1}{2}\cdot 3^{n}>0.$  
$\quad$ So $0<a_{n}:= \cfrac{1}{3^{n}-n^{\frac{1}{3}}} <2 \cdot \cfrac{1}{3^{n}}=:b_{n}$ (n>10)  
$\quad$ Consider G.S. $\sum \cfrac{2}{3^{n}},\;\implies$ it converges.  
$\quad$ 
  
eg 3:  
Test the convergency:  $\displaystyle\sum_{n=1}^{\infty} \frac{\ln(n)}{n};$ $\displaystyle\sum_{n=1}^{\infty} \frac{1}{n!}$.  
  
$\underline{Sol}$  1) 1. $\cfrac{\ln n}{n}>0$  *(Test non-negativity)*  
$\quad\quad\;\,$ 2. $\forall\,n\geq 3,$ we have $\cfrac{{\ln(n)}}{n} > \cfrac{1}{n},$  
$\quad$ $\quad$ so $0\leq a_{n}:= \cfrac{1}{n}< \cfrac{{\ln(n)}}{n}=:b_{n}.$  
$\quad$ $\quad$ Since **Harmonic Series** $\sum \cfrac{1}{n}$ diverges $\implies$ it diverges.  
   
$\quad$ 2) 1. $\cfrac{1}{n!}>0$  *(Test non-negativity)*  
$\quad$ $\quad$ 2. $\forall\,n\geq 3,$ we have $\cfrac{1}{n!}> \cfrac{1}{n(n-1)},$  
$\quad$ $\quad$ so $0\leq a_{n}:= \cfrac{1}{n!}< \cfrac{1}{n(n-1)}=:b_{n}.$  
$\quad$ $\quad$ Since **Telescoping Series** $\sum \cfrac{1}{n(n-1)}=:b_{n}$ converges $\implies$ it converges.  
  
## II. Limit Comparison Test  
  
> $a_{n}>0,\;b_{n}>0,\;\displaystyle\lim_{ n \to \infty } \frac{a_{n}}{b_{n}}=L$ *(or $\infty$)*  
> 1. $L\in\mathbb{R}^{+},$ $\sum a_{n}$ and $\sum b_{n}$ converges or diverges *simultaneously*;  
> 2. $L=0,$ $\sum b_{n}$ converges $\implies$ $\sum a_{n}$ converges;  
> 3. $L=\infty,$ $\sum b_{n}$ diverges $\implies$ $\sum a_{n}$ diverges.  
  
$\underline{Sol}$  1) $\displaystyle\lim_{ n \to \infty } \frac{a_{n}}{b_{n}}=L>0.$ By definition, $\forall\,\varepsilon>0,\; \exists\,N,$ s.t.  
$\quad$ $\forall\,n\geq N,$  $$\left|\frac{a_{n}}{b_{n}}-L\right|<\varepsilon.$$
$\quad$ Choose $\varepsilon=\cfrac{L}{2}>0,$ i.e. $\cfrac{a_{n}}{b_{n}}$ is $\cfrac{L}{2}$-close to $L,$ i.e. $\cfrac{L}{2}\leq \cfrac{a_{n}}{b_{n}}\leq \cfrac{3}{2}L.$  
$\quad$ 1. Suppose $\sum b_{n}$ converges, then $0\leq a_{n}\leq \cfrac{3}{2}L \cdot b_{n}.$  
$\quad$ $\quad$ By **Direct Comparison Test**, $\sum a_{n}$ converges.  
$\quad$ 2. Suppose $\sum b_{n}$ diverges, then $0\leq \cfrac{1}{2}L \cdot b_{n}\leq a_{n}.$  
$\quad$ $\quad$ By **D.C.T.**, $\sum a_{n}$ diverges.  
$\quad$ $\;$ $1. +2. \implies$ Simultaneity.  
  
$\quad$ 2) $\displaystyle\lim_{ n \to \infty } \frac{a_{n}}{b_{n}}=0.$ By definition, $\forall\,\varepsilon>0,\;\exists\,N,$ s.t.  
$\quad$ $\forall\,n\geq N,$  $$\left| \frac{a_{n}}{b_{n}}\right|<\varepsilon= \frac{L}{2}\;\text{(arbitrary)}\implies 0\leq \frac{a_{n}}{b_{n}}< \frac{L}{2}.$$
$\quad$ Suppose $\sum b_{n}$ converges, then  $a_{n}< \cfrac{L}{2}b_{n}. \;\dots$  
  
$\quad$ 3) Similarly. By definition, $\forall\,M>0,\;\exists\,N,$ s.t.  
$\quad$ $\forall\,n>N,$  $$\frac{a_{n}}{b_{n}}>M\implies a_{n}>Mb_{n}.$$
$\quad$ Suppose $\sum b_{n}$ diverges, then  $a_{n}$ diverges.   
$\quad$ 
  
eg 1:  
$\underline{Sol}$  1) $n\ln n>0,\;n^{2}>0,$ so  $\cfrac{{n\ln n-1}}{n^{2}+5}>0.$  
$\quad$ 2) $b_{n}= \cfrac{{n\ln n}}{n^{2}}=\cfrac{{\ln n}}{n}>0$ ($n\geq 4$)  
$\quad$ $\displaystyle\lim_{ n \to \infty }\frac{a_{n}}{b_{n}}=1 \implies \sum a_{n}$ and $\sum b_{n}$ are simultaneous.  
$\quad$ Because $\sum b_{n}$ diverges *(proved previously)*  
$\quad$ it's divergent.  
$\quad$ 
  
eg 2:  
$\underline{Sol}$  1) $a_{n}\geq 0;$  
$\quad$ 2) Choose **p-Series** to compare, $p \in\left( 1, \cfrac{5}{4} \right)$  
$\quad$ let $b_{n}= \cfrac{1}{n^{9/8}},$  $$\lim_{ n \to \infty } \frac{a_{n}}{b_{n}}=\lim_{ n \to \infty } \frac{{\ln n}}{n^{1/8}}$$
$\quad$ Consider $f(x)= \cfrac{{\ln x}}{x^{1/8}},$  
$$\lim_{ x \to \infty } f(x) \xlongequal{L'H} \lim_{ x \to \infty } \frac{8}{x^{1/8}}.$$
$\quad$ $\sum b_{n}$ converges $\implies$ $\sum a_{n}$ converges.  
  
**Question:** Why $p=\cfrac{9}{8}$?  
1. $b_{n}$ should converge, so $p>1;$  
2. $\displaystyle\lim_{x \to \infty} \frac{a_{n}}{b_{n}}$ should be 0, so $p - \cfrac{5}{4}<0.$  
$\quad$ 
  
eg 3:  
Test  $\displaystyle\sum_{n=1}^{\infty}\sin\left( \frac{1}{n} \right).$  
  
$\underline{Sol}$  1) $0< \cfrac{1}{n}\leq 1 < \cfrac{\pi}{2}$ ($\sin \frac{\pi}{2}=1$)  
$\quad$ $\implies\;a_{n}\geq 0.$  
$\quad$ 2) $b_{n}= \cfrac{1}{n}.$ Harmonic Series.  
$\quad$ $\displaystyle\lim_{ n \to \infty } \frac{a_{n}}{b_{n}} \overset{L'H}{=} 1,$ $\sum b_{n}$ diverges.  
$\quad$ 
  
eg 4:  
Test $\displaystyle\sum_{n=1}^{\infty}\left( 1-\cos\Big( \frac{1}{n} \Big) \right).$  
  
$\underline{Sol}$  1) $1-\cos\left( \frac{1}{n} \right)\geq 0.$  
$\quad$ 2) Notice that $1-\cos x\sim \cfrac{1}{2}x^{2},$  
$\quad$ so choose $b_{n}= \cfrac{1}{n^{2}},$  
$\quad$ $\displaystyle\lim_{ n \to \infty } \frac{a_{n}}{b_{n}} \overset{L'H}{=} \frac{1}{2}$  Simultaneous.  
$\quad$ Then $\sum b_{n}$ converges $\implies\;\sum a_{n}$ converges.  
  
## Commonly Used Series to Compare with:  
  
1. Geometric Series;  
2. p-Series;  
3. Logarithm Geometric Series;  
	$\cfrac{1}{n\ln^{p}(n)}$  
  
*All tests are some kinds of **comparison tests**, explicitly or implicitly.*  
  
# Root Test and Ratio Tests  
  
When testing with **non-negative** terms, we only need to test if the sequence of partial sums are **bounded** (which is easier to test than convergence).  
But the comparison test fails for neither-positive-nor-negative terms, so let's consider **absolute value**.  
  
## Definition of Absolute Convergence and Conditionally Convergence  
  
> $\sum a_{n}$ is **Absolutely Convergent** if $\sum|a_{n}|$ converges.  
> $\sum a_{n}$ is **Conditionally Convergent** if $\sum|a_{n}|$ diverges to $\infty$ but $\sum a_{n}$ converges.  
  
**==Corollary==**  
$\sum a_{n}$ converges $\implies$ $\sum|a_{n}|$ converges.  
  
![[A.C., C.C., and divergent.png]]
  
$\underline{Pf}$  Let $b_{n}=a_{n}+|a_{n}|=\begin{cases}0 \quad & a_{n}\leq 0 \\ 2|a_{n}| \quad & a_{n}>0 \end{cases}.$  
$\quad$ By D.C.T., $\sum b_{n}$ converges *(bounded)*, and $\sum a_{n}=\displaystyle\sum(b_{n}-|a_{n}|)$ also converges ($conv.-conv.$) also converges.  
  
**Remark:**  
the **converse** is NOT true. Counter-examples are C.C. series.  
eg:  $\displaystyle \sum \cfrac{{(-1)^{n-1}}}{n}=1 - \frac{1}{2} + \frac{1}{3} - \frac{1}{4}\dots$  $\sum a_{n}\to \ln 2,$ but $\sum|a_{n}|$ diverges.  
$\quad$ 
  
eg 1:  
Test $\displaystyle\sum_{n=1}^{\infty} \frac{\sin(n)}{n^{2}}.$  
  
$\underline{Sol}$  *As $\sin(n)$ is $(+,-)$, we can not use C.T. directly.*  
$\quad$ Notice that $0\leq |\sin(n)|\leq 1,$ we have  $$0\leq \left|\frac{{\sin(n)}}{n^{2}} \right|\leq \cfrac{1}{n^{2}}.$$
$\quad$ This series A.C. Thus it converges.  
  
*Now introduce two methods to test A.C.*  
  
## Ratio Test, or D'Alembert Test  
  
> Suppose $\displaystyle\lim_{ n \to \infty } \left|\frac{a_{n+1}}{a_{n}}\right|=r,$ we can conclude:  
> 1. If $r<1,$ then $\sum a_{n}$ **absolutely converges**;  
> 2. If $r>1\;or\;r=\infty,$ $\sum a_{n}$ diverges;  
> 3. If $r=1,$ the test **fails** / is inconclusive.  
  
**Remark:**  
1) $a_{n}$ need **NOT** to be *positive*.  
2) Extremely useful with $n!$ or $a^{n}$.  
3) Another form of comparison test $\impliedby$ Boundedness Test actually.  
  
$\underline{Pf}$  1) If $r<1,$ let us choose $l= \cfrac{{r+1}}{2}\implies 1<l<r,$  
$\quad$ $\forall\,\varepsilon>0,\;\exists\,N,$ s.t. $\forall \,n\geq N,$  $$|a_{n+1}|,l^{1}\cdot |a_{n}|\implies |a_{n}|< l^{n-N}\cdot |a_{N}|,$$
$\quad$ Therefore, consider the tail part after $N,$  $$\sum_{k=n}^{\infty}|a_{k}|\leq \sum_{k=n}^{\infty}|a_{N}|\cdot l^{k-N}\leq \frac{|a_{N}|}{1-l}.$$
$\quad$ It's bounded, thus convergent.  
  
$\quad$ 2) If $r>1,\;\exists\,N,$ s.t.  $\forall\,n>N,\;|a_{n+1}|>|a_{n}|,$ i.e. $\{ a_{n} \} \nearrow,$  
$\quad$ thus $\{ a_{n} \}\cancel{ \to }0.$ By the n-th term test, it's divergent.  
  
$\quad$ 3) If $r=1,$ $\sum \cfrac{1}{n}$ and $\sum \cfrac{1}{n^{2}}$ are examples with $r=1$ but the series converges or diverges, respectively.  
$\quad$ 
  
eg 1:  
Test  $\displaystyle\sum_{n=1}^{\infty} \frac{n!}{n^{n}}.$  
  
$\underline{Sol}$  Ratio Test.  $\displaystyle\lim_{ n \to \infty } \Bigg| \frac{{a_{n+1}}}{a_{n}} \Bigg| = \lim_{ n \to \infty }\left( \frac{n}{n+1} \right)^{n}=\lim_{ n \to \infty } \frac{1}{\left( 1+ \frac{1}{n} \right)^{n}}= \frac{1}{e}<1\implies$ converges.  
$\quad$ 
  
eg 2:  
Test  $\displaystyle\sum_{n=1}^{\infty} \frac{{2^{n}+5}}{3^{n}}.$  
$\underline{Sol}$  $\displaystyle\lim_{ n \to \infty } \Bigg| \frac{{a_{n+1}}}{a_{n}} \Bigg| = \lim_{ n \to \infty } \frac{{2+ \frac{5}{2^{n}}}}{3\left( 1+ \frac{5}{2^{n}} \right)} = \frac{2}{3}<1\implies$ converges.  
  
## Root Test, or Cauchy Test  
  
> $\displaystyle\lim_{ n \to \infty } \sqrt[n]{ |a_{n}| }=L,$ we can conclude:  
> 1. If $L<1,$ then $\sum a_{n}$ **absolutely converges**;  
> 2. If $L>1\;or\;L=\infty,$ $\sum a_{n}$ diverges;  
> 3. If $L=1,$ test **fails** / is inconclusive.  
  
**Remark:**  
1) Similarly, $a_{n}$ need **NOT** to be *positive*.  
2) Useful with $n^{n}$ or $a^{n}$ ($n!\;\times$).  
3) Depends on $a_{n}$ **only**.  
  
$\underline{Sol}$  1) If $L<1,$ let $r = \cfrac{L+1}{2},\;\exists\,N,$ s.t. $\forall\,n>N,$  $$\sqrt[n]{ |a_{n}| }<r\quad or \quad |a_{n}|<r^{n}.$$
$\quad$ Consider the tail part starting from $N:$  $$\sum_{k=N}^{\infty}|a_{n}|\leq \sum_{k=N}^{\infty}r^{k}= \frac{r^{N}}{1-r}.$$
$\quad$ Bounded, thus convergent.  
	  
$\quad$ 2) If $L>1,$ the $\forall\,n>N,\;|a_{n}|>1^{n}=1,$ by n-th term test, it diverges.  
  
$\quad$ 3) If $L=1,$ consider $\sum \cfrac{1}{n}$ and $\sum \cfrac{1}{n^{2}}.$  
  
## Relation with Geometric Series  
  
**Ratio Test:** Consider G.S. $a_{n}= a\cdot r^{n-1}.$ Utilize ratio test:  $$\lim_{ n \to \infty } \left| \frac{{a\cdot r^{n}}}{a\cdot r^{n-1}} \right|=\lim_{ n \to \infty } |r|\to \text{true "ratio"}.$$
$\quad$ The ratio test **regards** a general series **as** a "Geometric Series" with $r=$"ratio".  
**Root Test:** $$\lim_{ n \to \infty } \sqrt[n]{ |ar^{n-1}| }=\lim_{ n \to \infty } \left(  \Big|\frac{a}{r}\Big|\cdot |r|^{n} \right)^{\frac{1}{n}}= \Big| \frac{a}{r} \Big|^{0}\cdot|r|=|r|\to \text{true "ratio"}$$
	The root test is also a ***special* comparison test**, where you compare the series with G.S. implicitly.  
$\quad$ 
  
eg 1:  
Test  $\displaystyle\sum_{n=1}^{\infty}aq^{n}\;(a\neq 0).$  
  
$\underline{Sol}$  $\displaystyle \lim_{ n \to \infty } \sqrt[n]{ |aq^{n}| }=\lim_{ n \to \infty }(|a|\cdot q^{n})^{\frac{1}{n}}=q\to \begin{cases} converges,\quad &|q|<1\\ diverges, \quad & |q|\geq 1 \end{cases}.$  
$\quad$ 
  
eg 2:  
Test  $\displaystyle\sum_{n=1}^{\infty} \frac{n^{2}}{3^{n}}.$  
  
$\underline{Sol}$  $\displaystyle \lim_{ n \to \infty }\sqrt[n]{ \frac{n^{2}}{3^{n}} }=\lim_{ n \to \infty } \left(n^{2}\cdot \Big(  \frac{1}{3} \Big)^{n} \right)^{\frac{1}{n}}= \frac{1}{3}<1\implies$ converges.  
  
## Ratio Test vs. Root Test  
  
*Root Test is a little stronger.* If root test fails on a series, usually so will the ratio test.  
$\quad$
  
eg 1:  
Test  $\sum a_{n},$ where $a_{n}=\begin{cases} \cfrac{n}{2^{n}}, \quad & \text{n odd}\\ \cfrac{1}{2^{n}},\quad & \text{n even} \end{cases}.$  
  
$\underline{Sol}$  $\{ a_{n} \}=\left\{  \frac{1}{2},\; \frac{1}{4},\; \frac{3}{8},\; \frac{1}{16},\dots \right\}$  
$\quad$ Ratio Test:  $$\begin{cases}
\displaystyle \lim_{ n \to \infty } \frac{{n+1}}{2^{n+1}}\times \frac{{2^{n}}}{1}=\lim_{ n \to \infty } \frac{{n+1}}{2}\to \infty,\quad &\text{n even} \\
\displaystyle \lim_{ n \to \infty } \frac{1}{2^{n+1}}\times \frac{{2^{n}}}{n}= \lim_{ n \to \infty } \frac{1}{2n}\to_{0}, \quad & \text{n odd}
\end{cases}\quad fails.$$
$\quad$ Root Test:  $$\frac{1}{2}\leq \sqrt[n]{ |a_{n}| }\leq \frac{\sqrt[n]{ n }}{2}.$$
$\quad$ By Sandwich Thm, it converges to $\cfrac{1}{2}.$  
  
**Remark:**  
  
| Ratio Test | Root Test | 
| :--- | :--- | 
| useful in $n!$ | useful for $n^{n}$ |  
| because most terms factorial can be cancelled | similar reason | 
| rely on the relationship between 2 terms | rely on 1 term itself | 
$\quad$ 
  
[[MAT1002 Calculus II|Back to Menu]]  
  