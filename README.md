# Student Performance Prediction Analysis

A comprehensive machine learning project that predicts student exam scores based on various performance factors using linear and polynomial regression models.

## 📊 Project Overview

This project analyzes student performance data to identify key factors that influence exam scores and builds predictive models to estimate student performance. The analysis includes data cleaning, exploratory data analysis, and multiple regression approaches with different feature sets.

## 🎯 Objectives

- Predict student exam scores based on study habits and demographic factors
- Identify the most influential factors affecting student performance
- Compare different regression approaches (linear vs polynomial)
- Evaluate model performance using multiple metrics

## 📁 Dataset

The analysis expects a CSV file named `StudentPerformanceFactors.csv` with the following features:

### Core Features
- **Hours_Studied**: Number of hours spent studying
- **Attendance**: Class attendance percentage
- **Sleep_Hours**: Average hours of sleep per night
- **Previous_Scores**: Previous academic performance scores
- **Tutoring_Sessions**: Number of tutoring sessions attended
- **Physical_Activity**: Hours of physical activity per week

### Categorical Features
- **Teacher_Quality**: Quality rating of teachers
- **Distance_from_Home**: Distance from home to school
- **Parental_Education_Level**: Education level of parents

### Target Variable
- **Exam_Score**: Final exam score (target for prediction)

## 🛠️ Dependencies

```python
pandas>=1.3.0
numpy>=1.21.0
matplotlib>=3.4.0
seaborn>=0.11.0
scikit-learn>=1.0.0
```

## 📦 Installation

1. Clone or download the project files
2. Install required packages:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```
3. Place your `StudentPerformanceFactors.csv` file in the project directory
4. Run the analysis script

## 🚀 Features

### 1. Data Processing
- **Automated Data Loading**: Handles missing CSV files with sample data generation
- **Missing Value Handling**: Strategic imputation for numerical and categorical features
- **Duplicate Detection**: Automatic identification and removal of duplicate records
- **Data Type Validation**: Proper handling of numerical and categorical variables

### 2. Exploratory Data Analysis
- **Comprehensive Visualizations**: 4-panel subplot showing key relationships
- **Correlation Analysis**: Heatmap of feature correlations
- **Distribution Analysis**: Histograms of key variables
- **Scatter Plot Analysis**: Relationship between study hours and exam scores

### 3. Machine Learning Models

#### Simple Linear Regression
- Uses only study hours as predictor
- Baseline model for comparison
- Clear visualization of linear relationship

#### Polynomial Regression
- Second-degree polynomial features
- Captures non-linear relationships
- Enhanced predictive capability

#### Multi-Feature Linear Regression
- Utilizes all available features
- Advanced preprocessing pipeline
- Handles both numerical and categorical data
- Feature scaling and encoding

### 4. Model Evaluation
- **Mean Absolute Error (MAE)**: Average prediction error
- **Root Mean Square Error (RMSE)**: Penalizes larger errors
- **R-squared Score**: Proportion of variance explained
- **Comparative Analysis**: Performance comparison across models

## 📈 Results Interpretation

### Evaluation Metrics
- **MAE**: Lower values indicate better accuracy
- **RMSE**: Measures prediction precision
- **R²**: Values closer to 1 indicate better model fit

### Expected Performance Hierarchy
1. **Multi-feature model**: Best performance using all variables
2. **Polynomial regression**: Improved over linear with non-linear relationships
3. **Simple linear regression**: Baseline performance

## 🎨 Visualizations

The project generates several informative plots:

1. **Study Hours vs Exam Score**: Scatter plot showing primary relationship
2. **Exam Score Distribution**: Histogram showing score distribution
3. **Correlation Heatmap**: Feature correlation matrix
4. **Study Hours Distribution**: Distribution of study time
5. **Regression Line Plots**: Visual model performance comparison

## 🔧 Customization Options

### Adding New Features
```python
# Add new numerical features to num_cols list
num_cols = ['Hours_Studied', 'Your_New_Feature']

# Add new categorical features to cat_cols list
cat_cols = ['Teacher_Quality', 'Your_New_Category']
```

### Adjusting Model Parameters
```python
# Change polynomial degree
poly_features = PolynomialFeatures(degree=3)  # Default: 2

# Modify train-test split ratio
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.3)  # Default: 0.2
```

### Visualization Customization
```python
# Change plot style
plt.style.use('ggplot')  # Options: 'seaborn', 'classic', 'bmh'

# Modify color palette
sns.set_palette("Set2")  # Options: "viridis", "plasma", "Set1"
```

## 📊 Sample Output

```
Dataset Shape: (1000, 9)
Simple Linear Regression:
MAE: 12.45
RMSE: 15.67
R² Score: 0.6234

Polynomial Regression:
MAE: 11.23
RMSE: 14.56
R² Score: 0.6789

Multi-Feature Model:
MAE: 8.91
RMSE: 11.34
R² Score: 0.7856
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/improvement`)
3. Commit changes (`git commit -am 'Add new feature'`)
4. Push to branch (`git push origin feature/improvement`)
5. Create a Pull Request

## 📝 Notes

- The script includes fallback sample data generation if the CSV file is missing
- All warnings are suppressed for cleaner output
- Models use random_state=42 for reproducible results
- Categorical variables are handled with one-hot encoding
- Numerical features are standardized for optimal performance

## 🐛 Troubleshooting

### Common Issues
1. **File Not Found**: Ensure CSV file is in the correct directory
2. **Memory Issues**: Reduce dataset size or increase system RAM
3. **Import Errors**: Verify all required packages are installed
4. **Plot Display Issues**: Ensure matplotlib backend is properly configured

### Performance Tips
- For large datasets, consider feature selection techniques
- Use cross-validation for more robust model evaluation
- Implement early stopping for polynomial regression with high degrees

## 📄 License

This project is open source and available under the MIT License.

## 👥 Authors

- Data Science Analysis Team
- Machine Learning Implementation

## 🔗 References

- Scikit-learn Documentation: https://scikit-learn.org/
- Pandas Documentation: https://pandas.pydata.org/
- Matplotlib Documentation: https://matplotlib.org/
- Seaborn Documentation: https://seaborn.pydata.org/

---

*For questions or suggestions, please open an issue or contact the development team.*
