# Data Generation using Modelling and Simulation for Machine Learning

## 1. Objective

The objective of this project is to generate data using a simulation model and apply multiple machine learning models to predict system performance. The project demonstrates how modelling and simulation can be used to create realistic datasets for predictive analytics.

---

## 2. Simulation Tool Used

SimPy – A discrete-event simulation library in Python.

SimPy allows modeling of real-world systems involving processes, resources, and events. In this project, SimPy is used to simulate a hospital queue management system.

---

## 3. Problem Description

A hospital outpatient department is simulated where:

- Patients arrive randomly
- Doctors serve patients
- Patients may need to wait if all doctors are busy

The goal is to predict the average waiting time based on system parameters.

---

## 4. Simulation Parameters and Bounds

| Parameter         | Lower Bound | Upper Bound | Description |
|-------------------|------------|------------|-------------|
| Arrival Rate      | 0.05       | 0.5        | Patient arrival rate per minute |
| Service Time      | 5          | 20         | Consultation time (minutes) |
| Number of Doctors | 1          | 5          | Available doctors |


---

## 5. Data Generation Methodology

1. Random values were generated within defined parameter bounds.
2. Each parameter set was passed to the SimPy simulation.
3. The simulation returned the average waiting time.
4. This process was repeated 1000 times.
5. The generated dataset contained:
   - Arrival Rate
   - Service Time
   - Number of Doctors
   - Average Waiting Time (target variable)

---

## 6. Machine Learning Models Used

The following regression models were implemented:

1. Linear Regression  
2. Decision Tree Regressor  
3. Random Forest Regressor  
4. Gradient Boosting Regressor  
5. AdaBoost Regressor  
6. Support Vector Regressor (SVR)  
7. K-Nearest Neighbors Regressor  

The dataset was split into 80% training and 20% testing data.

---

## 7. Evaluation Metrics

Models were evaluated using:

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R² Score

---

## 8. Results

| Model | MAE | RMSE | R² Score |
|-------|------|------|----------|
| Random Forest | 27.51 | 53.50 | 0.9675 |
| Gradient Boosting | 37.20 | 61.01 | 0.9577 |
| Decision Tree | 33.55 | 66.10 | 0.9504 |
| AdaBoost | 107.00 | 124.59 | 0.8238 |
| KNN | 87.52 | 158.33 | 0.7155 |
| Linear Regression | 151.74 | 195.08 | 0.5681 |
| SVR | 151.09 | 306.00 | -0.0624 |

---

## 9. Result Visualization

<img width="547" height="520" alt="image" src="https://github.com/user-attachments/assets/be6b7d40-40d7-43f5-b55e-8dc31aa4e0be" />

---

## 10. Best Model

Random Forest Regressor performed the best with:

- Highest R² Score (0.9675)
- Lowest RMSE
- Lowest MAE

This indicates that ensemble tree-based models are highly effective for nonlinear simulation-based datasets.

---

## 11. Conclusion

This project demonstrates how simulation-based data generation can be integrated with machine learning techniques. By generating 1000 simulation runs using SimPy and comparing multiple regression models, it was observed that ensemble methods outperform linear models for complex system behavior.

The approach can be extended to other domains such as traffic systems, manufacturing processes, and service operations.
