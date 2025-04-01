# Deep Learning Challenge: Charity Donation Predictor

## Overview

This project applies a supervised deep learning model to predict whether applicants will be likely donors to a charitable organization. The goal is to help optimize fundraising efforts by identifying which applicants are most worth pursuing for donations.

The dataset comes from a real-world scenario provided by AlphabetSoup, a fictitious non-profit, and includes anonymized features related to application activity and demographics.

## Objectives

- Preprocess and encode categorical variables from the charity dataset.
- Build a binary classification model using TensorFlow/Keras.
- Optimize the model to achieve a minimum accuracy of **75%**.
- Evaluate the model’s performance and analyze its limitations.

---

## Technologies Used

- **Python**  
- **TensorFlow / Keras**  
- **Pandas**  
- **Scikit-learn**  
- **Jupyter Notebook**

---

## Approach

1. **Preprocessing the Data**
    - Loaded and inspected the dataset from `charity_data.csv`.
    - Dropped non-informative columns (like EIN and NAME).
    - Converted categorical features into numerical encodings using one-hot encoding.
    - Split the data into training and testing sets.

2. **Building the Neural Network**
    - Created a baseline Sequential model with:
        - Input layer matching the number of features.
        - Two hidden layers using ReLU activation.
        - Output layer using Sigmoid activation for binary classification.
    - Compiled the model using `binary_crossentropy` loss and the `adam` optimizer.
    - Trained the model for 100 epochs and evaluated performance.

3. **Optimization Attempts**
    - Tuned number of neurons and layers.
    - Tried additional dropout layers to reduce overfitting.
    - Tested with different activation functions and epoch counts.

---

## Results

- The final optimized model achieved a testing accuracy of **~75.3%**, meeting the target benchmark.
- Adding complexity (more neurons/layers) did not consistently improve performance.
- Feature engineering (e.g. excluding high-cardinality or irrelevant variables) played a bigger role in improving accuracy.

---

## Key Takeaways

- Neural networks can be effectively applied to classification problems with structured, tabular data.
- Preprocessing decisions—such as which features to encode or drop—can have as much impact as tuning hyperparameters.
- Even a relatively simple model can achieve strong performance when fed clean and relevant data.

---

## How to Use

1. Clone the repository:

```bash
git clone https://github.com/fbarffmann/deep-learning-challenge.git
```

2. Navigate to the project directory:

```bash
cd deep-learning-challenge
```

3. Install required libraries if needed:

```bash
pip install pandas scikit-learn tensorflow jupyter
```

4. Navigate to notebook:

```bash
cd "Deep Learning Challenge"
```

5. Launch the Jupyter Notebook:

```bash
jupyter notebook AlphabetSoupCharity.ipynb
```

6. Run all cells to reproduce the preprocessing, modeling, and evaluation workflow.

---

👨‍💻 Developed by **Finn Brennan Arffmann**  
🔗 GitHub: [@fbarffmann](https://github.com/fbarffmann)  
💼 LinkedIn: [linkedin.com/in/fbarffmann](https://linkedin.com/in/fbarffmann)
