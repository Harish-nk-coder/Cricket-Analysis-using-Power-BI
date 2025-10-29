# Cricket-Analysis-using-Power-BI
A Power BI-based cricket analytics project that identifies the world’s best 11 T20 players using data-driven parameters. It applies Power Query for cleaning, DAX for performance metrics, and interactive dashboards to build a balanced team capable of scoring 180+ and defending 150+

# 🏏 Codebasics Cricket Best 11 (Project Sportan)

## 📘 Project Overview
The **Codebasics Cricket Best 11** project, also known as **Project Sportan**, is a **data-driven cricket analytics dashboard** built using **Power BI**.  
The goal of this project is to identify the **best 11 T20 players in the world** based purely on **performance data and statistical analysis**, not opinions.

---

## 🎯 Objective
- To select a balanced **Best 11 T20 team** using player statistics.  
- The team should be able to:
  - Score **at least 180 runs on average**, and  
  - Defend **at least 150 runs on average**.  
- The selection process is automated and based on **data filtering and DAX calculations**.

---

## ⚙️ Tools and Technologies Used
| Tool | Purpose |
|------|----------|
| **Power BI** | Visualization, data modeling, dashboard design |
| **Power Query** | Data cleaning and transformation |
| **DAX (Data Analysis Expressions)** | Custom measures and KPIs |
| **Microsoft Excel** | Reference for calculated columns and DAX formulas |

---

## 📂 Project Files Description
| File Name | Description |
|------------|-------------|
| `t20_cric_1_power_query.pbix` | Power Query file for data cleaning and transformation |
| `Stage-2.pbix` | Intermediate Power BI model with relationships and role filters |
| `Stage-3.pbix` | Final dashboard with visuals and player comparisons |
| `Codebasics Cricket Best 11.pbix` | Integrated final Power BI report |
| `DAX Measures and Calculated columns.xlsx` | Contains all custom DAX measures |
| `Parameter Scoping.pdf` | Defines the selection criteria for each player role |
| `Codebasics_Cricket_Best_11_Presentation.pptx` | Project presentation slides |

---

## 🧩 Player Role Criteria (Parameter Scoping)

### **1. Openers**
- Batting Average > 30  
- Strike Rate > 140  
- Boundary % > 50  
- Batting Position < 4  
- Innings Batted > 3  

### **2. Anchors / Middle Order**
- Batting Average > 40  
- Strike Rate > 125  
- Avg. Balls Faced > 20  
- Batting Position > 2  

### **3. Finishers / Lower Order Anchors**
- Batting Average > 25  
- Strike Rate > 130  
- Avg. Balls Faced > 12  
- Bowled in at least 1 inning  

### **4. All-Rounders**
- Batting Average > 15  
- Strike Rate > 140  
- Bowling Economy < 7  
- Bowling Strike Rate < 20  

### **5. Specialist Fast Bowlers**
- Economy < 7  
- Bowling Average < 20  
- Strike Rate < 16  
- Dot Ball % > 40  
- Bowling Style contains "Fast"

---

## 🧮 DAX Measures Used
Some of the key calculated measures include:

```DAX
Batting Average = DIVIDE(SUM(Runs), COUNT(Innings))
Strike Rate = (SUM(Runs) / SUM(Balls)) * 100
Boundary % = ((SUM(Fours)*4 + SUM(Sixes)*6) / SUM(Runs)) * 100
Bowling Economy = DIVIDE(SUM(Runs Conceded), SUM(Overs))
Bowling Strike Rate = DIVIDE(SUM(Balls Bowled), SUM(Wickets))
