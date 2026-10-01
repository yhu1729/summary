# 2026WJPA

## ChatGPT (July 2026)

### Summary

EDAM, the Equilibrium Derivative in Arbitrary Mesh code, computes first-, second-, and third-order derivatives of tokamak equilibrium poloidal flux directly at nodes of an unstructured triangular mesh. After transforming the Grad--Shafranov operator to a Cartesian Laplacian form, the method derives a second-kind Fredholm boundary-integral equation for the normal flux derivative. Spectral tangential differentiation and the Grad--Shafranov equation supply higher boundary derivatives, while independently solved linear derivative equations propagate them through the interior by finite elements. Validation against Cicogna's nonlinear D-shaped analytic equilibrium shows approximately second-order $L^2$ convergence for all three derivative orders, avoiding the progressive accuracy loss of repeated direct differentiation. Applied to KSTAR discharge 18602 on a mesh of 19,838 triangles, EDAM yields smooth derivatives through third order at arbitrary nodes. The current boundary-integral formulation assumes a constant-flux boundary and is therefore unsuitable when a computational boundary outside the plasma crosses a diverted X-point. Third derivatives can also inherit spectral boundary error, and broader device validation remains needed.

### Contributions

1. Derived a boundary-integral equation for the normal derivative on constant-flux boundaries.
2. Constructed boundary formulas for second- and third-order poloidal-flux derivatives.
3. Formulated linear derivative Grad--Shafranov equations on arbitrary triangular meshes.
4. Implemented the modular EDAM workflow for equilibrium data, meshing, and finite-element solves.
5. Demonstrated uniform second-order convergence and a practical KSTAR reconstruction.
