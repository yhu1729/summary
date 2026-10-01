# 2026WH2

## ChatGPT (July 2026)

### Summary

This paper presents a dynamical low-rank solver that compresses the three-dimensional velocity dependence of kinetic equations in tensor-train (TT) form while treating physical space parametrically. A projector-splitting integrator updates the TT cores through directional sweeps, avoiding the full high-dimensional step followed by truncation used in step-and-truncate methods. The local representation limits rank growth caused by coupling space and velocity, and it exploits the rank-one structure of Maxwellian equilibria. The formulation is combined with problem-specific spatial and temporal discretizations and tested on homogeneous and inhomogeneous kinetic models, including Vlasov--Ampere--Fokker--Planck dynamics. Experiments reproduce relaxation, Landau damping, and two-stream behavior with small prescribed ranks, and diagnostics show that effective ranks remain low in collisional or near-equilibrium regimes. Collisionless phase mixing can demand higher ranks, which the authors identify as a limitation and motivation for local, anisotropic, and adaptive rank strategies.

### Contributions

1. Formulated a velocity-local tensor-train representation for multidimensional kinetic equations.
2. Adapted projector splitting to evolve TT cores without forming or truncating a full velocity tensor.
3. Exploited the rank-one Maxwellian structure to target near-equilibrium and collisional regimes efficiently.
4. Verified the method on homogeneous relaxation and spatially inhomogeneous plasma benchmarks.
5. Quantified effective-rank behavior and identified local and anisotropic rank adaptation as natural extensions.
