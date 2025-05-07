
# 📊 **Safety Intelligence Dashboard Using OSHA Injury Narratives & NLP**

## 📑 **Project Description**
This project applies **Natural Language Processing (NLP)** and **predictive modeling** to analyze safety risks using **OSHA injury narratives** and **machine-related safety data**. The goal is to develop a **Safety Intelligence Dashboard** for SEG, providing businesses with actionable insights to reduce workplace injuries. The analysis explores trends, safety risks, and predicts future incidents.

---

## 📂 **Dataset Information**
- **Source**: Internal OSHA data / Hand Injuries with Machines dataset 
- **Description**: The dataset contains information about workplace injuries, with a focus on hand injuries and their connection to machinery. Key fields in the dataset include:
  - **Injury Type**: Type of injury (e.g., hand, arm)
  - **Machine Type**: Type of machine associated with the injury
  - **Injury Severity**: Severity level of the injury (e.g., minor, severe)
  - **Machine Usage**: Frequency of machine use during incidents
- **Tools Used**: Power BI for dashboard creation, Python (Pandas, NLP) for data analysis

---

## **Objectives**
1. Analyze OSHA injury narratives using NLP to uncover common injury patterns.
2. Answer business-critical questions, such as:
   - Which machines are most frequently associated with hand injuries?
   - What is the correlation between machine types and injury severity?
   - Can NLP provide insights into improving safety protocols?
3. Build predictive models for identifying high-risk safety scenarios.
4. Generate actionable recommendations for reducing injury rates.

---

## 🔍 **Exploratory Data Analysis (EDA)**

### **SQL Queries and Insights**

#### 1. **Exploratory Data Analysis**

- **Number of Unique Machines**:
  ```sql
  SELECT COUNT(DISTINCT(machine_id)) AS uniqueMachines
  FROM HandInjuryData;
  ```
  **Result**: 500 unique machines.

---

- **Missing Values Check**:
  ```sql
  SELECT COUNT(*) AS MissingValues 
  FROM HandInjuryData 
  WHERE injury_type IS NULL OR machine_type IS NULL OR injury_severity IS NULL;
  ```
  **Result**: No missing values in key fields.

---

- **Number of Incidents per Machine**:
  ```sql
  SELECT machine_type, COUNT(DISTINCT incident_id) AS NoOfIncidents
  FROM HandInjuryData
  GROUP BY machine_type
  ORDER BY NoOfIncidents DESC;
  ```
  **Insight**: Machines such as forklifts and presses are most commonly associated with hand injuries.

---

#### 2. **Analysis of Injury Severity**

- **Overview of Injury Severity**:
  ```sql
  SELECT MIN(injury_severity) AS Min_Severity,
  MAX(injury_severity) AS Max_Severity,
  AVG(injury_severity) AS Avg_Severity
  FROM HandInjuryData;
  ```
  **Result**:
  - Minimum Severity: 1 (Minor)
  - Maximum Severity: 5 (Severe)
  - Average Severity: 2.8 (Moderate)

---

- **Machine Type vs Injury Severity**:
  ```sql
  SELECT machine_type, AVG(injury_severity) AS Avg_Severity
  FROM HandInjuryData
  GROUP BY machine_type
  ORDER BY Avg_Severity DESC;
  ```
  **Insight**: Some machine types (e.g., presses) are linked to higher severity injuries.

---

#### 3. **Additional Insights**

- **NLP Analysis of Injury Descriptions**:
  ```sql
  SELECT machine_type, LENGTH(injury_description) AS Description_Length, AVG(injury_severity) AS Avg_Severity
  FROM HandInjuryData
  GROUP BY machine_type;
  ```
  **Insight**: Longer injury descriptions often correlate with more severe injuries.

---

## **Final Recommendations**
1. **Focus on High-Risk Machines**: Pay attention to machines with high incident rates, such as presses and forklifts.
2. **Use NLP to Enhance Safety Protocols**: Injury narratives provide valuable insights that can be used to refine safety measures.
3. **Training for High-Injury Machines**: Offer specialized safety training for workers using high-risk machinery.
4. **Machine Safety Enhancements**: Consider adding more safety features to machines associated with high-severity injuries.
5. **Improve Descriptions**: Encourage more detailed injury descriptions, as they often correlate with better safety insights.

---

## 🛠 **Tools and Technologies**
- **SQL Database**: SQLite
- **Query Tool**: SQLiteOnline
- **NLP Tool**: Python (NLTK, spaCy)
- **Visualization**: Power BI
- **Dataset Source**: Internal Data / Hand Injuries with Machines Dataset

---

## 📬 **Contact**
- **Author**: Subham Mangi  
- **Email**: [subham.mangi@utdallas.edu](mailto:subham.mangi@utdallas.edu)  
- **GitHub**: [SUBHAMMANGI](https://github.com/SUBHAMMANGI)
