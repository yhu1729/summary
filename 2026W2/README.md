# 2026W2

## ChatGPT (July 2026)

### Summary

The paper develops an exact functional expansion built from recursive differential identities rather than local Taylor polynomials. In multiple dimensions, it writes a smooth function as divergence terms whose polynomial weights and derivatives are systematically related. Applying the divergence theorem converts volume integrals over flat-faced polytopes into facet integrals and recursively into lower-dimensional boundary data, avoiding interior tessellation. A complex displacement of the expansion center, chosen from roots of unity, cancels selected low-order remainder terms; conjugate pairing then produces real quadrature formulas with higher polynomial exactness and few function evaluations. The paper also derives the affine geometry needed for implementation, including transformations of normals and surface measures between parameter and physical facets. The framework provides a systematic route to high-order integration on arbitrary polytopes, although broad numerical benchmarking is not presented.

### Contributions

1. Derived a one-dimensional exact functional expansion from repeated product-rule identities.
2. Extended the construction to $\mathbb{R}^n$ as a recursive divergence expansion.
3. Used complex centers and roots of unity to cancel lower-order quadrature errors while retaining real-valued rules.
4. Formulated recursive polytope integration without simplex tessellation.
5. Proved affine transformation laws for facet normals and surface measures.
