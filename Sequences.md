#math #calculus #sequence 

# Definition  
  
**Sequence:** a list of numbers *in order*.  
Three expressions:  
* $\{ a_{1},\;a_{2},\;\dots\;a_{n},\;\dots \}$  
* $\{ a_{k} \}_{k=1}^{\infty}$  
* $\{ a_{n} \}$  
**Remark:**   
the index $k$ can start from $0$ or other numbers, not just $1$.  
  
$f(x),\;a_{n}=f(n),\;n \in \text{index set}$  
eg:  
$$\begin{cases}
 & f(x)=\cfrac{1}{x} \\
 & \;\;\;a_{n}=\cfrac{1}{n}\\
\end{cases} 
$$
$$\left\{  1,\; \frac{1}{2},\; \frac{1}{3},\;\dots\;, \frac{1}{n}  \right\}$$  
$\quad$  
Some seq. should be **recursively defined**.  
  
eg 1:  
**Fibonacci Seq.**  
$$\begin{align}
F_{1}=1,\;F_{2}=1,\; \tag{1} \\
F_{n+2}=F_{n+1}+F_{n}  \tag{2} \\
\{ 1,\;1,\;2,\;3,\;5,\dots \}
\end{align}$$    
where $(1)$ is the initial state(base case), and $(2)$ is the recursion.  
$\quad$  
  
