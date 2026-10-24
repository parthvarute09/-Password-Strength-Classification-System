# 🔐 Password Strength Classification System Using NLP & Machine Learning

## 📌 Project Overview

The **Password Strength Classification System** is a machine learning project that uses Natural Language Processing (NLP) techniques to classify passwords into three strength categories: **Weak, Medium, and Strong**.

The project uses character-level TF-IDF vectorization and Logistic Regression to identify patterns in passwords and predict their strength. It also performs data cleaning, exploratory data analysis (EDA), feature engineering, and model evaluation.

The goal is to demonstrate how NLP and machine learning can support password-strength assessment and help users understand the importance of stronger passwords.

## 🎯 Objectives

- Analyze password patterns using Python.
- Retrieve and process data stored in an SQLite database.
- Perform data cleaning and exploratory data analysis.
- Extract meaningful features from passwords.
- Apply NLP techniques to convert password text into numerical features.
- Train a machine learning classification model.
- Evaluate model performance using standard classification metrics.
- Predict the strength category of a user-entered password.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| Pandas | Data manipulation and analysis |
| NumPy | Numerical operations |
| SQLite | Database storage and data retrieval |
| Matplotlib | Data visualization |
| Seaborn | Statistical data visualization |
| Scikit-learn | NLP preprocessing, model training, and evaluation |
| TF-IDF Vectorizer | Character-level text feature extraction |
| Logistic Regression | Password strength classification |
| Jupyter Notebook | Interactive development and experimentation |

## 📊 Password Strength Categories

The model uses three target classes:

| Label | Category |
|---|---|
| 0 | Weak |
| 1 | Medium |
| 2 | Strong |

The categories represent the labels in the dataset and are not a guarantee of real-world password security.

## ⚙️ Project Workflow

1. **Data Collection:** Load password records and their strength labels from an SQLite database.
2. **Data Preprocessing:** Inspect the dataset, remove irrelevant columns, and prepare the data.
3. **Exploratory Data Analysis:** Examine password length, character frequencies, and relationships with strength labels.
4. **Feature Engineering:** Calculate password characteristics, including length and lowercase-character frequency.
5. **NLP Processing:** Use character-level TF-IDF to transform password strings into numerical features.
6. **Model Training:** Train a multinomial Logistic Regression classifier.
7. **Prediction:** Transform a new password using the same feature-processing steps and predict its category.
8. **Model Evaluation:** Evaluate predictions using accuracy, a confusion matrix, and a classification report.

## 📁 Repository Structure

```text
Password-Strength-Classification-System/
│
├── NLP_password_strength.ipynb
│   └── Data analysis, NLP, model training,
│       prediction, and evaluation
│
├── password_data.sqlite
│   └── SQLite database used by the notebook
│
└── README.md
    └── Project documentation
```

## 📦 Installation and Setup

### Prerequisites

- Python 3.10 or another compatible Python version
- Jupyter Notebook or Visual Studio Code
- Basic knowledge of Python and machine learning

### 1. Clone the Repository

```bash
git clone https://github.com/parthvarute09/-Password-Strength-Classification-System-Using-NLP-Machine-Learning.git
```

### 2. Navigate to the Project Directory

```bash
cd -Password-Strength-Classification-System-Using-NLP-Machine-Learning
```

### 3. Install Dependencies

```bash
python -m pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

SQLite support is included with Python through the `sqlite3` module.

### 4. Open the Jupyter Notebook

```bash
jupyter notebook NLP_password_strength.ipynb
```

Alternatively, open the notebook directly in Visual Studio Code and run its cells in order.

### 5. Configure the Database Path

Ensure that the SQLite database is available in your project directory. Update the database connection in the notebook to use the correct local path.

For example:

```python
import sqlite3
import pandas as pd

con = sqlite3.connect("password_data.sqlite")

data = pd.read_sql_query(
    "SELECT * FROM Users",
    con
)
```

The database must contain the expected `Users` table and the columns required by the notebook.

## 🤖 Machine Learning Model

The project uses **Logistic Regression** for multiclass classification.

### Feature Extraction

Character-level TF-IDF converts password strings into numerical representations. Additional engineered features, such as password length and lowercase-character frequency, are combined with the text features.

### Model Training

The dataset is divided into training and testing subsets. The training subset is used to fit the model, while the testing subset is used to evaluate its predictions.

### Model Evaluation

The notebook uses the following evaluation methods:

- **Accuracy Score:** Measures the proportion of correct predictions.
- **Confusion Matrix:** Shows correct and incorrect classifications for each category.
- **Classification Report:** Provides precision, recall, and F1-score for each class.

Actual performance depends on the dataset, preprocessing, and train-test split. No specific accuracy is claimed here.

## 💻 Example Usage

The notebook includes a prediction function that accepts a password entered by the user.

Example interaction:

```text
Enter a password: [enter a test password]

Predicted strength: Weak / Medium / Strong
```

The actual output depends on the trained model and the input. The prediction function must apply the same feature extraction steps used during training.

**Security note:** Use fictional test passwords when experimenting. Never enter or upload your actual passwords to a public notebook or repository.

## 🌟 Key Features

- SQLite database integration
- Data cleaning and preprocessing
- Exploratory data analysis and visualization
- Character-level NLP feature extraction
- Feature engineering for password characteristics
- Multiclass Logistic Regression classification
- Interactive password prediction
- Model evaluation using standard metrics

## 🔮 Future Improvements

- Develop a web interface using Streamlit or Flask.
- Compare Logistic Regression with Random Forest and other classification algorithms.
- Improve feature engineering and model validation.
- Add password-strength recommendations.
- Introduce secure, privacy-preserving password analysis.
- Build automated tests and a reproducible training pipeline.

## ⚠️ Dataset and Security Disclaimer

The notebook documents a password dataset associated with a historical third-party data breach. Passwords are sensitive credentials, even when used for research.

Do not publish leaked credentials, real user passwords, or other sensitive information. Before sharing this repository publicly, remove any database containing actual passwords and replace it with a properly licensed, sanitized, or synthetic dataset. Review the repository's Git history as well, because deleting a file from the latest version does not necessarily remove it from earlier commits.

This project is intended for educational purposes. Its predictions should not be treated as a definitive security assessment or as a substitute for established password-security practices.

## 👨‍💻 Author

**Parth Varute**

GitHub: [@parthvarute09](https://github.com/parthvarute09)

Project Repository: [Password Strength Classification System Using NLP & Machine Learning](https://github.com/parthvarute09/-Password-Strength-Classification-System-Using-NLP-Machine-Learning)

---

⭐ If you find this project useful for learning NLP and machine learning, consider starring the repository.
