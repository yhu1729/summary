# 2026B

## Claude (September 2026)

### Summary

The author studies how the aperiodic geometry that a field line samples in a stellarator affects the structure of ion-temperature-gradient (ITG) eigenmodes. Extending a reduced fluid drift-wave model with an ion temperature gradient and expanding about the drift-wave-resonant branch $\Omega=\omega/\omega_{*e}=1+\Lambda$ gives a Hill equation $\phi''+\epsilon_n(1+\eta_i)K(\theta)\phi=-\Lambda\phi$ in the ballooning angle, where $K$ is the normalized magnetic drift, $\epsilon_n=L_n/R$, and $\eta_i=L_n/L_{T_i}$. Because the line samples incommensurate Boozer harmonics, $K$ is modeled as $\cos\theta+\lambda\cos(\alpha\theta+\delta)$ with irrational $\alpha$. Projecting onto Wannier functions of the lowest Mathieu band gives the Aubry–André–Harper (AAH) model, whose eigenstates all localize above unit effective coupling. For the continuous equation, localization is diagnosed by a positive transfer-matrix Lyapunov exponent at $\Lambda=0$. With $\lambda=1$, $\alpha\approx2.14$, and $\epsilon_n=0.12$, the exponent becomes persistently positive above $\eta_i^*\approx2.3$, against 2.8 for the periodic case, where positivity marks a Floquet gap instead; the onset is non-monotonic because the spectrum is a Cantor set. The result concerns mode structure on the drift-wave branch, not the ITG branch proper, at weak magnetic shear. The author states that its effect on transport, even in sign, and any link to ion-temperature clamping are unsettled.

### Contributions

1. Derived the two-fluid equation $\phi''+[\Omega(\Omega-1)+\epsilon_d(\theta)(\Omega+\eta_i)]\phi=0$ from adiabatic electrons, $\boldsymbol{E}\times\boldsymbol{B}$ advection of the ion temperature, and ion continuity and parallel momentum, and bounded its drift-wave-resonant reduction by $\epsilon_n(1+\eta_i)\lesssim1$.
2. Related the incommensurate wavenumber ratio to Boozer harmonics through field-line wavenumbers $k_{m,n}=m-n/\iota$, so that $\alpha$ is irrational for irrational rotational transform unless both harmonics belong to one family, and argued that field-period modularity does not restore periodicity along a line.
3. Expressed the AAH coupling as $\lambda_\mathrm{AAH}=\epsilon_n(1+\eta_i)\lambda F_\alpha/(2|t|)$ through the lowest-band Wannier hopping amplitude $t$ and a form factor $F_\alpha$ of the Wannier probability density.
4. Reported Lyapunov exponents converged in period number, integrator tolerance, and phase $\delta$ (within 0.5%), with isolated positive windows below onset, and predicted that the localized mode's position along the line varies with field-line label.
5. Estimated that finite-Larmor-radius confinement from global shear competes with the aperiodic mechanism near $\hat s\approx0.1$, placing W7-X near that bound, and set out opposing suppression and enhancement arguments that prevent any conclusion about clamping.

### Comments

- Section 2.1, last paragraph: "The genuine breakdown is the limit $L_n\to\infty$ at fixed $L_{T_i}$ … that limit is approached with $\epsilon_n\to0$ and $\eta_i\to\infty$ such that $A$ remains finite", but with $\epsilon_n=L_n/R$ and $\eta_i=L_n/L_{T_i}$ as defined in the same section, $L_n\to\infty$ gives $\epsilon_n\to\infty$ and $A=\epsilon_n(1+\eta_i)\to\infty$.
- Fig. 2 caption: the aperiodic model is said to use $\alpha=2+\sqrt{2}/10\simeq2.14$ "(the legend rounds this to 2.1)", but the legend reads "Aperiodic: $\lambda=1$, $\alpha\simeq2.14$".
- Section 5, item 3: "Both values carry an uncertainty of order 0.1 arising from the Cantor structure of the spectrum", but the second value, 2.8, belongs to the periodic ($\lambda=0$) case, which Sections 2.2 and 3.1 describe as a Mathieu problem with ordinary bands and Floquet gaps, and Section 3.1 attaches the uncertainty of order 0.1 only to $\eta_i^*\approx2.3$; the Cantor-structure uncertainty evidently applies to the aperiodic value only.
- Appendix B, Eq. (22): $t=-\int_0^1E_0(k)e^{2\pi ik}\,\mathrm{d}k\approx[E_0(k=0)-E_0(k=\tfrac12)]/4$, but keeping only the fundamental harmonic, $E_0(k)=\bar E+e_1\cos2\pi k$, the integral gives $t=-e_1/2$ while $[E_0(0)-E_0(\tfrac12)]/4=+e_1/2$, so the approximation and the band width $W=E_0(0)-E_0(\tfrac12)$ used after it have the opposite sign; Eqs. (26)–(27) are unaffected because they use $|t|$.
