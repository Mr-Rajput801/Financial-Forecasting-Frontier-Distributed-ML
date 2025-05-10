# 🏦 Banking Data Analysis with Hadoop and Hive


[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Contributions](https://img.shields.io/badge/contributions-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![Status](https://img.shields.io/badge/status-active-success.svg)]

## 📌 Overview
This project demonstrates a **comprehensive analysis of banking data** using **Hadoop's MapReduce framework** and **HiveQL queries**. The dataset includes **client demographics, account balances, loan statuses, and marketing campaign outcomes**. The analysis covers **data ingestion, transformation, aggregation, and advanced analytics** to uncover valuable business insights.

## 🚀 Key Features
✅ **Hadoop MapReduce Jobs** – Implemented in **Python** for large-scale data processing.  
✅ **Hive Data Warehouse** – Structured querying for efficient data analysis.  
✅ **Comprehensive Analytics** – Covers **statistics, trends, and correlations** in banking data.  
✅ **Practical Implementation** – Step-by-step execution with **real insights**.  
✅ **Data-Driven Decision Making** – Helps banks optimize marketing campaigns and customer strategies.  

## 📊 MapReduce Jobs & Insights
### 📌 **1️⃣ Average Balance by Job Type**
🔹 **Calculates the average account balance for different professions**.  
🔹 **Key Findings:**
- 🏦 **Retired clients** have the highest average balance (**₹2319**).
- 🎓 **Students** have moderate balances but **high subscription rates**.

### 📌 **2️⃣ Housing Loan Analysis**
🔹 **Counts clients with/without housing loans by education level**.  
🔹 **Key Findings:**
- 📚 **Secondary education clients** are **most likely** to have housing loans.

### 📌 **3️⃣ Monthly Campaign Analysis**
🔹 **Examines client interactions by month**.  
🔹 **Key Findings:**
- 📅 **May had the highest client contacts (1398)** but only **6.65% success rate**.
- 🌟 **August had fewer contacts but a better conversion rate**.

### 📌 **4️⃣ Age-Balance Relationship**
🔹 **Finds correlation between age and balance**.  
🔹 **Key Findings:**
- 📈 **Weak positive correlation (0.084)** between age and balance.
- 🎯 **Notable balance peaks** at ages **68 (₹11,753) and 70 (₹5,085)**.

## 📊 HiveQL Insights
### 📌 **1️⃣ Top Performers**
- 👴 **Retired married clients** have the **highest balances** (avg **₹71,188**).
- 🏢 **Management professionals** consistently show **high balances**.

### 📌 **2️⃣ Campaign Effectiveness**
- ✅ **Previous success outcomes yield a 64.34% subscription rate**.
- ❌ **Unknown outcomes only convert 9.1%**.

### 📌 **3️⃣ Contact Duration Impact**
- ⏳ **Subscribers had 2.4x longer contact duration (553s vs 226s)**.

### 📌 **4️⃣ Education Analysis**
- 📚 **Tertiary educated clients** are **most likely to default**.
- 📊 **Secondary education dominates** the client base (**58% of defaults**).

## 🛠 Technologies Used
- 🐘 **Hadoop** – Distributed storage & processing.
- 🐝 **Hive** – Data querying and analytics.
- 🐍 **Python** – MapReduce jobs.
- 📊 **Pandas & NumPy** – Data manipulation.
- 🔢 **Scikit-learn** – Statistical analysis.

## 🏗️ How to Run
### 📌 **Prerequisites**
✅ **Hadoop 3.3.6**  
✅ **Hive 3.1.2**  
✅ **Python 3.x**  

### 📌 **Execution Steps**
1️⃣ **Start Hadoop services**
```bash
start-dfs.sh
start-yarn.sh
```
2️⃣ **Load data into HDFS**
```bash
hdfs dfs -put bank.csv /input
```
3️⃣ **Run MapReduce jobs**
```bash
hadoop jar hadoop-streaming.jar -mapper mapper.py -reducer reducer.py -input /input -output /output
```
4️⃣ **Execute Hive queries** through **Hive CLI**
```sql
SELECT job, AVG(balance) FROM bank GROUP BY job;
```

## 📂 Dataset Description
The `bank.csv` dataset contains key fields including:
- 🏷 **Client demographics** (age, job, marital status, education)
- 💰 **Financial information** (balance, loans, defaults)
- 📞 **Marketing campaign details** (contact duration, outcomes)
- ✅ **Subscription status** for term deposits

## 📜 Findings Summary
### 📌 **Demographic Insights**
- 👵 **Average client age varies by profession** (26 for students to 61 for retirees).
- 💑 **Married clients dominate the dataset (56%)**.

### 📌 **Financial Patterns**
- 📈 **Balance generally increases with age** but has **fluctuations**.
- 🏠 **Housing loans are common among secondary-educated clients**.

### 📌 **Marketing Effectiveness**
- ⏳ **Longer contact durations** correlate with **higher conversions**.
- 📅 **May campaigns** reach most clients but **have lower success rates**.

### 📌 **Behavioral Trends**
- ✅ **Clients with previous successful outcomes** are **5x more likely to subscribe**.
- ❓ **Unknown campaign outcomes represent missed opportunities**.

## 🔮 Future Improvements
✅ **Improve predictive models** for campaign effectiveness.  
✅ **Enhance UI** for better data visualization.  
✅ **Implement real-time analytics** with Spark.  

## 👤 Author
**Ashish Rajput**  

---
📊 *A deep dive into banking data analytics using Hadoop & Hive!* 🚀
