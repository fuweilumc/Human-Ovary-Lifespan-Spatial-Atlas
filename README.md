# Human Ovary Lifespan Spatial Atlas

Code associated with the manuscript:

**A single-cell spatial atlas of human ovarian development, cycling and ageing**

This repository contains the analysis and figure-generation code for a Xenium 5K spatial transcriptomic atlas of the human ovary spanning fetal development, childhood, reproductive life and post-reproductive ages.

The analyses include cell-type annotation, lineage-resolved subclustering, spatial analysis, pseudotime reconstruction, cell-niche analysis, pathway analysis and spatial cell-cell communication analysis.

---

## Repository structure

```text
Human-Ovary-Lifespan-Spatial-Atlas/
│
├── Main_figure.ipynb
├── Extended_Data_Fig.ipynb
├── Monocle3_Analysis.ipynb
├── companion_functions.py
├── environment.yml
└── README.md
```

### Files

- **Main_figure.ipynb**  
  Analysis and plotting code used to generate the main figures.

- **Extended_Data_Fig.ipynb**  
  Analysis and plotting code used to generate the Extended Data figures.

- **Monocle3_Analysis.ipynb**  
  Pseudotime and trajectory analyses performed using Monocle 3.

- **companion_functions.py**  
  Helper functions used by the analysis notebooks.

- **environment.yml**  
  Python/Conda environment used for the analyses.

---

## Main analyses

The repository contains code for:

- fetal germ-cell and pregranulosa-cell subclustering
- postnatal oocyte subclustering
- granulosa-, theca-, vascular- and immune-cell analysis
- differential gene-expression analysis
- Monocle 3 pseudotime analysis
- PAGA connectivity analysis
- spatial neighbourhood enrichment
- CellNEST ligand-receptor analysis
- CellCharter spatial niche analysis
- MSigDB Hallmark pathway scoring
- cortical-medullary spatial analysis
- generation of main and Extended Data figures

---

## Software

The main analyses were performed using Python 3.10 and R.

Major packages and software include:

- Scanpy 1.11
- rapids_singlecell 0.10
- scvi-tools 1.4.1
- CellCharter 0.3.0
- CellNEST 1.0.0
- Squidpy
- Matplotlib 3.9.4
- Seaborn 0.13.2
- SciPy 1.17.1
- Dash 2.18.1
- Plotly 5.24.1
- Monocle 3 1.3.1

Custom oocyte segmentation additionally used:

- MATLAB R2024b
- Python 3.11
- TensorFlow 2.19.0
- Xenium Ranger 4.0.0

The complete Python environment is provided in `environment.yml`.

---

## Installation

Clone the repository:

```bash
git clone https://github.com/fuweilumc/Human-Ovary-Lifespan-Spatial-Atlas.git
cd Human-Ovary-Lifespan-Spatial-Atlas
```

Create the Conda environment:

```bash
conda env create -f environment.yml
```

Activate the environment:

```bash
conda activate <environment-name>
```

Then open the notebooks using Jupyter:

```bash
jupyter lab
```

Local input and output paths may need to be adjusted before running the notebooks.

---

## Data requirements

The raw human spatial transcriptomic data are not included directly in this GitHub repository.

The analysis notebooks use processed Xenium data, including:

- gene-expression matrices
- spatial coordinates
- cell-type and subcluster annotations
- donor and section metadata
- follicle and corpus luteum annotations
- spatial niche annotations
- pseudotime results
- CellNEST interaction outputs

Please refer to the Data Availability statement of the associated manuscript for access to the underlying datasets.

---

## Reproducibility notes

Multiple sections from the same donor were not considered independent biological replicates for donor-level comparisons.

Pseudotime and PAGA analyses represent computational ordering or connectivity between transcriptional states and do not by themselves establish lineage relationships.

CellNEST analyses identify candidate spatially supported ligand-receptor interactions and do not demonstrate causal signalling.

---

## Code availability

The code used for this study is available at:

https://github.com/fuweilumc/Human-Ovary-Lifespan-Spatial-Atlas

---

## License

This repository is released under the **MIT License**.

---

## Citation

If you use this code, please cite:

**Wei F. et al. A single-cell spatial atlas of human ovarian development, cycling and ageing.**

The final journal citation and DOI will be added after publication.

---

## Contact

For questions regarding the code and analysis:

**Fu Wei**  
Department of Anatomy and Embryology  
Leiden University Medical Center

For correspondence regarding the study:

**Susana M. Chuva de Sousa Lopes**  
Leiden University Medical Center  
s.m.chuva_de_sousa_lopes@lumc.nl
