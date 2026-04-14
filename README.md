# Kano State NCD Community Health Needs Assessment (CHNA)
### End-to-End Public Health Data Analytics · Hypertension & Diabetes Surveillance · 2021–2024

---

## Overview

This project delivers a full-cycle public health analytics pipeline for Non-Communicable Disease (NCD) surveillance across Kano State, Nigeria. It covers everything from raw data cleaning and transformation through to three interactive dashboards, a stakeholder report, and a validated digital data collection system designed to eliminate the quality problems found in the original dataset.

---

## The Critical Finding

> **42.8% of all diagnosed patients across all 15 LGAs are not receiving medication.**
>
> 8,364 individuals diagnosed with hypertension or diabetes are untreated. This gap is consistent across every LGA in the state, indicating a systemic failure in the healthcare treatment.

---

## Key Metrics

| Metric | Value |
|---|---|
| Total patients screened | 37,000 |
| Hypertension prevalence | 34.7% (12,854 diagnosed) |
| Diabetes prevalence | 27.9% (10,315 diagnosed) |
| Comorbidity — both conditions | 9.8% (3,613 patients) |
| Treatment gap | **42.8%** (8,364 of 19,556 untreated) |
| Sedentary / low activity | 65.3% (24,146 patients) |
| Average BMI | 26.5 — overweight range (WHO) |
| Current smokers | 15.0% (5,541 patients) |
| Average systolic BP (hypertensive) | 134.0 mmHg — Stage 1 Hypertension |
| Average fasting blood glucose (diabetic) | 7.2 mmol/L |
| LGAs covered | 15 of 15 |

---

## Dashboards

### Dashboard 1 — NCD Overview & Prevalence

Summary of overall NCD burden. Five KPI cards with dynamic sub-labels, a disease prevalence donut chart, diabetes and hypertension by age group, disease by sex, and a monthly disease trend spanning 2021–2024.

**Key finding:** No age group shows meaningfully different prevalence rates. A flat distribution from 18–35 through 66+ that contradicts standard epidemiological expectations and warrants investigation.

### Dashboard 2 — Risk Factor Analysis

Analytical dashboard covering the behavioural and clinical drivers of NCD prevalence. Shows average systolic BP and blood glucose by LGA, BMI category, and Smoking & Alcohol charts.

### Dashboard 3 — Geographic Analysis

LGA-level operational dashboard. Six dynamic KPI cards name specific LGAs: Nassarawa (highest hypertension rate — 36.6%), Wudil (highest overall diagnosed rate — 54.9%), Rano (worst treatment gap — 45.5%). Ranked treatment gap by LGA and disease burden by LGA charts, plus facility type composition breakdown.

**All three dashboards** share five cross-filtering slicers — LGA, Sex, Age Group, Facility Type, and Year of Visit. The slicers update every KPI card, sub-label, and chart simultaneously.

---

## Data Quality — Issues Found and Fixed

The raw dataset (37,370 records) required systematic cleaning before any analysis was possible. Every problem listed below traces back to manual data entry with no validation at the point of collection.

| Problem | Scale | Fix applied |
|---|---|---|
| LGA naming inconsistencies | 19 variants → 15 LGA names | Standardised to the actual name of the LGAs |
| Sex field variants | 7 variants (M, MALE, f, Man…) | Standardised to Male / Female |
| Date format inconsistencies | 4 different formats | Standardised to Short Date - Day/Month/Year |
| Age outliers | Values: −5, 999 | Nulled — valid range: 0–120 |
| Systolic BP outliers | Values: −20, 500 mmHg | Nulled — valid range: 70–300 mmHg |
| BMI outliers | Values: −10, 120 | Nulled — valid range: 10–80 |
| Medication field variants | 7 Yes/No variants | Standardised to Yes / No |
| Duplicate rows | 740 rows (370 confirmed pairs) | 370 removed — 37,000 clean records |

---

## Calculated Columns

Calculated columns were added to the cleaned dataset to enable the dashboard KPIs and charts.

---

## XLSForm for Kobocollect 

A validated digital data collection form was built to prevent every data quality problem found in the original dataset from occurring in future data collection rounds.
7 sections · 30+ questions · 90+ answer choices · English · Fully validated

Four fields are auto-calculated at collection time: Age Group, BP Classification, BMI Classification, and Condition Status. Eliminating the need for post-collection transformation steps.

---

## Recommendations

1. Close the Treatment Gap — Emergency Medication Access Program

2. Implement Capacity Building for Public Health Workers

3. Launch Targeted Counselling for Smoking & Alcohol Exposed Patients

4. Prioritize All LGAs – The NCD Burden is High in All LGAs

5. Deploy Digital Data Collection

6. Introduce Physical Activity and Intervention Across All LGAs

---

## Tools and Technologies

Microsoft Excel - Power Query

---

## Data Note

The dataset used in this project is a simulated and anonymised public health dataset designed to replicate real-world NCD surveillance challenges in a Nigerian state context. All patient records are de-identified.
