# 2026DEM

## ChatGPT (July 2026)

### Summary

This paper determines worst-case matrix--vector query complexity for approximately solving general linear systems under randomized adaptive algorithms. For two-sided access to $A$ and $A^\top$, it proves a lower bound of essentially $\frac14\kappa\log(1/\varepsilon)$ products, within a factor of four of conjugate gradient on the normal equations. The proof reduces a sufficiently accurate linear solver to estimating $\operatorname{tr}(A^{-1})$ and combines this with polynomial inapproximability of $1/x$ on $[-\kappa,-1]\cup[1,\kappa]$. For transpose-free one-sided access, a hidden-Haar argument shows that an orthogonal, perfectly conditioned hard instance needs at least $\lceil n/2\rceil$ products for residual $1/2$ and all $n$ products for residual $0.2/\sqrt n$. Extensions give the sharp $\Omega(\sqrt\kappa\log(1/\varepsilon))$ symmetric-positive-definite dependence and a fine-grained $\Omega(k+\kappa_k\log(1/\varepsilon))$ bound. These are worst-case oracle results; structured matrices, preconditioners, and typical GMRES behavior may be much better.

### Contributions

1. Proved an explicit randomized two-sided lower bound proportional to $\kappa\log(1/\varepsilon)$.
2. Proved dimension-scale one-sided lower bounds even for orthogonal matrices.
3. Established a hidden-Haar theorem for information concealed from adaptive queries.
4. Connected linear solving to inverse-trace estimation and polynomial inapproximability.
5. Extended the framework to sharp positive-definite and fine-grained bounds.
