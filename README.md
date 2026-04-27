****[README.md](https://github.com/user-attachments/files/27098666/README.md)
# National-Scale Nitrogen Budget for Indian Agriculture: An Environmentally Extended Input–Output Model

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.XXXXXXX.svg)](https://doi.org/10.5281/zenodo.XXXXXXX)

> **Associated publication:** Babbar, D., & Balasubramanian, S. (provisionally accepted). *National-scale nitrogen budget reveals large inefficiencies in Indian agriculture.* Communications Earth & Environment.

---

## Overview

India has pledged to halve nitrogen (N) waste by 2030, yet achieving this target demands a system-scale understanding of where and how nitrogen is lost across the agricultural system. This repository provides the data and code underlying a national-scale Environmentally Extended Input–Output (EEIO) model that quantifies nitrogen inputs, flows, and losses across India's cropland, livestock, and aquaculture sectors for the years 2000 and 2020.

## Repository Structure

```
N-ag-EEIO-India/
│
├── Supplementary Information.xlsx   # Data for all figures and tables in the paper
├── uncertainty/                     # Python scripts for uncertainty analysis
│   └── uncertainty_analysis.py
└── README.md
```

---

## Model Description

The EEIO model tracks nitrogen through a fundamental flow balance:

**Input = Products + Pollutants + Accumulation**

- 15 N input sources tracked across inorganic and organic pathways — including synthetic fertilizers (urea, N-P-K), biological N fixation, atmospheric deposition, manure, irrigation, human/industrial/kitchen waste, straw recycled, and seed
- 8 N reservoirs — including grains for human consumption, livestock and fish feed, fuel/industrial/export products, soil N accumulation, manure, and surplus N pools
- 5 Nr loss processes — volatilization, biomass burning (crop residue and manure for cooking), nitrification/denitrification, leaching, and runoff
-  pollutant outputs — NH₃, NOₓ, N₂O, NO₂⁻, NO₃⁻

**Sector-specific EEIO formulations (SI-1) ensure no double-counting of N flows across the cropland, livestock, and aquaculture subsystems. Circularity is resolved prior to budget closure. Surplus N accumulation is computed as the residual between inputs and tracked outputs, consistent with other national-scale N budget methodologies.
**---

## Data

**`Supplementary Information.xlsx`** contains all data required to reproduce the figures and tables in the associated publication, including:

- N input source data by sector (cropland, livestock, aquaculture)
- N flow estimates for 2000 and 2020
- Nr loss estimates by process and pollutant
- NUE calculations by sector
- Data sources and references (Table S5)
- Model validation against global agriculture residue burning datasets (Figure S2)

**Software required:** Microsoft Excel (or compatible — Google Sheets, LibreOffice Calc)

---

## Uncertainty Analysis

The uncertainty code quantifies the propagated uncertainty in N flow and loss estimates.

**Software required:** Python 3.x or [Google Colab](https://colab.research.google.com/) (no local installation needed)

### Run in Google Colab (recommended)
1. Upload `uncertainty_analysis.py` to your Colab session
2. Run all cells

### Run locally
```bash
pip install numpy pandas matplotlib
python uncertainty_analysis.py
```

---

## Authors

**Deepakshi Babbar** and **Srinidhi Balasubramanian**  
Indian Institute of Technology Bombay (IIT Bombay)

---

## Citation

If you use this data or code, please cite the associated publication:

> Babbar, D., & Balasubramanian, S. (under review). National-scale nitrogen budget reveals large inefficiencies in Indian agriculture. *Communications Earth & Environment.*

And this repository:

> Babbar, D., & Balasubramanian, S. (2025). *N-ag-EEIO-India* [Dataset and code]. Zenodo. https://doi.org/10.5281/zenodo.XXXXXXX

---

## License

This repository is shared for research and educational purposes. Please contact the authors before reuse in commercial applications.

---

## Contact

For questions about the model or data, please open a GitHub Issue or contact the authors via IIT Bombay.
****
