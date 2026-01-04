# ✈️ Flight Delay & Operational Difficulty Analysis

**Exploratory Data Analysis | Airline Operations | United Airlines – SkyHack 3.0**

---

## 📌 Project Overview

Flight delays are one of the most critical challenges in aviation, directly affecting passenger satisfaction, airline costs, and operational efficiency. This project performs an **in-depth Exploratory Data Analysis (EDA)** on real-world airline operational data to uncover the **key drivers of flight delays** and assess operational complexity across routes and time periods.

The dataset was provided by **United Airlines** as part of their **SkyHack 3.0 Data Analytics Hackathon**, offering detailed insights into flight schedules, baggage handling, passenger services, and operational performance.

---

## 🎯 Objectives

* Analyze **operational and service-related factors** contributing to flight delays
* Study patterns in **flight difficulty, baggage handling, special service requests, and scheduling**
* Visualize daily operational trends and uncover correlations between performance metrics
* Generate **actionable, data-driven recommendations** to improve airline punctuality and efficiency

---

## 📊 Dataset Description

The dataset contains detailed flight-level and operational information, including schedules, delays, baggage handling, passenger services, and operational scoring metrics.

### Key Columns

| Category                   | Column Names                                                                                                         | Description                       |
| -------------------------- | -------------------------------------------------------------------------------------------------------------------- | --------------------------------- |
| **Flight Info**            | `FLIGHT_NUMBER`, `SCHEDULED_DEPARTURE_DATE_LOCAL`, `SCHEDULED_ARRIVAL_STATION_CODE`                                  | Flight identifiers and timing     |
| **Performance Metrics**    | `ARRIVAL_DELAY_MINUTES`, `DEPARTURE_DELAY_MINUTES`, `TURN_TIME_VIOLATION_FLAG`                                       | Delay and turnaround indicators   |
| **Passenger Services**     | `PEOPLE_OPTED_FOR_MANUAL_WHEELCHAIR`, `PEOPLE_OPTED_FOR_ELECTRIC_WHEELCHAIR`, `PEOPLE_OPTED_FOR_UNACCOMPANIED_MINOR` | Special service requests          |
| **Baggage Handling**       | `TOTAL_BAGS`, `TRANSFER_BAGGAGE`, `HOT_TRANSFER_BAGGAGE`                                                             | Luggage and transfer metrics      |
| **Operational Scores**     | `FLIGHT_DIFFICULTY_SCORE`, `GROUND_TIME_SCORE`, `BAGGAGE_SCORE`, `PASSENGER_SERVICE_SCORE`                           | Operational complexity indicators |
| **Passenger Demographics** | `TOTAL_PASSENGERS`, `TOTAL_BASIC_ECONOMY`, `TOTAL_STROLLER_USERS`, `TOTAL_LAP_CHILD`                                 | Passenger segmentation            |

---

## 🔄 Data Preprocessing & Feature Engineering

Prior to analysis, the dataset underwent structured cleaning and transformation:

* **Normalization:** Standardized column names (lowercase, consistent naming)
* **Missing Values:** Imputed or removed missing entries in delay and service-related fields
* **Data Types:** Converted date columns to `datetime`; enforced numeric types where applicable
* **Feature Engineering:**

  * Created **Total Special Services** (aggregated SSR metrics)
  * Categorized flights into **Easy / Medium / Hard** using Flight Difficulty Score
  * Engineered **Route** features (origin → destination)
  * Aggregated flight-level data into **daily operational summaries**

These steps ensured analytical consistency and reliable downstream insights.

---

## 🔍 Exploratory Data Analysis (EDA)

### 1️⃣ Flight Delay Trends

* Analyzed daily delayed flight counts to identify operational peaks
* **Highest delay volume observed on August 10 (382 delays)**
* Average daily delays ranged between **150–380 flights**, suggesting variability driven by congestion and external factors

---

### 2️⃣ Last-Minute Baggage Behavior

* Daily average of **50–80 last-minute checked bags**
* **Peak on August 9 (80 bags)** coincided with one of the highest delay counts
* Indicates a strong relationship between late baggage processing and flight delays

---

### 3️⃣ Flight Difficulty Score (FDS)

* Majority of flights clustered between **0.1–0.2**, indicating low operational complexity
* Very few high-difficulty flights (**FDS > 0.5**)
* Daily stacked bar charts showed **stable distribution** across Easy, Medium, and Hard flights

---

### 4️⃣ Passenger Service Usage

* **Airport wheelchair services dominated (~86%)** of all special service requests
* Manual wheelchairs (**7.1%**) and unaccompanied minors (**5.8%**) showed moderate usage
* Highlights heavy reliance on ground assistance and accessibility services

---

### 5️⃣ Passenger Demographics

* **Basic Economy** passengers formed the majority across all days
* Lap children and stroller usage remained stable, indicating consistent family travel patterns

---

## 🔗 Correlation Analysis

* Positive correlation between **Flight Difficulty Score and average arrival delay**
* Strong association between **transfer baggage load and ground time violations**
* Routes with higher operational complexity exhibited **greater delay variance**

---

## 📌 Key Findings

* Airport congestion, baggage inefficiencies, and tight ground schedules are primary delay drivers
* Last-minute operations (baggage, services) significantly impact departure punctuality
* Accessibility services add predictable—but manageable—boarding time extensions
* High FDS routes consistently experience longer delays, signaling operational strain

---

## 💡 Recommendations

### Operational Improvements

* Add buffer time for **high-complexity flights** during turnaround planning
* Deploy real-time ground tracking for baggage and boarding processes
* Use predictive delay modeling based on route, FDS, and operational load

### Passenger Handling

* Improve SSR management via **pre-scheduling and dedicated staffing**
* Streamline boarding flows for wheelchair and unaccompanied minor services

### Infrastructure Enhancements

* Invest in **automated baggage systems** and AI-driven logistics planning
* Use congestion heatmaps to redesign peak-hour slot allocations

### Data-Driven Planning

* Integrate historical delay patterns into flight scheduling algorithms
* Implement **Airport Collaborative Decision Making (A-CDM)** with ATC and airport ops

---

## 🛠️ Tools & Libraries

* **Python:** pandas, numpy
* **Visualization:** matplotlib, seaborn
* **Techniques:** GroupBy aggregations, correlation analysis, categorical binning, feature engineering

---

## 📈 Impact & Conclusion

This analysis demonstrates that **flight delays are largely driven by operational complexity, ground handling inefficiencies, and congestion effects**. By applying structured EDA and operational scoring, airlines can proactively identify high-risk flights and optimize resources.

**Estimated potential delay reduction:** **15–25%** across key routes through data-driven planning and operational improvements.


