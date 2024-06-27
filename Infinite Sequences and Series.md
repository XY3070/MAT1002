#math #calculus #series

# Alternating Series  
  
Most of the tests we’ve learnt apply to series with *non-egative* terms of for *absolutely* convergence. Now introduce for **conditional convergence**.  
  
## Definition  
  
> $\displaystyle\sum_{k=1}^{\infty}(-1)^{n-1}u_{n},\;u_{n}\geq 0,\;\forall\,n.$ *(or $u_n\leq 0,\;\forall\,n)$*  
> $=u_{1}-u_{2}+u_{3}-u_{4}\dots$  
  
   
## The Alternating Series Test, or Leibniz Test  
  
> $\begin{cases} 1.u_{n}\geq 0, \\ 2.u_{n}\to 0, \\ \mathbf{3.u_{n}\searrow}, \end{cases}$  $\to u_{n}\searrow\to 0$ *(which already shows its non-negativity)*  
> Then, the series *converges.*  
> *Remark:* for $\sum (-1)^{n}:\;u_{n}\nearrow \to 0.$  
  
$\underline{Pf}$  Let $S_{n}$ denote the partial sum. First, we want to show that $S_{2n}$ actually converges.  
$\quad$ We have  
$$\begin{align}
S_{2n} & = u_{1}-u_{2}+u_{3}-u_{4}+\dots+u_{2n-1}-u_{2n} \quad \text{ (Finite many terms!)} \\
 & = (u_{1}-u_{2}) + (u_{3}-u_{4})+\dots+(u_{2n-1}-u_{2n}).
\end{align}$$
$\quad$ By assumption, all brackets contribute something *positive*, implies that $\{ S_{2n} \}$ the even terms in the sequence of partial sums is *non-decreasing* and *non-negative*.  
$\quad$ We also have this sequence is bounded by $u_{1}:$  
$$S_{2n}=u_{1}-(u_{2}-u_{3})-\dots-(u_{2n-2}-u_{2n-1})-u_{2n}\leq u_{1}.$$
$\quad$ Non-decreasing and bounded above by $u_{1}$ implies it converges.  
$$\lim_{ n \to \infty } S_{2n}=L.$$
$\quad$ Lastly, we have $S_{2n-1}=S_{2n}-u_{2n}.$ By taking limit, the RHS converges to $L-0=L.$ Thus, the odd partial sum also converges to $L.$  
$\quad$ By definition, $\forall\,\varepsilon>0,\;\exists\,N_{1}\;\text{and } N_{2},$ s.t. $|S_{2n}-L|<\varepsilon$ for $n>N_{1}$ and $|S_{2n-1}-L|<\varepsilon$ for $n>N_{2}.$  
$\quad$ Let $N=max \{ 2N_{1},2N_{2}+1 \},$ we are done.  
  
**Remark:**  
Consider $a_{n}=b_{n}=(-1)^{n-1} \cfrac{1}{\sqrt{ n }},$ both converges. But the product diverges:  
$$\sum a_{n}b_{n}= \sum \frac{1}{n}.$$
$\quad$ 
  
eg 1:  
**Alternating Harmonic Series.**  
$\sum (-1)^{n-1} \cfrac{1}{n}= 1- \frac{1}{2} + \frac{1}{3} -\frac{1}{4}\dots$  
  
$\underline{Sol}$  $u_{n}=\frac{1}{n},\;\searrow \to 0. \implies$ it’s **conditionally convergent**.  
$\quad$ 
  
eg 2:  
**Alternating p-Series.**  
Show that $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^{n-1}}{n^{p}}$ converges for any $p>0.$  
  
$\underline{Pf}$  By Leibniz test 
  
## Approximation-Estimate $S$ Using $S_{n}$  
  
1. $S_{2n}<S<S_{2n+1}\implies 0<S-S_{2n}<S_{2n+1}-S_{2n}=u_{2n+1}.$  
2.  $S_{2n+1}<S<S_{2n+2}$ *($u_{n}<0$ version)* $\implies S_{2n+1}-S_{2n+2}=-u_{2n+2}<S<S-S_{2n+2}<0.$   
The error $E_{2n}=|S-S_{2n}|\leq u_{2n+1},$ which means it's bounded, by the first unused term. Similarly, $E_{2n+1}=|S-S_{2n+1}\leq u_{2n+2}.$ Thus, $$E_{n}=|S-S_{n}|\leq u_{n+1},\;\forall\,n.$$
  
eg:   
Find the approximation of $\displaystyle\sum_{n=1}^{\infty} \frac{{(-1)^{n-1}}}{(n-1)!}$ using $S_{n}$ with error $<0.001.$  
  
