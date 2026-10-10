<div align="center">

# 🎯 WQU Computer Vision Lab

**Six applied computer vision projects in PyTorch from image classification to object detection and generative AI.**

![Python](https://img.shields.io/badge/Python-3.11-3776AB?style=flat-square&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-2.3.1-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![Platform](https://img.shields.io/badge/Platform-Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)
![Status](https://img.shields.io/badge/Status-In%20Progress-orange?style=flat-square)

[Overview](#-overview) · [Projects](#-projects) · [Quick Start](#-quick-start) · [Structure](#-repository-structure) · [Workflow](#-project-workflow) · [Ethics](#-data-ethics-and-reproducibility)

</div>

---

## 📌 Overview

This repository contains my work for the **Computer Vision Lab** course at [WorldQuant University (WQU)](https://www.wqu.edu). Each project tackles a real-world problem across conservation, agriculture, urban systems, media, healthcare, and marketing, and follows the full machine learning lifecycle: data acquisition, preprocessing, modeling, training, evaluation, and documentation.

**Goals**

- Build practical, end-to-end computer vision pipelines in PyTorch.
- Apply transfer learning, data augmentation, and appropriate evaluation metrics.
- Keep experiments reproducible with fixed seeds, config files, and a clean structure.
- Document methodology, results, and limitations honestly.

> **Note:** This is an independent learning repository. It is not affiliated with or endorsed by WorldQuant University.

## 📁 Projects

| # | Project | Domain | Task | Status |
|:-:|---|---|---|:-:|
| 01 | [Wildlife Conservation — Côte d'Ivoire](./01-wildlife-conservation-cote-divoire) | Conservation | Image classification | 🔄 In progress |
| 02 | [Crop Disease — Uganda](./02-crop-disease-uganda) | Agriculture | Image classification | ⬜ Planned |
| 03 | [Traffic Monitoring — Bangladesh](./03-traffic-monitoring-bangladesh) | Urban systems | Object detection | ⬜ Planned |
| 04 | [Celebrity Sightings — India](./04-celebrity-sightings-india) | Media | Face recognition | ⬜ Planned |
| 05 | [Medical Data — Spain](./05-medical-data-spain) | Healthcare | Medical image analysis | ⬜ Planned |
| 06 | [Social Media Marketing — WQU](./06-social-media-marketing-wqu) | Marketing | Image analysis / generative AI | ⬜ Planned |

**Legend:** ✅ Complete · 🔄 In progress · ⬜ Planned

### Results

Results are added per project as each one is completed.

| # | Model | Key metric | Score | Notes |
|:-:|---|---|:-:|---|
| 01 | — | — | — | — |

## 🛠️ Tech Stack

| Area | Tools |
|---|---|
| Language | Python 3.11 |
| Deep learning | PyTorch, Torchvision |
| Data | NumPy, Pandas, Scikit-learn |
| Vision | Pillow, OpenCV, Albumentations |
| Visualization | Matplotlib |
| Config & tooling | YAML, Jupyter, Git, VS Code |

Exact versions are pinned in [`requirements.txt`](./requirements.txt). Individual projects may add their own dependencies.

## 🚀 Quick Start

**Prerequisites:** Git, Python 3.11, and (optionally) a CUDA-capable GPU.

```bash
# 1. Clone
git clone https://github.com/rabi-sah/wqu-computer-vision-lab.git
cd wqu-computer-vision-lab

# 2. Create a Python 3.11 virtual environment
python3.11 -m venv .venv
# or, with uv:
# uv venv --python 3.11 .venv

# 3. Activate it
source .venv/bin/activate          # Bash / Zsh
# source .venv/bin/activate.fish   # Fish

# 4. Install dependencies
python -m pip install -r requirements.txt
```

Verify the setup:

```bash
python -c "import torch; print(torch.__version__, torch.cuda.is_available())"
```

<details>
<summary><b>Troubleshooting</b></summary>

- **PyTorch install fails:** PyTorch 2.3.1 needs a build matching your Python version and hardware. See the [previous versions guide](https://pytorch.org/get-started/previous-versions/).
- **`pip` missing in the venv:** run `uv pip install --python .venv/bin/python pip`, then retry step 4.
- **Wrong interpreter in VS Code:** press `Ctrl+Shift+P` → `Python: Select Interpreter` → choose `.venv/bin/python`.

</details>

### Running a project

Each project has its own README with data download steps and run instructions:

```bash
cd 01-wildlife-conservation-cote-divoire
python main.py --config configs/config.yaml
```

*(Entry points and arguments vary by project.)*

## 📂 Repository Structure

```text
wqu-computer-vision-lab/
├── 01-wildlife-conservation-cote-divoire/
│   ├── README.md
│   ├── notebooks/        # Exploration and experiments
│   ├── src/              # Reusable code (datasets, models, training)
│   ├── configs/          # YAML configs
│   ├── data/             # Datasets (git-ignored)
│   └── outputs/          # Figures, metrics, checkpoints (mostly git-ignored)
├── 02-crop-disease-uganda/
├── 03-traffic-monitoring-bangladesh/
├── 04-celebrity-sightings-india/
├── 05-medical-data-spain/
├── 06-social-media-marketing-wqu/
├── certificates/         # Course credentials
├── environment.yml
├── requirements.txt
├── .gitignore
└── README.md
```

Layouts inside each project may evolve as development progresses.

## 🔄 Project Workflow

1. **Problem definition** — task, success criteria, evaluation metric.
2. **Data acquisition** — obtain the dataset and record its source and license.
3. **Preprocessing** — clean, split, resize, normalize, augment.
4. **Modeling** — baseline first, then transfer learning or stronger architectures.
5. **Training** — tracked hyperparameters, seeds, and learning curves.
6. **Evaluation** — task-appropriate metrics, confusion matrices, error analysis.
7. **Visualization** — predictions, failure cases, and training curves.
8. **Documentation** — methods, results, limitations, and lessons learned.

## 🔒 Data, Ethics, and Reproducibility

- Respect dataset licenses and terms of use; document every data source.
- Never commit private, restricted, or sensitive data.
- Consider consent, privacy, and bias, especially for face recognition (Project 04) and medical images (Project 05).
- Keep datasets, checkpoints, and logs out of Git unless there is a clear reason to version them.
- Record seeds, hyperparameters, and metrics so results can be reproduced.

<details>
<summary><b>Recommended <code>.gitignore</code> rules</b></summary>

```gitignore
# Python
__pycache__/
*.py[cod]
.venv/
venv/
env/

# Secrets
.env
.env.*

# Jupyter
.ipynb_checkpoints/

# Data
data/
datasets/

# Models and outputs
checkpoints/
*.pt
*.pth
*.ckpt
outputs/checkpoints/
outputs/logs/
logs/

# Editor / OS
.vscode/
.idea/
.DS_Store
```

</details>

## 🏆 Certification

| Credential | Status | Link |
|---|---|---|
| WQU Computer Vision Lab | 🔄 In progress | — |

Completed credentials are stored in [`certificates/`](./certificates).

## 📝 Learning Approach

I build these projects incrementally and prioritize understanding over leaderboard scores: starting from simple baselines, comparing alternatives, analysing failure modes, and writing down what each experiment taught me.

## 📄 License

Released under the [MIT License](./LICENSE). Datasets and pretrained models may carry their own licenses; check each project's README.

---

<div align="center">

**Built one project at a time.** 🚀

</div>
