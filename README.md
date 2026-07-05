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

\[
x=t\cos(\theta)-e^{M|t|}\sin(0.3t)\sin(\theta)+X
\]

\[
y=42+t\sin(\theta)+e^{M|t|}\sin(0.3t)\cos(\theta)
\]

where

- \(6 \le t \le 60\)

The unknown parameters are:

- θ
- M
- X

The goal is to estimate these parameters so that the predicted curve closely matches the given dataset.
