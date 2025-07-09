<img src="man/figures/logo.png" align="right" height="250" style="background: white; padding: 10px;" alt="PTSDdiag logo" />

# PTSDdiag with Model Validation

<!-- badges: start -->
<!-- badges: end -->

## Description

PTSDdiag with Model Validation is an extended version of the
R-Markdown file "short_version_PTSD_minimal_criteria" from the
comprehensive R package PTSDdiag on GitHub.

The original PTSDdiag package was created for analyzing and simplifying
PTSD diagnostic criteria using PCL-5 (PTSD Checklist for DSM-5) data. It
provides tools to identify optimal subsets of six PCL-5 items that maintain
diagnostic accuracy while reducing assessment burden.

This extended version includes additional validation methods to assess the
stability of the diagnostic models across multiple data subsets, providing
a more reliable estimate of their predictive accuracy.

## **Key Features**

- Data preparation and standardization for PCL-5 scores
- Implementation of DSM-5 diagnostic criteria
- Calculation of diagnostic metrics and summary statistics
- Simplification of diagnostic criteria through:
  - Hierarchical (cluster-based) approach
  - Non-hierarchical approach
- Comparison of different diagnostic approaches
- **NEW: Holdout Validation**: A procedure to split the data into a 70/30 training/testing set to evaluate the performance of the best symptom combinations (based on the training data subset) on the independent testing data subset.
- **NEW: Cross-Validation**: A procedure to assess the best symptom combinations — which were chosen more than one time in multiple training data subsets — and to evaluate their mean performance in multiple independent testing data subsets.

## Installation

The original PTSDdiag package is currently only hosted on GitHub. It can be installed
using the usual way:

``` r
install.packages("devtools")
devtools::install_github("WeidmannL/PTSDdiag")
```

An additional installation is required to access this new version:

``` r
devtools::install_github("SchueeppF/Model-Validation---PTSD-Short-Version")
```

## Getting Started

The vignette of the original PTSDdiag demonstrates how to use the
package to prepare the PCL-5 data, calculate some basic descriptive
statistics and reliability metrics, find the optimal minimal symptom
combinations for PTSD diagnosis and compare different diagnostic approaches.

- [An Introduction to PTSDdiag](https://osf.io/73bgx)

## Bugs, Contributions

- If you have any suggestions or if you find a bug, please report them
  using GitHub [issue
  tracker](https:://github.com/SchueeppF/Model-Validation---PTSD-Short-Version/issues).
- Contributions are welcome! Please feel free to submit a Pull Request.
