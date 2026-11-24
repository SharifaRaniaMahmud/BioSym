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
├── LICENSE
├── BioSym.ipynb
├── SingleObj.ipynb
├── Supplementary_Materials.pdf
└── data/
    ├── train219_dataset.csv
    └── validation_test99_dataset.csv
```

## Input Variables

The study uses eight hydrogeological factors (column names in the datasets are shown in brackets):

- Soil (`Soil`)
- Slope (`Slope`)
- Rainfall (`Rain`)
- Land Use/Land Cover (`LULC`)
- Lithology (`Lithology`)
- Lineament Density (`Lineament density`)
- Geomorphology (`Geomorphology`)
- Drainage Density (`Drainage density`)

The target variable is continuous net groundwater recharge (`Net Groundwater Recharge`).

## Source Code

### `BioSym.ipynb`

Contains the implementation of BioSym, the proposed bi-objective symbolic regression framework using genetic programming and NSGA-II. It also includes the multiple linear regression (MLR) baseline, the hypervolume and convergence analysis, validation, and the sensitivity analysis.

BioSym optimizes:

- $R^2$
- Expression complexity

### `SingleObj.ipynb`

Contains the single-objective symbolic regression implementation used for comparison.

This approach optimizes only $R^2$.

## Data

The `data/` directory contains:

- `train219_dataset.csv`: training dataset with 219 instances
- `validation_test99_dataset.csv`: validation dataset with 99 instances

### Data Source

The datasets are derived from the CIMCA study:

Zzaman, R.U., Nayeem, M.A., Nowreen, S., Newton, I.H., Islam, A.K.M.S., Zahid, A., Rahman, M.S., 2023. CIMCA: Infusing computational intelligence in multi-criteria analysis to assess groundwater potential for recharge. *Environmental Modelling & Software* 169, 105812. https://doi.org/10.1016/j.envsoft.2023.105812

Soil, LULC, and lithology are represented by class values from the CIMCA study, while rainfall, slope, drainage density, lineament density, and geomorphology are continuous values.

## Running the Code

The code was developed and executed in Google Colab.

1. Open the notebook in Google Colab.
2. Update the file paths to your own data location.
3. Run all cells.

Random seeds are fixed (42–61 for the 20 independent runs), so the results can be reproduced.

## Dependencies

The main Python libraries used are:

- pandas
- NumPy
- scikit-learn
- SciPy
- Matplotlib
- seaborn
- openpyxl

## Reproducing Main Results

- Run `BioSym.ipynb` to reproduce the BioSym results, including the set of non-dominated mathematical expressions representing different trade-offs between $R^2$ and expression complexity, the MLR baseline, and the hypervolume, convergence, validation, and sensitivity analyses.
- Run `SingleObj.ipynb` to reproduce the highest-$R^2$ single-objective symbolic regression expression used for comparison.
- The sensitivity analysis in `BioSym.ipynb` consists of 200 runs and takes several hours.
- Additional results are provided in `Supplementary_Materials.pdf`.

## Software Information

- Software name: BioSym v1
- Programming language: Python
- Development and execution environment: Google Colab
- Hardware requirements: Standard computer with internet access and a web browser
- Year first official release: 2026

## Supplementary Material

Additional information related to the study is provided in:

`Supplementary_Materials.pdf`

## License

The source code of BioSym is released under the MIT License. See the `LICENSE` file for details.

The datasets are derived from the CIMCA study. Please cite the CIMCA study when using the data.

## Associated Manuscript

**BioSym: A Bi-Objective Symbolic Regression Framework for Continuous Net Groundwater Recharge Estimation**

## Contact

Sharifa Rania Mahmud  
Email: 0423054003@grad.cse.buet.ac.bd
