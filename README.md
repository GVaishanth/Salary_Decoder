# Bangalore Tech Salary Decoder

A data-cleaning and exploratory analysis project that decodes compensation patterns across Bengaluru tech roles. The notebook cleans a synthetic salary dataset of 1,000 tech professionals and answers practical business questions about pay drivers such as role, experience, company type, skills, and education.

> Built as part of **The Unlox Academy — 2-Hour Live Project**.

---

## Project Overview

The goal of this project is to transform messy salary data into clear, decision-ready insights. The analysis focuses on current CTC in LPA and compares salaries across job families, experience bands, company types, and technical skills.

The final notebook produces:

- A cleaned and standardized salary dataset
- Role-wise CTC summaries
- Experience-based salary growth analysis
- Skill premium analysis for SDE roles
- Company-type salary comparison
- Identification of potentially underpaid professionals
- A formatted text report suitable for sharing on LinkedIn or in a portfolio

---

## Repository Structure

```text
Salary_Decoder/
├── LiveProject_Salary_Decoder_GVaishanth.ipynb   # Main analysis notebook
├── README.md                                     # Project documentation
└── .gitattributes
```

> Note: The notebook expects a CSV file named `bangalore_tech_salaries.csv` in the project root. If the dataset is not present in the repository, place it in the root folder before running the notebook.

---

## Key Business Questions Answered

1. **Which tech roles have the highest and lowest median CTC?**
2. **How does SDE Backend salary grow with experience?**
3. **Which skills create the strongest salary premium for SDEs?**
4. **How much does company type influence pay for the same role?**
5. **Which professionals appear most underpaid compared with their peer group?**

---

## Highlight Insights

### 1. Product Managers lead in median pay
Product Managers have the highest median CTC at **31.3 LPA**, while Data Analysts have the lowest median among the analyzed roles at **16.3 LPA**.

### 2. Early experience creates the biggest salary jump
For SDE Backend roles, median CTC grows from **11.6 LPA** at 0–1 years of experience to **40.4 LPA** at 6+ years. The largest percentage jump occurs between **0–1 years and 2–3 years**, with approximately **72% growth**.

### 3. System Design has the strongest skill premium
Among the tested skills, **System Design** shows the highest salary premium for SDEs, with a median CTC of **25.3 LPA** compared with **21.0 LPA** for those without it — a **20.5% premium**.

### 4. Unicorn companies pay a strong premium
For the same SDE Backend role, Unicorns show a median CTC of **27.4 LPA**, compared with **20.5 LPA** at MNCs — a **33.7% premium**.

### 5. Underpaid professionals are concentrated in MNCs
The analysis found that all top 10 most-underpaid professionals, relative to their peer groups, work at MNCs. The largest observed gap is **-7.9 LPA** against the peer median.

---

## Data Cleaning Performed

The notebook includes a structured cleaning pipeline:

- Standardized column names to `snake_case`
- Removed duplicate rows
- Consolidated inconsistent role names into clean role categories
- Converted CTC values from multiple formats into numeric LPA values
- Standardized company type labels
- Standardized education tier labels
- Standardized work mode values
- Cleaned skill text for skill-based filtering
- Created experience bands:
  - `0-1`
  - `2-3`
  - `4-5`
  - `6+`

---

## Tools and Libraries

The project uses:

- **Python**
- **Pandas** — data loading, cleaning, grouping, aggregation
- **NumPy** — numeric handling
- **Jupyter Notebook** — analysis and reporting

---

## How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/GVaishanth/Salary_Decoder.git
cd Salary_Decoder
```

### 2. Add the dataset

Place the dataset file in the project root with this exact name:

```text
bangalore_tech_salaries.csv
```

### 3. Install dependencies

If you do not already have the required packages installed, run:

```bash
pip install pandas numpy jupyter
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open and run:

```text
LiveProject_Salary_Decoder_GVaishanth.ipynb
```

Run the cells from top to bottom to reproduce the cleaning steps, analysis outputs, insights, and final printed report.

---

## Expected Dataset Columns

The notebook is designed for a salary dataset containing columns similar to:

| Column | Description |
|---|---|
| `Employee_ID` | Unique employee identifier |
| `Role` | Employee job role |
| `Years_Exp` | Years of professional experience |
| `Current_CTC` | Current compensation value |
| `Previous_CTC` | Previous compensation value |
| `Company_Type` | Employer type such as MNC, Unicorn, Mid-size, or Early-stage |
| `Education_Tier` | Education tier category |
| `Work_Mode` | Remote, hybrid, or onsite work setup |
| `Skills` | Skills associated with the employee profile |

---

## Analysis Methods

The project uses simple, interpretable analytics methods:

- Median and mean CTC comparison by role
- Experience-band salary curve analysis
- Skill-based median CTC comparison
- Company-type premium calculation
- Peer-group benchmarking using `(role, company_type, exp_band)` groups
- Underpayment detection based on CTC gap from group median

---

## Final Report Output

The notebook ends with a formatted report titled:

```text
BANGALORE TECH SALARY DECODER
```

The report summarizes:

- Median CTC by role
- SDE Backend CTC by experience band
- Skill premiums for SDEs
- Company-type premium for SDE Backend
- Top underpaid professionals
- Three key insights with actionable takeaways

---

## Project Status

Completed as a notebook-based analytics project. Future improvements could include:

- Adding visual charts with Matplotlib or Seaborn
- Exporting cleaned data to CSV
- Converting the notebook into a reusable Python script
- Building a Streamlit dashboard for interactive salary exploration
- Adding automated tests for cleaning functions

---

## Author

**G. Vaishanth**

- GitHub: [GVaishanth](https://github.com/GVaishanth)

---

## Disclaimer

This project uses a synthetic Bengaluru tech salary dataset for learning and portfolio purposes. The insights should be interpreted as dataset-specific findings, not as official market compensation benchmarks.
