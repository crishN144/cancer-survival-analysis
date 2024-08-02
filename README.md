
# Cancer Survival Analysis: Impact of Stages, Sites, and Treatment Regimes

## Project Overview

This project conducts a comprehensive analysis of cancer survival rates using the Simulacrum dataset, a synthetic dataset mimicking the Cancer Registration data in England. It aims to provide insights for oncologists, medical researchers, and health policy makers through various analytical approaches.

### What Was Done

- **Data Preprocessing**: Handled missing values, standardized formats, and prepared the dataset for analysis.
- **Exploratory Data Analysis (EDA)**: Investigated patterns in cancer site distribution, demographic factors, and their relation to survival rates.
- **Survival Analysis**: Performed Kaplan-Meier analysis to estimate survival probabilities for different cancer stages and treatment regimens.
- **Statistical Testing**: Conducted log-rank tests to compare survival curves between different cancer stages.
- **Visualization**: Created various plots and heatmaps to illustrate findings and patterns in the data.

### Key Findings

- Breast cancer (C509) is the most prevalent cancer site in the dataset, followed by prostate cancer (C619).
- Most cancers occur more frequently in older age groups (41-60, 61-80, 81+).
- Early-stage cancers generally show higher survival probabilities compared to advanced stages.
- Significant differences in survival rates exist between most pairs of cancer stages.
- Treatment regimens show varying patterns of survival probability over time.

## Skills Demonstrated

- Data Cleaning and Preprocessing
- Exploratory Data Analysis (EDA)
- Data Visualization (Matplotlib, Seaborn)
- Survival Analysis (Kaplan-Meier Estimator)
- Statistical Analysis (Log-rank Test)
- Heatmap Generation

## Dataset

### Description

The analysis in this study is based on the Simulacrum dataset, a synthetic dataset created by the National Disease Registration Service (NDRS) to mimic the structure and statistical properties of the original Cancer Registration data while preserving patient confidentiality.

