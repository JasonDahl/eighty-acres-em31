# EM31 Geostatistical Analysis – Eighty Acres Sanitary Landfill

## Overview

This repository contains a geostatistical analysis of EM31 electromagnetic conductivity and in-phase measurements collected over the Eighty Acres Sanitary Landfill site in northern Minnesota. The analysis demonstrates an uncertainty-aware spatial workflow suitable for interpreting legacy geophysical data and guiding follow-up field decisions.

The emphasis of this work is not on producing a definitive site characterization, but on illustrating a disciplined approach to spatial modeling, uncertainty calibration, and decision support using real, imperfect field data.

---

## Site and Environmental Context

The Eighty Acres Sanitary Landfill is a closed municipal solid waste disposal site that predates modern liner and leachate collection requirements. As with many legacy landfills, waste was placed directly on native soils, creating the potential for elevated subsurface conductivity associated with buried refuse, metallic debris, and leachate migration.

The site has been investigated under state environmental oversight, with attention to subsurface heterogeneity and pathways that may influence contaminant transport. Shallow electromagnetic methods, such as EM31 conductivity and in-phase measurements, are well suited to this setting due to their sensitivity to bulk electrical properties influenced by waste materials, moisture content, and dissolved ions.

---

## Data Provenance and Teaching Context

The EM31 dataset analyzed here was collected as part of an undergraduate **Geophysical Field Methods** course while I was an Assistant Professor of Geology at **Bemidji State University**. The site was selected as a practical survey location that combined real environmental relevance with logistical accessibility for students.

As a result, the dataset reflects many characteristics typical of *legacy geophysical data*:
- Student-collected measurements
- Minor inconsistencies in spacing and execution
- Instrument noise and small-scale placement uncertainty
- Limited metadata compared to modern surveys

Rather than treating these factors as liabilities, this analysis explicitly incorporates them into modeling assumptions and uncertainty interpretation. The dataset provides a realistic test case for methods intended to operate on imperfect, heterogeneous field data.

---

## Analytical Approach

The analysis follows a conservative geostatistical workflow:

- Exploratory spatial analysis of EM31 conductivity and in-phase responses
- Empirical variogram modeling to characterize spatial correlation
- Ordinary kriging for spatial interpolation
- Spatial cross-validation to assess predictive performance
- Conservative uncertainty calibration using cross-validation error
- Probability-of-exceedance mapping to support relative ranking of anomalies

Model outputs are interpreted as **decision-support tools**, not precise estimates of subsurface properties. Kriging variance is treated as a geometric measure and is not conflated with empirical prediction uncertainty.

---

## Repository Structure

```text
eighty-acres-em31-analysis/
├── data/            # Local placement of raw field data (not tracked in git)
├── notebooks/       # Jupyter notebooks with analysis workflow
├── figures/         # Generated plots and maps (regenerable)
├── environment.yml  # Reproducible conda environment
└── README.md


---

## Reproducibility

All analysis is performed in a reproducible Conda environment defined in `environment.yml`.

To recreate the environment:

```bash
conda env create -f environment.yml
conda activate GeoAI
```

Primary analysis is contained in:
```text
notebooks/01_em31_geostatistical_analysis.ipynb
```

---

## Scope and Limitations

This repository is intended as:

- A technical demonstration of spatial reasoning and uncertainty-aware modeling 
- An example of working responsibly with legacy environmental data 
- A portfolio artifact for data science and geoscience audiences

It is *not* intended for regulatory decision-making or site remediation planning.

---

## Author

Jason M. Dahl  
PhD, Earth, Environmental, and Planetary Sciences  
Former Assistant Professor of Geology, Bemidji State University

This repository reflects how I approach spatial problems where data quality, uncertainty, and decision context matter as much as model sophistication.
