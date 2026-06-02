# Predictive Maintenance of Turbofan Engines using LSTM

This project predicts the Remaining Useful Life (RUL) of aircraft turbofan engines using the NASA C-MAPSS FD001 dataset. An LSTM-based deep learning model was trained on multivariate time-series sensor data to learn degradation patterns and estimate the number of cycles remaining before engine failure.

Dataset used: NASA C-MAPSS Turbofan Engine Degradation Simulation Dataset (FD001)
Source: NASA Prognostics Center of Excellence
Subset Used: FD001
Description: Multivariate time-series sensor data for turbofan engines used for Remaining Useful Life (RUL) prediction.

Train trajectories: 100
Test trajectories: 100
Conditions: ONE (Sea Level)
Fault Modes: ONE (HPC Degradation)


Experimental Scenario

Data sets consists of multiple multivariate time series. Each data set is further divided into training and test subsets. Each time series is from a different engine – i.e., the data can be considered to be from a fleet of engines of the same type. Each engine starts with different degrees of initial wear and manufacturing variation which is unknown to the user. This wear and variation is considered normal, i.e., it is not considered a fault condition. There are three operational settings that have a substantial effect on engine performance. These settings are also included in the data. The data is contaminated with sensor noise.

The engine is operating normally at the start of each time series, and develops a fault at some point during the series. In the training set, the fault grows in magnitude until system failure. In the test set, the time series ends some time prior to system failure. The objective of the competition is to predict the number of remaining operational cycles before failure in the test set, i.e., the number of operational cycles after the last cycle that the engine will continue to operate. Also provided a vector of true Remaining Useful Life (RUL) values for the test data.

Methodology:-
1. Data Loading
2. Data Cleaning
3. RUL Computation
4. Feature Selection
5. Normalization
6. Sequence Generation
7. LSTM Training
8. Evaluation

Technologies Used:-
1.Python
2.PyTorch
3.NumPy
4.Pandas
5.Machine Learning
6.Deep Learning
7.LSTM

Results:-
RMSE: 13.364
MAE : 9.882
R²  : 0.8898

The model successfully learned degradation patterns from sensor data and achieved strong predictive performance on unseen test engines.
![prediction results](images/final_results.png)
