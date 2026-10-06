# FG-Hyperelastic-PINN

Representative physics-informed neural network (PINN) implementations for the forward analysis, inverse identification, and material optimization of functionally graded incompressible hyperelastic hollow cylinders.

These codes accompany the manuscript:

**“Multi-task analysis and design of axially constrained functionally graded hyperelastic cylinders by physics-informed neural networks”**


## Repository contents

### Forward problem
**Forward_problem_Forward_power_law.ipynb**

Representative forward PINN example for a functionally graded hyperelastic hollow cylinder with a power-law material distribution. The PINN predicts the large-deformation mechanical response subject to the governing equilibrium equation, incompressibility constraint, and traction boundary conditions.

### Inverse problem I: parameter identification
**Inverse_problemInverse_beta_general_linear.ipynb**

Representative inverse example for identifying the material-gradient parameter \(\beta\) in a prescribed general-linear material-distribution family from sparse deformation observations.

### Inverse problem II: spatial shear-modulus reconstruction
**Inverse_problem_Inverse_shear_modulus_distribution.ipynb**

Representative inverse example for directly reconstructing the spatial distribution of the shear modulus \(\mu(R)\) from sparse observations without prescribing its interior functional form.

### Optimization problem
**Optimization_problem_Optimize_shear_modulus+.ipynb**

Representative PINN-based material optimization example in which the spatial shear-modulus distribution is optimized to reduce the maximum von Mises stress while satisfying the governing mechanical constraints and material-distribution constraints.

## Reference FEM data

The CSV files included in this repository contain reference data used by the representative examples for comparison/validation.

## Requirements

The notebooks are written in Python and use common scientific-computing and deep-learning packages, including:

- Python
- PyTorch
- NumPy
- pandas
- Matplotlib
- SciPy

A CUDA-enabled GPU can accelerate PINN training, although the exact runtime depends on the hardware and training settings.

## Usage

Download or clone the repository and open the required Jupyter notebook. Run the cells sequentially. For notebooks that read reference CSV data, keep the corresponding data files accessible to the notebook or update the file path as appropriate for your local environment.

## Scope

The repository provides representative examples corresponding to the forward, inverse, and optimization tasks investigated in the manuscript. It is intended to support transparency and reproducibility of the computational framework rather than to serve as a general-purpose software package.
