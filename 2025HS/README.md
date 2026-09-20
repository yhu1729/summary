# 2025HS

## ChatGPT (July 2026)

### Summary

This paper improves error estimates for Gauss-Christoffel quadrature when the integrand has limited endpoint regularity. Classical Chebyshev-coefficient and quadrature bounds require a weighted bounded-variation condition involving $(1-x^2)^{-1/2}$, which can fail for functions with endpoint singularities. The authors derive a recurrence relation for derivatives of Chebyshev polynomials that permits a weaker assumption: absolute integrability of $f^{(r+1)}$ without the singular weight. This yields new Chebyshev coefficient decay estimates and a Gauss-Christoffel quadrature error bound depending on $U_r=\int_{-1}^{1}|f^{(r+1)}(x)|\,dx$ rather than the classical weighted quantity $V_r$. The estimates are extended to Gauss-Gegenbauer rules, including Gauss-Legendre and Gauss-Chebyshev cases. Numerical tests show that the new bounds remain finite and useful for endpoint-singular functions where older bounds become extremely large or infinite, and can also be smaller for smooth examples.

### Contributions

1. Proved a new recurrence identity for higher derivatives of Chebyshev polynomials.
2. Replaced weighted endpoint-regularity assumptions with an unweighted $L^1$ derivative condition.
3. Derived improved Chebyshev coefficient decay bounds under reduced regularity.
4. Established corresponding Gauss-Christoffel and Gauss-Gegenbauer quadrature error estimates.
5. Validated the estimates on endpoint-singular and smooth numerical examples.
