# 2026LLR

## ChatGPT (July 2026)

### Summary

This work addresses geometric robustness in the three-dimensional particle finite element method (PFEM) for chaotic free-surface flows. Instead of reconstructing the fluid domain with a classical $\alpha$-shape, it advects the boundary and uses winding-number tests to classify remeshed tetrahedra, improving the treatment of topology changes and mass conservation. Adaptation proceeds in two stages: edge splitting refines the free surface while preserving its shape, then circumcenter insertion refines the interior according to a prescribed size field. Solid and fluid geometries are decoupled through inside/outside queries, segment--triangle intersections, and point projections, which also support slip boundaries. Dam-break comparisons reproduce measured and published pressure histories, while tire-splash and point-cloud-derived ``triangle soup'' examples demonstrate operation on complex, poor-quality, and non-watertight inputs. The resulting framework makes PFEM remeshing locally adaptive and tolerant of industrial geometry defects, although sliver control and parallel or GPU acceleration remain future work.

### Contributions

1. Replaced $\alpha$-shape domain recovery with advected-boundary winding-number classification.
2. Designed separate surface edge-splitting and volume circumcenter-insertion adaptation stages.
3. Reduced topology-change mass errors while preserving free-surface geometry.
4. Decoupled solid and fluid meshes through a small set of robust geometric queries.
5. Validated the approach on dam-break, tire-splash, and non-watertight-geometry simulations.
