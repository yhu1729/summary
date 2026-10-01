# 2026CGG

## Claude (September 2026)

### Summary

The authors propose self-consistent beam-dynamics simulations including geometric wakefields without interpolating particle currents onto a mesh. In a scattered-field formulation, the total field is the sum of an incident field, taken as the beam's free-space space-charge field (SCF), and a scattered (wake) field that solves the source-free Maxwell equations with $\boldsymbol{n}\times\boldsymbol{E}_s=-\boldsymbol{n}\times\boldsymbol{E}_i$ on perfectly conducting walls. Discretized with the Finite Integration Technique (FIT) on a window moving at the speed of light, this boundary condition becomes an equivalent magnetic current, with a boundary-conformal variant for curved walls. The SCF comes from a rest-frame Green's-function solver at the particles and, at the walls, from a fast multipole method (FMM) or retarded Liénard–Wiechert (LW) fields; the wakefield uses a dispersion-free split-operator scheme. For a rigid 15 MeV bunch in uniform pipes, the steady-state field matches the analytic solution and converges at second order in rectangular pipes, and in a circular pipe the conformal current is far more accurate than a staircase one. In the seven-cell SuperKEKB RF photo-gun, wakefields raise the exit energy spread by about 14%, consistently with full electromagnetic particle-in-cell (CST) simulations, while needing about 8 GB and under 1.5 h instead of 160 GB and about 10 h.

### Contributions

1. Split the beam-driven Maxwell problem into space-charge and wakefield subproblems coupled only through a magnetic boundary current, so that each uses its own mesh, time step (with integer sub-cycling of the SCF solver), and specialized code.
2. Introduced a boundary-conformal magnetic current $(\mathbf{C}\mathbf{R}_l-\mathbf{R}_A\mathbf{C})\widehat{\mathbf{e}}_i$ built from cut-edge and cut-face ratios, which reduces to the staircase current on mesh-aligned walls.
3. Computed incident boundary voltages with an asymmetric source–target FMM that treats the cathode with image charges, and alternatively with LW fields whose retarded times are found by bisection over stored trajectories.
4. Decomposed the steady-state space-charge wake in a pipe into free-space SCF and scattered field, showing that the scattered field compensates the SCF, and simulated a dual-bunch corrugated waveguide with beam loading, giving witness gradients of 5.2 and 4.71 MV/m against measured 4.93 and 5.02 MV/m.
5. Showed that retardation delays the gun wakefield, so the quasistatic FMM model locally overestimates the energy spread near irises and systematically overestimates the energy loss, while the final energy spread nearly agrees and mean-energy differences remain at the few-per-mille level.

### Comments

- Section 4.1, Eq. (16): the back-transformed fields are written $B_x=-\sqrt{\gamma_0^2-1}\,E'_y$ and $B_y=\sqrt{\gamma_0^2-1}\,E'_x$, which are dimensionally inconsistent in the SI units used throughout ($\boldsymbol{D}=\varepsilon_0\boldsymbol{E}$, and $\boldsymbol{B}=\frac{1}{c}\boldsymbol{n}_p\times\boldsymbol{E}$ in Eq. (17)); the evident intended reading divides both by $c$.
- Section 6.3, Figs. 4 and 5: Fig. 5 is introduced as the decomposition of the steady-state solution for the $w=100$ mm, $h=15$ mm pipe shown in Fig. 4, but its total field peaks near 143 V/m, whereas Fig. 4 peaks near 162 V/m; Eqs. (19)–(20) with the Section 6.2 bunch give about 163 V/m for $h=15$ mm and 144 V/m for $h=10$ mm, so Fig. 5 appears to use the $h=10$ mm pipe of Fig. 6, which neither the text nor the caption states.
- Section 6.4, Fig. 7: the text states that "the second order convergence is fully recovered when the conformal boundary approach introduced in Section 3.3 is used" (and the Conclusion calls it "optimally convergent"), but the conformal errors in Fig. 7 fall from about $4\times10^{-3}$ at $\sigma_z/\Delta=4$ to about $4\times10^{-4}$ at 24, an average rate near 1.3, and remain above the plotted second-order guide line; unresolved.
