# Weight & Cost Reduction of Electrode Mast – Ladle Heating Furnace (LHF)

Static structural FEA-based redesign of the electrode mast-arm assembly of a Ladle Heating Furnace, performed during a summer internship at **SMS India Pvt. Ltd.** (Metallurgy Department).

**Author:** Ranveer Goyal, B.Tech. Mechanical Engineering, IIT Ropar
**Duration:** 25 May 2026 – 3 July 2026 (6 weeks)
**Software:** SolidWorks · ANSYS Mechanical 2019 (Student)

## Overview

A Ladle Heating Furnace (LHF) uses graphite electrodes mounted on cantilevered mast-arm assemblies to arc-heat liquid steel during secondary refining. This project performs static structural FEA on the existing electrode mast-arm assemblies and proposes redesigned mast cross-sections that reduce weight and material cost while keeping stresses and deformations within allowable limits.

The work covers four configurations — side arm (E-ARM#1) and middle arm (E-ARM#2), for both 508 mm and 457 mm electrode variants — plus a comparative study of a cylindrical mast alternative.

## Methodology

1. **Manual calculations** – Free-body moment equilibrium to estimate support roller reactions and hydraulic cylinder base load, used to cross-check FEA results.
2. **CAD simplification (SolidWorks)** – Original assemblies simplified by removing non-structural hardware (pipes, brackets, fittings) while preserving internal water-cooling chambers. Removed mass compensated using an effective-density approach with a 1.3 factor of safety.
3. **FEA (ANSYS Mechanical 2019)** – Static structural analysis with frictional contact at the moment-resisting roller pair, bonded contacts elsewhere (validated against a full bolt-pretension study), and loads including self-weight, cooling water weight, dynamic water pressure (9 bar), dust load, cable weight, clamping unit weight, and slag force.
4. **Redesign & comparison** – Mast cross-sections reduced and re-analyzed; results compared against the original (Mast 1) design for stress, deformation, and base load.

## Key Results

| Configuration | Mast 1 → Mast 2 (cross-section) | Weight Reduction | Estimated Cost Saving |
|---|---|---|---|
| E-ARM#1, 508 mm | 600×410 → 550×350 mm | 14.9% (≈790 kg) | ≈ ₹3.16 lakhs |
| E-ARM#2, 508 mm | 600×410 → 550×350 mm | 15.4% (≈959 kg) | ≈ ₹3.84 lakhs |
| E-ARM#1, 457 mm | 550×400 → 500×310 mm (proposed) | 22.6% (≈1054 kg) | ≈ ₹4.21 lakhs |
| E-ARM#2, 457 mm | 550×400 → 500×310 mm | 20.4% (≈1270 kg) | ≈ ₹5.08 lakhs |

Across all configurations, peak stress and hydraulic cylinder base load were reduced or held essentially constant, while mast weight dropped by roughly 15–23%. The trade-off is increased total deformation, which remains within allowable limits in every case. A cylindrical mast alternative was also evaluated and found structurally inferior (higher stress and deformation) to the rectangular section, and was not pursued further.

## Repository Structure

```
.
├── 508_Electrode/
│   ├── Middle_Mast_1/
│   │   ├── *.stp                  # SolidWorks STEP model
│   │   ├── *.wbpj / ANSYS files   # ANSYS Workbench project and subsequent files
│   │   └── Result_Photos/         # ANSYS result plots (stress, deformation, etc.)
│   ├── Middle_Mast_2/
│   │   ├── *.stp
│   │   ├── ANSYS files
│   │   └── Result_Photos/
│   ├── Side_Mast_1/
│   │   ├── *.stp
│   │   ├── ANSYS files
│   │   └── Result_Photos/
│   └── Side_Mast_2/
│       ├── *.stp
│       ├── ANSYS files
│       └── Result_Photos/
│
├── 457_Electrode/
│   ├── Middle_Mast_1/
│   │   ├── *.stp
│   │   ├── ANSYS files
│   │   └── Result_Photos/
│   ├── Middle_Mast_2/
│   │   ├── *.stp
│   │   ├── ANSYS files
│   │   └── Result_Photos/
│   └── Side_Mast_1/
│       ├── *.stp
│       ├── ANSYS files
│       └── Result_Photos/
│   (no Side_Mast_2 — see note below)
│
├── Cylindrical_Mast/
│   ├── *.stp
│   ├── ANSYS files
│   └── Result_Photos/
│
└── Internship_Report.docx
```

**Note:** The 457 mm electrode configuration has no `Side_Mast_2` folder — the redesigned side-arm mast for this variant was not separately modelled/analyzed in ANSYS; it is a proposed design based on the validated results of the 457 mm middle arm redesign (see Section 9.3.2 of the report).

Each `Mast 1` folder contains the original cross-section model and results; each `Mast 2` folder contains the redesigned (weight/cost-reduced) cross-section model and results. The `Cylindrical_Mast` folder contains the standalone comparative study of a circular hollow section mast (Section 9.5 of the report), evaluated under the 508 mm middle-arm Mast 1 loading conditions.

## Acknowledgements

This project was carried out under the guidance of the Metallurgy Department at SMS India Pvt. Ltd., a subsidiary of SMS group GmbH.
