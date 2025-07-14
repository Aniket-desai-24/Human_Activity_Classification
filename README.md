
# Human Activity Classification

[![License](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Python Version](https://img.shields.io/badge/Python-3.7+-blue.svg)](https://www.python.org/)
[![Contributions Welcome](https://img.shields.io/badge/Contributions-Welcome-brightgreen.svg)](https://github.com/yourusername/Human_Activity_Classification/blob/main/CONTRIBUTING.md)

## Overview

This project focuses on classifying human activities based on sensor data. It utilizes machine learning techniques to identify different activities such as walking, running, sitting, and standing, using data collected from wearable sensors. This project aims to provide an accurate and efficient system for activity recognition, which can be applied in various fields like healthcare, fitness tracking, and elderly care.

## Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Machine Learning Models](#machine-learning-models)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Evaluation](#evaluation)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgements](#acknowledgements)

## Dataset

> Describe the dataset used for this project. Include the source of the dataset, the number of features, and the number of instances. Also, mention any preprocessing steps applied to the dataset. For example:

The project utilizes the UCI Human Activity Recognition Using Smartphones dataset. This dataset contains data collected from 30 subjects performing activities of daily living (ADL) while carrying a waist-mounted smartphone with embedded inertial sensors. The experiments have been video-recorded to label the data. The dataset includes tri-axial acceleration from the accelerometer and tri-axial angular velocity from the gyroscope. A detailed description of the dataset and its features can be found at the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones).

Key features include:

-   Tri-axial acceleration from the accelerometer (total acceleration) and the estimated body acceleration.
-   Tri-axial angular velocity from the gyroscope.
-   A 561-feature vector with time and frequency domain variables.
-   Activity labels such as WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING.

Preprocessing steps involved:

-   Data cleaning (handling missing values, if any).
-   Feature scaling (e.g., using StandardScaler).
-   Data transformation (if necessary).

## Machine Learning Models

> Describe the machine learning models implemented in this project. Explain the rationale behind choosing these models and provide a brief overview of each model. For example:

The following machine learning models were implemented and evaluated for human activity classification:

1.  **Logistic Regression:** A linear model suitable for multi-class classification tasks. It's simple to implement and provides a good baseline performance.

2.  **Support Vector Machine (SVM):** An effective model in high dimensional spaces. SVM is used for its ability to handle non-linear data through the kernel trick.

3.  **Random Forest:** An ensemble learning method that operates by constructing a multitude of decision trees at training time and outputting the class that is the mode of the classes of the individual trees.

4.  **K-Nearest Neighbors (KNN):** A simple, non-parametric algorithm that classifies new data points based on the majority class among its k nearest neighbors in the feature space.

5.  **Gradient Boosting Machines (GBM):** A boosting algorithm that combines multiple weak learners (typically decision trees) to create a strong learner.

The choice of these models was based on their proven performance in classification tasks and their ability to handle different types of data and complexities. Hyperparameter tuning was performed to optimize the performance of each model.

## Project Structure

bash
    git clone https://github.com/yourusername/Human_Activity_Classification.git
    cd Human_Activity_Classification
    3.  **Install the dependencies:**

    bash
    python scripts/data_processing.py
        This script reads the raw data from the `data/raw/` directory, preprocesses it, and saves the processed data in the `data/processed/` directory.

2.  **Model Training:**

    Run the `model_training.py` script to train the machine learning models.

bash
    python scripts/model_training.py --model RandomForest
        This script loads the trained models from the `models/` directory, evaluates them on a test dataset, and generates evaluation metrics (e.g., accuracy, precision, recall, F1-score).  The evaluation metrics are saved in the `reports/metrics.txt` file.

4.  **Jupyter Notebooks:**

    Explore the data and models using the Jupyter notebooks in the `notebooks/` directory.  Start JupyterLab with:

        -   `data_exploration.ipynb`:  Explores the dataset and visualizes the data.
    -   `model_training.ipynb`:  Demonstrates the training and evaluation of different models.

## Evaluation

> Describe the evaluation metrics used to assess the performance of the models.

The performance of the models was evaluated using the following metrics:

-   **Accuracy:** The proportion of correctly classified instances out of the total instances.
-   **Precision:** The proportion of true positive predictions out of the total positive predictions.
-   **Recall:** The proportion of true positive predictions out of the total actual positive instances.
-   **F1-score:** The harmonic mean of precision and recall.

These metrics provide a comprehensive assessment of the models' ability to accurately classify human activities. The results are stored in `reports/metrics.txt` and visualized in the notebooks.

## Contributing

> Explain how others can contribute to the project.

Contributions are welcome! Please follow these steps:

1.  Fork the repository.
2.  Create a new branch for your feature or bug fix.
3.  Make your changes and commit them with descriptive messages.
4.  Test your changes thoroughly.
5.  Submit a pull request.

Please adhere to the [Contribution Guidelines](CONTRIBUTING.md) for more details.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgements

> Acknowledge any resources, libraries, or individuals that contributed to the project.

