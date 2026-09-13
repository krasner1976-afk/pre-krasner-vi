# Pre-Krasner VI: Phenomenological Framework for Disformal Spatial Curvature & Galactic External Field Effects

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.10+](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/downloads/)
[![Status: Working Paper](https://img.shields.io/badge/Status-Working%20Paper%20v8.2-orange.svg)]()

> **Disclaimer / Classification Note:** This repository contains a speculative phenomenological working paper and reproducible Python scripts for observational predictions (e.g., Oort Cloud comet precession under the Galactic External Field Effect), rather than a fully derived or peer-reviewed physical theory. All interpolating functions and prefactors are phenomenological Ansätze designed to bridge asymptotic regimes and should be evaluated on empirical grounds.

---

## 🌌 Overview

The **Pre-Krasner VI** framework explores a disformal scalar-tensor metric model where localized baryonic matter deforms space-time via a non-linear temporal metric component $\tilde{g}_{00} = g_{00} + q^2 c^2 D(\phi)$, while leaving the radial spatial metric $\tilde{g}_{rr} = g_{rr}$ standard General Relativistic. 

Key observational highlights of the framework include:
1. **Oort Cloud Comet Precession (ApJL Research Note Proposal):** At heliocentric distances $r > 500\text{ au}$, Solar acceleration falls below the critical scale $a_\star \approx 1.2 \times 10^{-10}\text{ m/s}^2$, exposing long-period comets to the Galactic External Field Effect (EFE). This induces an anomalous prograde precession $\dot{\varpi}_{\text{EFE}} \sim +10^2 - 10^3\text{ arcsec/century}$, exceeding classical planetary tides by 3--4 orders of magnitude with an inverted (prograde) sign.
2. **Vainshtein Screening & Inner Solar System Isolation:** On terrestrial scales ($r \le 1\text{ au}$), non-linear kinetic terms suppress fifth-force gradients by $\eta_{\text{Earth}} \sim 10^{-18}$, protecting standard General Relativity and classical electrodynamics.
3. **Phenomenological RAR Interpolation:** An Ansatz interpolating function $a_{\text{tot}}(a_{\text{bar}}) = a_{\text{bar}} + \sqrt{a_{\text{bar}} a_\star} e^{-a_{\text{bar}}/2a_\star}$ that reproduces the Deep MOND limit ($a_{\text{bar}} \ll a_\star$) and Newtonian behavior ($a_{\text{bar}} \gg a_\star$).

---

## 📂 Repository Structure

```
.
├── LICENSE                          # MIT Open Source License
├── README.md                        # Project documentation and quickstart
├── CONTRIBUTING.md                  # Contribution guidelines
├── requirements.txt                 # Python dependencies
├── .gitignore                       # Git ignore configuration
├── docs/
│   ├── WORKING_PAPER_v8.2.md        # Full Working Paper (v8.2 Final)
│   ├── RESEARCH_NOTE_APJL.md        # ApJL Research Note draft
│   └── COVER_LETTER_APJL.md         # Cover letter for ApJL submission
├── scripts/
│   ├── oort_efe_precession.py       # Oort Cloud EFE precession calculator & plotter
│   ├── rar_ansatz_comparison.py     # Comparison with McGaugh (2016) empirical RAR
│   └── vainshtein_screening_calc.py # Vainshtein screening scale & suppression estimator
└── figures/
    └── oort_efe_precession_comparison.png # Generated high-res comparison chart
```

---

## ⚡ Quickstart & Reproducibility

### 1. Installation

Clone the repository and install dependencies:
```bash
git clone https://github.com/your-username/pre-krasner-vi.git
cd pre-krasner-vi
pip install -r requirements.txt
```

### 2. Calculate Oort Cloud Comet Precession

Run the secular precession script to generate the numerical predictions and comparison plot:
```bash
python scripts/oort_efe_precession.py
```

**Sample Output:**
```
================================================================================
OORT CLOUD COMET SECULAR PRECESSION RATES (e = 0.98)
================================================================================
a (au)     Q (au)     q (au)    EFE Precession (''/cy)   Planetary Tide (''/cy)
--------------------------------------------------------------------------------
 1,000      1,980       20             ~ +56                   -0.047
 2,000      3,960       40             ~ +110                  -0.134
 5,000      9,900      100             ~ +280                  -0.530
10,000     19,800      200             ~ +560                  -1.500
20,000     39,600      400             ~ +1100                 -4.243
================================================================================
Estimated background perturbation noise: ~ 0.035 arcsec/century
Expected Signal-to-Noise Ratio (SNR) at 10,000 au: ~ 10^3 - 10^4
```

### 3. Compare Acceleration Interpolation with Empirical RAR

Run the RAR comparison script:
```bash
python scripts/rar_ansatz_comparison.py
```

---

## 📊 Key Results & Visualizations

![Oort Cloud EFE Precession Comparison](figures/oort_efe_precession_comparison.png)

*Figure 1: Prograde Galactic EFE precession rate (left) vs. decaying retrograde planetary tides (right) for long-period Oort Cloud comets ($e = 0.98$) as a function of aphelion distance $Q$.*

---

## 📝 Document Status & Pre-prints

- **Working Paper (v8.2 Final):** Located in [`docs/WORKING_PAPER_v8.2.md`](docs/WORKING_PAPER_v8.2.md).
- **ApJ Letters Research Note Draft:** Located in [`docs/RESEARCH_NOTE_APJL.md`](docs/RESEARCH_NOTE_APJL.md).
- **ApJ Letters Cover Letter:** Located in [`docs/COVER_LETTER_APJL.md`](docs/COVER_LETTER_APJL.md).

---

## 📬 Contact & Citation

For questions, feedback, or collaboration proposals, please open an issue or contact the authors.

```bibtex
@article{PreKrasnerVI2026,
  author = {Pre-Krasner VI Collaboration},
  title = {Working Paper: Phenomenological Framework for Disformal Spatial Curvature and Galactic External Field Effects},
  journal = {Zenodo Pre-print},
  year = {2026},
  version = {v8.2 Final}
}
```
