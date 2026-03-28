# RRIVis Notebooks

Jupyter notebooks exploring the sky models, beam patterns, and numerical precision considerations relevant to [RRIVis](https://github.com/RRI-interferometry/RRIVis).

## Setup

Requires [Pixi](https://pixi.sh). From this directory:

```bash
pixi install
pixi run lab      # launch JupyterLab
```

This installs all dependencies (healpy, pygdsm, pysm3, etc.) and RRIVis itself in editable mode.

## Notebooks

### `catalogs/` — Diffuse Sky Models

| Notebook | Model | Description |
|----------|-------|-------------|
| `gsm2008.ipynb` | GSM2008 | de Oliveira-Costa et al. (2008) PCA model, 10 MHz – 94 GHz. Basemap, interpolation, and CMB comparisons. |
| `gsm2016.ipynb` | GSM2016 | Zheng et al. (2017) PCA model, 10 MHz – 5 THz. Resolution, data unit, interpolation, and CMB comparisons. |
| `haslam.ipynb` | Haslam 408 MHz | Haslam et al. (1982) map with power-law spectral scaling. Spectral index sensitivity and GSM2008 comparison. |
| `lfsm.ipynb` | LFSM | Dowell et al. (2017) LWA1-based model, 10 – 408 MHz. GSM2008 comparison and CMB analysis. |
| `pysm3.ipynb` | PySM3 | Zonca et al. (2021) component-based model. Individual component SEDs, polarization, and dominance maps. |

### `beams/` — Antenna Beam Patterns

| Notebook | Description |
|----------|-------------|
| `analytic_beam_plotting.ipynb` | Visualization of analytic beam patterns (Gaussian, 2D cuts, feed illumination). |

### `precision/` — Numerical Precision

| Notebook | Description |
|----------|-------------|
| `exponential_precision_errors.ipynb` | Precision of `exp(x) - 1` vs `expm1(x)` in the RIME phase term. |
| `logarithm_precision_errors.ipynb` | Precision of `log(1 + x)` vs `log1p(x)` in the inverse Planck formula. |
| `rayleigh_jeans_vs_planck.ipynb` | Rayleigh-Jeans approximation vs full Planck function across radio frequencies. |
