# 2026MRHH

## Claude (September 2026)

### Summary

The authors perform integrated core–pedestal–scrape-off-layer (SOL) modeling of ARC H-modes with the ASTRA transport code to test whether high fusion power is compatible with a detached divertor. TGLF turbulent and FACIT neoclassical transport feed STRAHL, which evolves impurity charge states and radiation; a neural network trained on EPED predicts the pedestal; and the extended Lengyel model gives the SOL seeding fraction and separatrix temperature for a 2 eV divertor, all iterated to self-consistency. Pedestal and separatrix densities are prescribed, and the core seeded-impurity content follows an empirical SOL-to-core enrichment scaling imposed at the pedestal top. For an ARC V3A-like design with Ar seeding, the fusion power is about 900 MW. It varies little with pedestal density, drops to 800 MW when the separatrix-to-pedestal density ratio rises from 0.4 to 0.5 because the pedestal becomes ballooning-limited, and stays within 820–920 MW for enrichment factors of 50–200% of the scaling. Ne seeding gives lower enrichment, core accumulation, fuel dilution, lower fusion power, and less robust H-mode access. Turbulence dominates core impurity transport, giving nearly flat concentrations and weak W peaking, and modeled rotation changes little. Limitations include assumed separatrix density and enrichment, no ELM or He-ash modeling, and uncertain L–H thresholds.

### Contributions

1. Coupled the X-Lengyel, EPED neural-network, and core transport models by exchanging the power crossing the separatrix, separatrix temperature, SOL seeding fraction, divertor neutral pressure, enrichment, and pedestal $Z_\mathrm{eff}$, imposing detachment self-consistently in H-mode predictions.
2. Surveyed ARC-class designs with fields of 9.8–11.7 T and currents of 10.0–13.8 MA, finding that elongation slightly raises the mostly peeling-limited pedestal pressure while triangularity mainly shifts the density of the peeling-to-ballooning transition.
3. Traced the high predicted Ar pedestal concentrations to an enrichment of about 1.25 for ARC, against about 3 in ASDEX Upgrade, caused by the inverse dependence of the enrichment scaling on divertor neutral pressure.
4. Compared Ar, Ne, and an N-equivalent radiator, the latter giving 760–1000 MW with robust H-mode access, and showed that H-mode margins depend strongly on the chosen L–H threshold scaling.
5. Linked the lower W peaking at higher $Z_\mathrm{eff}$ to a larger W flux in standalone TGLF scans, and showed with standalone FACIT scans of density gradient, temperature gradient, and rotation that neoclassical W transport becomes large only above Mach number 0.4.

### Comments

- Section 4.4, Figs. 7–9: panel (c) is labelled $P_\mathrm{loss}/P_{LH,\mathrm{Schmidtmayr}}$, whereas the text defines the plotted $f_{LH,\mathrm{Schmidtmayr}}=P_{i,\mathrm{loss}}/P_{LH,\mathrm{Schmidtmayr}}$ with the ion power loss, and $P_\mathrm{loss}$ elsewhere, including panel (f), denotes the total power crossing the separatrix.
- Section 4.4, Table 2: the standard deviation of $\langle n_e\rangle$ for Ar is given as 0.26 (in $10^{19}$ m$^{-3}$) across the pedestal-density, enrichment, and separatrix-density scans, but Fig. 2(b) alone shows $\langle n_e\rangle$ from about 22.4 to 26.7 in the pedestal-density scan, which is incompatible with that value; the intended value is unresolved.
- Section 5: "Ne-seeded plasmas have shown lower fusion power (< 800 MW)" conflicts with the Abstract ("600–850 MW"), the Section 4.4 summary ("$600<P_{fus}<850$ MW"), and the Section 4.4 statement that Ne cases with lower accumulation reach "$P_{fus}>800$ MW"; the likely intended reading is 600–850 MW.
