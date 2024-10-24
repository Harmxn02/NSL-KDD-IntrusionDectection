# NSL-KDD Intrusion Detection

## Dataset

The NSL-KDD dataset is an improved version of the KDD'99 dataset, which was widely used for network intrusion detection. The original dataset had many redundant records, and NSL-KDD addressed these issues. It contains both normal and attack records.

The dataset includes various types of attacks such as Denial of Service (DoS), Probe, R2L (Remote-to-Local), and U2R (User-to-Root).

Dataset retrieved from [kaggle.com](<https://www.kaggle.com/datasets/hassan06/nslkdd>).

## Repository contents

1. `main.ipynb`: This Jupyter notebook contains the EDA (exploratory data analysis), preprocessing, model architecture, and model evaluation
1. `/data/`: contains the cleaned and encoded datasets, which were exported in the Jupyter notebook
1. `/models/`: contains the trained model which was exported in the Jupyter notebook

## What I learned from this project

I learned that you can read in a lot of different file formats into Pandas. The dataset here was stored in `.txt`-files, but there were also `.arff`-files, which is a filetype I didn't know before this project.
