# AI R&D Assignment - Parametric Curve Parameter Estimation

## Project Overview

The objective of this project is to estimate the unknown parameters of a given parametric curve using a dataset of 1500 coordinate points.

The unknown parameters to be estimated are:

- θ (Theta)
- M
- X

The solution was developed in Python by analyzing the dataset, implementing the mathematical model, constructing an optimization objective, and estimating the unknown parameters through numerical optimization.

## Problem Statement

The given parametric equations are:

```text
x = t*cos(theta) - exp(M*|t|)*sin(0.3*t)*sin(theta) + X

y = 42 + t*sin(theta) + exp(M*|t|)*sin(0.3*t)*cos(theta)
```

where

- 6 ≤ t ≤ 60

The unknown parameters are:

- θ (Theta)
- M
- X

The goal is to estimate these parameters such that the predicted curve closely matches the given dataset.

## Dataset

The provided dataset (`xy_data.csv`) contains **1500** coordinate points with two columns:
- x
- y

These points represent samples from the unknown parametric curve.

Before optimization, the dataset was inspected for:
- Missing values
- Duplicate records
- Data types
- Summary statistics

The dataset was found to be clean and required no preprocessing.

## Workflow

The following workflow was followed to estimate the unknown parameters:

1. Load the dataset.
2. Perform data quality checks.
3. Visualize the given curve.
4. Implement the parametric equations.
5. Analyze the effect of each unknown parameter.
6. Define the initial parameter values and bounds.
7. Generate a dense predicted curve.
8. Construct an L1-based objective function using KDTree.
9. Optimize the unknown parameters using the L-BFGS-B algorithm.
10. Validate the optimized model using numerical metrics and visual comparison.

## Technologies Used

The project was implemented using the following Python libraries:
| Library | Purpose |
|----------|---------|
| NumPy | Mathematical computations |
| Pandas | Data loading and analysis |
| Matplotlib | Data visualization |
| SciPy | Optimization and KDTree implementation |

## Results

After optimization, the estimated parameters are:
| Parameter | Estimated Value |
|-----------|----------------:|
| θ (Theta) | 29.999947° |
| M | 0.02999992 |
| X | 54.99994582 |

### Model Evaluation

| Metric | Value |
|--------|-------:|
| L1 Error | 4.849061 |
| Mean Error | 0.003233 |
| Maximum Error | 0.009295 |
| RMSE | 0.003785 |

The optimized curve closely overlaps the observed dataset, indicating that the estimated parameters accurately reconstruct the given parametric curve.

## Output Visualizations

### Scatter Plot of the Given Dataset

![Scatter Plot](images/scatter_plot_step3.png)

---

### Parameter Sensitivity Analysis

![Parameter Sensitivity](images/parameter_sensitivity_step5.png)

---

### Initial Predicted Curve

![Initial Curve](images/initial_curve_step7.png)

---

### Final Optimized Curve

![Final Curve](images/final_curve_step10.png)