$\underline{Sol}$  We have $E_{n}\leq u_{n+1}= \frac{1}{n!}\leq 0.001\implies n\geq 7.$  
	$S_{7}= 1-1 + \frac{1}{2!} - \frac{1}{3!} +\dots+ \frac{1}{6!}\approx 0.36805$  
	$S= \frac{1}{e}\approx 0.367879$  
  
## Absolutely Convergent vs. Conditionally Convergent  
  
### Definition  
  
> 1. $a_{n}^{+}=\begin{cases} a_{n},\quad &a_{n}\geq 0 \\ 0, \quad &a_{n}<0 \end{cases}$  
> 2. $a_{n}^{-}=\begin{cases} 0, \quad &a_{n}\geq 0 \\ -a_{n}, \quad & a_{n}<0 \end{cases}$  
> $\implies \begin{cases} a_{n}=a_{n}^{+}-a_{n}^{-}\\ |a_{n}|=a_{n}^{+}+a_{n}^{-} \end{cases}.$  
  
eg.  
Consider **alternating harmonic series.**  
$\begin{align}\sum (-1)^{n-1} \cfrac{1}{n} &=1- \frac{1}{2}+ \frac{1}{3}- \frac{1}{4}\dots\\ &= \left( 1+0+ \frac{1}{3}+0+\dots  \right)\\ & - \left( 0+ \frac{1}{2}+0+ \frac{1}{4} +\dots \right).\end{align}$  
  
==**Theorem**==  
  
> 1. $\sum a_{n}$ **absolutely converges**, *if and only if* $\sum a_{n}^{+}$ and $\sum a_{n}^{-}$ converges *(conv. - conv.)*  **(the converse is true)**  
> 2. One converges, the other diverges $\implies \sum a_{n}$ diverges.  
> 3. Both diverges $\to +\infty,$ **but** $\sum a_{n}$ diverges $\implies \sum a_{n}$ **conditionally converges**. *($\infty-\infty$, indeterminate form)*  
  
# Re-arrangement  
  
1+2+3 = 2+1+3 = 3+2+1 ...  
  
## Re-arrangement Theorem  
  
> If $\sum a_{n}$ **absolutely converges**, $\sum b_{n}$ is a **re-arrangement** of $\sum a_{n},$ then $\sum b_{n}$ also converges, with $\sum |a_{n}|=\sum|b_{n}|.$  
  
$\underline{Sol}$  Let $S_{n}:= \displaystyle\sum_{k=1}^{\infty}|a_{k}|\to S,\;T_{n}:=\sum_{k=1}^{\infty}|b_{k}|.$ Assume $S_{n}\nearrow \to S.$  
	*Want to show $\displaystyle \lim_{ n \to \infty }T_{n}$ converges.*   
	By definition, $\because\{ b_{n} \}$ is just a re-arrangement of $a_n,$ $\therefore T_{n} \_$$\nearrow$ and $T_{n}\leq S \;(\forall\,n).$  
	By **Monotonic Sequence Theorem**, $T_{n}\nearrow \to T,$ where $T\leq S.$ Then $$S_{n}\leq T\leq S.$$
	By Sandwich Theorem, $T=S.$  
  
*Things change for **conditionally convergent** series.*  
  
eg:  
**Dirichlet's Example.**  
  
**Alternating Harmonic Series**: $\displaystyle\sum_{n=1}^{\infty} (-1)^{n-1} \frac{1}{n}= 1- \frac{1}{2} + \frac{1}{3} - \frac{1}{4}\dots=A(=\ln 2)\neq 0.$  
$\displaystyle 2A= 2-1 + \frac{2}{3}- \frac{2}{4}\dots$  *(keep 2n-1 terms unchanged, move 2n terms to m)*  
    $\displaystyle =(2-1) - \left( \frac{2}{4} \right)+ \left( \frac{2}{3}-\frac{2}{6} \right)\dots$   
    $\displaystyle =1- \frac{1}{2}+ \frac{1}{3}\dots=A.$  
    $\implies 2A=A\neq 0\implies 2=1.\quad\times$  
  
### Riemann Re-arrangement Theorem  
  
> If $\sum a_{n}$ **conditionally converges**, we can **NOT** change the *order of the summation*. Otherwise, the re-arrangement $\sum b_{n}$ can result in *any number*, even diverges to $\infty.$  
  
**Question:**  
Does Associative Rule work for series?  
  
eg:  
$\begin{align} \sum(-1)^{n-1} & =1-1+1-1+\dots \\ & = (1-1)+(1-1)+\dots=0 \\ & = 1-(1-1)-(1-1)-\dots=1 \end{align}$  
But the result is **FALSE**. The series is infinite and we cannot figure out the ending term. So the result is actually **indetermined**. Therefore, the Associative Rule fails for series.  
  






  




[[MAT1002 Calculus II|Back to Menu]]  
  