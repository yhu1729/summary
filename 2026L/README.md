# 2026L

## ChatGPT (July 2026)

### Summary

Lai develops computational algorithms for constructing orthogonal and orthonormal polynomials over arbitrary polygonal domains in $\mathbb{R}^2$ using bivariate spline representations. A mature MATLAB spline-space implementation supplies exact polynomial representations over triangulated polygonal regions. Two algorithms are described: one constructs orthonormal polynomials up to degree $d$, and the other constructs degree-$d+1$ orthonormal polynomials in the complement of $\mathbb{P}_d$. Numerical examples for degrees 1--5 visualize polynomial structures and zero curves, including evidence against Gauss quadrature on centrally symmetric polygonal domains. The paper then uses odd- and even-degree orthogonal polynomials to reduce integration to residual quadratic or linear parts, motivating new quadrature rules. Polynomial interpolation further extends these rules to efficient high-precision quadrature on diverse polygonal domains, with possible extensions to weights, nonpolygonal approximations, Sobolev bases, wavelets, and higher dimensions.

### Contributions

1. Constructed orthonormal polynomial bases over arbitrary polygonal domains via bivariate splines.
2. Provided complementary algorithms for degree-limited and next-degree orthogonal spaces.
3. Used numerical zero-curve evidence to test Gauss-quadrature possibilities.
4. Derived polynomial-reduction strategies for odd- and even-degree integration.
5. Built high-precision quadrature schemes for polygonal domains from the constructed polynomials.
