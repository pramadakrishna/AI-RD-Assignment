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
