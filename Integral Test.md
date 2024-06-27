#math #calculus #sequence 

Each test method applies to a certain kind of series.  
Be careful with the **condition** and **conclusion**.  
  
# Non-negative Series  
  
> if all $a_{n}\geq 0.$  
  
Such series has a non-decreasing seq. of **partial sums**:  $$\forall\,n>1,\quad S_{n}\geq S_{n-1}.$$
  
See how I deal with them.  
  
## II. ==Theorem==  (Boundedness Implies Convergence)  
  
> Suppose $a_{n}\geq 0$, then $S=\sum a_{n}$ converges, *if and only if* the seq. of partial sums **are bounded**.  
  
$\underline{Pf}$  $S_{n}$ is **monotonic** and **bounded**, which suggests it's **convergent**. *(Monotonicity + Boundedness $\to$ Convergence)*  
  
**Remark:**  
Testing boundedness is *much easier* than testing convergence.  
$\quad$ 
  
eg:  
**Harmonic Series.**  
Test if the series of $a_{n}= \frac{1}{n}$ converges or not.  
  
$\underline{Sol}$  *Though $\lim_{ n \to \infty }a_{n}=0$, we will show it $\to \infty$. **Equivalently**, show it's* **unbounded.**  
$\quad$ $\forall\,N,$ let $n=2^{2N}$, we will show $S_{n}\geq N$.  
$$\begin{align}
S_{n} & = (1)+\left( \frac{1}{2} \right)+\left(  \frac{1}{3}+ \frac{1}{4} \right)+ \left( \frac{1}{5}+\frac{1}{6}+\frac{1}{7}+\frac{1}{8} \right)+\dots+\frac{1}{2^{2N-1}}+\frac{1}{2^{2N}}\bigg) \\
 & \geq (1)+\left( \frac{1}{2} \right) + \left( \frac{1}{4}+\frac{1}{4} \right)+\left( \frac{1}{8}+\frac{1}{8}+\frac{1}{8}+\frac{1}{8} \right)+\dots+ \frac{1}{2^{2N}}+ \frac{1}{2^{2N}} \\
 & =1+ \frac{1}{2}+ 2^{1}\times \frac{1}{2^{2}}+2^{2}\times \frac{1}{2^{3}}+\dots+ 2^{2N-1}\times \frac{1}{2^{2N}} \\
 & =1+ \underbrace{\frac{1}{2}+\frac{1}{2}+\dots+\frac{1}{2}}_{\text{2N terms}} \\
 & = 1+N
\end{align}$$
$\quad$ Therefore, $\{ S_{n} \}$ are unbounded and diverge to $\infty$.  
  
## III. Integral Test  
  
*Applied to non-negative and non-decreasing terms.*  
$\quad$ 
  
eg:  
Does the series of $\sum \cfrac{1}{n^{2}}$ converge or not?  ^integralTest
  
$\underline{Sol}$  Consider the seq. $\left\{  \frac{1}{n^{2}}  \right\}$ as the image of $f(n)$ with $f(x)= \frac{1}{x^{2}}$. Let's write $a_{n}= \frac{1}{n^{2}}\times 1$, and consider this as the **area** of a rectangle.  
![[integral test.png]]
$\quad$ The series is less than the area under the curve $\cfrac{1}{x^{2}}$, i.e.  
$$S\leq 1+ \int _{1}^{\infty} \frac{1}{x^{2}} \, dx =2.$$
$\quad$ As the series with *non-negative* terms bounded $\to$ convergence.  
  
> Let $\{ a_{n} \}$ be a **non-negative** seq. with $a_{n}=f(n),$ where $f$ is **continuous, positive** and **decreasing** for all $x\geq N$. Then $\sum a_{n}$ and $\int _{N}^{\infty} f(x) \, dx$ converge or diverge *simultaneously*.  
  
**Remark:**  
1. $f$ is cts.;  
2. $f\geq 0;$  
3. $f \searrow$;  
$\implies \sum a_{n}$ converges, *if and only if* $\int _{N}^{\infty} f(x) \, dx$ converges.  
  
