# Prototypical Multiple Instance Learning for Lymph-Node Metastasis (Camelyon16)

Reimplementation of Prototypical MIL for predicting lymph-node metastasis from whole-slide images with slide-level labels only: tile extraction, patch features, prototype discovery, patch-to-prototype soft-assignment histograms and slide classification, organised as storage-frugal Colab pipelines.

## Contents

| File | What it does |
|---|---|
| `notebooks/PMIL_colab_pipeline.ipynb` | PMIL — Storage-Frugal, Algorithm-Faithful Colab Pipeline (v2) |
| `notebooks/PMIL_Colab_SelfContained.ipynb` | PMIL on Colab — fully self-contained |
| `notebooks/pmil_camelyon16_pipeline.ipynb` | PMIL — Camelyon16 Data Prep Pipeline |
| `notebooks/PMIL_Colab_Runbook.ipynb` | PMIL reproduction — Google Colab runbook |
| `notebooks/PMIL_Colab.ipynb` | PMIL on Colab |

Notebooks are saved with the outputs of their last run, so results and figures can be read on GitHub without running anything.

## Data

CAMELYON16 whole-slide images (Grand Challenge). Slides and checkpoints are not committed.

## How to run

The notebooks were developed on Google Colab. Upload a notebook to Colab (File → Upload notebook) and run the cells in order; the first cells install anything missing. To run locally in VS Code instead: `python -m venv .venv`, activate it, `pip install -r requirements.txt jupyter`, then open the notebook and pick the `.venv` kernel. Cells that mount Google Drive (`google.colab`) can be skipped locally if the data files are placed next to the notebook. A GPU runtime is needed for feature extraction and training.

Python packages used: `gdown`, `matplotlib`, `numpy`, `openslide`, `pandas`, `pillow`, `requests`, `scikit-learn`, `torch`, `torchvision` (see `requirements.txt`).

## License

MIT, see `LICENSE`.
