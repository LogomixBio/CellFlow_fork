<img src="docs/_static/images/cellflow_dark.png" width="500" alt="CellFlow">

[![PyPI](https://img.shields.io/pypi/v/cellflow-tools.svg)](https://pypi.org/project/cellflow-tools/)
[![Downloads](https://static.pepy.tech/badge/cellflow-tools)](https://pepy.tech/project/cellflow-tools)
[![CI](https://img.shields.io/github/actions/workflow/status/theislab/cellflow/test.yaml?branch=main)](https://github.com/theislab/cellflow/actions)
[![pre-commit.ci status](https://results.pre-commit.ci/badge/github/theislab/CellFlow/main.svg)](https://results.pre-commit.ci/latest/github/theislab/CellFlow/main)
[![Codecov](https://codecov.io/gh/theislab/cellflow/branch/main/graph/badge.svg?token=Rgtm5Tsblo)](https://codecov.io/gh/theislab/cellflow)
[![Docs](https://img.shields.io/readthedocs/cellflow)](https://cellflow.readthedocs.io/en/latest/)

CellFlow - Modeling Complex Perturbations with Flow Matching 
============================================================

CellFlow is a framework for predicting single-cell phenotypes induced by complex perturbations. It is quite flexible and enables researchers to systematically explore how cells respond to a wide range of experimental interventions, including drug treatments, genetic modifications, cytokine stimulation, morphogen pathway modulation or even entire organoid protocols.

Check out the [preprint](https://www.biorxiv.org/content/10.1101/2025.04.11.648220v1.abstract) for details!

## Example Applications

- Modeling the effect of single and combinatorial drug treatments
- Predicting the phenotypic response to genetic perturbations
- Modeling the development of perturbed organisms
- Cell fate engineering
- Optimizing protocols for growing organoids
- ... and more; check out the [documentation](https://cellflow.readthedocs.io) for more information.


Installation (UV)
------------
Install **CellFlow** by running::
```
    uv sync
```

Installation (Conda)
------------
Install **CellFlow** by running::
```
    conda env create -f conda/rsc_rapids_25.10.yml
    conda activate cellflow_rapids
    pip uninstall bokeh holoviews shapely
    pip install transformers torch
    pip install cuda-toolkit[cublas,cufft,curand,cusolver,cusparse]>=12
    pip install -U "jax[cuda13]"
    pip install cellflow-tools
```
**NOTES:**
- Some pip dependency errors might appear during installation, but those can be ignored.
- A message about JAX not being able to get GPU information might also show up, however that can be ignored.

Installation (Other)
------------
Please refer to the original repository for other installation options.
For further instructions how to install jax, please refer to https://github.com/google/jax.
