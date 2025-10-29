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
