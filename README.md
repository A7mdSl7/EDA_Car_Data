# EDA & Cleaning - Car Data

This Jupyter Notebook (`EDA & Cleaning - car_data.ipynb`) performs Exploratory Data Analysis (EDA) and data cleaning on a car dataset (`car_data.csv`). The goal is to prepare the data for further analysis or modeling by handling missing values, inconsistencies, and outliers.

## Project Structure

- `EDA & Cleaning - car_data.ipynb`: The main notebook containing the data cleaning and EDA steps.
- `car_data.csv`: The input dataset (assumed to be in the same directory).

## Dataset

The dataset contains the following columns:

| Column Name | Description |
| :--- | :--- |
| **name** | Name/model of the car |
| **year** | Manufacturing year |
| **selling_price** | Selling price of the car |
| **km_driven** | Total kilometers driven |
| **fuel** | Fuel type (Petrol, Diesel, CNG, etc.) |
| **seller_type** | Type of seller (Individual, Dealer, etc.) |
| **transmission** | Transmission type (Manual, Automatic) |
| **owner** | Ownership history (First Owner, Second Owner, etc.) |

## Steps Performed

1.  **Initialization**:
    -   Importing necessary libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`.
    -   Loading the dataset `car_data.csv`.

2.  **Data Normalization**:
    -   Standardizing `fuel` column values (correcting typos like 'Petrrol' to 'Petrol').
    -   Standardizing `seller_type` column values.

3.  **Data Cleaning**:
    -   **Duplicate Removal**: Identifying and dropping duplicate rows.
    -   **Missing Value Handling**:
        -   Dropping rows with missing `name`.
        -   Imputing numerical columns (`year`, `selling_price`, `km_driven`) with the median.
        -   Imputing categorical columns (`fuel`, `seller_type`, `transmission`, `owner`) with the mode.
    -   **Type Conversion**: Converting `year`, `selling_price`, and `km_driven` to appropriate numeric types.

4.  **Outlier Removal**:
    -   Filtering invalid years (valid range: 1980 - 2025).
    -   Ensuring positive `selling_price`.
    -   Filtering realistic `km_driven` (less than 2,000,000 km).

5.  **Exploratory Data Analysis (EDA)**:
    -   Displaying summary statistics and inspecting the clean dataframe.

## Usage

To run this notebook:
1.  Ensure you have Python installed with `jupyter`, `pandas`, `numpy`, `matplotlib`, and `seaborn`.
2.  Place `car_data.csv` in the same directory.
3.  Open the notebook and run all cells.
