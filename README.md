# TrivialAugment implementation

A notebook-based implementation of TrivialAugment with a CIFAR-10 training experiment using WideResNet-28-10.

## Quick start

Open `TrivialAugment.ipynb` in Jupyter or Google Colab and execute the cells in order.

```bash
python -m venv .venv
# macOS/Linux
source .venv/bin/activate
# Windows PowerShell: .venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
jupyter notebook TrivialAugment.ipynb
```

A CUDA-capable GPU is recommended for training.

## Repository layout

- `TrivialAugment.ipynb` — canonical augmentation implementation, model, data pipeline, training, and observations.
- `docs/REPRODUCIBILITY.md` — environment and experiment notes.
- `requirements.txt` — Python dependencies.

## Experiment overview

The notebook samples one augmentation operation and a magnitude for each image, then trains a WideResNet on CIFAR-10. It includes its own configuration and reported observations. These should be interpreted as the results of this particular notebook run, not as an independently verified reproduction of the paper.

## Data

CIFAR-10 is downloaded through torchvision into `./data`.

The original notebook remains unchanged in this cleanup branch.