eg 2:  
**Newton's Method.**  
$g(x)=x^{2}-2$.  
$$\begin{align} 
x_{1} &=1 \tag{1}  \\
x_{n+1} &= x_{n}- \frac{g(x_{n})}{g'(x_{n})} \\
 & = x_{n}- \frac{{x_{n}^2-2}}{2x_{n}} \\
 & = \frac{x_{n}}{2}+ \frac{1}{x_{n}} \tag{2} \\
\Big\{1,\; &\frac{3}{2},\; \frac{17}{12}, \dots  \Big\} \\
\lim_{ n \to \infty } x_{n}  & =\sqrt{ 2 }\;\text{ (to be proved)}
\end{align}$$  
where $(1)$ is the initial state, and $(2)$ is the recursion.  
  
## Properties of Seq.  
  
### I. Boundedness  
  
> $a_{n}$ is *bounded from above*  
$\quad$  if $\exists \;M$ s.t. $a_{n}\leq M.$   
$\quad$  $M$ is called an **upper bound** (not unique)  
$\quad$  $M_{0}$ is called **the least upper bound** (unique)  
$\quad$  $\quad$  (eg: for $a_{n}=\cfrac{1}{n},\;M_{0}$ is $1$)  
  
Similarly, we define $L$ and $L_{0}$ (*bounded below*)  
$\{a_{n}\}$ is **bounded**, if bounded *both* above and below.  
  
### II. Monotonicity  
  
> $\{a_{n}\}\nearrow$ if $a_{n}\gt a_{n-1},\;\forall n$ (*strong*)  
> $\{a_{n}\}$ \_$\nearrow$ if $a_{n}\geq a_{n-1},\;\forall n$ (*loose*)  
  
### Convergence ($\varepsilon-N$ language)  
  
$a_{n}$ is convergent / converges to $L$.  $\Leftrightarrow$ $\displaystyle\lim_{ n \to \infty }a_{n}=L.$  
*Otherwise* it's divergent.  
  
> $\forall \,\varepsilon>0,$ we define a $\varepsilon$-dependent integer $N(\varepsilon)$, s.t.  
>    $$\forall\, n\geq N,(n>N),\;|a_{n}-L|<\varepsilon.$$  
  
$\quad$    
eg 1:  
Show that $\left\{  \cfrac{1}{n}  \right\}$ converges to 0.  
  
$\underline{Pf}$  $\forall \, \varepsilon>0,$ let $N=\underline{max \{1,\left\lceil  \cfrac{1}{\varepsilon}\right\rceil \} }$, s.t.  
$\quad$  $\forall\,n>N,\;\Big| \cfrac{1}{n}-0 \Big|< \varepsilon. \Longleftrightarrow \cfrac{1}{n}<\varepsilon \Longleftrightarrow n> \cfrac{1}{\varepsilon}.$

$\quad$  
eg 2:  
Show that $a_{n}= \cfrac{n}{2n+1}$ converges to $\cfrac{1}{2}$.  
  
$\underline{Pf}$  $\forall\,\varepsilon>0,$ let $N=\underline{\left\lceil  \cfrac{1}{4\varepsilon} - \cfrac{1}{2}  \right\rceil}$, s.t.  
$\quad$  $\forall\,n>N,\;\Big| \cfrac{n}{2n+1}- \cfrac{1}{2}\Big|<\varepsilon. \Longleftrightarrow \cfrac{1}{2(2n+1)}< \varepsilon \Longleftrightarrow n> \cfrac{1}{4\varepsilon} - \cfrac{1}{2}.$  

$\quad$  
eg 3:  
Show that $\{ (-1)^{n} \}$ diverges.  
  
$\underline{Pf}$ Suppose not, $\displaystyle\lim_{ n \to \infty }(-1)^{n}=L$.  $\quad \text{(Proof by Contradiction)}$  
$\quad$  $\forall \,n>N,\;$  $$|a_{n}-L|<\varepsilon \implies \begin{cases}
& |1-L|<\varepsilon  \\
 & |-1-L|<\varepsilon 
\end{cases}$$
$\quad$  no $L$ satisfies this two conditions. $\implies \impliedby$  
  
#### ==Uniqueness Theorem==  
  
> if $a_{n}$ is convergent, the the limit is unique.  
  
We will use **Contradiction**.  
$\underline{Pf}$  Assume that $\lim_{ n \to \infty }a_{n}=A,\;\lim_{ n \to \infty }b_{n}=B$  
$\quad$  $\forall\,\varepsilon>0,$ we can find $N_{1},\;N_{2},$ s.t.  
$\quad$  $$\begin{align} 
n>N_{1},\;|a_{n}-A|<\varepsilon \tag{1}  \\
n>N_{2},\;|a_{n}-B|<\varepsilon \tag{2}
\end{align}$$
$\quad$  Choose  $N=max\{ N_{1},N_{2} \}$, then  
$\quad$  $\forall\,n>N,\;(1)$ and $(2)$ both holds, so  
$$|A-B|=\Big|(a_{n}-A)-(a_{n}-B)\Big| \leq|a_{n}-A|+|a_{n}-B|<\varepsilon+\varepsilon=2\varepsilon$$
$\quad$  $\quad$  	Assume that $A \neq B$, so we have $|A-B|<2\varepsilon$ and $|A-B|=C$  
$\quad$  $\quad$  Since $\varepsilon$ is arbitrarily chosen, let $\varepsilon=\cfrac{C}{2}$ (or even smaller)  
$\quad$  $\quad$  So $|A-B|<C$ and $|A-B|=C,$ 
$\quad$  $\quad$  $\implies \impliedby$  
$\quad$  so $A=B$.  

$\quad$  
==**Theorem**==  **Convergence Implies Boundedness**  
  
> $\displaystyle\lim_{ n \to \infty }a_{n} \implies a_{n}$ is bounded.  
  
$\underline{Pf}$  By definition, choose $\varepsilon=1$, we have some $N$, s.t.  
$\quad$  $$\forall\,n\geq N,\;|a_{n}-L|\leq \varepsilon \;\underline{=1}$$
$\quad$  This suggests that for all terms $\underline{after}\; N$ (cut line)  
$\quad$  we have  $$L-1<a_{n}<L+1$$  
$\quad$  For the rest $\underline{finitely}$ many (the first $N$) terms,  
$\quad$  choose $$\begin{align} 
M & =max\{ a_{1},\;a_{2},\;\dots,\;a_{n} \},\\
m & =min\{ a_{1},\;a_{2},\;\dots,\;a_{n} \},
\end{align}$$
$\quad$  then   $$min\{ m,L-1 \} \leq a_{n} \leq max\{ M,L+1 \}.$$
$\quad$  
#### Definition of Divergence  
  
> $a_{n}\to +\infty$ if  
> $$\begin{align}
> & \forall \,M, \text{we can find }N, s.t.\\
> & \forall n\geq N,\;a_{n}\geq M. 
\end{align}$$  
  
Similarly,  
> $a_{n}\to -\infty$ if  
> $$\begin{align}
> & \forall \,m, \text{we can find }N, s.t.  \\
> & \forall n\geq N,\;a_{n} < m. 
> \end{align}$$
  
**Remark:**   
1) We write $\displaystyle\lim_{ n \to \infty }a_{n}=+\infty / -\infty$, does *NOT* mean $\{ a_{n} \}$ is *convergent*. It is still divergent.  
2) Seq. diverging to $\infty$ is unbounded, but an unbounded seq. *may not* diverge to $\infty$. (Consider $\{ (-1)^{n} \}$)  
  
