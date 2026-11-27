# Numerical Data

This directory is reserved for the numerical results underlying the associated manuscript.

| Gravitational model | Directory |
| --- | --- |
| General relativity | [GR/](GR/) |
| Chern–Simons gravity | [Chern-Simon/](Chern-Simon/) |
| General parity-violating gravity | [General parity violation/](General%20parity%20violation/) |

## Archiving results

For each calculation, keep the original CSV file and a record of the run settings (JSON when available, or a short Markdown/text file). Use separate subdirectories for different initial-state cases so that identical filenames do not overwrite one another. Include the manuscript figure or panel identifier in the run record once finalized.

Record the model parameters, initial-state mixing amplitudes and phases, wavenumber range and grid size, initial and final conformal times, normalization convention, and ODE solver tolerances. If the notebook saves a settings file, archive it without alteration.

The data are numerical predictions, not observational measurements.

## Column conventions

The exact column headers are provided in each CSV. Common quantities in the inspected GR and CS implementations are:

| Quantity | Meaning |
| --- | --- |
| k | Comoving wavenumber in the numerical convention |
| x_initial | Initial dimensionless scale, -k tau_i, when provided |
| P_LL, P_RR | Left- and right-helicity auto-spectra |
| P_LR, P_RL | Helicity cross-spectra (complex; some files store real and imaginary parts separately) |
| P_total | Sum of the two auto-spectra |
| Pi | Chirality, (P_LL - P_RR) / (P_LL + P_RR), in the inspected code |
| Normalizability margin / minimum eigenvalue | Diagnostic of positive definiteness of the Gaussian quadratic form |

For normalized ratios, identify the denominator explicitly. A GR BD reference is not the same as an unentangled reference in a parity-violating model. Some GR CSV files use complex-valued columns; read those using the dtype appropriate to the file rather than assuming that every column is real.

The directories below are ready for the final data files.
