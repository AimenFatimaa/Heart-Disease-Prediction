# Heart Disease Prediction Using Neural Networks

## Project Overview

This project focuses on binary classification for heart disease prediction using a neural network implemented with TensorFlow and Keras.

The objective is to explore how a Multi-Layer Perceptron (MLP) can learn patterns from health-related numerical data and classify records into two target classes.

## Dataset

The dataset was obtained from Kaggle:

**Dataset:** [Health Care: Heart Attack Possibility](https://www.kaggle.com/datasets/nareshbhat/health-care-data-set-on-heart-attack-possibility)

The dataset used in this project contains:

- **Total records:** 303
- **Input features:** 13
- **Target variable:** Binary classification

### Features

The dataset includes the following input variables:

- Age
- Sex
- Chest Pain Type (cp)
- Resting Blood Pressure (trestbps)
- Cholesterol (chol)
- Fasting Blood Sugar (fbs)
- Resting Electrocardiographic Results (restecg)
- Maximum Heart Rate Achieved (thalach)
- Exercise-Induced Angina (exang)
- ST Depression (oldpeak)
- Slope
- Number of Major Vessels (ca)
- Thalassemia (thal)

The target variable represents the two classification categories.

## Technologies and Libraries

The following tools and libraries were used:

- Python
- NumPy
- Pandas
- Scikit-learn
- TensorFlow
- Keras
- Matplotlib
- Google Colab

## Methodology

The project follows these main steps:

### 1. Data Loading and Exploration

The dataset was loaded using Pandas. Initial inspection was performed to understand the dataset structure, input features, and target variable.

### 2. Feature and Target Separation

The independent variables were separated from the target variable to prepare the data for model training.

### 3. Train-Test Split

The dataset was divided into training and testing subsets using an 80:20 split with a fixed random state of 42.

### 4. Feature Scaling

StandardScaler was applied to standardize the input features. The scaler was fitted on the training data and then used to transform the testing data.

### 5. Feature Selection

A custom feature-selection function was implemented to randomly select a subset of input features for model training.

### 6. Neural Network Architecture

A Multi-Layer Perceptron (MLP) was developed using TensorFlow/Keras.

The architecture consists of:

- An input layer corresponding to the selected features
- Five hidden Dense layers, each containing 64 neurons
- Sigmoid activation functions
- A single output neuron with sigmoid activation for binary classification
- Adam optimizer
- Binary cross-entropy loss function

### 7. Model Training

The model was trained using the following configuration:

- **Epochs:** 10
- **Batch size:** 32
- **Validation split:** 20%
- **Optimizer:** Adam
- **Loss function:** Binary Cross-Entropy

## Results and Discussion

The model was trained on a relatively small dataset containing 303 records and 13 input features.

The training accuracy remained approximately between 50% and 54%, while the validation accuracy reached approximately 57.14%.

These results indicate that the model did not learn the underlying patterns effectively and suggest possible underfitting.

### Possible Reasons for Underfitting

Several factors may have contributed to the model's limited performance:

1. **Small Dataset:** The dataset contains only 303 records, which may limit the model's ability to learn meaningful patterns.

2. **Feature Selection:** Randomly selecting a subset of features may exclude important information required for classification.

3. **Model Configuration:** The selected network architecture and activation functions may not be suitable for this particular dataset.

4. **Hyperparameter Settings:** The learning rate, batch size, number of epochs, and other hyperparameters may require further optimization.

5. **Training Duration:** Training for only 10 epochs may not provide sufficient learning opportunities.

These are possible explanations and would require further experiments to confirm.

## Conclusion and Future Improvements

This project demonstrates the implementation of a neural-network-based approach for binary heart disease classification.

Although the model was successfully developed and trained, its current performance indicates that further improvements are needed.

Possible future improvements include:

- Applying more suitable feature-selection techniques.
- Experimenting with different neural network architectures.
- Performing systematic hyperparameter tuning.
- Increasing the number of training epochs where appropriate.
- Comparing the neural network with traditional machine learning classifiers.
- Evaluating performance using additional metrics such as precision, recall, F1-score, and a confusion matrix.

## Repository Contents

```text
Heart-Disease-Prediction/
│
├── Heart_Disease_Prediction.ipynb
├── README.md
└── requirements.txt
```

The Jupyter Notebook contains the complete implementation, code cells, training outputs, and experimental results.

## How to Run the Project

1. Clone or download this repository.
2. Install the required Python libraries.
3. Open the notebook using Jupyter Notebook or Google Colab.
4. Download the dataset from the Kaggle link provided above.
5. Upload the CSV file to your working environment.
6. Update the dataset file path in the notebook if necessary.
7. Run the notebook cells sequentially.

## Disclaimer

This project is developed for educational and experimental purposes only. The model is not intended for medical diagnosis or clinical decision-making.
