# Pre-registered Ger-26 test plan for 3I/ATLAS (C/2025 N1)

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Lumina26/ger26-atlas-prereg/blob/main/notebooks/atlas_prereg_stub.ipynb)

This repository hosts the public materials for the preregistered, falsifiable test plan for interstellar comet 3I/ATLAS (C/2025 N1), based on the Ger-26 framework and the Ger-Goldschmidt Core Equation (GGCE).

**DOI (Zenodo):** https://doi.org/10.5281/zenodo.16945756  
**Preprint:** ResearchGate (same title)

## What's here

- `notebooks/atlas_prereg_stub.ipynb` - a stub notebook that opens in Google Colab.
- `docs/analysis_spec_v0.3.md` - analysis spec v0.3 (frozen) that details spectral windows and processing choices.
- `notebooks/test_b_lightcurve_form.ipynb` - a ready-made form for Test B (phase-locked light-curve microstructure).
- `notebooks/test_d_polarimetry_form.ipynb` - a ready-made form for Test D (polarimetric texture).
- `data_templates/photometry_epoch1.csv` and `data_templates/photometry_epoch2.csv` - templates for two photometry epochs used by Test B.
- `data_templates/polarimetry.csv` - a template for polarimetry input used by Test D.

Launch the Test B and Test D notebooks directly in Colab:

[![Run Test B in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Lumina26/ger26-atlas-prereg/blob/main/notebooks/test_b_lightcurve_form.ipynb)

[![Run Test D in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Lumina26/ger26-atlas-prereg/blob/main/notebooks/test_d_polarimetry_form.ipynb)

## What's coming (within 10 days)

- **Test A**: Orbit residual harmonics (Lomb-Scargle / wavelets; nuisance jet/spin models)
- **Test B**: Phase-locked light-curve microstructure (folding; matched filtering)
- **Test C**: Isotopic/compositional clustering (high-S/N spectra; Bayesian mixtures)
- **Test D**: Polarimetric texture (residuals vs standard phase curve)

All methods will be runnable in Colab with clear parameters and figures.

## License

- Code: MIT (see `LICENSE`)
- Text in this repo: © 2025 Goldschmidt & Ger. All textual content is available under **CC BY 4.0**.

**Contact:** ngoldsch@citadel.edu
