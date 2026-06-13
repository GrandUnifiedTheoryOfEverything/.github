# Grand Unified Theory of Everything (GUToE)

### A pedagogical and computational framework for the composite action of fundamental physics

<div align="center">

<img src="https://raw.githubusercontent.com/GrandUnifiedTheoryOfEverything/gutoe/main/gfx/4d/tesseract_rotation.gif" alt="Tesseract under double rotation, perspective-projected from 4D to 3D" width="420">

*A tesseract (4D hypercube) under double rotation in the (x,w) and (y,w) planes, perspective-projected to 3D.
Vertex color encodes the fourth coordinate w — the "inner" and "outer" cubes trading places **is** the 4D rotation.*

</div>

---

## What this project is

GUToE organizes the standard action functionals of fundamental physics — the
Einstein–Hilbert action of general relativity, the Dirac and Higgs actions in
curved spacetime, the Yang–Mills gauge action of the Standard Model, and the
formal loop expansion of quantum corrections — into a single composite
expression:

$$S = S_{\text{gravity}} + S_{\text{matter}} + S_{\text{gauge}} + S_{\text{quantum}}$$

and then **computes the piece of unification physics that is honestly
computable at this level**: the renormalization-group running of the three
gauge couplings at one and two loops, the unification scale in the minimal
supersymmetric extension, and the proton-lifetime estimate it implies.

The headline numbers, reproducible with `python3 -m toe_math.rg_running`:

| Model | Loops | M<sub>GUT</sub> [GeV] | α<sub>GUT</sub>⁻¹ | Mismatch | Unifies | τ<sub>p</sub> [yr] |
|---|---|---|---|---|---|---|
| Standard Model | 2 | 3.8×10¹⁴ | 41.7 | 11.5% | no | 1.0×10³⁰ — **excluded by Super-K** |
| MSSM (m<sub>SUSY</sub> = 1 TeV) | 2 | 1.3×10¹⁶ | 25.1 | 0.7% | **yes** | 4.5×10³⁵ — above the Super-K bound |

The Standard Model couplings *nearly* meet at high energy — the famous "near
miss." With supersymmetry at the TeV scale they unify, and the resulting
proton-decay estimate survives the experimental bound while the SM scenario
is excluded by four orders of magnitude: the classic demise of minimal
non-supersymmetric SU(5), recomputed from scratch in this repository.

## What this project is **not**

