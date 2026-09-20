# 2026LXWZ

## ChatGPT (July 2026)

### Summary

The paper resolves a discrepancy between theoretical and observed polynomial-degree convergence of a one-dimensional $hp$ local discontinuous Galerkin method for convection--diffusion equations with singular solutions. Its central device is a fractional-regularity framework in which endpoint singularities are characterized through Caputo derivatives, while exact Legendre-coefficient formulas yield sharp Gauss--Radau projection estimates. These estimates produce explicit $h$- and $p$-version a priori bounds for pure convection and convection--diffusion problems. The analysis distinguishes endpoint singularities, interior singularities aligned with a mesh node, and interior singularities lying inside an element; the unfitted case has substantially lower $p$-convergence. For a singularity behaving as $|x-\theta|^\alpha$, attainable rates depend on $\alpha$, an additional fractional regularity index, diffusion, and mesh alignment. Numerical experiments reproduce all predicted rates and correct the earlier interpretation of the diffusion example. The analysis is restricted to the one-dimensional Castillo--Cockburn--Sch\"otzau--Schwab LDG formulation, although the framework suggests how analogous $p$-suboptimality may be addressed elsewhere.

### Contributions

1. Introduced Caputo-derivative spaces that characterize algebraic singularities for Gauss--Radau approximation.
2. Derived sharp Legendre-coefficient projection bounds and $p$-optimal LDG estimates for endpoint singularities.
3. Extended the theory to mesh-fitted interior singularities and quantified their convective and diffusive rates.
4. Established lower rates for unfitted interior singularities, showing the benefit of mesh alignment.
5. Validated the endpoint, fitted, and unfitted estimates and corrected the motivating diffusion convergence rate.
