# Temp

這是一個範本

## Features


## 🎨 Qualitative Results


## Project Structure

```
.
|-- README.md
|-- configs
|   `-- cfg.yaml
|-- datasets
|-- pyproject.toml
|-- scripts
|-- src
|   `-- temp
|       |-- datasets
|       |-- models
|       `-- utils
|-- tests
`-- uv.lock
```


## Setup and Installation

### 1. Clone the Repository

```bash
uv sync
```

### 1.5. cuda測試
```
python -c "import torch; print(f'CUDA available: {torch.cuda.is_available()}'); print(f'CUDA version: {torch.version.cuda}')"
```

### 2. Create a Python Environment

It is highly recommended to use a virtual environment (e.g., `venv` or `conda`) to manage dependencies. This project requires **Python >= 3.10**.

```bash
# Using conda
conda create -n meanflow python=3.10
conda activate meanflow
```

### 3. Install PyTorch

PyTorch installation depends on your system's CUDA version. It is **intentionally excluded** from `requirements.txt` to ensure a correct installation. Please visit the [official PyTorch website](https://pytorch.org/get-started/locally/) to find the appropriate command for your setup.

**Example for CUDA 12.4:**
```bash
conda install mkl==2023.1.0 pytorch==2.5.1 torchvision==0.20.1 torchaudio==2.5.1 pytorch-cuda=12.4 -c pytorch -c nvidia
```

### 4. Install Other Dependencies

Once PyTorch is installed, install the remaining packages (including `pytorch-fid`) using the provided `requirements.txt` file.

```bash
pip install -r requirements.txt
```


## Dataset Preparation

### 1. Download AFHQ v2 Dataset


### 2. Preprocess Dataset


**Output Structure:**


## Training

### Basic Training

```bash
uv run src/train
```

### Configuration


### Training Outputs


### Monitoring Training


## Hardware & Efficiency


## Inference

### Basic Inference (Grid Visualization)


### FID Generation Mode

**Options:**
| Argument | Default | Description |
|----------|---------|-------------|
| `--ckpt` | Required | Path to checkpoint |
| `--split` | val | Dataset split |





## Performance Analysis


## Acknowledgments

- [MeanFlow](https://arxiv.org/abs/2505.13447) - Original paper
- [ControlNet](https://github.com/lllyasviel/ControlNet) - Zero-convolution and edge preprocessing insights
- [Stable Diffusion VAE](https://huggingface.co/stabilityai/sd-vae-ft-mse) - Pre-trained VAE
- [AFHQ](https://github.com/clovaai/stargan-v2) - Dataset




