# Palmer Penguins Exploratory Data Analysis (EDA)

## Overview

This project demonstrates a complete Exploratory Data Analysis (EDA) workflow using the Palmer Penguins dataset. The script loads data, performs data quality checks, generates descriptive statistics, analyzes correlations, and creates visualizations to help understand relationships among penguin species and their physical characteristics.

The project serves as both a learning resource and a reusable template for future EDA projects.

---

## Authors

* Ralph Massaquoi

**Date:**May 2026

---

## Dataset

### Palmer Penguins Dataset

The dataset contains observations of penguins from the Palmer Archipelago in Antarctica.

**Source:** Seaborn built-in datasets

### Features

| Column            | Description                       |
| ----------------- | --------------------------------- |
| species           | Penguin species                   |
| island            | Island where penguin was observed |
| bill_length_mm    | Bill length in millimeters        |
| bill_depth_mm     | Bill depth in millimeters         |
| flipper_length_mm | Flipper length in millimeters     |
| body_mass_g       | Body mass in grams                |
| sex               | Penguin sex                       |
| year              | Year observed                     |

---

## Project Objectives

This project demonstrates how to:

* Load a dataset with Seaborn
* Inspect data structure using Pandas
* Create a data dictionary
* Identify missing values and duplicates
* Clean data for analysis
* Generate descriptive statistics
* Perform grouped analysis by species
* Calculate correlation matrices
* Visualize relationships with charts
* Summarize findings and suggest next steps

---

## Technologies Used

* Python 3.11+
* Pandas
* NumPy
* Seaborn
* Matplotlib
* DataFun Toolkit

---

## Project Structure

```text
project-root/
│
├── datafun/
│   └── app_case.py
│
├── README.md
├── pyproject.toml
├── requirements.txt
└── .venv/
```

---

## Installation

### 1. Clone the Repository

```bash
git clone <your-repository-url>
cd <repository-folder>
```

### 2. Create and Activate a Virtual Environment

#### Windows

```bash
python -m venv .venv
.venv\Scripts\activate
```

#### macOS/Linux

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install Required Packages

Using pip:

```bash
pip install pandas numpy seaborn matplotlib datafun-toolkit
```

Or install from requirements.txt:

```bash
pip install -r requirements.txt
```

### 4. Optional: Install UV

This project can also be run using UV.

```bash
pip install uv
```

---

## Running the Application

### Using UV (Recommended)

From the project root folder:

```bash
uv run python -m datafun.app_case
```

### Using Python

```bash
python -m datafun.app_case
```

or

```bash
python datafun/app_case.py
```

---

## EDA Workflow

### 1. Load Dataset

The script loads the Palmer Penguins dataset directly from Seaborn:

```python
sns.load_dataset("penguins")
```

---

### 2. Inspect Dataset

The script examines:

* Dataset dimensions
* Column names
* Data types
* Non-null counts
* Sample records

---

### 3. Build Data Dictionary

Creates a summary table containing:

* Column name
* Data type
* Missing value count
* Missing value percentage

---

### 4. Data Quality Checks

Performs:

* Missing value analysis
* Duplicate row detection
* Numeric summaries using `describe()`

---

### 5. Data Cleaning

Creates a clean analytical dataset by removing rows with missing values in:

* species
* bill_length_mm
* bill_depth_mm
* flipper_length_mm
* body_mass_g

---

### 6. Descriptive Statistics

Computes:

#### Overall Statistics

* Count
* Mean
* Standard deviation
* Minimum
* Maximum
* Quartiles

#### Grouped Statistics

Aggregates statistics by penguin species using:

```python
groupby().agg()
```

---

### 7. Correlation Analysis

Calculates correlations among numeric variables and visualizes the results with a heatmap.

Typical finding:

* Flipper length and body mass show a strong positive correlation (~0.87).

---

### 8. Visualizations

#### Scatter Plot

Displays the relationship between:

* Flipper Length
* Bill Length

Colored by species.

#### Box Plot

Shows the distribution of flipper length across species.

#### Correlation Heatmap

Visualizes relationships among numeric variables.

---

## Example Outputs

### Console Output

The script logs:

* Dataset information
* Data quality summaries
* Statistical summaries
* Correlation analysis
* Final recommendations

### Generated Visualizations

* Correlation Heatmap
* Species Scatter Plot
* Species Box Plot

---

## Key Findings

Typical observations include:

* Penguin species exhibit distinct physical characteristics.
* Flipper length is strongly correlated with body mass.
* Species differ noticeably in bill measurements.
* Missing values are minimal and manageable.

---

## Future Enhancements

Potential next steps include:

* Linear regression modeling
* Species classification
* Outlier detection
* Predictive analytics
* Interactive dashboards
* Automated reporting

---

## Educational Purpose

This project is intended as a reference implementation for students learning:

* Exploratory Data Analysis
* Pandas
* NumPy
* Data Visualization
* Statistical Data Exploration

The code is heavily documented to explain both the "how" and the "why" behind each step of the analysis process.

---

## Notes

This script opens chart windows using Matplotlib.

After reviewing the charts:

1. Close the chart windows.
2. Return to the terminal.
3. Stop execution if needed using:

```bash
CTRL + C
```

---

## License

This project is provided for educational and instructional purposes. The Palmer Penguins dataset is publicly available through the Seaborn library.
