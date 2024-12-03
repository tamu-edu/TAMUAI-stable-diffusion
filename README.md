# Stable Diffusion for TAMU-AI

## Overview

This repository is a **customized fork** of the original [Stable Diffusion Web UI](https://github.com/AUTOMATIC1111/stable-diffusion-webui) created by AUTOMATIC1111. It has been tailored for use by **TAMU-AI** with specific modifications to simplify installation and usage.

For the original repository, please visit: [AUTOMATIC1111/stable-diffusion-webui](https://github.com/AUTOMATIC1111/stable-diffusion-webui).

---

## Installation Instructions

Follow the steps below to set up and run the customized Stable Diffusion Web UI:

### **Step 1: Set Up Conda Environment**

1. Create a Conda environment with Python 3.11:
   ```bash
   conda create -n python3.11 python=3.11 -y
   ```
2. Activate the Conda environment:
   ```bash
   conda activate python3.11
   ```
3. Install `pip`:
   ```bash
   conda install pip -y
   pip install --upgrade pip
   ```

---

### **Step 2: Clone the Repository**

1. Clone the customized repository:
   ```bash
   git clone https://github.com/tamu-edu/TAMUAI-stable-diffusion.git
   ```
2. Navigate to the repository directory:
   ```bash
   cd TAMUAI-stable-diffusion
   ```

---

### **Step 3: Install Dependencies**

1. Install the required Python packages:
   ```bash
   pip install -r requirements.txt
   ```

2. Place your model files in the appropriate directory:
   - For example, **`v2-1_768-ema-pruned.ckpt`** and **`v2-1_512-ema-pruned.ckpt`** should be placed in:
     ```plaintext
     models/Stable-diffusion/
     ```

---

### **Step 4: Launch the Web UI**

#### Option 1: Launch Directly with Python
1. Run the application:
   ```bash
   python launch.py
   ```
2. If running without a GPU, use the following command:
   ```bash
   python launch.py --no-half --api --listen --skip-torch-cuda-test
   ```

#### Option 2: Use `webui.sh` Script
1. Replace the default `webui-user.sh` with the Conda-specific version:
   ```bash
   mv webui-user.sh webui-user.sh-bak
   mv webui-user.sh-conda webui-user.sh
   ```
2. Edit `webui-user.sh` and update the Python path:
   ```bash
   python_cmd="/path/to/conda/env/python"
   ```
   Replace `/path/to/conda/env/python` with your Python executable path.

3. Start the Web UI:
   ```bash
   ./webui.sh
   ```

---

## Customization Details

This fork includes adjustments for TAMU-AI usage, including:
- Simplified installation and setup instructions.
- Added commands for CPU-only usage.
- Conda environment configuration.

---

## Acknowledgments

This project is a fork of the original **Stable Diffusion Web UI** created by AUTOMATIC1111. For full documentation and features, please refer to the [original repository](https://github.com/AUTOMATIC1111/stable-diffusion-webui).

---

## What's Next?

Additional features and improvements are under development. Stay tuned for future updates!

---

Created by [Chuck Zuo, Ph.D.](https://github.com/dkflameEDU) - Let's make TAMU-AI great together!
