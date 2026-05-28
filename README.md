# Customer Data Preprocessing Pipeline

## Overview

This project implements a complete customer data preprocessing workflow using Python.

The raw customer dataset was transformed from a flat CSV structure into nested JSON records suitable for downstream analytics, reporting and machine learning workflows.

The project demonstrates practical data engineering and preprocessing techniques including:
- Data cleaning
- Missing value handling
- Nested JSON transformation
- Customer segmentation
- Credit card validation
- Feature engineering
- Exploratory data analysis (EDA)
- Data visualisation

---

## Project Objectives

The main objectives of this project were to:

- Import and preprocess customer data from a CSV file
- Convert flat tabular data into structured nested JSON
- Clean and validate customer records
- Segment customers based on employment status
- Detect potentially invalid credit card records
- Engineer new analytical features
- Perform exploratory data analysis and visualisation
- Export processed outputs for downstream use

---

## Tools Used

- Python
- Pandas
- JSON
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## Dataset

The dataset contains customer information including:

- Personal details
- Address information
- Vehicle information
- Credit card details
- Salary information
- Employment status
- Commute distance

The original dataset was provided in CSV format and transformed into structured JSON outputs.

---

## Project Workflow

### 1. Data Ingestion
- Imported customer CSV data using Pandas
- Inspected dataset structure and datatypes

### 2. Data Cleaning
- Handled missing values
- Converted numerical columns to appropriate datatypes
- Standardized records for consistency

### 3. Nested JSON Transformation
Flat customer records were transformed into nested JSON structures including:
- Vehicle information
- Address information
- Credit card information

### 4. Customer Segmentation
Created separate JSON outputs for:
- Retired customers
- Employed customers

### 5. Credit Card Validation
Identified customer credit cards with durations exceeding 10 years.

### 6. Feature Engineering
Calculated salary-to-commute ratios for customer analysis.

### 7. Exploratory Data Analysis
Generated visualisations to analyze:
- Age distribution
- Salary distribution
- Dependants distribution
- Salary vs age relationships

---

## Repository Structure

```text
customer-data-preprocessing-pipeline/
│
├── data/
│   └── acw_user_data.csv
│
├── notebook/
│   └── customer_data_preprocessing.ipynb
│
├── outputs/
│   ├── processed.json
│   ├── retired.json
│   ├── employed.json
│   ├── remove_ccard.json
│   └── commute.json
│
├── visualisations/
│   ├── age_distribution.png
│   ├── dependants_distribution.png
│   ├── salary_distribution.png
│   └── salary_vs_age.png
│
├── requirements.txt
├── README.md
└── .gitignore
```

---

## Sample JSON Structure

```json
 {
        "first_name": "Malcolm",
        "second_name": "Hamilton",
        "age": 87,
        "sex": "Male",
        "retired": true,
        "marital_status": "single",
        "dependants": 2,
        "salary": 66157.0,
        "pension": 29587.0,
        "company": NaN,
        "commute_distance": 0.0,
        "Vehicle": {
            "make": "Dodge",
            "model": "Impreza",
            "year": 2015,
            "category": "Sedan"
        },
        "Credit Card": {
            "start_date": "10/13",
            "end_date": "10/13",
            "number": 213198388220332,
            "ccv": 766,
            "iban": "GB74TXVQ82130006568515"
        },
        "Address": {
            "street": "Studio 77c Gail tunnel",
            "city": "Garyberg",
            "postcode": "S7W 4DW"
        }
    }
```

---

## Visualisations

### Age Distribution
Analyses customer age demographics across the dataset.

### Salary Distribution
Explores yearly salary patterns and outliers.

### Dependants Distribution
Examines household dependency trends.

### Salary vs Age
Investigates relationships between salary and age.

---

## How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/Greatness-O/customer-data-preprocessing-pipeline.git
```

### 2. Navigate to the Project Directory

```bash
cd customer-data-preprocessing-pipeline
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

### 5. Open the Notebook

Open:

```text
notebook/customer_data_preprocessing.ipynb
```

Run all cells to generate processed outputs and visualisations.

---

## Output Files

| File | Description |
|---|---|
| `processed.json` | Fully transformed customer dataset |
| `retired.json` | Retired customer records |
| `employed.json` | Employed customer records |
| `remove_ccard.json` | Invalid credit card records |
| `commute.json` | Salary-to-commute ratios |

---

## Key Skills Demonstrated

- Data preprocessing
- Data transformation
- JSON structuring
- Data cleaning
- Feature engineering
- Exploratory data analysis
- Data visualisation
- Python programming
- Jupyter Notebook workflows

---

## Future Improvements

Potential future enhancements include:

- Converting notebook logic into reusable Python modules
- Building an automated preprocessing pipeline
- Adding unit tests
- Creating a Streamlit dashboard
- Adding machine learning workflows
- Deploying the pipeline as an API

---

## Author
Greatness Okeremeta
- GitHub: github.com/Greatness-O
- LinkedIn: www.linkedin.com/in/greatness-okeremeta
