# Human Activity Recognition Using Hidden Markov Models

## Overview

This project implements a Hidden Markov Model (HMM) to recognize human activities using smartphone sensor data collected with the Sensor Logger application.

The objective is to model hidden activity states from noisy accelerometer and gyroscope measurements. Four activities were recorded and used to train and evaluate the model:

- Standing
- Walking
- Jumping
- Still (phone placed on a flat surface)

The project was completed as part of a Machine Learning assignment focusing on sequential probabilistic models.

## Dataset

The dataset was collected using a smartphone equipped with accelerometer and gyroscope sensors.

Each recording lasts approximately 10 seconds and includes:

- Accelerometer (x, y, z)
- Gyroscope (x, y, z)
- Timestamp

The recordings are divided into training and testing sets.

data/
├── train/
│ ├── standing/
│ ├── walking/
│ ├── jumping/
│ └── still/
└── test/
├── standing/
├── walking/
├── jumping/
└── still/

## Methodology

The project follows these main steps:

1. Load and organize the recorded sensor data.
2. Estimate the sampling rate and harmonize the recordings.
3. Extract time-domain and frequency-domain features from sliding windows.
4. Build observation sequences for the Hidden Markov Model.
5. Train the HMM using the Baum–Welch algorithm.
6. Decode the most likely activity sequence using the Viterbi algorithm.
7. Evaluate the model on previously unseen recordings.

## Features Extracted

### Time-domain

- Mean
- Variance
- Standard deviation
- Signal Magnitude Area (SMA)
- Correlation between sensor axes

### Frequency-domain

- Dominant frequency
- Spectral energy
- FFT-based features

## Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- SciPy
- hmmlearn
- Scikit-learn

## Results

The trained Hidden Markov Model predicts the sequence of human activities from sensor observations and is evaluated using unseen recordings. Model performance is summarized using a confusion matrix together with sensitivity, specificity and overall accuracy for each activity.

## Repository Structure

├── HMM_Activity_Recognition.ipynb
├── data/
├── README.md
└── requirements.txt

## Author

Sheryl Otieno