It is **not a theory of everything**, and it says so everywhere. The
composite action is an *additive juxtaposition* of separately established
actions — an organizing definition, not a unification. The project was
examined by an independent academic evaluation (PDF in the
[`gutoe`](https://github.com/GrandUnifiedTheoryOfEverything/gutoe)
repository root); its findings were accepted and the entire project was
restructured around them, with formal apparatus (Definitions, Propositions
proved *by computation*, and explicitly stated Open Problems) replacing
rhetorical claims. The full point-by-point response:
[docs/CONCLUSION.md](https://github.com/GrandUnifiedTheoryOfEverything/gutoe/blob/main/docs/CONCLUSION.md).

## Exploring the fourth dimension

<div align="center">

<img src="https://raw.githubusercontent.com/GrandUnifiedTheoryOfEverything/gutoe/main/gfx/4d/field_w_sweep.gif" alt="A 4D scalar field displayed one hyperplane slice at a time" width="420">

*A scalar field f(x, y; w) on four coordinates, displayed one hyperplane
w = const at a time. Each frame is genuinely a different 4D location — slicing,
not a camera move.*

</div>

You cannot look at four dimensions, but you can be honest about how you
display them. The project uses two techniques throughout, and labels every
figure with the one it uses:

- **Projection** — rotate the object in 4-space, then cast a 3D shadow with
  a perspective map p = d/(d−w), exactly as your screen casts a 2D shadow
  of a 3D scene (the tesseract above);
- **Slicing** — intersect the object or field with the hyperplane
  w = const and sweep the slice (the field animation above).

Both are interactive in the apps: drag, zoom, spin the dials.

## Quantitative centerpiece

<div align="center">

<img src="https://raw.githubusercontent.com/GrandUnifiedTheoryOfEverything/gutoe/main/gfx/rg/rg_unification.png" alt="Two-loop running of the gauge couplings: SM near-miss vs MSSM unification" width="760">

*Two-loop running of the GUT-normalized inverse couplings. Left: Standard
Model — the near miss. Right: MSSM — unification at M<sub>GUT</sub> ≈ 1.3×10¹⁶ GeV.*

</div>

## The repository

[**gutoe**](https://github.com/GrandUnifiedTheoryOfEverything/gutoe) — the
complete framework (v2.0.0):

- **Three UI deliveries, one physics core** — a
  [Streamlit explorer](https://grandunifiedtheoryofeverything.streamlit.app/)
  (live demo), a Dash scientific dashboard with pure-D3.js panels, and a
  NiceGUI "Control Room" where every concept expands into its component
  parts with increasing complexity, ending in interactive moments driven by
  knobs and levers
- **Formal documentation** —
  [THEORY.md](https://github.com/GrandUnifiedTheoryOfEverything/gutoe/blob/main/docs/THEORY.md)
  (Definitions, Propositions, Open Problems),
  [RG_UNIFICATION.md](https://github.com/GrandUnifiedTheoryOfEverything/gutoe/blob/main/docs/RG_UNIFICATION.md)
  (methods and results),
  [GUT_EMBEDDING.md](https://github.com/GrandUnifiedTheoryOfEverything/gutoe/blob/main/docs/GUT_EMBEDDING.md)
  (the SU(5)/SO(10) arithmetic, anomaly cancellation verified exactly)
- **A typeset paper** —
  [paper/](https://github.com/GrandUnifiedTheoryOfEverything/gutoe/tree/main/paper)
  with theorem environments and full bibliography
- **Tests** — the physics is pinned to literature values by regression
  tests; every figure and number regenerates from code

## Official physics references

**Data and reviews**

- [Particle Data Group — Review of Particle Physics](https://pdg.lbl.gov/) — the experimental inputs (α<sub>em</sub>, sin²θ<sub>W</sub>, α<sub>s</sub> at M<sub>Z</sub>)
- [INSPIRE-HEP](https://inspirehep.net/) — high-energy physics literature database
- [arXiv hep-ph](https://arxiv.org/list/hep-ph/recent) / [arXiv hep-th](https://arxiv.org/list/hep-th/recent) — preprint archives

**Foundational papers used by this project**

- Georgi & Glashow, [*Unity of All Elementary-Particle Forces*](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.32.438), PRL 32, 438 (1974)
- Georgi, Quinn & Weinberg, [*Hierarchy of Interactions in Unified Gauge Theories*](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.33.451), PRL 33, 451 (1974)
- Goroff & Sagnotti, [*The Ultraviolet Behavior of Einstein Gravity*](https://doi.org/10.1016/0550-3213(86)90193-8), NPB 266, 709 (1986) — why naive quantum gravity fails
- Amaldi, de Boer & Fürstenau, [*Comparison of GUTs with Electroweak and Strong Coupling Constants Measured at LEP*](https://doi.org/10.1016/0370-2693(91)91641-8), PLB 260, 447 (1991)
- Martin & Ramond, [*Sorting out the Minimal Supersymmetric Standard Model*](https://arxiv.org/abs/hep-ph/9501244), arXiv:hep-ph/9501244
- Martin, [*A Supersymmetry Primer*](https://arxiv.org/abs/hep-ph/9709356), arXiv:hep-ph/9709356

**Experiments that get the last word**

- [Super-Kamiokande](https://www-sk.icrr.u-tokyo.ac.jp/en/sk/) — proton-decay bound τ(p → e⁺π⁰) > 2.4×10³⁴ yr ([arXiv:2010.16098](https://arxiv.org/abs/2010.16098))
- [ATLAS at CERN](https://atlas.cern/) — superpartner mass limits ([arXiv:2010.14293](https://arxiv.org/abs/2010.14293))
- [Planck (ESA)](https://www.esa.int/Science_Exploration/Space_Science/Planck) — the cosmological constant, **with units**: Λ = 1.1056×10⁻⁵² m⁻² ([arXiv:1807.06209](https://arxiv.org/abs/1807.06209))

---

<div align="center">

*An AI-assisted project of Gregory L. Magnusson, developed as "Professor Codephreak" —
restructured in 2026 around an independent academic evaluation, whose verdict is
accepted, incorporated, and kept in plain sight.*

[gutoe repository](https://github.com/GrandUnifiedTheoryOfEverything/gutoe) ·
[live demo](https://grandunifiedtheoryofeverything.streamlit.app/) ·
[Professor-Codephreak](https://github.com/Professor-Codephreak)

</div>
