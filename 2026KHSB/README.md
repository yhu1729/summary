# 2026KHSB

## ChatGPT (July 2026)

### Summary

Forest-of-refinement-trees adaptive mesh refinement uses space-filling curves to distribute dynamic meshes cheaply, but mixed tetrahedral--hexahedral meshes require pyramids as conforming bridge elements. This paper supplies the missing pyramidal primitive for the open-source t8code framework. A pyramid is recursively divided into six pyramids and four tetrahedra in a construction that commutes with cubic refinement. Encoding each descendant by its enclosing subcube and one of two pyramid orientations yields a Morton-type index, which the authors prove is a valid space-filling-curve index. They derive parent, child, same-tree neighbor, inter-tree neighbor, and face transformations despite heterogeneous descendants and triangular and quadrilateral faces. At forest level, they generalize uniform construction, adaptation, partitioning, and ghost exchange, including load balancing for root shapes with different refinement counts. Large-scale tests show behavior comparable to existing element types and near-ideal scaling for central operations. A hybrid airplane-like mesh demonstrates the complete method with every supported three-dimensional element shape.

### Contributions

1. Defined a commutative pyramidal refinement into six pyramids and four tetrahedra using two pyramid orientations.
2. Constructed and proved validity of a Morton-type pyramidal space-filling-curve index.
3. Developed the complete set of low-level parent, child, face-neighbor, and cross-tree transformation algorithms.
4. Generalized forest construction and uniform partition bounds to mixed root shapes with unequal descendant counts.
5. Implemented the design in t8code and demonstrated scalable adaptation, partitioning, construction, and ghost exchange.
