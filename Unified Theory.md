#calculus #math 

This theory is also called the **Newton-Leibniz-Gauss-Green-Ostrograsky-Stokes' Formula**. Today we usually call it the Unified Theory of (Vector) Calculus, or merely Stoke's Thm.  

# Boundary Operator  

We start with an operator $\partial$ the **boundary operator**:  

![[Boundary operator.jpg]]

The operator can *decrease the dimension* by 1. 
We have that the boundary of a boundary is the *empty set*: $\partial^{2}=\emptyset$.  
Next we have two formulae $\nabla \cdot (\nabla \times \vec{F}) = 0$ and $\nabla \times (\nabla f)= 0$.  

We can make a brief summary of **"Differentiation Operators"**.  

# Differentiation Operator  

## $\frac{d}{dx}$  

$$\mathop{f(x)}\limits_{\mathop{\text{scaler}}\limits_{\text{(real-valued)}}} \xrightarrow{\cfrac{d}{dx}} \mathop{f'(x)}\limits_{\text{scaler}}$$  
**FTC**:
$$\int _{[a,b]} f'(x) \, dx := \int _{a}^{b} f'(x) \, dx = f(b)-f(a)$$  
## grad  

$$\mathop{f(x, y, z)}\limits_{\text{scaler}} \xrightarrow{\text{grad}} \mathop{\nabla f(x, y, z)}\limits_{\text{vector}}$$  
**FTLI**  
$$\int _{C}\nabla f\cdot d\vec{r} = f(B)-f(A)$$

## curl  

$$\mathop{\vec{F}(x, y, z)}\limits_{\text{vector}} \xrightarrow{\text{curl}} \mathop{\text{curl } \vec{F}}\limits_{\text{vector}} \,\text{ or } \nabla \times \vec{F}$$ 
**Green's Thm (Circulation) (x-y plane)**

$$\iint_{R} \text{curl }\vec{F}\cdot \vec{k} \, dA = \oint_{C} \vec{F} \cdot d\vec{r}$$

**Stokes' Thm (3D)**  

$$\iint_{S} \text{curl }\vec{F}\cdot \vec{n}\,d\sigma = \oint_{C} \vec{F} \cdot d\vec{r}$$

## div  

$$\mathop{\vec{F}}\limits_{\text{vector}} \xrightarrow{\text{div}} \mathop{\text{div } \vec{F}}\limits_{\text{scaler}} \text{ or } \nabla \cdot \vec{F}$$

**Green's Thm (Flux)(2D)**  

$$\iint_{R} \text{div }\vec{F} \,dA = \oint_{C} \vec{F}\cdot \vec{n}\,ds$$

**Divergence Thm / Gauss' Thm (3D)**  

$$\iiint_{E} \text{div }\vec{F} \,dV = \iint_{S} \vec{F}\cdot \vec{n} \, d\sigma$$

See, do you feel some kinds of relationship between the **boundary operator** and the **differentiation operator**?  

Now let's bridge these two chains!  

# Unified Theory  

The diagram below is actually a representation of **de Rham Cohomology**.  

$$\begin{CD}
  @.
  \text{fn}                   @>\mathop{\nabla(\text{ })}\limits^{\text{Gradient}}>>          \text{v.f.}                        @>\mathop{\nabla \times(\text{ })}\limits^{\text{Curl}}>>              \text{v.f.}                        @>\mathop{\nabla \cdot(\text{ })}\limits^{\text{Divergence}}>>          \text{fn} @>0>> 0 \\ 
  @.@| @| @| @|\\
  \emptyset @<\partial<< \text{pts} @<\partial<< C @<\partial<< \Omega @<\partial<< \Sigma 
\end{CD}$$






$\mathop{expr1}\limits_{expr_{2}}^{expr_{3}}$