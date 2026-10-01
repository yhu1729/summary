# 2026GCSB

## Claude (September 2026)

### Summary

The authors couple the full-wave solver AORSA, which computes a whistler eigenmode at 200 MHz and toroidal mode number $n=35$ in a DIII-D equilibrium, with the full-orbit code KORC to study pitch-angle scattering of runaway electrons (REs) in 3D tokamak geometry beyond quasilinear diffusion. The coupling is one-way: 10,240 REs with energies uniform in 1–20 MeV and initial pitch angle $10^\circ$ first relax without waves for 1 ms and then evolve for 2 ms in the prescribed fields, with no damping mechanism included. After the waves are switched on, the mean and variance of the pitch-angle distribution increase monotonically, skewness and kurtosis rise transiently, a high-pitch-angle tail develops, and the number of confined REs decays linearly. Pitch-angle increments over one wave period have Gaussian cores and Laplace (exponential) tails. The variance of pitch-angle displacements scales as $t^\alpha$ with $\alpha$ depending on initial energy: sub-diffusive for 1–3 MeV, diffusive only in a few bins, and super-diffusive for most energies between 4 and 17 MeV. The authors conclude that the dynamics are intermittent and not captured by quasilinear theory over these time scales, and caution that the finite simulation time may not reveal the asymptotic scaling.

### Contributions

1. Coupled AORSA full-wave whistler fields with KORC full-orbit tracking, capturing eigenmodes with many coupled poloidal harmonics and a range of local parallel wavenumbers that slab and single-mode resonance models omit.
2. Measured Laplace tail scales of 1 and 0.65 for positive and negative pitch-angle kicks at $1$–$5^\circ$ and 8–10 MeV, and a symmetric scale of 0.75 at $6$–$16^\circ$ and 8–9 MeV, as input for kick-type reduced transport models.
3. Resolved the transport exponent both in broad initial-energy groups and in 1 MeV bins, the latter alternating between diffusive and super-diffusive behavior above 12 MeV.
4. Found that 1–5 MeV REs roughly double their mean kinetic energy, 10–15 MeV REs lose energy on average, and 15–20 MeV REs keep a nearly constant mean energy, with a power-law positive tail (exponent about 1.39) in normalized energy changes.
5. Argued that the Laplace statistics and anomalous variance scaling contradict the small, uncorrelated kicks assumed by quasilinear theory, and linked the pitch-angle increase to possible RE mitigation through enhanced synchrotron losses.

### Comments

- Section IV, Eq. (5): the kurtosis is written $\gamma_{2,\eta}=\langle(\eta-\mu_\eta)^4-3\rangle/\sigma_\eta^4$, which subtracts a pure number inside an average of a quantity in degrees$^4$; the text calls it the normalized fourth central moment, and the values near 3 in Fig. 2(d) before the waves are switched on indicate $\langle(\eta-\mu_\eta)^4\rangle/\sigma_\eta^4$.
- Section IV, Fig. 4: the text reports "a prompt loss of about 700 particles", but Fig. 4 drops from 10,240 to about 9,350 confined particles at the start, a loss of about 900.
- Section IV, Fig. 5(b): the text assigns $\lambda=1$ to the positive tail and $\lambda=0.65$ to the negative tail, but the legend labels the blue dashed line on the positive tail "$\lambda$=0.65" and gives "$\lambda$=1.0" a red dashed style shared with the Gaussian; the slope of the positive-tail line corresponds to $\lambda\approx1$, so the legend labels appear swapped.
- Fig. 5 caption: panel (b) is described as the distribution "on log-log scale", but it plots $\log_{10}$ of the PDF against a linear $\Delta\eta$ axis that includes negative values, i.e. on a semi-log scale.
- Section VI, Fig. 9: the text lists four groups, (a) 1–5, (b) 5–10, (c) 10–15, and (d) 15–20 MeV, but Fig. 9 labels only (a) 1–5, (b) 10–15, and (c) 15–20 MeV; its fourth, unlabelled plot starts at 7.5 MeV and is evidently the 5–10 MeV group.
- Section VI: "those with $K_0>10$ MeV exhibit modest energy gain of approximately 1 MeV" conflicts with the next sentences, which state that the 10–15 MeV group loses energy and the 15–20 MeV group stays nearly constant, as Figs. 9(b) and 9(c) show; the unlabelled 5–10 MeV plot rises by about 1 MeV, so the evident intended reading is $K_0=5$–10 MeV.
