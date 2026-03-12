# MNIST Experiments for Anonymous Submission

This repository contains the code used for our MNIST experiments.  
It includes the main method, the baseline implementations, and the ablation studies used in the paper.

## What is included

There are two main notebooks in this repository.

### `MHD_FL_and_Baslines.ipynb`
This notebook contains the main pipeline together with the baseline methods:
- data preparation and deterministic client partitioning,
- non-IID label distribution visualization,
- FedAvg training,
- MHD-FL,
- LL-FT,
- FedGKD / model-level KD,
- FedPSD,
- Ditto.

### `Ablation_Study.ipynb`
This notebook contains the ablation experiments:
- the same MNIST setup and FedAvg initialization,
- Strict Decoupling,
- G→P Only KD,
- P→G Only KD.

## Setup

The experiments use MNIST with heterogeneous client partitions.  
Each client is missing a subset of labels, which creates a controlled non-IID setting.

The code reports both:
- performance on the full test set, and
- personalized performance on client-specific specialization test sets.

## How to run

Each notebook is designed to be run from top to bottom.

In general, the workflow is:
1. prepare the client datasets,
2. train the FedAvg initialization model,
3. run the main method, baselines, or ablations.

Some later cells expect the FedAvg checkpoint to already exist.


