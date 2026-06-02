🧠 Calcium Imaging Course
======

Welcome to the class! Follow these instructions sequentially to set up your computer with the necessary notebook, data analysis pipeline and libraries that are required for our calcium imaging tutorial. For this tutorial we will use [CaImAn](https://github.com/flatironinstitute/CaImAn), which is a calcium imaging data analysis toolbox.

# Environment Setup Guide
## Prerequisite: Install Miniforge

Before starting, you should install **Miniforge** on your machine. Miniforge is a community-driven installer for the `conda` package manager. 

* If you do not have it, download and run the installer for your operating system from the [Official Miniforge Page](https://conda-forge.org/download/).

## 🚀 Step-by-Step Installation

Open your **Miniforge Prompt** and run the following blocks of commands one by one.

### 1. Clone the Course Repository

Download our repository of CaImAn containing all custom pipeline configurations, assignment notebooks, and scripts needed for the course:

**NOTE:** prior running the following commands in your miniforge prompt terminal, you might go into the directory where you would like to store the `caiman_class` folder. 

```powershell
git clone https://github.com/MacsmM/caiman_class.git
cd caiman_class
```

### 2. Create the Isolated Python Environment

We provide you with an isolated virtual environment containing Python 3.11, the pre-compiled CaImAn binary core, and the Jupyter Notebook. This step should handle the entire setup: 

```powershell
conda create -n caiman_student python=3.11 uv caiman jupyterlab jupyter_bokeh pyqtgraph -c conda-forge -y
```

### 3. Activate the Environment

Tell your terminal session to use our newly constructed classroom environment space:

```powershell
conda activate caiman_student
```

### 4. Sync Supplemental Libraries

Run the `uv` packages sync command to match the requirements of the project:

```powershell
uv sync
```

### 5. Initialize CaImAn

downloads the official CaImAn tutorial notebooks, creates a `caiman_data` folder and stores example datasets into the directory: 

```powershell
caimanmanager install
```


## 🧪 Testing Your Installation

To verify that your installation was successful, launch the interactive user interface from your terminal:

```powershell
jupyter notebook
```

### Verification Steps inside Jupyter Notebook:

1. When Jupyter Lab opens in your web browser, double-click to open **`demo_pipeline_cnmfE_AS_2026.ipynb`**.
2. Run the first cell of the notebook if it works, you are good to go to follow along with the tutorial.


