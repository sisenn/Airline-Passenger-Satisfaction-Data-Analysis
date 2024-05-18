

# Airline Passenger Satisfaction Data Analysis

## Table of Contents
- [Requirements](#requirements)
- [Project Structure](#project-structure)
- [Functions](#functions)
- [Usage](#usage)

## Requirements
To run the code in this project, you need the following libraries:

- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- plotly

You can install the required libraries using pip:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn plotly
```

## Project Structure
The main script in this project is `airline_passenger_satisfaction_analysis.py`, which includes all the functions and the execution code. Here is an overview of the key functions defined in the script.

## Functions

### `data_discovery(dataframe)`
Explore the given dataframe.

### `explore_data_types(df)`
Explore data types in the given dataframe.

### `visualize_numeric_columns_plotly(dataframe)`
Visualize numeric columns of the given dataframe using Plotly.

### `handle_missing_values(df)`
Handles missing values in the DataFrame by visualizing and dropping them.

### `label_encode_dataframe(df)`
Encode categorical columns of a dataframe using LabelEncoder.

### `detect_and_plot_outliers(df)`
Detect and plot outliers for each column in the dataframe.

### `remove_outliers(df, outliers)`
Remove outliers from the DataFrame.

### `visualize_scatterplots(df_original, df_cleaned)`
Visualize scatter plots of each column in the original and cleaned dataframes for comparison.

### `standardize_dataframe(df)`
Standardizes all numerical columns in the DataFrame.

### `correlation_analysis(df)`
Perform correlation analysis on the dataframe.

### `feature_selection(df, threshold=0.7)`
Perform feature selection based on correlation matrix.

### `plot_feature_importance(df, target_variable)`
Plot feature importance based on correlation with the target variable.

### `remove_low_importance_features(df, low_importance_features)`
Remove features with low importance.

### `visualize_cleaned_data(df)`
Visualize numerical columns using histograms.

## Usage
To use the script, follow these steps:

1. **Load the dataset**: Load the dataset from a CSV file.
```python
import pandas as pd

# Load the dataset from the specified file path.
df = pd.read_csv("/path/to/your/airline_passenger_satisfaction.csv")
```

2. **Explore the dataset**: Call the `data_discovery` function to explore the dataset.
```python
data_discovery(df)
```

3. **Explore data types**: Perform data type exploration using the `explore_data_types` function.
```python
explore_data_types(df)
```

4. **Visualize numeric columns**: Use the `visualize_numeric_columns_plotly` function to visualize numeric columns with Plotly.
```python
visualize_numeric_columns_plotly(df)
```

5. **Handle missing values**: Handle missing values in the dataframe and visualize them.
```python
df_processed = handle_missing_values(df)
```

6. **Encode categorical columns**: Apply the `label_encode_dataframe` function.
```python
df = label_encode_dataframe(df)
```

7. **Detect and plot outliers**: Call the function to detect and plot outliers for each column.
```python
detect_and_plot_outliers(df)
```

8. **Remove outliers**: Remove outliers from the dataframe.
```python
df_cleaned = remove_outliers(df, outliers)
```

9. **Visualize scatter plots**: Call the function to visualize scatter plots.
```python
visualize_scatterplots(df, df_cleaned)
```

10. **Standardize the dataframe**: Test the function and check the standardized data.
```python
df_standardized = standardize_dataframe(df)
```

11. **Perform correlation analysis**: Call the function for correlation analysis.
```python
correlation_analysis(df)
```

12. **Feature selection**: Perform feature selection.
```python
df_selected = feature_selection(df_cleaned)
```

13. **Plot feature importance**: Plot feature importance based on correlation with the target variable.
```python
plot_feature_importance(df_selected, 'Satisfaction')
```

14. **Remove low importance features**: Remove features with low importance.
```python
low_importance_features = ['ID', 'Gate Location', 'Gender']
df_selected = remove_low_importance_features(df_selected, low_importance_features)
```

15. **Visualize cleaned data**: Visualize numerical columns.
```python
visualize_cleaned_data(df_selected)
```