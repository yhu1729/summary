# 2026DBTT

## Claude (September 2026)

### Summary

The Godunov–Peshkov–Romenski (GPR) model describes fluids and solids by one first-order hyperbolic system for density, momentum, energy, a distortion field $A$, and a thermal impulse $J$, whose stiff relaxation sources recover the compressible Navier–Stokes–Fourier equations as the relaxation times $\tau_1,\tau_2\to0$. Its acoustic, shear, and heat waves make explicit schemes costly. Extending an earlier Cartesian four-split scheme to unstructured triangles, the authors split the system into convective, temperature, mechanical, and pressure subsystems. Only convection is explicit, so the time step depends on material velocity alone. The implicit stages reduce to symmetric positive definite scalar wave equations for temperature and pressure, solved by conjugate gradients, and a nonsymmetric vector wave equation for the nodal velocity, solved by GMRES. Momentum, $A$, and $J$ live in cells and density, energy, pressure, and temperature at vertices; corner-normal discrete operators satisfying discrete curl–gradient and divergence–curl identities keep $A$ and $J$ curl-free when sources are absent or linear. Formal expansions show consistency with the Navier–Stokes stress and Fourier heat flux, and the pressure step recovers the low-Mach limit. Tests include Taylor–Green vortex, Riemann, shear-flow, lid-driven-cavity, solid-rotor, and explosion problems. Rescaling $A$ to enforce its determinant constraint, applied only in viscous regimes, breaks the curl-free property.

### Contributions

1. Extended the four-split semi-implicit GPR scheme to unstructured triangular meshes, which the authors describe as the first all-Mach-number GPR solver on unstructured meshes that respects both discrete vector-calculus identities.
2. Built a vertex-staggered collocation with mutually adjoint corner-normal gradient, divergence, and curl operators and a compatible final update of the distortion field and thermal impulse that starts from the old time level.
3. Reduced the mechanical subsystem, written for the trace-free metric tensor, to a single vector wave equation for the nodal velocity by eliminating the metric tensor and thermal impulse through semi-implicit stress approximations.
4. Showed by Chapman–Enskog-type expansions that the discrete scheme yields the Navier–Stokes stress with viscosity $\mu=\rho_0c_s^2\tau_1/6$ as $\tau_1\to0$ and a consistent Fourier heat flux as $\tau_2\to0$.
5. Verified second-order convergence of density errors in the acoustic Mach number down to $\mathrm{Ma}=5\times10^{-4}$ and curl errors of $A$ and $J$ at machine precision in a solid-rotor test.

### Comments

- §2.2, Eq. (17c): the primitive-variable temperature subsystem is written as $\frac{c_v}{Tc_h^2}\frac{\partial T}{\partial t}+\frac{\partial J_k}{\partial x_k}=0$, but eliminating $\mathcal E$ from (16b)–(16c) with $\rho$, $\mathbf v$, and $\mathbf A$ fixed, using $\mathcal E_1=\rho c_vT$ (from (3) and $T=\partial_{\rho S}\mathcal E$), $\mathcal E_4=\frac12c_h^2\rho J_iJ_i$ (3), $q_k=\rho c_h^2TJ_k$ (5), and $\theta_2=\rho c_h^2\tau_2$ (7), gives the right-hand side $J_kJ_k/(\tau_2T)$, the relaxation heating that corresponds to $\beta_k\beta_k/(T\theta_2)$ in (2); the discrete form (45b) also omits it. Whether the term was dropped deliberately is unresolved.
