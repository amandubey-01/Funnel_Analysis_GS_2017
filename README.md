# 🛒 E-commerce Funnel Analysis – Google Analytics Sample Dataset

This project analyzes the **user journey in an E-commerce store** using the Google Analytics Sample Dataset available on **BigQuery**. It focuses on identifying **conversion rates, drop-offs**, and **customer behavior patterns** across multiple funnel stages such as **landing**, **product view**, **add to cart**, and **purchase**.

---

## 📊 Objectives

- Analyze user sessions to understand conversion behavior
- Identify major **drop-off points** in the sales funnel
- Segment funnels by **traffic source**, **device type**, and **user type**
- Calculate **time taken** between funnel steps for deeper behavioral insights
- Explore **repeat interactions** and **high-intent behavior** among users

---

## 📁 Dataset

- **Source**: Google Analytics Sample Dataset on BigQuery  
- **Table Used**: `bigquery-public-data.google_analytics_sample.ga_sessions_20170801`  
- The dataset contains **website sessions** with nested fields such as hits, products, and transaction data.

---

##  Key Concepts Used

- `UNNEST()` & `STRUCT` to extract nested fields like products and page hits
- `WITH` clauses for **modular queries** and CTEs
- `LAG()` & `LEAD()` for analyzing **step transitions**
- `CASE WHEN`, `COUNT(DISTINCT)`, `GROUP BY`, and **conditional logic** to define funnel steps
- Funnel segmentation by **channelGrouping**, **deviceCategory**, and **userType**

---

## 🔍 Funnel Steps Defined

1. **Landing** (session started)
2. **Product View** (user viewed product detail page)
3. **Add to Cart**
4. **Purchase**

Each step is based on event actions tracked in nested hit fields. The analysis computes:

- **Step-wise conversion rate**
- **Drop-off percentage** at each stage
- **Average time** between steps
- **Behavior of returning users**

---

##  Insights Generated

- Majority of drop-offs occur **after product views** and before cart addition
- **Returning users** show higher conversion rates
- **Organic traffic** has a higher conversion efficiency than direct or referral
- Sessions with **shorter time gaps** between product view and cart addition are more likely to convert

---

## 📂 Folder Structure

├── SQL_queries/
│ ├── funnel_step_identification.sql
│ ├── funnel_conversion_rates.sql
│ ├── time_between_steps.sql
│ └── segmentation_analysis.sql
├── insights/
│ └── funnel_analysis_summary.pdf
├── README.md

yaml
Copy
Edit

---

## 🚀 Getting Started

To run this project:

1. Have access to **Google Cloud Platform (BigQuery)**.
2. Use the public dataset:  
   `bigquery-public-data.google_analytics_sample.ga_sessions_20170801`
3. Copy the SQL queries from the `/SQL_queries` folder into your BigQuery console and run them step-by-step.

---

## 🛠 Tools & Skills Used

- Google BigQuery
- SQL (Advanced)
- Google Analytics Data Structure
- E-commerce Funnel Metrics
- Session Analysis
- Behavioral Segmentation

---

## 📌 Author

**Aman Dubey**  
📫 [LinkedIn](https://www.linkedin.com/in/aman-dubey01) | [GitHub](https://github.com/amandubey-01)  

---

## ⭐️ If you find this helpful, feel free to star ⭐ the repo and fork 🍴 for your own use!
