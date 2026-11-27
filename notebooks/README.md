# Numerical Notebooks

The notebooks are organized by gravitational model. Each notebook contains numerical calculations and plotting cells. Start with a fresh kernel and execute cells sequentially after installing the dependencies in [requirements.txt](../requirements.txt).

| Model | Notebook | Initial reference prescription | Generated output directory |
| --- | --- | --- | --- |
| GR | [GR_LR.ipynb](GR/GR_LR.ipynb) | Exact de Sitter auxiliary mode | `GR_LR_BD_outputs/` |
| Chern–Simons | [PV_CS.ipynb](Chern-Simon/PV_CS.ipynb) | Hypergeometric CS reference (current default) | `parity_violation_CS_BD_outputs/` |
| General PV | [PV_General_WKB.ipynb](General%20parity%20violation/PV_General_WKB.ipynb) | WKB prescription (see notebook) | See notebook |

## Reproducibility notes

- The GR code currently sets the diagonal asymmetry coefficient `b3` to zero and uses `btilde1` and `btilde2` for mixing. Some older explanatory cells and comments use different coefficient labels or settings. The current executable definitions and the final manuscript conventions should be reconciled before release.
- The CS notebook contains a saved error from an earlier execution. Its comparison cell refers to `results_13`, whereas the current third case is stored in `results_31`. The third-case Markdown label also differs from the executable parameter values. Confirm the intended manuscript case before editing and rerunning.
- The General PV notebook was recovered from the original uploaded Git version after an empty file appeared during a file move. Its numerical implementation and dependencies have not yet been independently inspected or rerun.
- The notebooks have not yet been verified together in a clean environment. A successful run and comparison with the manuscript figures are required before declaring a reproducible release.

## Output handling

The GR and CS notebooks save relative to the kernel's current working directory. Copy the final numerical tables and parameter records into the corresponding [data directory](../data/), and the manuscript figures into the corresponding [figure directory](../figure/). Keep different cases in separate folders.