## Evaluation of Limit of Seq.  
  
### I. Properties  
  
$\displaystyle\lim_{ n \to \infty }a_{n}=A,\;\lim_{ n \to \infty }b_{n}=B.$  
1) Sum Rule: $\displaystyle\lim_{ n \to \infty }(a_{n}+ b_{n})=A+ B$  
2) Difference Rule: $\displaystyle\lim_{ n \to \infty }(a_{n}-b_{n})=A-B$  
3) Product Rule: $\displaystyle\lim_{ n \to \infty }(a_{n}\cdot b_{n})=AB$  
4) Constant Rule: $\displaystyle\lim_{ n \to \infty }(k\cdot a_{n})=kA$  
5) Quotient Rule: If $B\neq 0$, we have $\displaystyle\lim_{ n \to \infty } \cfrac{a_{n}}{b_{n}}= \cfrac{A}{B}$  
  
Here gives the proof of 5).  
  
$\underline{Pf}$  For the definition of limit, let $\varepsilon= \frac{|B|}{2},$ then $\exists \,N$, s.t.  
$\quad$  $\forall\,n\geq N,$ $|a_{n}-B|\leq\varepsilon= \frac{|B|}{2}$, which means these terms stay away from 0.  
$\quad$  *Note that the first $N$ terms don't affect the limit.*  
$\quad$  (Now show the limit $= \frac{A}{B}$)  
$\quad$  Choose some $\varepsilon>0$ small, we can find some $N$, s.t.  
$\quad$  $\forall n\geq N,\;a_{n}$ & $b_{n}$ are $\varepsilon$*-close* to $A$ & $B$ respectively.  
$$\begin{align} 
\Bigg| \cfrac{a_{n}}{b_{n}}- \cfrac{A}{B}\Bigg| & = \Bigg|\cfrac{{a_{n}B-Ab_{n} \mathbf{-a_{n}b_{n}+a_{n}b_{n}}}}{b_{n}B}\Bigg|  \\
 & =\Bigg| \cfrac{{a_{n}(B-b_{n})+b_{n}(a_{n}-A)}}{b_{n}B} \Bigg| \\
 & \leq \cfrac{{|a_{n}|+|b_{n}|}}{b_{n} B}\varepsilon  \\
 & \leq \cfrac{{|A|+\varepsilon+|B|+\varepsilon}}{(B-\varepsilon)B} \varepsilon  \\
 & \leq 2 \cfrac{{|A|+|B|}}{|B|^{2}} \varepsilon.
\end{align}$$
$\quad$  the coefficient before $\varepsilon$ is a constant.  
$\quad$  
  
**Application:** $\displaystyle\lim_{ n \to \infty } \cfrac{n}{2n+1} = \lim_{ n \to \infty } \cfrac{1}{2+ \frac{1}{n}}= \frac{\lim_{ n \to \infty }(1)}{\lim_{ n \to \infty }\left( 2+ \frac{1}{n} \right)} =\cfrac{1}{2}.$  
  
### II. Sandwich Theorem  
  
> 1. $a_{n}\leq b_{n}\leq c_{n},\;\forall n\geq N$  
> 2. $\displaystyle\lim_{ n \to \infty }a_{n}=\lim_{ n \to \infty }b_{n}=L$  
> Then $\displaystyle\lim_{ n \to \infty }b_{n}$ exists, $\displaystyle\lim_{ n \to \infty }b_{n}=L$  
  
eg: Evaluate $\displaystyle\lim_{ n \to \infty } \cfrac{n!}{n^{n}}$.  
  
$\underline{Sol}$  Choose $a_{n}=0$ and $c_{n}= \cfrac{1}{n}$, we have  
$\quad$  $$a_{n}<b_{n}= \cfrac{1}{n}\times \cfrac{2}{n} \times \dots \times \cfrac{n}{n} \leq \cfrac{1}{n}=c_{n}.$$  
$\quad$  By Sandwich Thm., $\displaystyle\lim_{ n \to \infty }b_{n}=0.$  
  
### III. The Continuous Function Thm. for Sequences  
  
> Let $\{ a_{n} \}$ be a **convergent** seq. with the limit $L$  
> Given a **continuous** $f(x)$, we have  
> $$\lim_{ n \to \infty }f(a_{n})=f(\lim_{ n \to \infty }a_{n})=f(L).$$
  
The proof involves $\varepsilon-\delta$ language.  

