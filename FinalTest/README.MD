#  Student Performance & Behavior Analysis Dashboard (Power BI)

##  Project Overview

This project presents an **interactive Power BI dashboard** designed to analyze student performance, attendance, and behavior across subjects, classes, and terms.

The dashboard enables users to **track academic trends, identify performance gaps, and explore student-level insights** through dynamic filtering and drillthrough features.

---

##  Objectives

* Analyze **student academic performance** across multiple subjects
* Track **attendance trends and impact on scores**
* Understand **behavior distribution patterns**
* Provide **interactive insights for decision-making**

---

##  Dataset Description

The dataset includes:

* Student ID & Name
* Class & Section
* Subject-wise Scores (English, Math, Science, etc.)
* Attendance %
* Term (Term 1, Term 2, Term 3)
* Behavior Type (Late, Disruptive, Helpful, etc.)

---

##  Data Preparation & Modeling

* Cleaned column names and corrected data types
* Handled missing/null values
* Created relationships between tables (Students, Scores, Behavior, Attendance)
* Structured data in a **star schema format**

---

##  DAX Measures Used

```
% Score = DIVIDE(SUM(Score), SUM(MaxScore))
Average Score = AVERAGE(Score)
Attendance % = AVERAGE(Attendance)
Total Students = DISTINCTCOUNT(StudentID)
Behavior Count = COUNT(BehaviorType)
Performance Category =
SWITCH(
    TRUE(),
    [% Score] >= 0.8, "High",
    [% Score] >= 0.5, "Medium",
    "Low"
)
```

---

##  Dashboard Features

###  KPI Cards

* Total Students: **1K**
* Average Attendance: **90.05%**
* Average Score: **49.96**

---

###  Visualizations

####  Bar Chart – Avg Score by Subject

* Compares performance across subjects
* Helps identify strong and weak subjects

####  Line Chart – Avg Score by Term

* Tracks performance trends over time
* Identifies improvement or decline

####  Donut Chart – Behavior Distribution

* Shows proportion of behavior types
* Helps understand student discipline patterns

####  Table – Student Performance

* Displays subject-wise scores
* Includes **conditional formatting**

---

##  Interactivity Features

###  Slicers

* Class
* Section
* Subject
* Term

 Enables dynamic filtering across all visuals

---

###  Drillthrough Page

* Individual **student profile view**
* Displays:

  * Subject-wise scores
  * Attendance
  * Total performance

---

###  Tooltips

* Mini insights on hover
* Shows additional metrics without clutter

---

###  Bookmark Navigation

* Toggle between:

  * Academic View
  * Behavioral View

---

##  Mobile Optimization

* Designed mobile-friendly layout
* Optimized visual arrangement for small screens

---

##  Key Insights

* Attendance is consistently high (~90%), but **average scores remain moderate (~50%)**
* Certain subjects like **Math show lower performance trends**
* Behavior distribution is evenly spread, indicating **balanced discipline patterns**
* Slight decline observed in **Term 2 performance**

---

##  Skills Demonstrated

* Data Cleaning & Transformation
* Data Modeling (Star Schema)
* DAX Calculations
* Data Visualization
* Dashboard Design
* Business Insight Generation

---

##  Conclusion

This dashboard provides a **comprehensive and interactive view of student performance**, enabling stakeholders to make **data-driven academic decisions** and identify improvement areas efficiently.

---

