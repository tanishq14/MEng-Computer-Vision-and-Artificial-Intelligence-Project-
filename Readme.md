# Master's Thesis — Techniques to overcome class imbalance using anomaly/defect detection

**Overview**
This repository contains the notebooks, experiments, and utilities used for a Master's thesis investigating approaches that treat rare classes as anomalies (or defects) to mitigate severe class imbalance. The work covers three domains: medical imaging (NIH Chest X-ray), industrial inspection (MVTec AD), and network intrusion (UNSW-NB15).

---

## 📁 Background
The repository is notebook-driven and the active files are at the project root.

- `AnomalyDetection_ChestXray_supervised.ipynb` — Experiments on NIH Chest X-ray images (autoencoder, feature extraction, reconstruction-based anomaly scoring, evaluation). 🔬
- `mvtec_anomaly_detection.ipynb` — MVTec AD workflows for industrial defect detection using CNN feature extraction and classical anomaly detectors. 🏭
- `MEng_UN_SW15_Unsupervised_supervised.ipynb` — Network intrusion experiments using UNSW-NB15 features and unsupervised detectors (OC-SVM, Isolation Forest, etc.). 🌐
- `requirements.txt` — Python package requirements used for reproducing the notebooks.

> Note: The notebooks generate intermediate outputs (models, CSV results) when run, but pre-trained model files are not included in the repository by default.

---

## ✅ Quick start (Run locally)
1. Create and activate a Python 3.9+ environment.

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Open and run the notebooks in a Jupyter environment (Jupyter Lab or Notebook). Run cells sequentially.

4. If available, enable GPU to speed up training/feature extraction. Notebooks check `torch.cuda.is_available()` and use it when present.

---

## 📦 Dependencies
Dependencies are listed in `requirements.txt`. Key packages include:

- Python >= 3.9
- torch, torchvision
- scikit-learn, numpy, pandas, scipy
- Pillow (image IO)

---

## 📥 Datasets & Where to get them
Datasets are not included due to licensing and size. Example sources:

- NIH Chest X-ray (CXR) dataset — https://nihcc.app.box.com/v/ChestXray-NIHCC
- MVTec AD dataset — https://www.mvtec.com/company/research/datasets/mvtec-ad/
- UNSW-NB15 — https://research.unsw.edu.au/projects/unsw-nb15-dataset

Place datasets in a folder the notebooks expect (see top cells of each notebook where `DATA_DIR` or dataset path is configured). Update paths in the notebook if your local layout differs.

---

## 🔬 Reproducibility & Outputs
- Notebooks save models and results (check for `models/`, `outputs/` or `results_*.csv` after running cells).
- Set seeds where noted in the notebooks for reproducible runs.

---

## 👩‍💻 Tips & Troubleshooting
- If a notebook fails to find a dataset, verify the `DATA_DIR` path and dataset folder names.
- For large image experiments, use a machine with at least 8–16GB RAM and a CUDA-enabled GPU for practical run times.
- If package versions cause errors, create a fresh virtualenv and install exact versions from `requirements.txt`.

---

## 📚 References
A detailed background reading is included inside the notebooks; see citations and banners within the `report.pdf` for algorithm references.

---

**Short summary:** The repository is notebook-first — open the three notebooks at the project root, install `requirements.txt`, add datasets locally, and run cells to reproduce the experiments. 🔧💡

**Note:** This API is based on research and model experiments conducted in the Master's Thesis Experiments repository.
