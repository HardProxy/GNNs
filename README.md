======================================================

**GNNs to predict physical properties**

Author: Otaviano da Cruz Neto
Class: Deep Learning (CAP-421-3)


National Institute of Spatial Research (INPE)

======================================================

# Deep Learning Finals Project

This directory is splitted in `references` and `code`. The code directory have the `gridsearch` directory to evaluate all models using parallel jobs to compute different models.

## QM9 Dataset

The [QM9 dataset](https://arxiv.org/abs/1703.00564) compile 134K organic molecules graphs that contains 19 physical properties based in DFT calculations. The data will downloaded will running the `searchgrid.py` code.

## Requirements 

The project require the follow libraries:

- `optuna`: MLOps library to run different models in parallel.
- `tensorboard`: MLOps library to compile information through the different models.
- `torch`: General purpose ML modeling.
- `torch geometric`: General prupose ML modeling on graph aproach.

The `setup.sh` install all requirements needed in this project.

> After all installation processes and you are using a RTX device from NVIDIA, read the `pytorch_RTX3060.txt` file.

## Grid Search

To run the `gridsearch.py` program you just need to execute the follow:

> `python3.9 gridsearch.py`

This program will save two `files` and one `directory`:

- `df_all_trials.csv`: All hyperparameters from all trials and the metrics values.
- `df_best_trials.csv`: All hyperparameters from the best models, ranked.
- `/runs`: All information about learning process.

## Tensorboard dashboard

To view `tensorboard` dashboard is needed to run the follow comand:

> `tensorboard --logdir=runs`

This comand will show the `url` to view the dashboard with all informations.
