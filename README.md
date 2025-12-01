# Preliminary Data Analysis – ENT6907

This repository contains the preliminary data analysis for my qPCR study evaluating viral gene expression (H5N1, H7N2) across different vaccine groups and administration routes.

### Files Included
- **Prelim-Data Analysis Semester Project.qmd** – Quarto document containing R code, data visualization, and model selection explanation.
- **Prelim-Data Analysis Semester Project.pdf** – Rendered PDF version of the analysis.
- **ENT_Project_Tracheal_qPCR_Clean.xlsx** – Cleaned qPCR dataset used for analysis.

### Summary
The preliminary analysis included exploratory visualization (histograms, QQ plots) and assessment of data normality.  
Given the nested experimental design (Bird_ID within Timepoint within Virus), a **Linear Mixed Model (LMM)** was identified as the most suitable model for normally distributed outcomes (Ct, log10GE).  
For future analyses, if residual skew persists, a **Tweedie GLMM** will be considered to handle positive, right-skewed data.



`
# Final Semester Project Data Analysis – ENT6907

This repository contains the final data analysis for my qPCR study evaluating tracheal viral load in broiler chickens vaccinated with a bovine adenovirus–vectored avian influenza vaccine (BAds-AIV). Birds were challenged with H5N1 or H7N2 and sampled at three post-challenge timepoints (DPC2, DPC4, DPC6).

## Files Included
Final Semester Project-Data-Analysis-ENT6907.qmd  
Quarto document containing all R code for data import, wrangling, visualization, model fitting, and diagnostics.

## Final Semester Project-Data-Analysis-ENT6907.pdf (and `.html`)  
  Rendered report with figures, model results, and interpretation.

# Updated ENT_Project_Tracheal_qPCR_Clean.xlsx**  
  Clean qPCR dataset with an added `Metadata` sheet describing variables and data structure.

## Summary

The final analysis uses Gaussian linear mixed-effects models for two continuous outcomes:

- Ct (cycle threshold)  
- log10GE (log10 genome equivalents)

Both models include Vaccine_Group, Virus, Route, and Timepoint as fixed effects and Bird_ID as a random intercept to account for repeated measures. Model diagnostics (residual plots, Q–Q plots) support the use of Gaussian mixed models. Results show strong virus-specific differences in viral load (H7N2 > H5N1) and partial vaccine effects, especially for H7N2, with little influence of administration route.
