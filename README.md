# 🏋️ Gym Members Workout Analysis
### Python | Pandas | NumPy | Plotly Express | EDA | Google Colab

---

## 📌 Project Overview

An Exploratory Data Analysis (EDA) project analyzing **973 gym member records across 16 health and fitness features** — uncovering workout effectiveness, BMI distribution, calorie burn efficiency, and age-based fitness trends using Python and Plotly.

**Tech Stack:**
- **Python** (Pandas, NumPy) — Data Cleaning, Feature Engineering
- **Plotly Express** — Interactive Visualizations
- **Google Colab** — Cloud Development Environment

---

## 🏗️ Project Architecture

```
Raw Dataset (973 records | 16 features)
        ↓
Python (Data Cleaning + Duplicate Removal)
        ↓
Feature Engineering (HRR, BMI Category, Calories/Hour, Age Group)
        ↓
EDA (Workout + BMI + Gender + Age Analysis)
        ↓
Plotly Visualizations (Bar, Pie, Histogram, Scatter)
        ↓
Business Insights & Fitness Recommendations
```

---

## 📊 Dataset Overview

| Metric | Value |
|--------|-------|
| Total Members | 973 |
| Age Range | 18 — 59 years |
| Avg Age | 38.7 years |
| Avg Calories Burned | 905.4 per session |
| Max Calories Burned | 1,783 per session |
| Min Calories Burned | 303 per session |
| Total Calories Burned | 8,80,976 |
| Avg BMI | 24.91 |
| Avg Session Duration | 1.26 hours |
| Avg Water Intake | 2.63 liters |
| Avg Fat Percentage | 24.98% |
| Avg Workout Frequency | 3.32 days/week |
| Avg Max BPM | 179.9 |
| Avg Resting BPM | 62.2 |
| Total Features | 16 |

---

## 🧹 Data Processing Steps

### 🔹 Data Cleaning
- Checked dataset structure, shape, and missing values using df.info() and df.isnull().sum()
- Removed duplicate records using df.drop_duplicates()
- Converted data types — Age to int, Gender and Workout_Type to category

### 🔹 Feature Engineering
- **HRR (Heart Rate Reserve)** = Max_BPM − Resting_BPM — fitness intensity indicator
- **BMI Category** — classified members into Under Weight, Normal Weight, Over Weight, Obese
- **BMI Verification** = Weight(kg) / Height(m)² — validated existing BMI values
- **Calories per Hour** = Calories_Burned / Session_Duration — efficiency metric
- **Age Group** — segmented members into Young (20-30), Adult (31-40), Middle-aged (41-50), Senior (51+)

---

## 📈 Key Analysis Performed

### 🔹 Workout Effectiveness (Calories Burned)

| Workout Type | Members | Avg Calories | % of Total |
|-------------|---------|-------------|------------|
| HIIT | 221 | 925.8 | 22.7% |
| Strength | 258 | 910.7 | 26.5% |
| Yoga | 239 | 903.2 | 24.6% |
| Cardio | 255 | 884.5 | 26.2% |

### 🔹 BMI Category Distribution

| BMI Category | Members | % of Total |
|-------------|---------|------------|
| Normal Weight | 370 | 38.0% — Largest group |
| Over Weight | 243 | 25.0% |
| Obese | 192 | 19.7% |
| Under Weight | 168 | 17.3% |

### 🔹 Gender Analysis

| Gender | Members | Avg Calories | Avg Frequency |
|--------|---------|-------------|---------------|
| Male | 511 (52.5%) | 944.5 cal | 3.31 days/week |
| Female | 462 (47.5%) | 862.2 cal | 3.34 days/week |

### 🔹 Age Group vs Experience Level

| Age Group | Members | % | Avg Experience |
|-----------|---------|---|----------------|
| Senior (51+) | 263 | 27.0% | 1.75 |
| Middle-aged (41-50) | 253 | 26.0% | 1.84 |
| Young (20-30) | 242 | 24.9% | 1.83 |
| Adult (31-40) | 215 | 22.1% | 1.82 |

### 🔹 Experience Level Distribution

| Level | Members |
|-------|---------|
| Level 1 (Beginner) | 376 |
| Level 2 (Intermediate) | 406 |
| Level 3 (Advanced) | 191 |

---

## 📊 Visualizations Used

| Chart Type | Analysis |
|-----------|----------|
| Bar Chart | Most effective workout type by calories burned |
| Bar Chart | Gender vs workout frequency comparison |
| Pie Chart | Workout type distribution (% of members) |
| Pie Chart | Age group vs experience level |
| Histogram | BMI category distribution |
| Scatter Plot | Age vs BMI relationship |

---

## 📈 Key Business Insights

| Finding | Metric | Insight |
|---------|--------|---------|
| Most Effective Workout | HIIT — 925.8 avg calories | Best for calorie burn efficiency |
| Largest BMI Group | Normal Weight — 370 members (38%) | Majority maintaining healthy BMI |
| Male vs Female Calories | 944.5 vs 862.2 | Males burn 9.5% more calories per session |
| Senior Experience | 27% of members are Seniors | Experience grows with age |
| Workout Frequency | 3.32 days/week avg | Members workout 3-4 times weekly |
| High BMI Risk | 19.7% Obese + 25% Overweight = 44.7% | Nearly half need fitness intervention |
| Advanced Members | Only 191 (19.6%) at Level 3 | Large beginner and intermediate base |

---

## 📂 File Structure

```
📁 Gym-Members-Workout-Analysis
├── gym_data.ipynb       # Python EDA notebook
├── gymdata.xlsx         # Raw dataset (Excel)
└── README.md            # Project documentation
```

---

## 🚀 How to Use

1. Open **gym_data.ipynb** in Google Colab or Jupyter Notebook
2. Upload **gymdata.xlsx** to your environment
3. Run all cells sequentially — data cleaning → feature engineering → EDA → visualizations
4. All charts are interactive — built with Plotly Express

---

## 🎯 Conclusion

This project analyzes **973 gym member records** to uncover that:
- 💪 **HIIT burns the most calories** at 925.8 avg per session — most efficient workout type
- ⚖️ **44.7% of members are Overweight or Obese** — significant fitness intervention opportunity
- 👨 **Males burn 9.5% more calories** (944.5 vs 862.2) despite similar workout frequency
- 🧓 **Seniors (27%) lead in membership count** — experience grows with age confirmed
- 📊 **Normal Weight members (38%)** form the largest BMI group — healthy majority base
