# 2025GST

## ChatGPT (July 2026)

### Summary

This paper presents algorithms for computing classical Gaussian quadrature rules, including Gauss--Jacobi, Gauss--Laguerre, and Gauss--Hermite formulas. The methods combine globally convergent fourth-order iteration with asymptotic approximations selected for complementary parameter regimes. This improves speed, accuracy, and usable parameter ranges relative to existing algorithms. For Gauss--Jacobi quadrature, the MATLAB implementation removes earlier upper restrictions such as $\alpha,\beta\le 5$ and can compute nodes and weights up to degree $10^6$ for broad parameter ranges subject to underflow and overflow limits. The paper also gives a specialized efficient approach for Gauss--Legendre quadrature, adds subsampling and scaling strategies for Laguerre and Hermite rules, and treats Gauss--Radau, Gauss--Lobatto, and barycentric weights. Arbitrary-precision Maple algorithms are provided for symmetric cases, supporting high-precision computations with thousands of nodes.

### Contributions

1. Developed fast algorithms for classical Gaussian quadrature nodes and weights.
2. Combined fourth-order globally convergent iteration with asymptotic starting approximations.
3. Expanded the practical parameter range for Gauss--Jacobi quadrature.
4. Added efficient Gauss--Legendre, Laguerre, Hermite, Radau, Lobatto, and barycentric-weight computations.
5. Provided arbitrary-precision algorithms for symmetric high-accuracy cases.
