# 2026SHJH

## Claude (September 2026)

### Summary

The authors present grid generation and geometry computation for a standard field-aligned coordinate system $(\psi,\alpha,\theta)$ that enables two-dimensional axisymmetric gyrokinetic simulations spanning the core, scrape-off layer, and private-flux regions of diverted tokamaks. Such coordinates are singular at X-points, where the poloidal field vanishes and the Jacobian $J_c=s(\psi)R/|\nabla\psi|$ diverges. Here $\theta$ is poloidal arc length along a flux surface normalized to $2\pi$, and $\alpha$ is a field-line label giving $\boldsymbol{B}=\nabla\psi\times\nabla\alpha$. Each topologically distinct region is split at the X-point into blocks, 12 for double null and 6 for single null, whose cell corners meet exactly at the X-point, leaving no gap. Because the discontinuous-Galerkin scheme of Gkeyll evaluates characteristics and fluxes only at interior and surface Gauss–Legendre points, no geometric quantity is evaluated at the X-point. Grid points come from root finding on a piecewise-polynomial $\psi(R,Z)$, and metric coefficients follow from analytic $\theta$-derivatives and finite differences in $\psi$. Enclosed-volume, manufactured-solution Poisson, and Gaussian-advection tests converge at average orders above one, though more slowly near the X-point. A double-null STEP simulation remains well behaved at the X-points and conserves particles to machine precision. The authors note coarse grid spacing near the X-point and leave 3-D turbulence simulations to future work.

### Contributions

1. Wrote the drift-kinetic gyrokinetic equation and Poisson equation in general computational coordinates and their axisymmetric limit with $\alpha$ ignorable, evolving $JJ_cf$ in conservative form.
2. Chose the parallel coordinate as normalized poloidal arc length, which, unlike the poloidal angle or $Z$, works on both open and closed field lines and allows arbitrarily shaped divertor plates.
3. Kept block boundaries consistent by sharing surface quadrature nodes and normal vectors and by rescaling fluxes with the block Jacobian normalizations at radial block boundaries, the only place they change.
4. Quantified the X-point penalty: the average enclosed-volume order drops from 3.31 to 1.42, and the high-resolution Poisson order from 1.44 away from the X-point to 1.2 on it, while advection past the X-point converges at 1.55.
5. Generated multi-block grids for double-null STEP and single-null ASDEX Upgrade equilibria and ran a 100 MW deuterium STEP simulation with ad hoc diffusivities chosen for a 2 mm heat-flux width, releasing the input files.

### Comments

- Section 2: "At the X- and O-points of a tokamak configurations, however, we have $J_c=0$ for field-line-following coordinates" conflicts with Eq. (4.4), $J_c=s(\psi)R/|\nabla\psi|$, and with Sections 4.1, 5, and 6.1, which state that the vanishing $\nabla\psi$ makes the Jacobian diverge; the evident intended reading is that $J_c$ diverges ($J_c^{-1}\to0$).
- Section 3.3, Eq. (3.26): the last term of $\dot z^3$ is printed as $+\frac{b_2}{qJ_cB_\parallel^*}\frac{\partial H}{\partial z^1}$, but taking $i=3$ in Eq. (3.20) gives $\epsilon^{321}b_2\,\partial H/\partial z^1$ with $\epsilon^{321}=-1$; with the printed sign, Eqs. (3.25)–(3.27) do not conserve $H$, so the evident intended sign is minus.
- Section 5, Eq. (5.1): the equation for $F=\mathcal{J}J_cf$ is written in advective form, $\partial_tF+\dot z^i\,\partial F/\partial z^i+\dot v_\parallel\,\partial F/\partial v_\parallel=0$, whereas Eq. (3.16) is the conservative form, and the weak form Eq. (5.3), said to follow from Eq. (5.1) by integration by parts, is that of the conservative form; the conservative form is evidently intended.
- Fig. 1(a): the sub-caption says tracing "starts in each region at $Z_\mathrm{lower}(\psi)$ (marked in blue) and stops at $Z_\mathrm{upper}(\psi)$ (marked in red)", but the panel legend marks the upper boundary in blue and the lower boundary in red, as does the Fig. 1(b) sub-caption.
- Section 7.1, Table 1: the caption gives the average order of convergence without the X-point as 3.37, whereas the text states 3.31, which is the mean of the tabulated orders (0.58, 5.02, 2.16, 5.47).
- Section 7.3: the simulation is said to run for "$2.0\times10^6$ s", but Fig. 7(b) is labelled $t=2.0\mathrm{e}{-06}$ s, and only $2\times10^{-6}$ s moves the bump the stated 0.2 m at $v_0=10^5$ m s$^{-1}$.
- Section 7.3: the initial and final bumps are centred by $(Z-2.1)$ and $(Z-1.9)$, i.e. at $Z=+2.1$ and $+1.9$, which would move them in $-\hat Z$ against $\boldsymbol{v}=v_0\hat Z$, whereas Fig. 7 shows them at $Z\approx-2.1$ and $-1.9$ beside the X-point at $(2,-2)$; the evident intended reading is $(Z+2.1)$ and $(Z+1.9)$.
- Section 7.3: both "Gaussian" profiles are written $n=e^{[(R-2.2)^2+(Z\mp\ldots)^2]/0.1^2}$ without the minus sign in the exponent, which makes them grow away from the centre, contrary to the bumps shown in Fig. 7.
