# Cost-Effectiveness Model Structure for Technologies that Reduce Time to Appropriate Antibiotic Therapy in Sepsis Patients (SPEARHEAD Project)

On behalf of the SPEARHEAD consortium

https://spearhead-project.ch/

https://www.swissre.com/reinsurance/events/fight-against-antimicrobial-resistance.html

This model was built by Mark J. Lambiris, PhD (European Center of Pharmaceutical Medicine, University of Basel) as part of Subproject 4 (SP4) of the SPEARHEAD consortium.

COPYRIGHT 2026, European Center of Pharmaceutical Medicine and University of Basel

## Overview

This repository contains R/Quarto code for a decision-analytic cost-effectiveness model evaluating technologies that reduce **time to appropriate antibiotic therapy (TTAA)** in **hospitalised patients with bloodstream infection (BSI)**.

The model was developed within the **SPEARHEAD** project as part of work on the economic evaluation of antimicrobial-resistance-related technologies. It was designed as a flexible framework that can be adapted to different diagnostic technologies, patient populations, clinical assumptions, and cost scenarios.

## Purpose

It showcases a model structure that can be used to explore how earlier appropriate therapy may affect survival, QALYs, costs, and cost-effectiveness, and how these results change under alternative assumptions relevant to pricing, reimbursement, and HTA.

## Decision Problem

The model compares:

- **Standard care**: delayed TTAA
- **Intervention**: earlier TTAA enabled by a diagnostic technology

The aim is to estimate the downstream health and economic consequences of earlier treatment.

## Model Structure

The code implements a flexible decision-analytic framework with:

- a **short-term acute phase** modelling mortality during the first 30 days
- a **long-term Markov state-transition model** for survivors
- transformation of a **per-hour treatment effect** into the effect associated with a user-defined reduction in TTAA
- estimation of **incremental costs**, **incremental QALYs**, **net monetary benefit (NMB)**, and **ICERs**

## Key Analytical Features

The model includes:

- acute and long-term survival modelling
- costs linked to hospitalisation, length of stay, technology price, and long-term care
- utility-based QALY estimation
- **probabilistic sensitivity analysis (PSA)**
- **one-way sensitivity analysis (OWSA)**
- standard CEA outputs such as:
  - cost-effectiveness plane
  - cost-effectiveness acceptability curve (CEAC)
  - tornado plot
- **stratified subgroup analysis** to explore heterogeneity and equity-relevant differences in cost-effectiveness

## Practical Usefulness of the Framework

Beyond a single illustrative example, the model structure is useful because it can be adapted to support:

- **early economic evaluation** of diagnostic technologies
- **pricing and reimbursement exploration**
- **headroom-style analysis**
- scenario analysis when product-specific evidence is still incomplete
- assessment of whether pooled cost-effectiveness masks important subgroup differences

## Files

- `CEA TTAA v4.qmd` – main Quarto file containing the model code and analysis workflow

## Data and Inputs

The repository contains the modelling framework and illustrative parameterisation logic.

Per-hour hazard ratio of death (earlier vs delayed TTAA) and standard error were estimated via meta-analysis in a separate sub-goal of SP4.

Underlying project-specific data and some project deliverables are not reproduced here where they are confidential, unpublished, or otherwise not appropriate for public sharing.

## Software

The analysis is written in **R** / **Quarto**.
