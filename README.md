# 🏋️ Gym Members Workout Analysis
Python · Pandas · NumPy · Plotly Express · EDA · Google Colab

---

## 📌 Overview

Most gym datasets tell you how many people showed up. This one goes deeper — analyzing 973 member records across 16 health and fitness features to find which workouts actually burn the most calories, how BMI distributes across the membership, and where age and experience intersect.

**Tech stack:**
- Python (Pandas, NumPy) — data cleaning, feature engineering
- Plotly Express — interactive visualizations
- Google Colab — development environment

---

## 🏗️ How it works
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

## 📊 Dataset

| Metric | Value |
|--------|-------|
| Total members | 973 |
| Age range | 18 — 59 years |
| Avg age | 38.7 years |
| Avg calories burned | 905.4 per session |
| Max calories burned | 1,783 per session |
| Min calories burned | 303 per session |
| Total calories burned | 8,80,976 |
| Avg BMI | 24.91 |
| Avg session duration | 1.26 hours |
| Avg water intake | 2.63 liters |
| Avg fat percentage | 24.98% |
| Avg workout frequency | 3.32 days/week |
| Avg max BPM | 179.9 |
| Avg resting BPM | 62.2 |
| Total features | 16 |

---

## 🧹 Data processing

**🔹 Data cleaning**
- Checked structure, shape, and missing values using df.info() and df.isnull().sum()
- Removed duplicate records using df.drop_duplicates()
- Converted data types — Age to int, Gender and Workout_Type to category

**🔹 Feature engineering**
- HRR (Heart Rate Reserve) = Max_BPM − Resting_BPM — fitness intensity indicator
- BMI Category — classified members into Underweight, Normal Weight, Overweight, Obese
- BMI Verification = Weight(kg) / Height(m)² — validated existing BMI values
- Calories per Hour = Calories_Burned / Session_Duration — efficiency metric
- Age Group — segmented into Young (20-30), Adult (31-40), Middle-aged (41-50), Senior (51+)

---

## 📈 Analysis

**🔹 Workout effectiveness (calories burned)**

| Workout type | Members | Avg calories | % of total |
|-------------|---------|-------------|------------|
| HIIT | 221 | 925.8 | 22.7% |
| Strength | 258 | 910.7 | 26.5% |
| Yoga | 239 | 903.2 | 24.6% |
| Cardio | 255 | 884.5 | 26.2% |

**🔹 BMI category distribution**

| BMI category | Members | % of total |
|-------------|---------|------------|
| Normal weight | 370 | 38.0% — largest group |
| Overweight | 243 | 25.0% |
| Obese | 192 | 19.7% |
| Underweight | 168 | 17.3% |

**🔹 Gender analysis**

| Gender | Members | Avg calories | Avg frequency |
|--------|---------|-------------|---------------|
| Male | 511 (52.5%) | 944.5 cal | 3.31 days/week |
| Female | 462 (47.5%) | 862.2 cal | 3.34 days/week |

**🔹 Age group vs experience level**

| Age group | Members | % | Avg experience |
|-----------|---------|---|----------------|
| Senior (51+) | 263 | 27.0% | 1.75 |
| Middle-aged (41-50) | 253 | 26.0% | 1.84 |
| Young (20-30) | 242 | 24.9% | 1.83 |
| Adult (31-40) | 215 | 22.1% | 1.82 |

**🔹 Experience level distribution**

| Level | Members |
|-------|---------|
| Level 1 (Beginner) | 376 |
| Level 2 (Intermediate) | 406 |
| Level 3 (Advanced) | 191 |

---

## 📊 Visualizations

| Chart type | Analysis |
|-----------|----------|
| Bar chart | Most effective workout type by calories burned |
| Bar chart | Gender vs workout frequency comparison |
| Pie chart | Workout type distribution (% of members) |
| Pie chart | Age group vs experience level |
| Histogram | BMI category distribution |
| Scatter plot | Age vs BMI relationship |

---

## 📈 Key findings

| Finding | Numbers | Note |
|---------|---------|------|
| Most effective workout | HIIT — 925.8 avg calories | Highest calorie burn per session |
| Largest BMI group | Normal weight — 370 members (38%) | Majority maintaining healthy BMI |
| Male vs female calories | 944.5 vs 862.2 | Males burn 9.5% more per session |
| Senior membership | 27% of total members | Largest age group in the dataset |
| Workout frequency | 3.32 days/week avg | Consistent 3-4 sessions weekly |
| Overweight + obese combined | 44.7% of members | Nearly half fall above healthy BMI |
| Advanced members | Only 191 (19.6%) at Level 3 | Most members are beginner or intermediate |

---

## 📂 File structure
```
Gym-Members-Workout-Analysis/
├── gym_data.ipynb
├── gymdata.xlsx
└── README.md
```

---

## 🚀 How to run

1. Open `gym_data.ipynb` in Google Colab or Jupyter Notebook
2. Upload `gymdata.xlsx` to your environment
3. Run all cells in order — data cleaning → feature engineering → EDA → visualizations
4. All charts are interactive — built with Plotly Express

---

## 🎯 Conclusions

The calorie burn gap between workout types is smaller than most people expect. HIIT leads at 925.8 calories per session, but Cardio — which many assume is the top calorie burner — sits last at 884.5. That's only a 41-calorie difference across four workout types. The ranking matters less than the consistency.

The BMI picture is worth paying attention to. 38% of members are at normal weight, which sounds healthy, but the flip side is that 44.7% fall into the overweight or obese categories. That's nearly half the membership. The workout frequency data shows these members are showing up (3.32 days/week on average), so the issue isn't attendance.

The gender calorie gap is real but probably explained by body composition rather than effort. Males burn 9.5% more calories per session (944.5 vs 862.2) despite females actually working out slightly more frequently (3.34 vs 3.31 days/week). Frequency isn't the variable that matters here.

Seniors making up 27% of the membership — the largest age group — is the most interesting demographic finding. It's not a typical gym profile and probably reflects something about this particular facility worth exploring further.