$\underline{Pf}$  Since $f(x)\nearrow$ for $x>N$, we have $\forall\,n>N$,  
$$a_{n}=f(n)>f(x)>f(n+1)=a_{n+1},\;\forall\,x \in(n,n+1).$$
$\quad$ $\implies a_{n}\geq \int _{n}^{n+1}f(x) \, dx \geq a_{n+1},$ Thus, for any $M$ large integer,  
$\quad$ we sum the terms from $N$ to $M$, we get  
$$\sum_{k=N}^{M-1}a_{k}\geq \int _{N}^{M}f(x) \, dx \geq \sum_{k=N+1}^{M}a_{k}.$$
![[proof of integral test.png]]
$\quad$ Let $M\to \infty$, we have  
$$\sum_{k=N}^{\infty}a_{k}\geq \int _{N}^{\infty}f(x) \, dx \geq \sum_{k=N+1}^{\infty}a_{k}.$$
$\quad$ If the **improper integral** converges, this means $S_{n}$ bounded thus convergent.  
$\quad$ If it diverges, the right inequality suggests that the series is unbounded, thus diverges as well.  
$\quad$ 
  
eg 1:  
$\sum \cfrac{1}{n},\;f(x)= \cfrac{1}{x}$.  
  
$\underline{Sol}$  1. $f$ is cts.;  
$\quad\;$ 2. $f$ is decreasing;  
$\quad\;$ 3. $f\geq 0$.  
$$\displaystyle\int _{1}^{\infty} \frac{1}{x} \, dx=\ln x\Big|_{1}^{\infty}  \quad \text{ diverges} \implies \sum \cfrac{1}{n}\quad \text{diverges.}$$

$\quad$ 
  
eg 2:  
**p-Series.**  
$\sum \cfrac{1}{n^{p}};\;f(x)= \cfrac{1}{x^{p}}.$  
  
$\underline{Sol}$  $$\displaystyle\int _{1}^{\infty} \frac{1}{x^{p}} \, dx= \frac{1}{1-p}\cdot x^{p-1}\Big|_{1}^{\infty}(p\neq 1)\implies \begin{cases}
converges, \quad &p>1 \\
diverges, \quad & p\leq 1\;(\text{p=1 as supplement})
\end{cases}$$
  
**Remark:**  
can only be used to **test for convergence**, not to evaluate the series. Here, $\displaystyle\sum_{n=1}^{\infty} \frac{1}{n^{p}}\neq \int _{1}^{\infty} \frac{1}{x^{p}} \, dx,$ it's only an *upper bound*.  
$\quad$ 
  
eg 3:  
Check the convergence:  $\displaystyle\sum_{n=2}^{\infty} \frac{1}{n\ln^{p}(n)}$.  
  
$\underline{Sol}$  Consider $f(x)= \frac{1}{x\ln^{p}(x)}$ for $x=2$, cts., $\geq 0$, $\searrow$.  
$$\int _{2}^{\infty} \frac{1}{x\ln^{p}(x)} \, dx = \frac{1}{1-p} \ln^{1-p}(x)\Big|_{2}^{\infty}\implies \begin{cases}
converges, \quad & p>1 \\
diverges, \quad & p\leq 1
\end{cases}$$
$\quad$ 
  
# Error Estimation  
  
Use **definite integral** to approximate the series.  
  
## Tail of Series  
  
> Define the **Remainder** of the series:  
> $$R_{N}=a_{N+1}+a_{N+2}+\dots=\sum_{n=N+1}^{\infty}a_{n}=S-S_{N}$$
  
**Remark:**  
Assume the **improper integral of** $f(x)$ converges, using the similar argument in the proof of the ***Integral Test***, we get  
$$\int _{N+1}^{\infty}f(x) \, dx \leq R_{N}\leq \int _{N}^{\infty}f(x) \, dx .$$
Adding $S_{N},$ we have  
$$S_{N}+\int _{N+1}^{\infty}f(x) \, dx \leq S=S_{N}+R_{N}\leq S_{N}+\int _{N}^{\infty}f(x) \, dx .$$
$S$ must be somewhere there within $S_{N}+\int _{N+1}^{\infty}f(x) \, dx$ and $S_{N}+\int _{N}^{\infty}f(x) \, dx$.  
$$E_{N}\leq \frac{1}{2}\int _{N}^{N+1}f(x) \, dx \leq \frac{1}{2}a_{n}.$$
where $E_{N}$ is the **error** of the estimation of $S$ using $S_{N}$.  
$\quad$ 
  
[[MAT1002 Calculus II|Back to Menu]]  
  