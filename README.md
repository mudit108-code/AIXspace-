# Anomaly Detection System using LSTM Autoencoder

This project implements a deep learning-based anomaly detection pipeline designed for early fault detection and system health monitoring in spacecraft telemetry or any time series system.

It uses:

1.LSTM Autoencoder for unsupervised learning of normal patterns

2.Anomaly score generation via reconstruction error

3.Label-based anomaly injection for simulation and benchmarking

##  How It Works

**Step 1: **Data Loading and Parsing

Time series data is simulated per telemetry channel .

Anomalies from **labels_cleaned.csv** are injected into the signal for realism.

**Step 2: **Preprocessing

Sliding window sequences are created for training.

Normal sequences are used for training.

**Step 3: **LSTM Autoencoder

The model learns to reconstruct normal sequences.

On unseen data, it reconstructs normal well and fails on anomalies.

**Step 4: Anomaly Detection**

A dynamic threshold is applied to flag anomalies.

Binary prediction:
0 = Normal
1 = Anomaly

