# Physics-Informed Motion Planner (ECE 228 Final Project)

This repository contains the code for our ECE 228 final project (Track 2), where we explore the use of Physics-Informed Neural Networks (PINNs) for trajectory prediction in autonomous driving. The model is trained and evaluated on the Lyft Level 5 Prediction Dataset.

## Project Overview

Our goal is to improve the accuracy and physical realism of trajectory forecasts by integrating domain knowledge—such as motion smoothness and dynamic feasibility—into the training process using soft constraints. We implement and evaluate this within a ResNet-based prediction model, using both standard MSE loss and PINN-augmented loss.

## Model Features
- Baseline architecture: ResNet-18 / ResNet-50
- Loss function: MSE + optional PINN regularization
- Dataset: Lyft Level 5 Prediction Dataset
- Evaluation metric: Average Displacement Error (ADE)
- Physics-informed constraints: velocity and acceleration smoothness

## Files
- `Trajectory_Prediction_With_PINN.ipynb`: The main notebook for training and evaluating the models.

## Results Summary
| Model       | Loss Type      | ADE (meters) |
|-------------|----------------|--------------|
| ResNet-18   | MSE            | 2.34         |
| ResNet-18   | MSE + PINN     | 2.11         |
| ResNet-50   | MSE            | 2.25         |
| ResNet-50   | MSE + PINN     | 2.04         |
