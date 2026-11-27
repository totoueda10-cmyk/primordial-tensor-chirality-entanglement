# Primordial Tensor Chirality and Quantum Entanglement

Numerical research notebooks for studying how initial quantum entanglement between primordial tensor helicities affects their power spectra and chirality during inflation, using the Schrödinger wave-functional formalism.

This repository accompanies a study comparing general relativity (GR), Chern–Simons (CS) gravity, and general parity-violating (PV) gravity. It distinguishes effects associated with the initial Gaussian state from those associated with helicity-dependent propagation.

**Publication and reproducibility status:** this repository is being prepared for the associated manuscript. The archived numerical tables and publication figures will be added to the directories below. The manuscript citation, release identifier, and tested dependency versions will be recorded when finalized. See [notebook notes](notebooks/README.md) for current verification status.

## Physical framework

| Gravitational model | Parameter choice | Tensor helicity evolution |
| --- | --- | --- |
| General relativity | α = β = 0 | Identical equations of motion |
| Chern–Simons gravity | α = β ≠ 0 | Helicity-dependent evolution, with equal phase velocities |
| General parity-violating gravity | α ≠ β | Helicity-dependent evolution, generally including different phase velocities |

The parameter choices refer to the parity-violating quadratic tensor action used in the study. The notebooks compare initial Gaussian states with and without off-diagonal helicity mixing.

The main quantities are the left- and right-handed tensor auto-spectra, the cross-spectrum, the total tensor power, and the degree of circular polarization. With the L/R ordering and sign convention used in the inspected GR and CS code,

$$
\mathcal{P}_{\mathrm{T}}=\mathcal{P}_{\mathrm{LL}}+\mathcal{P}_{\mathrm{RR}},\qquad
\Pi=\frac{\mathcal{P}_{\mathrm{LL}}-\mathcal{P}_{\mathrm{RR}}}{\mathcal{P}_{\mathrm{LL}}+\mathcal{P}_{\mathrm{RR}}}.
$$

For the restricted GR initial-state family with zero diagonal helicity asymmetry, the two auto-spectra are equal and the chirality vanishes. This is a property of that family, not a restriction on every possible initial state in GR. A nonzero off-diagonal helicity spectrum also requires care in interpreting statistical isotropy.

## Repository structure

| Location | Contents |
| --- | --- |
| [notebooks/](notebooks/) | Numerical calculations and plotting routines |
| [data/](data/) | Archived numerical results and run settings |
| [figure/](figure/) | Archived figures associated with the manuscript |
| [requirements.txt](requirements.txt) | Preliminary Python dependencies |
| [CITATION.cff](CITATION.cff) | Provisional software citation metadata |

### Numerical notebooks

| Model | Notebook |
| --- | --- |
| GR | [GR_LR.ipynb](notebooks/GR/GR_LR.ipynb) |
| Chern–Simons gravity | [PV_CS.ipynb](notebooks/Chern-Simon/PV_CS.ipynb) |
| General parity-violating gravity | [PV_General_WKB.ipynb](notebooks/General%20parity%20violation/PV_General_WKB.ipynb) |

## Installation

Clone the repository and create a Python virtual environment. On macOS or Linux:

```bash
git clone https://github.com/totoueda10-cmyk/primordial-tensor-chirality-entanglement.git
cd primordial-tensor-chirality-entanglement
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
jupyter lab
```

Select the Python kernel associated with the virtual environment. The GR and CS notebooks record Python 3.9.6 in their metadata; exact Python and package versions for the final manuscript runs have not yet been verified. The requirements file is a starting environment, not a locked reproduction environment.

## Running the calculations

1. Open the notebook corresponding to the gravitational model.
2. Check the parameter definitions and initial-state cases against the desired manuscript result.
3. Restart the kernel and run cells in order. Do not rely on variables from a previous session.
4. Inspect the numerical diagnostics, including Gaussian normalizability and the model-specific consistency checks.
5. Compare the generated numerical tables and plots with the archived results in [data/](data/) and [figure/](figure/) once available.

The GR and CS notebooks use relative output paths. Their generated directories are relative to the kernel's working directory, not automatically the repository's data or figure directory. Keep separate case directories to avoid overwriting results with identical filenames. For details, see [notebook notes](notebooks/README.md).

## Numerical data and figures

The data directory is organized by gravitational model. Archive the CSV files underlying the final figures together with their parameter settings, and preserve the original case names or use descriptive names. See [data documentation](data/README.md) for the recommended file layout and conventions.

The figure directory contains the intended archive locations for the manuscript plots. Use PDF for vector figures and PNG for previews when both are available. See [figure documentation](figure/README.md).

## Citation

For now, cite this repository with its URL and the exact commit used. The [citation metadata](CITATION.cff) uses the public repository account as a provisional identifier; formal author names, manuscript details, and any release DOI will be added after confirmation.

## License

A redistribution license has not yet been specified. Public visibility alone should not be interpreted as a license grant. Please contact the repository maintainers about reuse until the license is finalized.
