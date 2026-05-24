# 🧠 Calcium Imaging Course: Environment Setup Guide

Welcome to class! Follow these instructions sequentially to set up your computer with the necessary data analysis tools, libraries, and sample datasets required for our calcium imaging tutorial.

## Prerequisite: Install Miniforge

Before starting, you must have **Miniforge** installed on your machine. Miniforge provides the terminal architecture (`conda`) used to download the heavy scientific software libraries.

* If you do not have it, download and run the installer for your operating system from the [Official Miniforge GitHub Page](https://github.com/conda-forge/miniforge).
* *Windows users:* During installation, ensure you check the box to add Miniforge to your local environment paths if prompted.

---

## 🚀 Step-by-Step Installation

Open your **Miniforge Prompt** (Windows) or standard terminal (Mac/Linux) and run the following blocks of commands one by one.

### 1. Clone the Course Repository

Download our master classroom repository containing all custom pipeline configurations, assignment notebooks, and scripts:

```powershell
git clone https://github.com/MacsmM/caiman_class.git
cd caiman_class

```

### 2. Create the Isolated Python Environment

We will provision an isolated virtual environment containing Python 3.11, the pre-compiled CaImAn binary core, and our Jupyter interface tools. This step completely handles complex system dependencies without requiring you to install a C++ compiler:

```powershell
conda create -n caiman_student python=3.11 uv caiman jupyterlab jupyter_bokeh pyqtgraph -c conda-forge -y

```

### 3. Activate the Environment

Tell your terminal session to use our newly constructed classroom environment space:

```powershell
conda activate caiman_student

```

### 4. Sync Supplemental Libraries

Run the speed-optimized `uv` package sync to verify and secure all locked background framework interfaces:

```powershell
uv sync

```

### 5. Initialize the CaImAn Data Playground

Extract the large default testing datasets, calcium movie loops (`.tif`), and analysis metrics directly into your user profile profile layout:

```powershell
caimanmanager install

```

---

## 🧪 Testing Your Installation

To verify that your installation was completely successful and ready for lab work, launch the interactive user interface from your terminal:

```powershell
jupyter lab

```

### Verification Steps inside Jupyter Lab:

1. When Jupyter Lab opens in your web browser, double-click to open **`demo_pipeline_cnmfE_AS_2026.ipynb`** from the left sidebar file navigator.
2. Run the first cell of the notebook if it works, you are good to go to follow along with the tutorial.


