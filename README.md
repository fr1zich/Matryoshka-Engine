# d-factor-engine

**A tool for measuring space tension density in galaxies**

---

## What is this

This project is a computational tool that calculates the **D-factor** — a dimensionless quantity characterizing the tension density of space in a given region — using three observable parameters of a galaxy: mass, radius, and rotation velocity.

The model does not use dark matter particles. Instead, it describes an additional binding force (Omega) as a property of space itself.

---

## Formula
V_total = sqrt( (G * M / R) + Omega )

Omega = alpha * log10(M) * D * sqrt(R)

text

---

## Parameters

| Symbol | Name | Value | Meaning |
|:---|:---|:---|:---|
| `G` | Gravitational constant | `6.674e-11` | Fundamental constant |
| `M` | Galaxy mass | — | Total visible mass (stars, gas, dust) |
| `R` | Galaxy radius | — | Distance from center to measurement point |
| `alpha` | Vacuum viscosity constant | `1.8e-2` | Fundamental «stiffness» of space |
| `D` | D-factor | `0.02 – 2.79` | **Measured** tension density of space |
| `log10(M)` | Mass logarithm | — | Nonlinear mass accounting |
| `sqrt(R)` | Radius square root | — | Smooth tension growth with distance |

---

## What D-factor measures

D-factor is the **tension density of space** in the region of a galaxy.

- **D > 0:** space is tense, stars are held stronger than Newton predicts.
- **D → 0:** space is «relaxed», tension is almost absent.
- **D < 0:** impossible in the observable Universe (would cause antigravity and structure disintegration).

The model **does not interpret** D-factor as a coordinate inside any structure. It is a purely physical quantity extracted from observational data.

---

## Results (13 galaxies)

| Galaxy | Type | D-factor | Accuracy |
|:---|:---|:---|:---|
| NGC 2841 | Spiral | 2.79 | 99.96% |
| NGC 7331 | Spiral | 2.29 | 99.80% |
| Milky Way | Spiral | 1.95 | 96.99% |
| Andromeda (M31) | Spiral | 1.45 | 93.17% |
| NGC 3198 | Spiral | 0.55 | 99.16% |
| NGC 0055 | Irregular | 0.52 | 99.16% |
| NGC 2403 | Spiral (transitional) | 0.47 | 93.89% |
| NGC 0300 | Irregular | 0.44 | ~99% |
| NGC 6503 (Void) | Void | 0.22 | 91.45% |
| IC 2574 | Irregular | 0.16 | 99.99% |
| DDO 154 | Irregular | 0.12 | 98.18% |
| DDO 168 | Irregular | 0.08 | 99.65% |
| DDO 210 | Irregular (dwarf) | 0.02 | 97.04% |

**Average accuracy: ~97%.**  
**D-factor range:** from 0.02 to 2.79.  
**Negative values:** none detected (predicted as impossible by the model).

**Blind tests passed:** NGC 2403 and NGC 3198 — D-factor and velocity were calculated **before** real data was obtained.

---

## Limitations

1. **D-factor is currently fitted manually.** It is a measured quantity, not yet computable from independent data. Automation is a task for future research.
2. **The model is phenomenological.** It describes reality with high accuracy but is not derived from first principles of General Relativity.
3. **No negative D values.** This is not a bug but a prediction: negative tension is incompatible with the existence of galaxies.
