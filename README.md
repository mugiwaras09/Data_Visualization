# 📊  Data Visualization  ( Data Analyst & Candidate Selection )

A Python-based **Data Visualization and Candidate Selection Tool** that processes structured Excel data to identify candidates with **Data Analysis** skills, generate a shortlist of the top 5 matching records, export the results to Excel, and visualize candidate skill information using charts.

## 🚀 Project Overview

The project demonstrates an end-to-end data analysis workflow using **Python, Pandas, Matplotlib, and Excel**.

The application takes an Excel dataset as input and performs the following workflow:

**Excel Dataset → Data Loading → Skill Filtering → Candidate Selection → Excel Export → Data Visualization**

The solution is designed to demonstrate practical skills in **data extraction, filtering, transformation, reporting, and visualization**.

## 🎯 Objectives

* Read structured candidate data from an Excel file.
* Identify candidates with **Data Analysis** skills.
* Extract relevant candidate information.
* Select the first 5 matching candidates.
* Export the selected records into a new Excel file.
* Provide optional visual analysis through:

  * Pie Chart
  * Bar Chart
* Build a simple reusable Python data-processing workflow.

## 🛠️ Technologies Used

| Technology       | Purpose                                        |
| ---------------- | ---------------------------------------------- |
| **Python**       | Application development and data processing    |
| **Pandas**       | Excel reading, filtering and data manipulation |
| **Matplotlib**   | Data visualization                             |
| **Excel / XLSX** | Input and output data format                   |
| **Datetime**     | Timestamp-based output file generation         |
| **OS**           | File-system related operations                 |

## 📂 Project Structure

```text
Data-Visualization/
│
├── main.py
├── Unstructured.xlsx
├── top_data_analyst_candidates_20260911_204531.xlsx
└── README.md
```

### File Description

**`main.py`**
Main Python application responsible for reading the dataset, filtering candidates, exporting results, and generating visualizations.

**`Unstructured.xlsx`**
Source Excel dataset containing candidate information such as:

* Name
* Mobile Number
* Skill
* Age

**`top_data_analyst_candidates_20260911_204531.xlsx`**
Example generated output containing the selected Data Analysis candidates.

## 🔄 Data Processing Workflow

### 1. Load Excel Dataset

The application reads the Excel file using Pandas:

```python
df = pd.read_excel(file_path)
```

This allows the program to process the candidate dataset directly from an `.xlsx` file.

### 2. Filter Data Analysis Candidates

Candidates are filtered based on the presence of **Data Analysis** in the `Skill` field.

```python
candidates = df[df['Skill'].str.contains('Data Analysis')]
```

The application then selects the relevant columns:

```text
Name
Mobile Number
Skill
Age
```

and returns the first five matching records.

## 📈 Data Visualization

The application supports two visualization modes.

### Pie Chart

The pie chart displays the distribution of skills among the selected candidates.

```python
top_candidates['Skill'].value_counts().plot(
    kind='pie',
    autopct='%1.1f%%',
    title='Top Candidates Skills Distribution'
)
```

This provides a quick view of the skill-level composition of the selected candidate group.

### Bar Chart

The bar chart converts skill levels into numerical values:

```text
Beginner      → 1
Intermediate  → 2
Advanced      → 3
Expert        → 4
```

It then aggregates the skill-level scores by candidate and presents them as a bar chart.

This makes it easier to compare the relative skill levels represented in the filtered dataset.

## 📤 Output

The selected candidates are automatically exported to an Excel file.

The output filename follows the format:

```text
top_data_analyst_candidates_YYYYMMDD_HHMMSS.xlsx
```

For example:

```text
top_data_analyst_candidates_20260911_204531.xlsx
```

This timestamp-based naming approach helps prevent accidental overwriting of previous results.

## ▶️ How to Run the Project

### Prerequisites

Install Python 3.x and the required libraries:

```bash
pip install pandas matplotlib openpyxl
```

### Run the Application

Clone the repository:

```bash
git clone https://github.com/mugiwaras09/Data_Visualization.git
```

Navigate to the project directory:

```bash
cd Data-Visualization
```

Run the Python program:

```bash
python main.py
```

The program will ask for the Excel file path:

```text
Enter the path to the Excel file:
```

Enter the path to your dataset, for example:

```text
Unstructured.xlsx
```

The application will display the selected Data Analyst candidates and save the output Excel file.

You can then choose:

```text
none
pie
bar
```

to control whether a visualization should be generated.

## 📊 Sample Dataset Fields

The project works with candidate records containing:

| Column          | Description                     |
| --------------- | ------------------------------- |
| `Name`          | Candidate name                  |
| `Mobile Number` | Candidate contact number        |
| `Skill`         | Candidate skill and proficiency |
| `Age`           | Candidate age                   |

Example skill values include:

```text
Data Analysis - Expert
Data Analysis - Intermediate
Web Development - Beginner
```

## 🔐 Data Privacy

The project processes candidate information from Excel files. When publishing this project publicly on GitHub, avoid committing real **mobile numbers or other personally identifiable information**.

For a public repository, use anonymized or synthetic data.

## 🔮 Future Enhancements

Possible improvements include:

* Add candidate ranking based on skill proficiency.
* Add multiple skill filters.
* Add age-based filtering.
* Add interactive visualizations using Plotly.
* Build a Streamlit dashboard.
* Add CSV support.
* Add automated data-quality validation.
* Add statistical summaries.
* Add candidate scoring and ranking.
* Add filtering by Beginner/Intermediate/Advanced/Expert level.
* Add downloadable reports.
* Add a web-based user interface.
* Implement unit tests and error handling.

## 📌 Project Use Case

This project can be used as a foundation for a **candidate analytics and recruitment data-processing system**.

A production-ready version could help recruiters or analysts:

1. Upload candidate data.
2. Filter candidates based on required skills.
3. Analyze skill proficiency.
4. Compare candidate profiles.
5. Generate shortlist reports.
6. Visualize candidate distributions.

## 📈 Future Production Architecture

```text
                ┌─────────────────┐
                │  Excel / CSV    │
                │ Candidate Data  │
                └────────┬────────┘
                         │
                         ▼
                ┌─────────────────┐
                │ Data Processing  │
                │     Pandas      │
                └────────┬────────┘
                         │
                         ▼
                ┌─────────────────┐
                │ Filtering &     │
                │ Transformation  │
                └────────┬────────┘
                         │
              ┌──────────┴──────────┐
              ▼                     ▼
       ┌─────────────┐       ┌─────────────┐
       │ Excel Report│       │ Visualization│
       └─────────────┘       └─────────────┘
```

## 👨‍💻 Author

**Niranjan Kadam**

Computer Engineering | Data Analytics | Python | SQL | Power BI | Data Visualization

### Core Interests

* Data Analytics
* Data Visualization
* Python Development
* Business Intelligence
* SQL & Database Analytics
* Machine Learning
* AI-driven Applications

---
