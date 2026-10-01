# 2026BC

## Claude (September 2026)

### Summary

Particle simulations with thermal walls commonly reinject particles with flux-weighted Maxwellian momenta, which earlier simulations showed to thermalize an ideal gas whereas half-Maxwellian sampling does not. The authors consider non-interacting particles in a one-dimensional external potential $U$ that vanishes at both walls, reinjected with momentum density proportional to $p^ne^{-p^2/(2T)}$ for integer $n$: $n=0$ is the half-Maxwellian, $n=1$ the mass flux, and $n=3$ the energy flux. Equating the incoming phase-space flux at the walls to this rule and applying Jeans' theorem along trajectories that reach the walls gives the stationary distribution $f_n\propto H^{(n-1)/2}e^{-H/T}$ for any $U$, where $H$ is the single-particle energy; it is Maxwell–Boltzmann only for $n=1$. For $U=2\cos(q/2)$ on $[-\pi,\pi]$, a dimensionless coronal-loop potential, closed-form density and kinetic-temperature profiles show, for $n=0$, a logarithmically diverging density and logarithmically vanishing temperature at the walls; for $n=1$, an isothermal Boltzmann profile; and for $n=3$, a non-monotonic density with temperature falling from $3T$ at the walls. Fourth-order symplectic simulations with $2^{16}$ particles at $T=3$ reproduce all profiles. The authors state that self-consistent mean fields make the problem nonlinear and that trapped regions disconnected from the walls require additional information.

### Contributions

1. Derived the normalization $A_{T,n}=2^{(1-n)/2}T^{-(n+1)/2}/\Gamma(\frac{n+1}{2})$ and inverse-transform samplers, the absolute value of a Box–Muller Gaussian for $n=0$, $p=\sqrt{-2T\ln(1-r)}$ for $n=1$, and $p=\sqrt{2T[-1-W_{-1}(-(1-r)/e)]}$ for $n=3$, with the lower Lambert branch $W_{-1}$ computed by a branch-safeguarded Halley iteration started from branch-point and $x\to0^-$ asymptotic guesses.
2. Expressed the $n=0$ moments through modified Bessel functions, $n_0\propto e^{-U/(2T)}K_0(U/(2T))$ and $T_0=U[K_1(U/(2T))/K_0(U/(2T))-1]$, and expanded both about the domain center $q=0$ to show opposite-curvature quadratic behavior without linear terms, a density minimum and a temperature maximum there.
3. Obtained $n_3\propto(U+T/2)e^{-U/T}$ and $T_3=T(U+\frac32T)/(U+\frac12T)$ for energy-flux injection, attributing the non-monotonic density to competition between the energy prefactor $H$ and the Boltzmann factor.
4. Initialized every run in unit-temperature equilibrium by von Neumann rejection sampling, integrated with a fixed step $10^{-2}$, declared stationarity once the mean kinetic energy fluctuated about a constant, and compared time-averaged profiles with the analytic curves on the half-domain $[-\pi,0]$.
5. Offered a theoretical explanation of the earlier numerical finding that only mass-flux sampling thermalizes an ideal gas, extended it to arbitrary $n$ and general potentials, argued that it also holds when particles can escape, and proposed energy-flux injection ($n=3$) as an alternative model of heating pulses in the authors' two-component coronal-plasma simulations.

### Comments

- §1: long-range interactions are described as "mediated by two-body potentials decaying slower than $1/r^{-d}$ at large distances $r$", but $1/r^{-d}=r^{d}$ grows with $r$; the evident intended bound is $1/r^{d}$.
- §2 and Fig. 1 caption: the threshold $x_{\rm th}$ that switches between the $W_{-1}$ initial guesses Eq. (12) and Eq. (13) "is chosen empirically to ensure continuity of the initial guess", but at the reported $x_{\rm th}\simeq-0.30$ Eq. (12) gives $-1.39$ and Eq. (13) gives $-1.73$ (with $W_{-1}(-0.30)\approx-1.78$), a jump of 0.34, nearly the largest gap between the two guesses for $x\in[-1/e,-0.16]$, and they coincide only near $x\approx-0.16$; the intended threshold is unresolved.
