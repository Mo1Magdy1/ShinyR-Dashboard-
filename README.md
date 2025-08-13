# 🩺 Cancer Survival Dashboard

![Dashboard](https://github.com/user-attachments/assets/632fcc9c-778c-4e83-854a-4b1f202b56b4)


**Interactive R Shiny app** for exploring cancer patient survival data with Kaplan–Meier curves, demographic filters, and interactive visualizations.

## 🚀 Key Highlights
- **Filter patients** by age & gender
- **Automatic p-value updates** – recalculated instantly based on current filter selections
- **Visual analytics**: gender split, intervention distribution, patient count gauge
- **Kaplan–Meier survival analysis** with p-values & confidence intervals
- **Risk tables** for survival analysis
- **Scatter plots** (Age vs. Survival Time)
- **Searchable patient table**
- **Real-time notification** when new patient data is loaded

## 📂 Data Requirements
CSV file: `cancer_survival.csv` with:
- `time` – Survival time (days)
- `status` – 1 = alive, 2 = deceased (auto-converted to 0/1)
- `intervention` – `Standard_Care` / `Drug`
- `age` – Age in years
- `sex` – 1 = Male, 2 = Female

*(Sample data is generated automatically if CSV is missing)*

## 🛠 Quick Start
```r
install.packages(c(
  "shiny", "shinydashboard", "survival", "DT", "flexdashboard",
  "survminer", "ggplot2", "dplyr", "tidyverse", "ggforce", "scales"
))
shiny::runApp("path_to_app_folder")
