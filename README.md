# Financial-Analysis-PBI

## Table of Contents

1. [📌  Overview](#-overview)  
2. [📂 Dataset & Data Model](#-dataset--data-model)  
3. [🧠 Design Thinking Process](#-design-thinking-process)  
4. [📊 Key Insights & Visualizations](#-key-insights--visualizations)  
5. [🔎 Final Conclusion & Recommendations](#-final-conclusion--recommendations)
---

## 📌 Overview

### Project Overview
This project focuses on analyzing corporate financial data for the year 2023 using Power BI. 
By building an interactive financial dashboard, it provides a comprehensive visualization of the company's financial health.

### Problem Statement

* **Track Profitability Flow:** Clearly map out the exact journey from total revenue to final net profit.
* **Analyze Cost Structures:** Identify which specific expense categories are consuming the largest portions of the budget.
* **Evaluate Performance:** Compare the financial efficiency of different business lines over time to support strategic and operational decisions.

### Core Business Questions
To solve this problem, the dashboard was designed to answer three critical financial questions:
* **The Profit Bridge:** What is the exact path from Gross Revenue down to Net Profit, and which major expense categories (COGS vs. Opex) are putting the most pressure on our margins?
* **Segment Profitability:** Among our core business lines (Sportswear, Sports Equipment, and Nutrition), which are the true "cash cows" driving profit, and which are operating at a loss?
* **Operational Efficiency:** How do our total expenses trend month-over-month compared to revenue growth, and where can we optimize costs ?

## 📂 Dataset & Data Model
The dataset (`Financial_analysis_dataset.xlsx`) contains the core financial data:
* **`revenue_expense`:** Raw transaction-level data including Date, Amount, Category (Revenue/Expense), Subgroup, and Business Line.
* **`dictionary`:** A reference sheet explaining the definitions and hierarchies of the financial categories used in the dataset.

### Data Model
This project utilizes a Star Schema architecture to ensure performance and analytical flexibility in Power BI.
One main Fact table tracks all financial transactions (revenue and expenses).
This connects to shared Dimension tables for dates (`Calendar`), categories (`Dim_category`, `Dim_SubGroup`), and business units (Dim_Business_line).
<img width="976" height="567" alt="image" src="https://github.com/user-attachments/assets/172d5f08-81c5-4017-a661-b277d1f8ea64" />

## 🧠 Design Thinking Process
To ensure this dashboard delivers real business value rather than just displaying raw numbers, I applied a structured Design Thinking approach. This helped bridge the gap between technical data modeling and the actual needs of the business stakeholders (CFOs & Finance Managers).

### 1️⃣ Empathize (5W1H Problem Statement)
| Dimension | Question | Core Finding |
| :--- | :--- | :--- |
| **WHO** | Who is experiencing the problem? | CFOs, Finance Managers, and Business Unit Directors. |
| **WHAT** | What is the exact issue? | Inability to trace the exact flow of revenue down to net profit and identify root causes of profit leaks (COGS/Opex). |
| **WHY** | Why does it matter? | To stop bleeding cash on unprofitable segments and optimize operational costs to protect the overall margin. |
| **WHEN / WHERE** | When do they need this data? | During monthly/quarterly financial reviews and strategic budget planning sessions. |
| **HOW** | How will this dashboard help? | By providing a centralized, interactive view of Profit Bridges and detailed cost breakdowns to enable fast decisions. |

### 2️⃣ Define Point of View (POV)
* **North Star Metrics:** **Net Profit** & **Net Profit Margin %**.
* **Key Analytical Perspectives:**
    * **Macro (Profit Bridge):** Tracking how Gross Revenue is consumed by COGS and Opex to result in Net Profit.
    * **Segment Level (Business Lines):** Pinpointing which business units are generating profit versus bleeding cash.
    * **Operational Level (Expense Subgroups):** Monitoring granular cost drivers (Labor, Materials, Packaging) over time.

### 3️⃣ Ideate (Dashboard Information Architecture)
To avoid overwhelming the users, I structured the dashboard into three distinct pages based on the level of detail required for decision-making:

| Information Tier | Page 1: Overview | Page 2: Analysis | Page 3: Operational Details |
| :--- | :--- | :--- | :--- |
| **Critical Info (Top KPIs & Core Visuals)** | Total Revenue, Total Expense, Net Profit, NP Margin % | Profit Decomposition Tree (Net Profit ➔ Business Line ➔ Category ➔ Qtr ➔ Month) | Dynamic Financial Performance Matrix (with Margin Status Indicators) |
| **Important Info (Trends & Breakdowns)** | Revenue to Net Profit Bridge (Waterfall), Revenue by Category, Qtr/Month Trends | Revenue & Expense by Business Line, Business Unit Performance | Total Expense MoM % by Subgroup, Total Expense by Month and Expense Subgroup |

## 📊 Key Insights & Visualizations  

### 🔍 Dashboard Preview  

#### 1️⃣ Dashboard 1 Preview  
<img width="1237" height="698" alt="image" src="https://github.com/user-attachments/assets/95223927-29ae-4b3a-a026-712ebeba11bf" />
* **Observation:** The company show Total Revenue reaching $17.6M and  Net Profit Margin of 24.6%. However, the Revenue to Net Profit Bridge (Waterfall chart) shows the revenue is consumed by COGS ($7M) and Opex ($6M), heavily low down to a final Net Profit of $4.3M.
* **Recommendation:** Since COGS and Opex account for over 69% of total revenue, the operations team must to audit internal inefficiencies. Optimizing these two major cost buckets by just 5% will significantly scale the final net profit.

#### 2️⃣ Dashboard 2 Preview 
<img width="1236" height="705" alt="image" src="https://github.com/user-attachments/assets/f2ce705b-9f2b-4e98-9c17-ebbf14d36790" />
* **Observation:** While "Sports Equipment" generates high revenue volume, the true profit engine is "Sportswear", delivering  $2.74M in Net Profit. Also, the "Nutrition" segment is lost -$0.71M.
* **Recommendation:** Need financial audit into the "Nutrition" cost. If the -$0.71M loss cannot be reversed through cost-cutting, leadership should consider pausing this segment. Also, reallocate capital to scale the highly efficient "Sportswear" division.

#### 3️⃣ Dashboard 3 Preview  
<img width="1249" height="698" alt="image" src="https://github.com/user-attachments/assets/ccf652e6-a209-4529-90f0-a884f804ea43" />
* **Observation:** When breaking down these costs, the bar chart explicitly shows that  Labor is the most massive expense subgroups, outweighing other operational costs.
* **Recommendation:** Implement stricter budget caps and monthly tracking  specifically for Labor.

## 🔎 Final Conclusion & Recommendations

📌 Key Takeaways:

* **Heavy Cost Burden:** Top-line revenue is strong ($17.6M), but operational costs (COGS and Opex) consume over 69% of it. The company maintains a 24.6% profit margin, but it is heavily pressured by these expenses.

* **Winner vs Loser Segment:** The "Sportswear" division is the ultimate profit engine ($2.74M Net Profit), while the "Nutrition" segment is actively bleeding cash (-$0.71M loss).

* **Top Expense Drivers:** The  analysis proves that Labor í the most operational expenses.

🚀 Key Actions:

* **Stop the Bleed:** Conduct a  financial audit on the "Nutrition" division. If costs cannot be cut, pause this segment to protect the total company profit.

* **Focus on Stars** Reallocate capital and strategic focus toward the highly efficient "Sportswear" line to maximize overall Return on Investment.

* **Control Key Costs:** Implement strict monthly budget caps and ROI tracking specifically for the Labor departments to prevent further margin erosion.
