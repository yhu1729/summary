# 2026FPBT

## ChatGPT (September 2026)

### Summary

This study compares electromagnetic load models for mirrors in the ITER electron cyclotron emission diagnostic during a prescribed severe plasma disruption. The diagnostic's copper mirrors experience eddy-current forces and torques that must be supplied to subsequent structural analysis. A simplified ANSYS Maxwell model uses six Helmholtz coil pairs to impose locally uniform magnetic fields and their time derivatives. The authors compare this approximation with an existing global APDL model and a new transient Maxwell model covering a $20^\circ$ ITER sector with the Bay3 components. For the plasma-facing mirrors, global-model torques are approximately 40–50% of the simplified-model values because the latter combines conservative field-variation envelopes. Conversely, the global Maxwell model predicts peak net forces about five times larger than the simplified model. The study therefore recommends global transient modeling to capture spatial field variations and obtain loads consistent with the APDL reference. The comparisons concern one disruption scenario and electromagnetic loading; combined thermal, nuclear, seismic, and structural qualification remains subsequent work.

### Contributions

1. Constructed a local Helmholtz-coil model that independently prescribes background magnetic fields and field-variation rates in three directions for ITER ECE load estimation.
2. Developed a transient $20^\circ$ global Maxwell sector model incorporating the Bay3 mirrors for the same prescribed disruption used in the APDL reference.
3. Showed that conservative local field-variation envelopes overestimate plasma-facing mirror torques relative to both global modeling approaches.
4. Identified an opposing force discrepancy: global Maxwell peak forces are about five times the local-model predictions, so torque conservatism does not imply conservative force estimates.
5. Established a comparison-based workflow for supplying component electromagnetic loads to later structural assessments, favoring the global Maxwell model for the ECE system.
