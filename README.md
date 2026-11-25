# Find frequency peak of PSD data

<!-- brainlife-app:begin (generated from the App manifest; edit the manifest, not this block) -->

> **Finds the peak frequency of each channel's power spectral density within a chosen frequency band with MNE-Python and outputs a TSV of peaks and summary plots.**

Reads a PSD table (channels by frequencies), restricts it to frequencies between fmin and fmax, and finds the main spectral peak per channel with mne.preprocessing.peak_finder. Use it, for example, to estimate individual alpha peak frequency from MEG/EEG PSDs. It needs a PSD .tsv with a 'channels' column, such as produced by brainlife PSD Apps.

| | |
|---|---|
| 📥 **Inputs** | `neuro/meeg/psd` |
| 📤 **Outputs** | `neuro/meeg/psd` · `raw` |
| 🐳 **Container** | `brainlife/mne:0.23dev` |
| ⚙️ **Resources** | 1 CPUs |
| 🔗 **Run it** | [doi.org/10.25663/brainlife.app.531](https://doi.org/10.25663/brainlife.app.531) |

#### 📥 Inputs

| Input | Datatype | Required | Description |
|---|---|---|---|
| `psd01` | `neuro/meeg/psd` | yes | Power spectral density table (.tsv) with one row per channel and one column per frequency. Must have a 'channels' column; frequency column names must be numeric. |

#### 📤 Outputs

| Output | Datatype | Description |
|---|---|---|
| `out_dir` | `neuro/meeg/psd` | psd.tsv with the peak frequency of each channel. |
| `out_figs` | `raw` | Histogram of peak frequencies across channels and per-channel PSD plots with the detected peaks. |

<details>
<summary><b>⚙️ Parameters</b> (2)</summary>

| Parameter | Type | Default | Description |
|---|---|---|---|
| `fmin` | number | `7.8` | Min frequency of the range (Hz) |
| `fmax` | number | `12.2` | Max frequency of the range (Hz) |

</details>

📚 **References used by this App:**
- Hayashi S, Caron BA, et al. brainlife.io: A decentralized and open source cloud platform to support neuroscience research. arXiv (2023).

<!-- brainlife-app:end -->

[![Abcdspec-compliant](https://img.shields.io/badge/ABCD_Spec-v1.1-green.svg)](https://github.com/brain-life/abcd-spec)
[![Run on Brainlife.io](https://img.shields.io/badge/Brainlife-bl.app.531-blue.svg)](https://doi.org/10.25663/brainlife.app.531)

## Documentation

Detects peak frequency of PSD for each channel on a given bandwith

1) Detect peak frequency for each channel for a given bandwith
2) Input file is:
    * a `.tsv` file containing the signal PSD, Power Spectral Densities
5) Ouput files are:
    * a `.tsv` file containing the peak frequency for each channel
    * a plot with the distribution of all peak frequencies across channels
    * a plot the PSD frequency peak for each channel (peak found in the psd)

## Authors
- [Guiomar Niso](guiomar.niso@ctb.upm.es), Instituto Cajal, CSIC, Spain

## Citations
We kindly ask that you cite the following articles when publishing papers and code using this app. 

1. **brainlife. io: A decentralized and open source cloud platform to support neuroscience research**. Hayashi, S., Caron, B. A., et al. & Pestilli, F. (2023). ArXiv. https://www.ncbi.nlm.nih.gov/pmc/articles/PMC10274934/

## Funding Acknowledgement
brainlife.io is publicly funded and for the sustainability of the project we kindly ask that you acknowledge the following funding sources:

[![NSF-BCS-1734853](https://img.shields.io/badge/NSF_BCS-1734853-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=1734853)
[![NSF-BCS-1636893](https://img.shields.io/badge/NSF_BCS-1636893-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=1636893)
[![NSF-ACI-1916518](https://img.shields.io/badge/NSF_ACI-1916518-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=1916518)
[![NSF-IIS-1912270](https://img.shields.io/badge/NSF_IIS-1912270-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=1912270)
[![NIH-NIBIB-R01EB030896](https://img.shields.io/badge/NIH_NIBIB-R01EB030896-green.svg)](https://grantome.com/grant/NIH/R01-EB030896-01)


#### MIT Copyright (c) 2021 brainlife.io The University of Texas at Austin and Indiana University