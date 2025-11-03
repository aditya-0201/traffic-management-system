Intelligent Traffic Management System

This project implements a multi-stage intelligent traffic management system using a combination of machine learning and heuristic optimization techniques. The system first predicts future traffic flow using an optimized neural network and then uses that data to optimize and adapt traffic signal timings to minimize congestion.

This notebook is divided into five key modules:

Traffic Flow Prediction (GA-LSTM)

Signal Timing Optimization (PSO)

Mamdani Fuzzy Logic Controller

Adaptive Neuro-Fuzzy Inference System (ANFIS)

1. Traffic Flow Prediction (GA-LSTM)

This module builds a traffic flow predictor using a Long Short-Term Memory (LSTM) neural network. To achieve the highest accuracy, a Genetic Algorithm (GA) is employed to find the optimal set of hyperparameters for the LSTM model.

Objective: Minimize the validation Mean Squared Error (MSE).

Hyperparameters Tuned:

L (Lookback window)

u (Hidden units)

d (Dropout rate)

α (Learning rate)

B (Batch size)

Opt (Optimizer: Adam, RMSprop, SGD)

Dataset: Uses the metr_la_speed.csv dataset for training.

Output: The best-performing LSTM model is saved as metr_lstm_ga_optimized.h5.

2. Signal Timing Optimization (PSO)

This module takes the predicted traffic flows from the GA-LSTM model and uses them to optimize static traffic signal timings for a network of intersections.

Objective: Minimize the average vehicle delay across all approaches.

Method: Particle Swarm Optimization (PSO).

Parameters Optimized:

Cycle time (C)

Green splits (S₁, S₂, ...)

Offsets (O)

Fitness Function: Uses the Akçelik delay model to calculate delay based on the predicted flows.

Output: The optimal signal timings are saved in pso_results.npz.

3. Adaptive Signal Control (Fuzzy Logic & ANFIS)

These modules design an adaptive controller to dynamically refine the signal timings based on real-time conditions, building on the PSO-optimized base timings.

Module 3: Mamdani Fuzzy Controller

A standard Mamdani fuzzy logic controller is implemented to adjust the signal cycle time.

Inputs: Queue (vehicles), Delay (seconds)

Output: ΔCycle (change in cycle time, seconds)

Rules: A 9-rule base (Low/Medium/High for each input) determines the output.

Module 4: ANFIS Controller

An Adaptive Neuro-Fuzzy Inference System (ANFIS) is developed as a more advanced hybrid controller. It combines the interpretability of fuzzy logic with the learning capabilities of a neural network to automatically tune and refine the fuzzy membership functions and rules from data.

Technologies Used

Python

TensorFlow / Keras

Pandas & NumPy

Scikit-learn

Matplotlib

Genetic Algorithm (GA)

Particle Swarm Optimization (PSO)

Mamdani Fuzzy Logic

ANFIS (Adaptive Neuro-Fuzzy Inference System)

How to Use

Clone the repository:

git clone [https://github.com/aditya-0201/traffic-management-system.git](https://github.com/aditya-0201/traffic-management-system.git)
cd traffic-management-system


Install dependencies:
It is recommended to create a virtual environment.

pip install tensorflow pandas numpy scikit-learn matplotlib


Add Dataset:
This project requires the metr_la_speed.csv dataset. Please download it and place it in the root of the repository.

Update File Paths:
The notebook currently uses Google Drive paths (e.g., /content/drive/MyDrive/...). You must update these paths to read/write from the local repository (e.g., change to metr_la_speed.csv, metr_lstm_ga_optimized.h5, etc.).

Run the Notebook:
Open and run the Traffic.ipynb notebook using Jupyter or Google Colab.

File Structure

.
├── Traffic.ipynb             # Main Jupyter Notebook with all modules
├── README.md                 # This file
├── metr_la_speed.csv         # (Must be added) Traffic speed dataset
├── metr_lstm_ga_optimized.h5 # (Generated) Trained LSTM model
├── ga_tuning_log.csv         # (Generated) Log from the GA tuning
└── pso_results.npz           # (Generated) Optimized signal timings from PSO
