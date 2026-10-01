# Task 1: Data Cleaning & Preprocessing

## Objective

The objective of this task is to learn how to clean and prepare raw data for Machine Learning.

The Titanic dataset from Kaggle is used for this task.

## Dataset

**Dataset:** Titanic Dataset  
**Source:** Kaggle  
**Dataset URL:** https://www.kaggle.com/datasets/yasserh/titanic-dataset

The dataset contains information about Titanic passengers, including their age, gender, passenger class, fare, and survival status.

## Tools and Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- KaggleHub
- Jupyter Notebook

## Tasks Performed

### 1. Import and Explore the Dataset

The dataset is downloaded directly from Kaggle using `kagglehub`.

The following operations are performed:

- Display the first few rows
- Check dataset shape
- Check data types
- Display statistical information
- Identify missing values

### 2. Handle Missing Values

Missing values are handled using appropriate techniques.

- `Age` → Missing values are replaced using the median.
- `Embarked` → Missing values are replaced using the mode.
- `Cabin` → The column is removed because it contains a large number of missing values.

### 3. Convert Categorical Features into Numerical Values

Categorical variables are converted into numerical form so that they can be used by machine learning algorithms.

- `Sex` is converted using label mapping:
  - Male → 0
  - Female → 1
- `Embarked` is converted using one-hot encoding.

### 4. Remove Unnecessary Features

The following columns are removed because they are not required for the preprocessing task:

- `PassengerId`
- `Name`
- `Ticket`

### 5. Detect and Remove Outliers

Boxplots are used to visualize possible outliers in numerical features.

The following columns are analyzed:

- `Age`
- `SibSp`
- `Parch`
- `Fare`

The Interquartile Range (IQR) method is used to identify and remove potential outliers.

### 6. Standardize Numerical Features

The numerical features are standardized using `StandardScaler` from Scikit-learn.

Standardization transforms the features so that they are approximately centered around a mean of 0 with a standard deviation of 1.

## Project Structure

```text
Task-1-Data-Cleaning/
│
├── Task_1_Data_Cleaning.ipynb
│
└── README.md
```

The dataset does not need to be manually stored in the project folder because it is downloaded directly from Kaggle using KaggleHub.

## Installation

Install the required Python packages using:

```bash
pip install kagglehub pandas numpy matplotlib seaborn scikit-learn jupyter
```

If you are using a Jupyter Notebook in VS Code, you can also install them directly inside a notebook cell:

```python
%pip install kagglehub pandas numpy matplotlib seaborn scikit-learn
```

## Execution

1. Open the `.ipynb` file in VS Code.
2. Select the appropriate Python/Jupyter kernel.
3. Run the notebook cells sequentially.
4. The Titanic dataset will be downloaded automatically from Kaggle.
5. The data will then be cleaned, encoded, visualized, and standardized.

## Preprocessing Workflow

```text
Kaggle Dataset
      ↓
Load Dataset
      ↓
Explore Dataset
      ↓
Check Missing Values
      ↓
Handle Missing Values
      ↓
Encode Categorical Variables
      ↓
Remove Unnecessary Columns
      ↓
Detect Outliers
      ↓
Remove Outliers
      ↓
Standardize Numerical Features
      ↓
Cleaned Dataset
```

## Key Concepts Learned

- Missing value handling
- Mean, median, and mode imputation
- Categorical variable encoding
- One-hot encoding
- Label encoding
- Outlier detection
- IQR method
- Data standardization
- Exploratory data analysis
- Importance of data preprocessing in Machine Learning

## Result

The raw Titanic dataset is transformed into a cleaner and machine-learning-ready dataset by:

- Handling missing values
- Converting categorical variables into numerical values
- Removing unnecessary columns
- Detecting and removing potential outliers
- Standardizing numerical features

This completes **Task 1: Data Cleaning & Preprocessing**.