# Titanic Survival Prediction

A machine learning project that predicts whether a passenger survived the Titanic disaster using classification models.

## Overview

This project uses the famous Titanic dataset to build and train machine learning models that predict passenger survival. The analysis includes data preprocessing, feature engineering, and model training & evaluation.

## Dataset

The project uses the Titanic dataset from the [Seaborn](https://seaborn.pydata.org/) library, which contains information about 891 passengers aboard the Titanic.

### Key Features
- **Survived**: Target variable (0 = Did not survive, 1 = Survived)
- **Pclass**: Passenger class (1st, 2nd, or 3rd)
- **Sex**: Passenger gender
- **Age**: Passenger age
- **SibSp**: Number of siblings/spouses aboard
- **Parch**: Number of parents/children aboard
- **Adult Male**: Whether the passenger is an adult male
- **Alone**: Whether the passenger was traveling alone

## Project Workflow

### 1. **Data Loading & Exploration**
   - Load the Titanic dataset from Seaborn
   - Display basic statistics and data shape
   - Identify missing values

### 2. **Data Preprocessing**
   - Handle missing values (fill age with median)
   - Drop irrelevant columns (deck, embark_town, alive, fare, class, who)
   - Encode categorical columns to numerical values:
     - Sex: male → 0, female → 1
     - Adult Male & Alone: Convert to integer

### 3. **Data Splitting**
   - Split data into training (80%) and testing (20%) sets
   - Features used: pclass, sex, age, sibsp, parch, adult_male, alone

### 4. **Model Training**
   - Train a **Logistic Regression** model
   - Fit the model to the training data

### 5. **Model Evaluation**
   - Calculate accuracy score
   - Generate confusion matrix
   - Print classification report with precision, recall, and F1-score
   - Visualize confusion matrix with heatmap

## Installation

### Prerequisites
- Python 3.7+
- pip or conda

### Dependencies
Install the required packages:

```bash
pip install scikit-learn pandas seaborn matplotlib numpy jupyter
```

Or use the provided environment:

```bash
pip install -r requirements.txt
```

## Usage

### Running the Notebook

1. Navigate to the project directory:
   ```bash
   cd titanic_survival_prediction
   ```

2. Activate your virtual environment (if using one):
   ```bash
   .\.venv\Scripts\Activate.ps1  # Windows
   source .venv/bin/activate     # macOS/Linux
   ```

3. Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```

4. Open `titanic_survival_prediction.ipynb` and run all cells

## Results

The project outputs:
- **Model Accuracy**: Percentage of correct predictions on test data
- **Confusion Matrix**: Visual representation of true positives, false positives, true negatives, and false negatives
- **Classification Report**: Detailed metrics including precision, recall, and F1-score

## Model Performance

The Logistic Regression model provides baseline predictions for Titanic survival. Results typically show decent accuracy due to clear patterns in survival rates based on passenger class and gender.


## Project Structure

```
titanic_survival_prediction/
├── titanic_survival_prediction.ipynb    # Main project notebook
├── README.md                             # This file
└── requirements.txt                      # Python dependencies (optional)
```

## Technologies Used

- **Python**: Programming language
- **Pandas**: Data manipulation
- **Scikit-learn**: Machine learning models and evaluation metrics
- **Seaborn**: Data visualization and datasets
- **Matplotlib**: Plotting and visualization
- **Jupyter Notebook**: Interactive notebook environment


## License

This project is open source and available under the MIT License.

## References

- [Titanic Dataset on Kaggle](https://www.kaggle.com/c/titanic)
- [Scikit-learn Documentation](https://scikit-learn.org/)
- [Seaborn Datasets](https://seaborn.pydata.org/generated/seaborn.load_dataset.html)