$\quad$  
eg:  
Evaluate the limits of: $a_{n}= \sqrt{ \frac{{n+1}}{n} }$;  $b_{n}= \frac{{4-7n^{6}}}{{n^{6}}+3}$.  
  
$\underline{Sol}$  (1) $c_{n}= \cfrac{{n+1}}{n}$. $\lim_{ n \to \infty }c_{n}= \lim_{ n \to \infty } \cfrac{{1+n^{-1}}}{1}=1$  
$\quad$  Since $f(x)=\sqrt{ x }$ is cts. at $x=1$,  
$\quad$  $$\lim_{ n \to \infty }a_{n}= \lim_{ n \to \infty }f(c_{n})=f(\lim_{ n \to \infty }c_{n})=1.$$
$\quad$  (2) Can not use Quotient Rule directly.  
$\quad$  Since both $\displaystyle\lim_{ n \to \infty }(4-7n^{6})$ and $\displaystyle\lim_{ n \to \infty }(n^{6}+3)$ D.N.E.  
$\quad$  $$b_{n}= \cfrac{{4n^{-6}-7}}{1+3n^{-6}},\text{ and } \displaystyle\lim_{ n \to \infty }b_{n}= \cfrac{-7}{1}=-7.$$
$\quad$  
  
### IV. Theorem (Connection with Functions) 
  
> If $a_{n}=f(n)$ for **larger** $n$, then we have   
> 	$\lim_{ x \to \infty }f(x)=L \implies \lim_{ n \to \infty }a_{n}=L$  
  
*if you can find the underlying functions easily.*  
  
**Remark:**  
The **converse** may be *NOT* true.  
eg:  $f(x)=\sin(2\pi x)$, we have $a_{n}=0$, but $\lim_{ x \to \infty }f(x)$ D.N.E.  
  
$\underline{Pf}$  $\forall\,\varepsilon >0$, we can find some $M$, s.t.  
$\quad$  $x>M\implies |f(x)-M|<\varepsilon$. Now let $n>M$. We are done.  

$\quad$  
eg:  
Evaluate the limits:  $\lim_{ n \to \infty } \cfrac{{\ln n}}{n}$;  $\lim_{ n \to \infty } \sqrt[n]{ n }$.  
  
$\underline{Sol}$  (1) Consider $f(x)= \cfrac{{\ln x}}{x}$. Using $L'H\hat{o}s\pi tal's\;Rule$.  
$$\lim_{ x \to \infty }f(x)=\lim_{ x \to \infty } \cfrac{1}{x}=0.$$
$\quad$  So  $\displaystyle\lim_{ n \to \infty } \cfrac{{\ln n}}{n}=0$  
$\quad$  
$\quad$  (2) Consider $f(x)= e^{ {\ln x}/x }$. Since $y=e^{ x }$ is cts.,  
$\quad$  So  $\lim_{ x \to \infty }f(x)= e^{ \lim_{ x \to \infty } {\ln x}/x }=e^{ 0 }=1$  
$\quad$  then  $\lim_{ n \to \infty } \sqrt[n]{ n }=\lim_{ n \to \infty }e^{ \ln \sqrt[n]{ n }}=\lim_{ x \to \infty }e^{ \ln x/x }=1$.  

$\quad$  
**Some Results of Sequential Limits**  
  
* $\cfrac{{\ln n}}{n}\to 0$  
* $\sqrt[n]{ n }\to 1$  
* $a^{\frac{1}{n}}\to 1\;(a>0)$  
* $a^{n}\to 0\;(0\leq a<1)$  
* $\left( 1+ \cfrac{a}{n} \right)^{n}\to e^{ a }$  
* $\cfrac{a^{n}}{n!}\to 0$  
  
Proof of the last one:  
  
$\underline{Pf}$  As $a$ is a fixed constant, lt $|a|\in [N,N+1]$  
$\quad$  Then, for $n>N$, we have  
$\quad$  $0\leq \cfrac{|a|^{n}}{n!}= \frac{{a}^{N}}{}$


#### L'H$\hat{o}$spital's Rule  


#### Bonus: Stoltz-Cesaro Theorem  
  
> 1. $\lim a_{n}=\lim b_{n}=0\;or\;\infty$  
> 2. $\lim \cfrac{{a_{n}-a_{n-1}}}{b_{n}-b_{n-1}}=L$  
> Then  $\lim \cfrac{a_{n}}{b_{n}}=L$  
  



### Monotonic Seq. Theorem  
  
Monotonicity + Boundedness $\implies$ Convergence  
