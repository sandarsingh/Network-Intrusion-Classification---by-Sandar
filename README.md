
Network Intrusion Classification

Author: Sandar
Tech Stack: Python, TensorFlow / Keras, Pandas, Scikit-Learn, NumPy
Environment: Google Colab (Recommended)

About The Project

This project is a simplified Network Intrusion Detection System (NIDS) built with a 3-Layer Deep Learning Neural Network (Input -> Hidden -> Output). It performs binary classification to determine whether incoming network traffic is "Normal" or a potential "Attack".

This repository serves as a practical introduction to neural network architecture, data preprocessing, and applying machine learning to cybersecurity challenges.

Features

Synthetic Dataset Generation: Includes a Python script to generate a realistic 1,000-row dataset featuring connection duration, source bytes, destination bytes, and failed login attempts.

Data Preprocessing: Utilizes StandardScaler to normalize feature distributions, a critical step for stable neural network training.

Simple & Fast Architecture: Implements a highly efficient 3-layer neural network that trains in seconds and achieves high accuracy on the target dataset.

Live Traffic Simulation: Includes a testing module that simulates a real-time network packet to evaluate the model's predictive capabilities and trigger alerts.

How to Run (Google Colab)

Generate the Dataset:
Run the first cell/script to generate network_traffic.csv. This will automatically save the dataset to your local Colab environment.

Train the Model:
Run the model training script. This script will load the CSV, split the data (80% Training / 20% Testing), scale the features, and train the neural network for 15 epochs.

Simulate an Attack:
Once training is complete, the script automatically generates a suspicious network packet (high bytes, multiple failed logins) and feeds it to the model to verify if it successfully triggers an intrusion alert.

Model Architecture

Input Layer: 4 Features (duration, src_bytes, dst_bytes, failed_logins)

Hidden Layer: 16 Neurons (Activation: ReLU)

Output Layer: 1 Neuron (Activation: Sigmoid for 0-1 probability output)

Loss Function: Binary Crossentropy

Optimizer: Adam
