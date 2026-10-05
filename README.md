# BioSym

BioSym is a bi-objective symbolic regression framework for estimating continuous net groundwater recharge using hydrogeological factors.

The framework uses genetic programming and NSGA-II to optimize two objectives:

- Maximize the coefficient of determination ($R^2$)
- Minimize expression complexity

BioSym produces a set of non-dominated mathematical expressions representing different trade-offs between $R^2$ and expression complexity.

## Repository Structure

```text
BioSym/
├── README.md
├── biosym.py
├── single_objective.py
├── Supplementary_Materials.pdf
└── data/
    ├── train219_dataset.csv
    └── validation_test99_dataset.csv
```

## Input Variables

The study uses eight hydrogeological factors:

- Soil
- Slope
- Rainfall
- Land Use/Land Cover (LULC)
- Lithology
- Lineament Density
- Geomorphology
- Drainage Density

The target variable is continuous net groundwater recharge.

## Source Code

### `biosym.py`

Contains the implementation of BioSym, the proposed bi-objective symbolic regression framework using genetic programming and NSGA-II.

BioSym optimizes:

- $R^2$
- Expression complexity

### `single_objective.py`

Contains the single-objective symbolic regression implementation used for comparison.

This approach optimizes only $R^2$.

## Data

The `data/` directory contains:

- `train219_dataset.csv` — training dataset with 219 instances
- `validation_test99_dataset.csv` — validation dataset with 99 instances

## Running the Code

The source code was developed and executed in Google Colab using Python.

The scripts contain Google Drive paths used during the experiments. Before running the code:

1. Open the script in Google Colab.
2. Mount Google Drive.
3. Upload the required datasets to Google Drive.
4. Update the dataset path in the script according to your own Google Drive location.

The datasets used in this study are also provided in the `data/` directory of this repository.

## Software Information

- Software name: BioSym v1
- Programming language: Python
- Development environment: Google Colab
- Hardware requirements: Internet-connected computer
- Year first official release: 2026

## Supplementary Material

Additional information related to the study is provided in:

`Supplementary_Materials.pdf`

## Associated Manuscript

**BioSym: A Bi-Objective Symbolic Regression Framework for Continuous Net Groundwater Recharge Estimation**
