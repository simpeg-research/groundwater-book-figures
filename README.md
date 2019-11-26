**[summary](#summary) | [contents](#contents) | [usage](#usage) | [running the notebooks](#running-the-notebooks) | [issues](#issues) | [citation](#citation) | [license](#license)**

# groundwater-book-figures

[![Build Status](https://travis-ci.org/simpeg-research/groundwater-book-figures.svg?branch=master)](https://travis-ci.org/simpeg-research/groundwater-book-figures)
[![Binder](https://mybinder.org/badge.svg)](https://mybinder.org/v2/gh/simpeg-research/groundwater-book-figures/master?filepath=index.ipynb)
[![License](https://img.shields.io/github/license/simpeg-research/groundwater-book-figures.svg)](https://github.com/simpeg-research/groundwater-book-figures/blob/master/LICENSE)
[![SimPEG](https://img.shields.io/badge/powered%20by-SimPEG-blue.svg)](http://simpeg.xyz)

Notebooks and python scripts to reproduce the figures shown in
"[Open source software for simulations and inversions of airborne electromagnetic data](https://doi.org/10.1080/08123985.2019.1583538),"
published in the AEM 2018 special edition of Exploration Geophysics.


<img src="figures/currents.png" width=40% align="middle">

## Summary

Here we run 2D DC resistivity simulations to generate images of the currents, sensitivity and model resolution matrix. 

## Contents

There is 1 notebook in this repository:

- [1_TEM_VerticalConductor_2D_forward.ipynb](/notebooks/1_TEM_VerticalConductor_2D_forward.ipynb) : runs a forward simulation of an airborne electromagnetic simulation over a conductive plate. This notebook was used to generate figures 1-4 in the abstract
- [2_TEM_VerticalConductor_1D_stitched_inversion.ipynb](/notebooks/2_TEM_VerticalConductor_1D_stitched_inversion.ipynb) : Using the forward simulated data from the previous notebook, we run 1D inversions over the plate (Figure 5 in the abstract).
- [3_TEM_VerticalConductor_2D_inversion_load.ipynb](/notebooks/3_TEM_VerticalConductor_2D_inversion_load.ipynb) : This notebook loads the 2D inversion results over the plate (Figure 6 in the abstract). The 2D inversion was run using the script [2dinv_smooth.py](/notebooks/2d_inv_smooth/2dinv_smooth.py).
- [4_TEM_VerticalConductor_parametric_inversion_load.ipynb](/notebooks/4_TEM_VerticalConductor_parametric_inversion_load.ipynb) : This notebook loads the 2D parametric inversion inversion results (Figure 7 in the abstract). The 2D parametric inversion was run using the script [2dinv_parametric.py](/notebooks/2d_inv_parametric/2d_inv_parametric.py) .

In addition, there are two notebooks used for demos in the workshop [3D EM Modelling and Inversion with Open Source Resources](https://courses.geosci.xyz/aem2018):

- [TEM_VerticalConductor_2D_forward.ipynb](/demo_notebooks/TEM_VerticalConductor_2D_forward.ipynb) : runs a forward simulation of an airborne electromagnetic simulation over a conductive plate. Similar to that in the notebooks directory.
- [TDEM_1D_inversion.ipynb](/demo_notebooks/TDEM_1D_inversion.ipynb): In this notebook, we run a 1D inversion for a single airborne time domain EM sounding

## Usage

To run the notebooks locally, you will need to have python installed,
preferably through [anaconda](https://www.anaconda.com/download/) .

You can then clone this repository. From a command line, run

```
git clone https://github.com/simpeg-research/groundwater-book-figures.git
```

Then `cd` into the `groundwater-book-figures` directory:

```
cd groundwater-book-figures
```

To setup your software environment, we recommend you use the provided conda environment

```
conda env create -f environment.yml
conda activate groundwater-book
```

You can then launch Jupyter

```
jupyter notebook
```

Jupyter will then launch in your web-browser.

## Running the notebooks

Each cell of code can be run with `shift + enter` or you can run the entire notebook by selecting `cell`, `Run All` in the toolbar.

<img src="https://em.geosci.xyz/_images/run_all_cells.png" width=80% align="middle">

For more information on running Jupyter notebooks, see the [Jupyter Documentation](https://jupyter.readthedocs.io/en/latest/)

## Issues

Please [make an issue](https://github.com/simpeg-research/groundwater-book-figures/issues) if you encounter any problems while trying to run the notebooks.

## Citation

If you build upon or use these examples in your work, please cite:

Cockett, R., Kang, S., Heagy, L. J., Pidlisecky, A., & Oldenburg, D. W. (2015). SimPEG: An open source framework for simulation and gradient based parameter estimation in geophysical applications. Computers & Geosciences, 85, 142-154.

```
@article{cockett2015simpeg,
  title={SimPEG: An open source framework for simulation and gradient based parameter estimation in geophysical applications},
  author={Cockett, Rowan and Kang, Seogi and Heagy, Lindsey J and Pidlisecky, Adam and Oldenburg, Douglas W},
  journal={Computers \& Geosciences},
  volume={85},
  pages={142--154},
  year={2015},
  publisher={Elsevier}
}
```

Heagy, L. J., Cockett, R., Kang, S., Rosenkjaer, G. K., & Oldenburg, D. W. (2017). A framework for simulation and inversion in electromagnetics. Computers & Geosciences, 107, 1-19.

```
@article{heagy2017framework,
  title={A framework for simulation and inversion in electromagnetics},
  author={Heagy, Lindsey J and Cockett, Rowan and Kang, Seogi and Rosenkjaer, Gudni K and Oldenburg, Douglas W},
  journal={Computers \& Geosciences},
  volume={107},
  pages={1--19},
  year={2017},
  publisher={Elsevier}
}
```


## License
These notebooks are licensed under the [BSD-3 License](/LICENSE) which allows academic and commercial re-use and adaptation of this work.
