# VISTA-Z

VISTA-Z is an automated Python-based pipeline for vascular imaging, segmentation, and topology analysis in zebrafish confocal microscopy data. This repository provides the notebooks used for VISTA-Z analyses and benchmarks, including preprocessing, segmentation, quantitative metrics, and visualisation.

## Developers

- fishyvessels (repository owner)
- ignaciorodriguezpastrana (repository contributor)
- Contributors (see repository history for additional contributors)

## Repository Contents

The primary analysis workflows are provided as Jupyter notebooks in the Codes directory:

- VISTA-Z_dorsal.ipynb: Dorsal brain vasculature analysis workflow.
- VISTA-Z_lateral.ipynb: Lateral vasculature analysis workflow.
- VISTA-Z_ROI.ipynb: Region-of-interest analysis workflow.
- VISTA-Z_ISV_loss.ipynb: Intersegmental vessel loss analysis.
- 3D_volume_rendering.ipynb: 3D rendering and visualisation.
- Colocalisation_analysis.ipynb: Colocalisation analysis.

## Inputs and Outputs

### Inputs

- Raw microscopy images (typically CZI) of zebrafish vasculature.
- Optional metadata such as pixel size and z-step (used for physical unit conversion).
- Optional region-of-interest (ROI) definitions for targeted analysis.

### Outputs

- Segmentation masks and vessel centreline (skeleton) images.
- Quantitative metrics tables (Excel), including:
    - Summary results per embryo (vessel density, total network length, segment count branchpoint density, diameter measurements, etc.).
    - Raw results from diameter and vessel length measurements.
- Visualisation figures for quality control and data analysis.

## Installation

### Windows

1. Install Python 3.10 from https://www.python.org/downloads/
	- Ensure you check "Add Python to PATH" during installation.
2. Install Visual Studio Code from https://code.visualstudio.com/
3. Install VS Code extensions:
	- Python (Microsoft)
	- Jupyter (Microsoft)
	- Pylance (Microsoft)
4. Open this repository folder in VS Code.
5. Create and activate a virtual environment:
	- Open the VS Code terminal and run:
	  - python -m venv .venv
	  - .venv\Scripts\activate
6. Install dependencies:
	- pip install -r Codes/requirements.txt

### macOS

1. Install Python 3.10:
	- Option A: Download from https://www.python.org/downloads/
	- Option B (Homebrew): brew install python@3.10
2. Install Visual Studio Code from https://code.visualstudio.com/
3. Install VS Code extensions:
	- Python (Microsoft)
	- Jupyter (Microsoft)
	- Pylance (Microsoft)
4. Open this repository folder in VS Code.
5. Create and activate a virtual environment:
	- python3.10 -m venv .venv
	- source .venv/bin/activate
6. Install dependencies:
	- pip install -r Codes/requirements.txt

## Running the Analysis

1. Open a notebook in the Codes directory.
2. When prompted, select the Python 3.10 interpreter from the .venv environment.
3. Run cells from top to bottom. Each notebook contains parameter fields for input paths and output directories.
4. Outputs will be written to the directories specified in the notebook.

## References and Datasets

If you use this repository, please cite the following manuscripts and datasets as appropriate.

### Manuscripts

1. Rodriguez-Pastrana, I., Richens, J., and Wilkinson, R. N. (2026).
	Automated analysis of zebrafish vascular networks using the VISTA-Z pipeline (preprint). https://doi.org/10.21203/rs.3.rs-8402098/v1

2. McGarry, S. D., Adjekukor, C., Ahuja, S., Greysson-Wong, J., Vien, I.,
	Rinker, K. D., and Childs, S. J. (2024).
	Vessel Metrics: A software tool for automated analysis of vascular structure in confocal imaging. Microvascular Research, 151, 104610.
	https://doi.org/10.1016/j.mvr.2023.104610

### Datasets

1. Rodriguez-Pastrana, I., Richens, J. and Wilkinson, R. N. (2026).
	Automated analysis of zebrafish vascular networks using the VISTA-Z pipeline.
	Test image datasets are available at BioImages Archive: https://doi.org/10.6019/S-BIAD2914

## Licence

This project is licensed under the MIT License. See LICENSE for details.

