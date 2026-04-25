# HueP³-LLM

HueP³-LLM is a photovoltaic power forecasting framework based on pre-trained large language models.

This project focuses on photovoltaic power time-series forecasting and explores how the sequence representation capability of pre-trained large language models can be transferred to photovoltaic power prediction.

> The manuscript is currently under submission. To avoid affecting anonymous review and subsequent publication, this README only provides a high-level project description, the main entry points, and limited workflow information.

## Project Status

- Working model name: `HueP³-LLM`
- Task: photovoltaic power forecasting
- Technical direction: photovoltaic power sequence forecasting based on pre-trained LLMs
- Current status: manuscript under submission
- Source code plan: the full reproducible version will be released after paper acceptance

## Repository Overview

This repository contains research-stage code for training, testing, prediction, and ablation experiments. The primary workflow is organized around the following internal modules:

```text
Config.py       # Main experiment configuration
DataModule.py   # Data loading, preprocessing, splitting, and DataLoader logic
AutoModel.py    # HueP³-LLM model wrapper and Lightning training logic
run_setting.py  # Training, testing, and prediction entry points
```

Additional modules are used for model components, baseline methods, ablation studies, fine-tuning experiments, and analysis utilities. Their organization may be adjusted before the public release.

## Main Workflow

The current internal experiment workflow is roughly as follows:

1. Prepare photovoltaic power sequences, meteorological variables, and timestamps.
2. Place the pre-trained LLMs under the local `PretrainedModels/` directory.
3. Configure the LLM name, input sequence length, prediction length, patch length, batch size, learning rate, and other parameters through the configuration module.
4. Use the data module for data loading, normalization, train/validation/test splitting, and nighttime mask construction.
5. Build HueP³-LLM with the model wrapper, then train, test, or predict through PyTorch Lightning.

The current root-level script entry points include:

```bash
python train.py
python test.py
python predict.py
```

These scripts still retain research-stage local paths, default experiment settings, and checkpoint conventions. They are not yet intended as a formal public reproduction interface.

## Environment

The project uses Python, PyTorch, PyTorch Lightning, Transformers, DeepSpeed, FlashAttention, and related dependencies. Dependency information can be found in:

```text
pyproject.toml
uv.lock
```

Since the current version is still under submission, dataset paths, pre-trained model paths, checkpoint paths, and complete experimental parameters have not yet been organized into a public reproduction format.

## Source Code Availability

HueP³-LLM is currently under manuscript submission. The complete source code and reproducible experiment settings will be released after the paper is accepted.

More details will be made available after acceptance.