You can download the Simulacrum data at [Simulacrum Data Download](https://simulacrum.healthdatainsight.org.uk/).

### Dataset Linkage Diagram

The Simulacrum dataset consists of several interconnected tables, as illustrated in the dataset linkage diagram below. This dataset establishes a relationship between the Cancer Outcomes & Services Dataset (COSD) and the Systemic Anti-Cancer Therapy (SACT) data. These tables are crucial for understanding patient treatments, outcomes, and other vital information.

![Dataset Linkage Diagram](https://github.com/user-attachments/assets/b450b4d0-796d-4930-9f4e-7810313a730b)

### Main Tables

1. **SIM AV PATIENT**: Contains demographic information about patients, including their NHS number, sex, ethnicity, and vital status details.
2. **SIM AV TUMOUR**: Provides details about each tumor, such as the cancer site, cancer stage, grade, and date of first surgery.
3. **SIM SACT PATIENT**: Links patient information from the SIM AV PATIENT table to the Systemic Anti-Cancer Therapy (SACT) data.
4. **SIM SACT TUMOUR**: Contains information about the primary diagnosis and morphology (cancer type) related to the SACT data.
5. **SIM SACT REGIMEN**: Provides details about the treatment regimens, including the regimen start date, intent of treatment, and a benchmark group for analysis.
6. **SIM SACT CYCLE**: Contains information about the treatment cycles, such as the cycle number and the start date of each cycle.
7. **SIM SACT DRUG DETAIL**: Provides detailed information about the drugs administered during each treatment cycle, including the drug name, dose, and administration route.

### Key Attributes

| Attribute Name     | Description                        | Data Type | Example Value |
|--------------------|------------------------------------|-----------|---------------|
| `AGE`              | Age of the patient                 | Integer   | 65            |
| `SEX`              | Sex of the patient                 | String    | Male          |
| `ETHNICITY`        | Ethnicity of the patient           | String    | White         |
| `SITE_ICD10_O2`    | Cancer site code                   | String    | C509          |
| `STAGE_BEST`       | Best estimate of cancer stage      | String    | Stage II      |
| `NEWVITALSTATUS`   | Vital status of the patient        | String    | Alive         |
| `VITALSTATUSDATE`  | Date of vital status               | Date      | 2023-05-01    |

The key variables used in the analysis include patient demographics (age, sex, ethnicity, geographical region), tumor characteristics (cancer site, cancer stage, tumor grade), treatment information (regimen details, start dates, drug details), and survival information (vital status and date of vital status).

Here's the revised section with main findings highlighted in bold and descriptions kept short and pointwise:

## Visualization

### 1. Distribution of Cancer Sites

<div align="center">
    <img width="509" alt="Distribution of Top 10 Cancer Sites" src="https://github.com/user-attachments/assets/6d132d20-6b14-4110-b36a-ee291208dd8d">
    <p><strong>Distribution of Top 10 Cancer Sites</strong></p>
</div>

- **Top cancer site:** C509 (Breast cancer).
- **Second most common:** C619 (Prostate cancer).
- **Purpose:** Identifies the most prevalent cancer sites for further analysis or targeted interventions.

### 2. Cancer Sites by Age Group

<div align="center">
    <img width="509" alt="Cancer Sites by Age Group (Top 10)" src="https://github.com/user-attachments/assets/24e13682-144c-4c5b-a883-59e3793e39c2">
    <p><strong>Cancer Sites by Age Group (Top 10)</strong></p>
</div>

- **Older age groups (61-80, 81+):** Higher cancer prevalence.
- **Notable types:** C61 (Prostate), C449 (Rectal) concentrated in 61-80 age group.
- **Purpose:** Reveals age-related patterns or associations with cancer sites.

### 3. Cancer Sites by Sex

<div align="center">
    <img width="509" alt="Cancer Sites by Sex" src="https://github.com/user-attachments/assets/e490a1c9-c0eb-4d52-8912-79fcfafbf583">
    <p><strong>Cancer Sites by Sex</strong></p>
</div>

- **Females:** Higher prevalence of C509 (Breast cancer).
- **Males:** Exclusive occurrence of C619 (Prostate cancer).
- **Purpose:** Identifies sex-related differences in cancer site prevalence.

### 4. Cancer Sites by Geographical Region

<div align="center">
    <img width="509" alt="Cancer Sites by Geographical Region (Top 10)" src="https://github.com/user-attachments/assets/d459183c-a624-468c-85d5-a2d52ccbe25e">
    <p><strong>Cancer Sites by Geographical Region (Top 10)</strong></p>
</div>

- **Regional variation:** Notable differences in cancer prevalence.
- **Higher cases:** Some regions report much higher totals.
- **Purpose:** Highlights regional patterns or associations in cancer sites.

### 5. Kaplan-Meier Curves for Different Cancer Stages

<div align="center">
    <img width="509" alt="Kaplan-Meier Curves for Different Cancer Stages" src="https://github.com/user-attachments/assets/906d865e-8285-4d30-b605-deed94abeca7">
    <p><strong>Kaplan-Meier Curves for Different Cancer Stages</strong></p>
</div>

- **Early stages (C20, C349):** Higher initial survival and gradual declines.
- **Advanced stages (C900, C509):** Sharper survival drops.
- **Purpose:** Provides insights into survival probabilities based on cancer stage.

### 6. Kaplan-Meier Curves for Different Therapies

<div align="center">
    <img width="525" alt="Kaplan-Meier Curves for Different Therapies" src="https://github.com/user-attachments/assets/d04a3834-0dc5-4582-94ba-2a21fb6e8f3d">
    <p><strong>Kaplan-Meier Curves for Different Therapies</strong></p>
</div>

- **Regimens with steep drops:** Oxaliplatin + de Gramont, FEC 100, Carboplatin + Paclitaxel.
- **Gradual decline:** Capecitabine, Trastuzumab, CHOP R.
- **Sharp early drop:** Capecitabine + Oxaliplatin 21-day regimen.
- **Purpose:** Evaluates treatment efficacy and long-term outcomes.

### 7. Heatmap of P-values

<div align="center">
    <img width="509" alt="Heatmap of P-values" src="https://github.com/user-attachments/assets/0ea8b7c2-6db0-4805-ae11-8dc34bd0f850">
    <p><strong>Heatmap of P-values for Log-rank Tests Between Cancer Stages</strong></p>
</div>

- **Significant differences:** Dark red indicates low p-values (significant differences).
- **Purpose:** Identifies significant survival differences among cancer stages.


## Conclusion

This comprehensive analysis of cancer survival rates using the Simulacrum dataset has revealed several key insights:

1. **Cancer Site Distribution**: Breast and prostate cancers are the most prevalent in the dataset.

2. **Age-related Patterns**: Most cancers occur more frequently in older age groups, particularly 61-80 years old.

3. **Survival Probabilities**: Early-stage cancers generally show higher survival probabilities compared to advanced stages.

4. **Treatment Efficacy**: Different treatment regimens show varying patterns of survival probability over time.

5. **Statistical Significance**: Significant differences in survival rates exist between most pairs of cancer stages.

These findings provide valuable insights for oncologists, medical researchers, and health policy makers, offering data-driven guidance for treatment strategies and resource allocation in cancer care.

## How to Use

To explore and utilize this project:

1. **Clone the Repository**:
   ```
   git clone https://github.com/crishN144/cancer-survival-analysis.git
   cd cancer-survival-analysis
   ```

2. **Set Up the Environment**:
   - It's recommended to use a virtual environment:
     ```
     python -m venv venv
     source venv/bin/activate  # On Windows use `venv\Scripts\activate`
     ```
   - Install required dependencies:
     ```
     pip install -r requirements.txt
     ```

3. **Run the Analysis**:
   - Open Jupyter Notebook:
     ```
     jupyter notebook
     ```
   - Navigate to and open the following notebooks:
     - `EDA.ipynb`
     - `FINALHEATMAP.ipynb`
     - `KAPLANCURVE.ipynb`
     - `KAPLAN CURVE2.ipynb`
   - Run the cells sequentially to reproduce the analysis

4. **Explore the Results**:
   - Examine the generated visualizations and statistical outputs
   - Refer to the markdown cells for explanations and interpretations

5. **Modify and Extend**:
   - Feel free to modify parameters, add new analyses, or apply the techniques to different datasets


## Future Work

1. **Machine Learning Models for Survival Prediction**:
   - Develop and evaluate machine learning algorithms (e.g., Random Survival Forests, Cox Proportional Hazards) to predict survival probabilities and identify key predictors.

2. **Treatment Efficacy and Comparative Analysis**:
   - Analyze the impact of various treatment regimens on survival rates and explore interactions with cancer stages or sites.
   - Compare findings with real-world data to validate the synthetic dataset's reliability.


