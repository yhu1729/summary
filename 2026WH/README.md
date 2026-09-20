# 2026WH

## ChatGPT (July 2026)

### Summary

Wang and Hu improve the local-relabeling bidirectional buffer used for open boundaries in SPHinXsys, targeting particle flows with strong backflow or several closely arranged inlets and outlets. A hysteresis-like offset separates particle relabeling from particle generation, preventing repeated creation and overlap during backflow. Unique buffer identifiers and geometric containment checks stop one buffer from deleting or processing another buffer's particles. A reproducing-kernel gradient correction with a mirror treatment raises the pressure boundary from zeroth- to first-order consistency. The modifications apply to laminar weakly compressible smoothed particle hydrodynamics and turbulent Reynolds-averaged calculations and require limited changes to the existing framework. Straight and U-shaped channels, laminar and turbulent plane jets, and a three-dimensional self-rotational micromixer demonstrate improved stability and agreement with finite-volume or experimental references. Residual equation-of-state pressure fluctuations, resolution dependence, and an empirically selected buffer offset remain limitations.

### Contributions

1. Introduced an offset generation boundary that prevents runaway particle creation under strong backflow.
2. Added buffer ownership identifiers that eliminate erroneous cross-buffer particle deletion.
3. Constrained effective buffer domains geometrically so arbitrarily arranged inlets and outlets remain independent.
4. Derived a mirror-corrected reproducing-kernel pressure treatment with first-order boundary consistency.
5. Validated laminar and turbulent flows in channels, jets, and a 1.35-million-particle three-dimensional micromixer.
