# 2026MNM

## ChatGPT (July 2026)

### Summary

This paper constructs a fully discrete continuous Galerkin finite-element method for initial-boundary-value advection--diffusion problems using summation-by-parts operators in both space and time. Initial and boundary conditions are imposed weakly through simultaneous approximation terms. Matching the discrete integrations by parts to the continuous energy argument yields a bound controlled by initial and external boundary data, establishing energy stability for the complete space--time discretization rather than only its spatial part. The authors analyze both global temporal elements and a one-step multistage implementation. Manufactured-solution tests across diffusion- and advection-dominated regimes show superconvergence of order $\mathcal{O}(p+2)$ in space and time for Lagrange degree $p\geq2$. An oscillatory advection--diffusion application demonstrates that coarse temporal meshes still resolve space--time variation, while comparisons with explicit fourth-order Runge--Kutta integration report two to three orders of magnitude lower normalized computational cost in the studied cases. The present analysis is restricted to linear equations; extension to nonlinear problems is left for future work.

### Contributions

1. Formulated a continuous Galerkin discretization with summation-by-parts structure in both space and time.
2. Imposed initial and boundary data weakly with simultaneous approximation terms.
3. Proved a fully discrete energy estimate controlled by prescribed data.
4. Demonstrated $\mathcal{O}(p+2)$ spatial and temporal superconvergence for $p\geq2$.
5. Showed coarse-mesh accuracy and large cost reductions relative to explicit RK4 in oscillatory tests.
