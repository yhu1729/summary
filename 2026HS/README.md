# 2026HS

## ChatGPT (July 2026)

### Summary

This paper constructs and analyzes local time-integration methods for discontinuous Galerkin discretizations of two-field Friedrichs systems, including Maxwell and acoustic wave equations. These problems become locally stiff when only a small mesh region is highly refined or has large wave speed. The method applies leapfrog integration to the nonstiff degrees of freedom and modifies the evolution locally through a general filter function. Polynomial Chebyshev filters yield fully explicit local time stepping, while a rational filter recovers a known locally implicit method. The authors establish sufficient filter conditions for stability under a CFL restriction independent of the fine mesh region and prove second-order convergence in time with optimal spatial order. Maxwell-equation experiments validate the estimates and show that the explicit leapfrog-Chebyshev method is most efficient when refinement is confined to a small portion of the mesh.

### Contributions

1. Formulated a leapfrog-based local time-integration family for central-flux discontinuous Galerkin discretizations of two-field Friedrichs systems.
2. Unified fully explicit local time stepping and locally implicit integration through a common filter-function framework.
3. Constructed Chebyshev polynomial filters that remove the fine-region restriction from the global CFL condition.
4. Proved stability, second-order temporal convergence, and optimal spatial convergence under verifiable filter assumptions.
5. Showed on Maxwell problems that the explicit method is efficient when stiffness is confined to a small refined region.
