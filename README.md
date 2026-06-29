# Bangalore Tech Salary Decoder

A professional data-cleaning and exploratory data analysis project focused on decoding salary patterns in Bengaluru's tech industry. This project uses the included `bangalore_tech_salaries.csv` dataset and analyzes how compensation varies by role, experience, company type, skills, education tier, and work mode.

> Built as part of **The Unlox Academy — 2-Hour Live Project**.

---

## Project Summary

The objective of this project is to convert a messy real-world-style salary dataset into clean, structured insights. The dataset contains salary records for Bengaluru tech professionals, including job roles, experience, current and previous CTC, company type, skills, location, education tier, joining year, and work mode.

The notebook performs end-to-end analysis starting from raw data inspection, followed by cleaning, standardization, business-question analysis, and a final formatted report.

---

## Dataset

The dataset is included in this repository:

```text
bangalore_tech_salaries.csv
```

### Raw Dataset Details

- **Rows:** 1,015
- **Columns:** 12
- **Duplicate rows:** 15
- **Cleaned records used for analysis:** 1,000
- **Domain:** Bengaluru tech salary analytics
- **Dataset type:** Synthetic learning dataset

### Dataset Columns

| Column | Description |
|---|---|
| `Employee_ID` | Unique employee identifier |
| `Role` | Job role of the professional; contains multiple naming variations before cleaning |
| `years_exp` | Total years of professional experience |
| `Current_CTC` | Current compensation, stored in multiple formats such as LPA and rupees |
| `Previous_CTC` | Previous compensation; missing for freshers or first-job professionals |
| `Company` | Company name |
| `company_TYPE` | Type of company such as MNC, Unicorn, Mid-size, or Early-stage |
| `Skills` | Skills listed for the professional |
| `Location` | Bengaluru location/area |
| `Education_Tier` | Education tier category |
| `Joining_Year` | Year of joining the current company |
| `Work_Mode` | Remote, hybrid, or onsite work mode |

---

## Repository Structure

```text
Salary_Decoder/
├── bangalore_tech_salaries.csv                    # Dataset used for analysis
├── LiveProject_Salary_Decoder_GVaishanth.ipynb   # Main Jupyter Notebook
├── README.md                                     # Project documentation
└── .gitattributes
```

---

## Key Business Questions

This project answers five practical salary-analysis questions:

1. **Which roles have the highest and lowest median CTC?**
2. **How does salary grow with experience for SDE Backend professionals?**
3. **Which skills provide the strongest salary premium for SDE roles?**
4. **How much does company type affect salary for the same role?**
5. **Which professionals appear underpaid compared with their peer group?**

---

## Data Cleaning Process

The raw dataset contains inconsistent formatting, duplicate records, missing values, and mixed salary formats. The notebook cleans the dataset through the following steps:

- Renames columns into a consistent `snake_case` format
- Removes duplicate rows
- Standardizes role names such as `DS`, `BA`, `SDE-Backend`, `FullStack`, and `PM`
- Converts CTC values into numeric LPA format
- Handles salary formats such as:
  - `15.5 LPA`
  - `15.5`
  - `15,50,000`
  - `Rs 15.5 LPA`
- Standardizes company type labels
- Standardizes education tier values
- Standardizes work mode values
- Cleans skills text for skill-based comparison
- Creates experience bands:
  - `0-1`
  - `2-3`
  - `4-5`
  - `6+`

---

## Analysis Performed

The notebook uses simple and interpretable analytics methods, including:

- Role-wise median, mean, minimum, and maximum CTC comparison
- Experience-band salary growth analysis
- Skill premium analysis for SDE roles
- Company-type salary premium comparison
- Peer-group salary benchmarking
- Identification of underpaid professionals using group median comparison

Peer groups are created using:

```text
role + company type + experience band
```

This makes the underpayment analysis more meaningful because each person is compared with similar professionals.

---

## Key Insights

### 1. Product Managers have the highest median salary
Product Managers show the highest median CTC at **31.3 LPA**, while Data Analysts have the lowest median CTC at **16.3 LPA** among the analyzed roles.

### 2. SDE Backend salary grows strongly with experience
For SDE Backend professionals, median CTC increases from **11.6 LPA** for 0–1 years of experience to **40.4 LPA** for 6+ years of experience. The largest percentage jump happens from 0–1 years to 2–3 years, with approximately **72% growth**.

### 3. System Design is the strongest salary-differentiating skill
For SDE roles, professionals with **System Design** skills have a median CTC of **25.3 LPA**, compared with **21.0 LPA** for those without it. This represents a **20.5% salary premium**.

### 4. Unicorn companies pay a clear premium
For the same SDE Backend role, Unicorn companies show a median CTC of **27.4 LPA**, while MNCs show **20.5 LPA**. This indicates a **33.7% premium** for Unicorn companies over MNCs.

### 5. Underpaid professionals are concentrated in MNCs
The top 10 most-underpaid professionals identified by the analysis are all from MNCs. The largest observed gap is **-7.9 LPA** compared with the peer-group median.

---

## Tools and Technologies

- **Python**
- **Pandas**
- **NumPy**
- **Jupyter Notebook**

---

## How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/GVaishanth/Salary_Decoder.git
cd Salary_Decoder
```

### 2. Install dependencies

```bash
pip install pandas numpy jupyter
```

### 3. Open Jupyter Notebook

```bash
jupyter notebook
```

### 4. Run the notebook

Open the notebook below and run all cells from top to bottom:

```text
LiveProject_Salary_Decoder_GVaishanth.ipynb
```

The dataset is already included in the repository, so no additional data download is required.

---

## Final Output

The notebook ends with a formatted salary report titled:

```text
BANGALORE TECH SALARY DECODER
```

The report includes:

- Median CTC by role
- SDE Backend salary by experience band
- Skill premium comparison for SDEs
- Company-type premium analysis
- Top underpaid professionals
- Three action-oriented salary insights

---

## Possible Future Improvements

- Add salary visualizations using Matplotlib or Seaborn
- Export the cleaned dataset as a CSV file
- Convert repeated cleaning logic into reusable Python functions
- Build a Streamlit dashboard for interactive salary exploration
- Add more analysis by location, work mode, joining year, and education tier
- Add automated checks for data quality and duplicate detection

---

## Author

**G. Vaishanth**

- GitHub: [GVaishanth](https://github.com/GVaishanth)

---

## Disclaimer

This project uses a synthetic Bengaluru tech salary dataset for educational and portfolio purposes. The insights are specific to this dataset and should not be treated as official salary benchmarks.
