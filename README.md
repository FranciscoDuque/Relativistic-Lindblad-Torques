# Relativistic Lindblad Torques for EMRIs

[![arXiv](https://img.shields.io/badge/arXiv-2510.02433-b31b1b.svg)](https://arxiv.org/abs/2510.02433)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

This repository provides code to compute **relativistic Lindblad torques** in thin accretion discs around Kerr black holes, relevant for extreme-mass-ratio inspirals (EMRIs). Lindblad resonances are locations in the disc where the gravitational influence of a small orbiting body excites density waves, leading to angular momentum exchange and torques on the orbit. In the relativistic regime, these torques can be strongly amplified, change sign near the ISCO, and differ significantly from Newtonian predictions.

The main results and methods follow [arXiv:2510.02433](https://arxiv.org/abs/2510.02433). The code uses Teukolsky-based amplitudes and Novikov–Thorne disc profiles to capture strong-field effects.


## Notebook Contents

The tutorial notebook (`lindblad_torques_tutorial.ipynb`) covers:

- Kerr geometry and resonance locations
- Teukolsky amplitudes and torque calculation
- Novikov–Thorne disc model
- Summing torques with a pressure cutoff
- Comparison with gravitational-wave torques


## Requirements

- Python ≥ 3.9
- NumPy, SciPy, Matplotlib
- [pybhpt](https://github.com/BlackHolePerturbationToolkit/pybhpt)
- [pylaplace](https://github.com/BlackHolePerturbationToolkit/pylaplace) (optional, for Newtonian comparison)

Install core packages with:

```bash
pip install numpy scipy matplotlib
```

See the linked repositories for installing `pybhpt` and `pylaplace`.

## Quick Start

```bash
git clone https://github.com/FranciscoDuque/Relativistic-Lindblad-Torques.git
cd lindblad-torques-tutorial
jupyter notebook lindblad_torques_tutorial.ipynb
```

> **Note:** Some cells (especially the Teukolsky equation solves in Sections 5 and 7–8) are computationally expensive and may take several minutes to run. Reduce `l_max` or the calibration grid for faster exploratory runs.

## Citation

If you use this code or find it useful for your research, please cite:

```bibtex
@article{Duque:2025lindblad,
    author = {Duque, Francisco and Sberna, Laura and Spiers, Andrew and Vicente, Rodrigo},
    title = {Extreme-mass-ratio inspirals in relativistic accretion discs},
    eprint = {2510.02433},
    archivePrefix = {arXiv},
    primaryClass = {gr-qc},
    year = {2025}
}
```

## License

This project is licensed under the [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).
