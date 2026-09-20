# 2026TDAZ

## ChatGPT (July 2026)

### Summary

This work extends the hermes-3 drift-reduced fluid model to rapidly rotating, low-$\beta$ plasmas by adding centrifugal inertia and relaxing the Boussinesq approximation, then studies Kelvin--Helmholtz (KH), curvature-driven interchange (CDI), and rotation-driven interchange (RDI) modes in two-dimensional simulations. The implementation reproduces theoretical KH and CDI growth rates and first-order finite-Larmor-radius stabilization. For RDI, the authors distinguish weak-shear, strong-shear, and fully shear-stabilized regimes and propose the local susceptibility condition $|L_v|/L_n>-1$. Profiles satisfying it everywhere avoid full RDI turbulence in the tested runs, but stability is highly profile-sensitive. Finite-Larmor-radius effects are appreciable for $\rho_i/a=0.16$ and small for $0.01$. A KH-unstable quartic velocity profile can trigger interchange crashes even when the initial criterion predicts stabilization. The analysis is limited to $k_\parallel=0$ azimuthal dynamics; three-dimensional mirror geometry may change the conclusions.

### Contributions

1. Added centrifugal-force physics and a non-Boussinesq vorticity formulation to hermes-3.
2. Verified simulated KH and CDI growth rates against analytic or semi-analytic predictions.
3. Demonstrated gyroviscous finite-Larmor-radius stabilization and its dependence on $\rho_i/a$.
4. Identified three RDI regimes and proposed the profile criterion $|L_v|/L_n>-1$.
5. Showed that global KH modes can defeat nominal RDI shear stabilization.
