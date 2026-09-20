# 2026CMSV

## ChatGPT (July 2026)

### Summary

The paper develops a kinetic-equilibrium-prediction workflow for preparing complete TCV tokamak discharges by loosely coupling RAPTOR's rapid 1.5D transport prediction to FBT's inverse free-boundary equilibrium solver. Pulse-schedule inputs, an assumed confinement factor, and line-averaged density drive predictions of current, density, electron and ion temperature, pressure-gradient $p'$, and $TT'$ profiles; FBT returns equilibrium geometry and feedforward poloidal-field coil currents. The authors extend RAPTOR's gradient-based model to ion transport and negative-triangularity plasmas and adapt the Martin scaling to predict confinement transitions across magnetic configurations. A 211-shot benchmark spanning ohmic and NBI heating, L/H modes, and varied shapes finds total thermal energy generally within 20% when experimental line-averaged density is supplied; 48 of 51 confidently classified H-mode transitions are predicted within $100\,\mathrm{ms}$. RAPTOR--FBT converges self-consistently within a few iterations and minutes. Experimental deployment improves X-point alignment and stabilizes a challenging upper-negative-triangularity snowflake configuration, while exposing density prediction and radiation modeling as important limitations.

### Contributions

1. Introduced a RAPTOR--FBT workflow for rapid, full-discharge TCV shot preparation.
2. Extended RAPTOR's reduced model to ion heat transport, negative triangularity, and geometry-dependent L/H-transition prediction.
3. Validated the pre-shot transport model statistically over 211 diverse TCV discharges.
4. Established a fast iterative exchange of kinetic profiles, geometry, and coil currents that reaches self-consistency within minutes.
5. Demonstrated improved feedforward shape control, including sustained X-point positioning in an upper-negative-triangularity snowflake plasma.
