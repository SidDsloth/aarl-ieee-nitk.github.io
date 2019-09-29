# Control Theory

This entire section deals with how we can control systems and drive them towards stability. It revolved around eigenvalues and the stability tests.

## Concepts Learned
a) **Eigen Vectors** 

Solving $$\dot{x}=Ax$$,

$$x(t)=e^{At}x(0)$$

$$A\varepsilon=\Lambda \varepsilon$$, where $$\varepsilon$$ is the eigenvalue matrix of A.

$$AT=TD$$, where D is a diagonal matrix of $$\Lambda$$.

In eigen coordinate system,

$$x=Tz$$,

$$\dot{x}=T\dot{z}=Ax$$

$$\dot{z}=T^{-1}ATz$$

$$\dot{z}=Dz$$

$$A=TDT^{-1}$$

Therefore,

$$e^{At}=Te^{Dt}T^{-1}$$

b) **Stability of a System** 

The stability of a system is decided by its characteristics roots. If the roots exists on the positive real plane or repeated roots on imaginary axis, it leads to instability, while on the negative real plane to stability.

In discrete time system the same stability was with respect to a unit circle. When the roots were values beyond the unit circle or repeated roots on unit circle, while roots within ensured stability.

c) **Linearisation about a Fixed Point**

Given $$\dot{x}=f(x)$$

To linearise about a fixed point, we note that in $$\dot{x}$$, all the higher order time of the Taylor Expansion tend to 0, therefore resulting in $$\dot{x}$$ being equal to the Jacobian of f at the fixed point.

To add controllability to a system the equation was modified to 
$$\dot{x}=Ax+Bu$$

Considering $$B=-kx$$, 
$$\dot{x}=(A-Bk)x$$

$$C=[B \quad AB \quad A^2B \quad A^3B\quad ...\; A^{(n-1)}B]$$

If rank of C = n, then the system is controllable. Based on the values of the matrix, the direction proportionality of control of a system is determined.

In discrete time system, the solution of a system consists of a natural and a forced component. The impulse response triggers a zero state response which is obtained by convolution.

d) **PBH Test**

(A,B) for a system implies controllability if :
$$Rank(A-\Lambda I)=n$$, given

i) $$Rank(A-\Lambda I)=n$$ ( except for eigen values $$\Lambda$$)

ii) B needs to have some component in each direction of eigen vector direction.

iii) If B is a random vector then probability of its component being in that direction higher.

e) **Cayley Hamilton Theorem**

Every matrix A satisfies its own characteristic equation

$$det(A-\Lambda I)=0$$

Let $$\Lambda+a_{(n-1)}\Lambda^{(n-1)} \; ...+a_0=0$$

By the theorem,

$$A^n+a_{(n-1)}A^{(n-1)} \;...+a_0=0$$

Therefore $$e^{At}=\phi_0(t)+\phi_1(t)A+...+\phi_n(t)A^{(n-1)}$$
