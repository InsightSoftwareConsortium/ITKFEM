# ITKFEM

Finite Element Method (FEM) modules extracted from the Insight Toolkit
(ITK) as a remote module. This repository contains two ITK modules,
preserved at their in-tree paths:

- `Modules/Numerics/FEM` — `ITKFEM` (FE solver framework: `Element`,
  `Material`, `Load`, `Solver`, `RobustSolver`, `LinearSystemWrapper`).
- `Modules/Registration/FEM` — `ITKFEMRegistration`
  (`FEMRegistrationFilter`, physics-based non-rigid registration).

## Status: unmaintained

FEM was a grant-funded ITKv4 research deliverable (NLM A2D2 ARRA); the
funding ended ~2014. The modules are `EXCLUDE_FROM_DEFAULT`, have no
Python wrapping, and have no known downstream users. They are extracted
here as a remote module so that ITK can retire them from the main tree
while keeping them reachable. **Scheduled for removal in ITK 7** unless a
user dependency surfaces — see
[InsightSoftwareConsortium/ITK#6511](https://github.com/InsightSoftwareConsortium/ITK/issues/6511).

## Use

Consumed in-tree via ITK's `Modules/Remote/FEM.remote.cmake`, which
fetches this repository into `Modules/Remote/FEM/`. ITK's module
discovery finds both modules automatically (the test data continue to
resolve from the ITKData store).

## History and authorship

The complete commit history (from the original 2001 check-in by Aljaž
Noe through the 2010–2011 ITKv4 RobustSolver rewrite) is preserved.
`git log --follow` traces each file across the 2011 `Code/` → `Modules/`
modularization.

## License

Apache 2.0 — see `LICENSE` and `NOTICE`, carried over from ITK.
