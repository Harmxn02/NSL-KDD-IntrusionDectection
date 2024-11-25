# NSL-KDD Intrusion Detection

## Dataset

The NSL-KDD dataset is an improved version of the KDD'99 dataset, which was widely used for network intrusion detection. The original dataset had many redundant records, and NSL-KDD addressed these issues. It contains both normal and attack records.

The dataset includes various types of attacks such as Denial of Service (DoS), Probe, R2L (Remote-to-Local), and U2R (User-to-Root).

**Dataset**: NSL-KDD. (2019, April 25). <https://www.kaggle.com/datasets/hassan06/nslkdd>

## Repository contents

1. `main.ipynb`: This Jupyter notebook contains the EDA (exploratory data analysis), preprocessing, model architecture, and model evaluation
1. `/data/`: contains the cleaned and encoded datasets, which were exported in the Jupyter notebook
1. `/models/`: contains the trained model which was exported in the Jupyter notebook

## What I learned from this project

I learned that you can read in a lot of different file formats into Pandas. The dataset here was stored in `.txt`-files, but there were also `.arff`-files, which is a filetype I didn't know before this project.

## Model performance

### Classification report

|              | precision | recall | f1-score | support |
| ------------ | --------- | ------ | -------- | ------- |
| normal       | 1.00      | 0.95   | 0.97     | 12992   |
| neptune      | 1.00      | 1.00   | 1.00     | 4043    |
| ipsweep      | 0.97      | 0.97   | 0.97     | 706     |
| satan        | 0.61      | 0.98   | 0.75     | 711     |
| smurf        | 0.93      | 1.00   | 0.96     | 511     |
| portsweep    | 0.97      | 1.00   | 0.98     | 501     |
| nmap         | 0.88      | 0.99   | 0.93     | 312     |
| back         | 0.88      | 1.00   | 0.94     | 179     |
| teardrop     | 1.00      | 1.00   | 1.00     | 166     |
| warezclient  | 0.48      | 0.99   | 0.65     | 111     |
|              |           |        |          |         |
| accuracy     |           |        | 0.96     | 20232   |
| macro avg    | 0.87      | 0.99   | 0.92     | 20232   |
| weighted avg | 0.98      | 0.96   | 0.97     | 20232   |

The model performs pretty good in general, with an accuracy of **96%**. If we look at the performance per attack type, there are some outliers:

- **Satan**: the precision and f1-score are not on par with the other attack types. In previous runs they were, so this is most likely fixable by training the model again.

- **Warezclient**: the precision and f1-score are not on par with the other attack types. Contrary to Satan, this was the case across different runs.
