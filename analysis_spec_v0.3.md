# Ger-26 Analysis Spec v0.3 (Test C)

Date: 2025‑09‑07

This document freezes the analysis settings for **Test C** (Isotopic/compositional clustering) as preregistered in the Ger‑26 test plan for interstellar comet **3I/ATLAS (C/2025 N1)**. These settings must not be modified after this date, except in the case of later public errata from instrument teams.

## Spectral windows

### JWST/NIRSpec windows

The table below lists the wavelength windows that will be used to extract line fluxes from JWST/NIRSpec spectra.  Continuum windows adjacent to each line will be used to fit and subtract the continuum prior to measuring the net line flux.  These choices are frozen now.

| Species | Line window (µm) | Continuum windows (µm) | Notes |
|-------|------------------|-------------------------|-------|
| **H₂O (ν₃)** | 2.64 – 2.80 | 2.58 – 2.62 and 2.82 – 2.85 | Continuum fitted using a sigmoid×linear function to account for the broad water‑ice absorption. |
| **CO₂ (ν₃)** | 4.24 – 4.35 | 4.15 – 4.22 and 4.38 – 4.45 | Continuum fitted with a third‑order polynomial. |
| **CO (Δv = 1)** | 4.62 – 4.74 | 4.55 – 4.60 and 4.75 – 4.85 | Continuum fitted with a third‑order polynomial. |
| **OCS (ν₃)** | 4.83 – 4.88 | Same as CO continuum windows | OCS is measured jointly with the CO window. |

### Optical emission lines

Recent VLT observations detected strong **CN** and **Ni I** emission and found **Fe I** absent.  To incorporate these findings into the mixture model we adopt a fixed ±0.20 nm window around each optical line centre.  Continuum windows span 0.40 nm on either side of the line and are fitted with a first‑order polynomial.  The g‑factor values used to convert fluxes to production rates will be fixed ahead of time and documented separately.

| Line | Centre wavelength (nm) | S/N threshold |
|-----|------------------------|--------------|
| **CN (388.3 nm group)** | 388.3 | ≥ 5 |
| **Ni I (342.6 nm)** | 342.6 | ≥ 5 |
| **Fe I (372.0 nm)** | 372.0 | ≥ 5 |

## Analysis procedure

1. **Extraction:**  For each spectrum, extract fluxes within the line windows above.  Fit the continuum in the adjacent windows and subtract it to obtain a net line flux.  Propagate per‑pixel uncertainties to obtain line‑flux uncertainties.
2. **Conversion to column densities:** Convert net line fluxes to molecule production rates or column densities using published fluorescence efficiencies or g‑factors appropriate for 3I/ATLAS at the observing geometry.  These g‑factor values are fixed now and will be released alongside the code.
3. **Ratios:**  Form compositional ratios such as CO₂/H₂O, CO/H₂O, CN/H₂O, Ni/Fe, and isotopic ratios such as ¹²C/¹³C from CO₂ and CN isotopologues.  Ratios use line fluxes or column densities and their uncertainties.
4. **Bayesian mixture model:** Compare the derived ratios to the distribution of ratios for known Oort‑cloud and Jupiter‑family comets using the preregistered Bayesian mixture model.  Compute posterior probabilities for membership in each natural family and the Bayes factor for the engineered hypothesis.
5. **Decision rule:**  If the posterior probability of belonging to the natural family is less than 0.1 % or the ratio lies more than five standard deviations from the natural distribution, **Test C** returns an **engineered‑pass**.  Otherwise it returns a **natural‑pass**.

## Signal‑to‑noise thresholds

We require a signal‑to‑noise ratio ≥ 5 for each line to include it in the ratio analysis.  Lines below this threshold are treated as nondetections and handled with upper limits in the mixture model.

## Data policy

Some raw spectra may be subject to proprietary periods.  In compliance with our preregistration, we will release only derived line fluxes, ratios, uncertainties, and Bayes factors until the public release of the underlying spectral products.  Once the embargo is lifted, the full spectra and code will be released publicly without modification to the analysis settings frozen here.