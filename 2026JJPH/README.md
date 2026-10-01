# 2026JJPH

## ChatGPT (July 2026)

### Summary

This work introduces a continuum modal discontinuous Galerkin solver for the relativistic Vlasov--Maxwell equations in Gkeyll. A mixed nodal--modal representation of the Lorentz factor and current eliminates weak-form aliasing, proving semidiscrete energy conservation and $L^2$ stability, while independently mapped four-velocity coordinates span large energy ranges without particle-in-cell sampling noise. In a pulsar-inspired pair discharge, density grows by about $10^3$ and particles reach $\gamma\sim5\times10^3$; Gkeyll screens the electric field and resolves a smooth distribution over four decades in four-velocity. A $2x3v$ reconnection run at magnetization $\sigma=1$ recovers the expected local $dN/d\gamma\propto\gamma^{-4}$ spectrum. Linear instability tests match warm relativistic theory, and temporal energy errors scale as $\Delta t^3$. The method is expensive: the reconnection example costs about $5\times10^5$ CPU-hours. It presently lacks exact Gauss-law enforcement, strict positivity, photons, and self-consistent pair production.

### Contributions

1. Constructed an energy-conserving, $L^2$-stable relativistic Vlasov--Maxwell DG method.
2. Introduced mapped four-velocity grids with conservation-compatible geometric factors.
3. Resolved a noise-free pair discharge across large density and velocity ranges.
4. Matched relativistic instability theory and verified temporal energy convergence.
5. Recovered spatially local nonthermal spectra in relativistic magnetic reconnection.
