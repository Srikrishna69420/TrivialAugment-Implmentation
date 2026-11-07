# Reproducibility notes

## Canonical implementation

Run `TrivialAugment.ipynb` from top to bottom. It defines the augmentation operations and pool, TrivialAugment transform, WideResNet, CIFAR-10 loaders, optimizer/scheduler, training loop, and observations.

## Dataset

CIFAR-10 is loaded using `torchvision.datasets.CIFAR10(download=True)` and stored under `./data` relative to the notebook's working directory.

## Environment

Install `requirements.txt`. The notebook uses PyTorch, torchvision, NumPy, and Pillow. For GPU runs, install a compatible PyTorch/torchvision build for the host's CUDA runtime.

## Configuration

The notebook defines epoch count, batch size, learning rate, momentum, weight decay, label smoothing, and data-loader worker count in its configuration cell. Record these values, random seeds, Python/PyTorch/torchvision versions, GPU model, and runtime when reporting results.

## Results and caveats

The notebook contains the experiment's own runtime and accuracy observations. These are not guaranteed to reproduce on different hardware/software. Do not compare results without matching the data pipeline, training configuration, and evaluation protocol.

## Artifacts

CIFAR-10 data is downloaded locally. Keep generated checkpoints and logs out of Git unless they are deliberately selected as project artifacts.
