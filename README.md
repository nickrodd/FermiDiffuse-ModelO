# FermiDiffuse-ModelO

**An improved model of the diffuse emission in the inner galaxy, ideal for studying the galactic center excess.**

[![arXiv](https://img.shields.io/badge/arXiv-2002.0xxxx%20-green.svg)](https://arxiv.org/abs/2002.0xxxx)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

![model_o](https://github.com/nickrodd/FermiDiffuse-ModelO/blob/master/ModelO/Model_O.png "Pi0+Brem emission in default ROI")

## Maps

Counts templates for the neutral pion plus bremsstrahlung (pibrem) and inverse Compton (ics) emission appropriate for analyses of the Fermi galactic center excess are provided. Both files are in the `ModelO` directory and are [healpix](https://healpix.jpl.nasa.gov/) `nside=128` maps provided as numpy arrays. As described in [2002.0xxxx](https://arxiv.org/abs/2002.0xxxx), this model represents a significantly improved fit of the inner galaxy and therefore helps alleviate the central systematic for galactic center excess analyses: uncertainties in the diffuse emission model. 

**NB:** these maps are tailored to a specific region of interest, energy range, and Fermi dataset, and should not be used more generally. See the caveats section below for details.

If you make use of these maps, please cite [2002.0xxxx](https://arxiv.org/abs/2002.0xxxx) for which these specific  maps were created, but also [1611.06644](https://arxiv.org/abs/1611.06644) and [1901.03822](https://arxiv.org/abs/1901.03822) where closely related maps were generated.

## Caveats

The maps provided are designed for use with the following caveats:

- **Region of Interest:** working in galactic coordinates, these maps are designed to be used in a region defined by |b|>2 degrees and r<30 degrees, where r is the angle from the galactic center. 
- **Fermi Dataset:** the maps are designed to be used with the default dataset provided with [NPTFit](https://github.com/bsafdi/NPTFit), see [here](https://nptfit.readthedocs.io/en/latest/Example1_Overview_of_the_Fermi_Data.html) for specifics.

Both maps are normalised so that a coefficient of O(1) is returned from a fit. The units of maps are counts/pixel and thus they have been exposure corrected, and also smoothed according to the appropriate Fermi point spread function.

Equivalent versions of the maps in other regions of interest can be made available upon request.
