# PTSD Diagnostics Models and Model Validation

## Description

This project is part of a Master thesis in Human Medicine at the University of Zurich, conducted in collaboration with the University Hospital of Psychiatry Zurich. It aims to improve the diagnostic validity of Post-Traumatic Stress Disorder (PTSD) using simplified polythetic symptom models combined with computational symptom selection implemented in R.

## R Markdown file "Model Validation - PTSD Short Version.Rmd"

Parts 1-3 of the code were adopted from PTSDdiag (https://github.com/WeidmannL/PTSDdiag).
They include the following:
- Data preparation and standardization for PCL-5 (PTSD Checklist for DSM-5) scores
- Implementation of DSM-5 diagnostic criteria
- Calculation of diagnostic metrics and summary statistics
- Simplification of diagnostic criteria through:
  - Hierarchical (cluster-based) approach
  - Non-hierarchical approach

Part 4 of the code was written from scratch.
It includes additional validation methods to assess the stability of the diagnostic models across multiple data subsets, providing a more reliable estimate of their predictive accuracy:
- **Holdout Validation**: A procedure to split the data into a 70/30 training/testing subset to evaluate the performance of the best symptom combinations (based on the training subset) on the independent testing subset.
- **Cross-Validation**: A procedure to assess the best symptom combinations — selected more than once across multiple training data subsets — and to evaluate their average performance in multiple independent testing subsets.

### Required Input Data
This R Markdown file operates on a dataset in `.csv` format containing responses to the PCL-5 (PTSD Checklist for DSM-5). The dataset should have the following structure:
- Rows: Individual participants  
- Columns: PTSD-related symptoms, rated on a Likert scale (e.g., 0–4)

A sample dataset can be downloaded at: https://github.com/WeidmannL/PTSDdiag/tree/main/data.

## How to Run

1. Open `Model Validation - PTSD Short Version.Rmd` in RStudio.
2. Ensure all required packages are installed:
   ```r
   install.packages(c("tidyverse", "data.table", "DT", "gtsummary", "psych", "modelr"))
   ```
3. Ensure your dataset has the required structure (see section: Required Input Data).
4. Knit the R Markdown file to HTML or run code chunks manually in RStudio.

## Bugs, Contributions

- If you have any suggestions or if you find a bug, please report them
  using GitHub [issue
  tracker](https://github.com/SchueeppF/Model-Validation---PTSD-Short-Version/issues).
- Contributions are welcome! Please feel free to submit a Pull Request.
