# Python_Projects
Wall Following Robot - Machine Learning Model for Multi-Class Classification
Overview
This project focuses on building a Machine Learning model to navigate a SCITOS G5 robot, using sensor data to predict its next movement. The robot moves in a clockwise direction following a wall, and the task is to classify its movement based on ultrasonic sensor readings. The primary objective is to find the most suitable machine learning algorithm for the robot’s navigation using a multi-class classification approach.

Problem Statement
The robot's navigation task is framed as a multi-class classification problem with four possible movements:

Move Forward
Slight Right Turn
Sharp Right Turn
Slight Left Turn
The robot uses 24 ultrasonic sensors arranged around its waist to capture its surroundings. The goal is to predict the robot's next movement based on these sensor readings, ensuring it can navigate through the room without collisions.

Data Description
The dataset consists of sensor readings collected from the SCITOS G5 robot during wall-following in a clockwise direction. The data is provided in three formats, and this project uses the raw sensor data for more complexity and room for optimization.

Dataset Files:
Raw Sensor Data: Measurements from all 24 sensors with corresponding class labels.
Simplified Distance Data (4 Sensors): Four simplified sensor readings (front, left, right, back) with class labels.
Simplified Distance Data (2 Sensors): Only the front and left simplified distances with class labels.
For this project, the raw sensor data (first dataset) is used, as it provides richer information for exploration and optimization.

Sensors:
Sensor 1: Front of the robot.
Sensor 9: Right side of the robot.
Sensor 19: Left side of the robot.
Sensor 13: Back of the robot.
The front distance in the simplified datasets is calculated using Sensor 13 and surrounding sensors, meaning that the robot is moving backwards.

Classes (Target Labels):
Move-Forward
Slight-Right-Turn
Sharp-Right-Turn
Slight-Left-Turn
Data Source:
The dataset is available from the UCI Machine Learning Repository:
Sensor Readings Dataset

Project Goals
Data Exploration & Preparation:

Load and clean the raw sensor data.
Explore and analyze the features.
Feature engineering (e.g., identifying key sensors for movement decisions).
Model Development:

Test various machine learning algorithms such as Decision Trees, Random Forests, Support Vector Machines (SVM), K-Nearest Neighbors (KNN), and Neural Networks.
Optimize and tune hyperparameters.
Evaluation Metrics:

Loss Function: Categorical Cross-Entropy (for Neural Networks).
Accuracy: Measures the percentage of correctly classified movements.
Precision: Measures the accuracy of the model for each class.
Machine Learning Approach
Supervised Learning:
The task is supervised since we have labeled data.
The model will be trained using sensor readings as input features and movement classes as target labels.
Algorithms Considered:
Decision Tree
Random Forest
K-Nearest Neighbors (KNN)
Support Vector Machines (SVM)
Neural Networks
Loss and Evaluation Metrics
Loss Function: Categorical Cross-Entropy (especially for Neural Networks).
Success Metrics: Log-loss, Accuracy, and Precision to evaluate the model’s performance.

Getting Started
Prerequisites
Python 3.x
Required Python packages (listed in requirements.txt):
pandas
numpy
scikit-learn
tensorflow (if using Neural Networks)
matplotlib
seaborn
jupyter

Conclusion
This project explores the application of machine learning to a robot’s wall-following navigation task. By using raw sensor data, we are able to implement and optimize various machine learning models to predict the robot’s movement. The evaluation metrics such as accuracy, precision, and loss are used to assess the model performance.
