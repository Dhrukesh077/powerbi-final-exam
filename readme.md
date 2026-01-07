# 🎓 Student Performance Dashboard – Academic & Behavioral Insights (Power BI)

This repository contains a **comprehensive Power BI dashboard project** developed as part of a **Practical Final Exam for Power BI – Data Analysis & Data Science**.

The project focuses on analyzing **student academic performance, attendance, and behavioral patterns** using real-world structured data and advanced Power BI capabilities such as **data modeling, DAX measures, interactive visuals, drillthroughs, and storytelling**.

---

## 📸 Dashboard Preview

![Student Performance Dashboard](final-dashboard.png)

---

## 🏫 Project Context

- **Project Type:** Practical Examination  
- **Tool Used:** Microsoft Power BI Desktop  
- **Duration:** 2.5 – 3 Hours  
- **Total Marks:** 50  
- **Organization:** RED & WHITE Skill Education  

This project was evaluated on:
- Data Modeling & Cleaning
- DAX Calculations
- Visualizations & Storytelling
- Slicers, Filters & Drillthrough
- Optional Enhancements

---

## 🎯 Project Objective

The primary objective of this project is to design an **interactive and visually appealing Power BI dashboard** that enables stakeholders such as **teachers, administrators, and academic coordinators** to:

- Monitor student academic performance
- Analyze attendance patterns
- Track student behavior incidents
- Compare performance across subjects, classes, and terms
- Categorize students into performance bands (High / Medium / Low)
- Derive actionable insights to improve academic outcomes

---

## 🗂️ Dataset Overview

The project uses **four structured datasets**, each serving a specific analytical purpose.

### 1️⃣ Students Dataset (`Students.csv`)
Contains master information about students.

**Columns:**
- StudentID
- Name
- Gender
- Class
- Section

This table acts as the **primary dimension table** in the data model.

---

### 2️⃣ Scores Dataset (`Scores.csv`)
Contains academic performance data.

**Columns:**
- StudentID
- Subject
- ExamType
- Score
- MaxScore
- Term

This table is used to calculate:
- Average scores
- Percentage scores
- Performance trends
- Performance categories

---

### 3️⃣ Attendance Dataset (`Attendance.csv`)
Contains daily attendance records.

**Columns:**
- StudentID
- Date
- Status (Present / Absent)
- Reason

This dataset is used to analyze:
- Attendance percentage
- Attendance trends
- Correlation with academic performance

---

### 4️⃣ Behaviour Dataset (`Behaviour.csv`)
Contains behavioral incident records.

**Columns:**
- StudentID
- Date
- BehaviorType
- Notes

This dataset helps in:
- Identifying behavioral patterns
- Counting behavior incidents
- Analyzing impact on performance

---

## 🧱 Data Modeling Approach

A **Star Schema** data model was implemented to ensure optimal performance and clarity.

### ⭐ Model Design

- **Dimension Table:** Students
- **Fact Tables:** Scores, Attendance, Behaviour
- **Primary Key:** StudentID
- **Relationship Type:** One-to-Many
- **Cross Filter Direction:** Single

### 🔗 Relationships

| From Table | Column | To Table | Column |
|----------|--------|----------|--------|
| Scores | StudentID | Students | StudentID |
| Attendance | StudentID | Students | StudentID |
| Behaviour | StudentID | Students | StudentID |

This structure ensures:
- Accurate aggregation
- Efficient filtering
- Clean drillthrough functionality

---

## 🧹 Data Cleaning & Preparation

All datasets were cleaned using **Power Query**:

- Corrected data types
- Renamed columns for clarity
- Replaced null values in:
  - Attendance Reason → “Not Mentioned”
  - Behaviour Notes → “No Notes”
- Ensured consistency in StudentID formatting

---

## 📐 DAX Measures Created

All measures were organized inside a dedicated **Measures table**.

### 🔢 Core Measures

- Total Students  
- Total Score  
- Total Max Score  
- % Score  
- Average Score  
- Total Attendance  
- Present Count  
- Attendance %  
- Behavior Count  

---

### 🏷️ Performance Categorization

Students were classified using a **DAX SWITCH statement**:

- **High:** ≥ 80%
- **Medium:** ≥ 40%
- **Low:** < 40%

This categorization enables quick identification of at-risk students.

---

## 📊 Dashboard Visualizations

### 🔹 KPI Cards
- Total Students
- Total Attendance
- Average Score

These KPIs provide a **high-level overview** of overall performance.

---

### 🔹 Bar Chart – Average Score by Subject
- Compares subject-wise academic performance
- Helps identify strong and weak subjects

---

### 🔹 Donut Chart – Behavior Count by Type
- Displays distribution of behavior incidents
- Useful for behavior monitoring and intervention planning

---

### 🔹 Line Chart – % Score by Term
- Shows performance trends across terms
- Helps evaluate academic improvement or decline

---

### 🔹 Student Performance Table
Includes:
- Student Name
- Subject
- Score
- Percentage Score
- Performance Category

#### Conditional Formatting:
- 🟢 Green for scores > 80%
- 🔴 Red for scores < 40%

---

## 🎛️ Interactivity Features

### 🎚️ Slicers
- Subject
- Class
- Term

Allow users to dynamically filter the dashboard.

---

### 🔍 Drillthrough Page
A dedicated student-level drillthrough page includes:
- Individual performance
- Attendance %
- Behavior count

---

### 🧭 Tooltips
Custom tooltips were implemented to show **quick insights** without cluttering visuals.

---

### 🔖 Bookmarks
Used to toggle between:
- Academic view
- Behavioral view

Enhances storytelling and usability.

---

## 📱 Mobile Optimization (Optional Feature)

A mobile-friendly layout was created using **Power BI Mobile View**, ensuring usability on smaller screens.

---

## 💡 Key Insights Derived

- Students with **higher attendance consistently perform better**
- Frequent disruptive behavior is often linked to **lower academic scores**
- Performance varies slightly across terms, indicating opportunities for targeted intervention
- Certain subjects show consistent performance gaps across classes

---

## 📁 Repository Structure

powerbi-final-exam/
│
├── Final-exam.pbix
│   └─ Power BI report file containing:
│      - Data model
│      - DAX measures
│      - Visualizations
│      - Interactivity (slicers, drillthrough, tooltips)
│
├── raw-data.xlsx
│   └─ Raw dataset used for analysis, including:
│      - Students data
│      - Scores data
│      - Attendance data
│      - Behaviour data
│
├── final-dashboard.png
│   └─ Exported image of the final Power BI dashboard
│      - Used as preview image in README
│
└── README.md
    └─ Detailed project documentation including:
       - Project overview
       - Dataset description
       - Data modeling approach
       - DAX calculations
       - Dashboard features
       - Insights and outcomes


---

## 🚀 Tools & Technologies Used

- Microsoft Power BI Desktop
- Power Query
- DAX (Data Analysis Expressions)
- Git & GitHub

---

## 🧠 Learning Outcomes

Through this project, the following skills were strengthened:

- Real-world data modeling
- Writing optimized DAX measures
- Designing clean and aesthetic dashboards
- Applying business logic to data
- Presenting insights through storytelling

---

## 📌 Author

**Dhrukesh**  
Power BI | Data Analytics | Dashboard Design  

---

## ✅ Project Status

✔ Completed  
✔ Exam Ready  
✔ Portfolio Ready  

---


