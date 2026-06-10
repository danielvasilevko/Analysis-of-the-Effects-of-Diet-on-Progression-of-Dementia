# Analysis-of-the-Effects-of-Diet-on-Progression-of-Dementia
This repository contains an R Markdown report and supporting analysis examining cognitive aging in the HCA/AABC cohort, exploring how metabolic, dietary, and demographic factors relate to memory and IQ outcomes across longitudinal study visits, along with missingness diagnostics, GAM/LMM modeling, and cross-validation results.

# Repository Structure

* Final_Report.Rmd - R Markdown file featuring the full longitudinal analysis of diet, metabolic health, and memory performance.
* Link Between a Patient's Diet and Cognitive Function.pdf - Presentation compiling and summarizing key results from the analysis.

# What Final_Report.Rmd Does

* Reads and merges HCA and AABC study data, ordering events chronologically and constructing patient-level longitudinal trajectories.
* Quantifies and visualizes missingness across blood, diet, and cognitive feature categories, identifying systematic patterns at roughly 0%, 60%, 90%, and 100% rates.
* Computes pairwise correlations among Memory, Fluid IQ, and Crystallized IQ at both the observation and patient-averaged levels, and examines diet-cognition correlations across all three outcomes.
* Fits a stepwise linear regression at the patient level, identifying age, sex, Crystallized IQ, HbA1c, insulin, and dietary fiber as significant predictors of Memory.
* Fits cross-sectional GAMs with smooth terms to capture nonlinear relationships, explaining approximately 49% of variance in Memory scores, and performs 10-fold cross-validation to assess generalizability.
* Fits longitudinal linear mixed-effects models with random intercepts per patient, confirming high within-person correlation (ICC ≈ 0.81) and identifying age, HbA1c, and dietary fiber as stable longitudinal predictors.
* Compares all models by AIC, with the cross-sectional GAM achieving the best fit and longitudinal models providing complementary within-person inference.
