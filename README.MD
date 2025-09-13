

# 🚖 Urban Mobility Analysis – Ride Booking Trends & Insights

*Analyzing ride booking data to uncover customer behavior, driver performance, cancellations, payment trends, and overall efficiency using Python, SQL, and Power BI.*

---

## 📌 Table of Contents

* <a href="#overview">Overview</a>
* <a href="#business-problem">Business Problem</a>
* <a href="#dataset">Dataset</a>
* <a href="#tools--technologies">Tools & Technologies</a>
* <a href="#project-structure">Project Structure</a>
* <a href="#data-cleaning--preparation">Data Cleaning & Preparation</a>
* <a href="#exploratory-data-analysis-eda">Exploratory Data Analysis (EDA)</a>
* <a href="#research-questions--key-findings">Research Questions & Key Findings</a>
* <a href="#dashboard">Dashboard</a>
* <a href="#how-to-run-this-project">How to Run This Project</a>
* <a href="#final-recommendations">Final Recommendations</a>
* <a href="#author--contact">Author & Contact</a>

---

<h2><a class="anchor" id="overview"></a>Overview</h2>  

This project leverages **urban mobility booking data** to analyze patterns in ride success, cancellations, payment methods, and customer–driver ratings. Using Python for cleaning & analysis, SQL for structured queries, and Power BI/Seaborn for visualizations, the study identifies **reliability of vehicle types, cancellation behaviors, revenue trends, and service quality indicators**.

---

<h2><a class="anchor" id="business-problem"></a>Business Problem</h2>  

Ride-hailing platforms face challenges such as:

* High cancellation rates by drivers and customers
* Mismatched supply-demand for different vehicle types
* Revenue leakage due to failed or unpaid rides
* Reliability issues across vehicle segments (e.g., SUV vs Bike)
* Understanding driver & customer rating gaps

This project addresses these by analyzing large-scale booking data (\~100K+ rows) to optimize **revenue, ride reliability, and customer satisfaction**.

---

<h2><a class="anchor" id="dataset"></a>Dataset</h2>  

* **Bookings Data (\~103,000 rows):**
  Columns → Booking\_ID, Customer\_ID, Driver\_ID, Vehicle\_Type, Booking\_Status, Ride\_Distance, Ride\_Value, Payment\_Method, Driver\_Rating, Customer\_Rating, Booking\_Date

---

<h2><a class="anchor" id="tools--technologies"></a>Tools & Technologies</h2>  

* **Python (Pandas, NumPy):** Data cleaning, feature engineering, statistical analysis
* **Matplotlib & Seaborn:** Visualizations (EDA, categorical analysis, distribution plots)
* **SQL (MySQL):** Advanced queries for cancellations, top customers, average ride metrics
* **Power BI:** Interactive dashboards for stakeholders
* **Jupyter Notebook:** Step-by-step analysis and documentation
* **GitHub:** Version control & portfolio showcase

---

<h2><a class="anchor" id="project-structure"></a>Project Structure</h2>  

```
urban-mobility-analysis/
│
├── README.md
├
├
├── Urban_Mobility_Report.pdf
│
├── notebooks/                  
│   
│├── DATA  
│  
│
├── scripts/                    
│   
│     ├── booking_queries.sql
│   
│
├── dashboard/                  
│   └── urban_mobility_dashboard.pbix
│
├── data/                       
│   ├── bookings.csv
│   
|── Graphs/ 

```

---

<h2><a class="anchor" id="data-cleaning--preparation"></a>Data Cleaning & Preparation</h2>  

* Dropped duplicate & irrelevant rows (e.g., incomplete bookings)
* Handled missing values in `Driver_Rating` and `Customer_Rating`
* Standardized categorical values in `Booking_Status` and `Payment_Method`
* Converted dates into `Booking_Week`, `Booking_Month`, `Day_of_Week`
* Created new features:

  * `Profit_Per_KM = Ride_Value / Ride_Distance`
  * `Is_Cancelled = 1 if Booking_Status in [Cancelled_By_Customer, Cancelled_By_Driver]`

---

<h2><a class="anchor" id="exploratory-data-analysis-eda"></a>Exploratory Data Analysis (EDA)</h2>  

**Key Visualizations (Seaborn/Power BI):**

1. Booking Status by Vehicle Type → *booking\_status\_vehicle.png*
2. Ride Distance Distribution by Status → *ride\_distance\_status.png*
3. Booking Value by Payment Method → *booking\_value\_payment.png*
4. Driver vs Customer Ratings → *ratings\_comparison.png*

---

<h2><a class="anchor" id="research-questions--key-findings"></a>Research Questions & Key Findings</h2>  

1. **Which vehicles have the highest booking success?**
   → Bikes, Minis, and Sedans dominate successful rides; SUVs and eBikes show higher cancellations.

2. **What’s the distance pattern for cancellations?**
   → Cancelled rides mostly had `0 km` distance, likely canceled before start.

3. **Which payment methods dominate?**
   → Cash dominates low-value rides; UPI & Credit Cards dominate high-value ones.

4. **What about customer–driver rating alignment?**
   → Successful rides typically see ratings 3.5–5.0; cancelled rides often have missing/low ratings.

---

<h2><a class="anchor" id="dashboard"></a>Dashboard</h2>  

* **Power BI Dashboard Includes:**

  * Ride status distribution across vehicle types
  * Revenue trends by payment methods
  * Cancellation patterns over time
  * Ratings heatmap: Driver vs Customer satisfaction

```markdown
![Dashboard Screenshot](images/urban_mobility_dashboard.png)
```

---

<h2><a class="anchor" id="how-to-run-this-project"></a>How to Run This Project</h2>  

1. Clone the repository:

```bash
git clone https://github.com/Ankit-workbook/urban-mobility-analysis.git
```

2. Install dependencies:

```bash
pip install -r DATA
```

3. Run the Jupyter notebooks inside `/notebooks/`.
4. Open Power BI dashboard (`.pbix` file).

---

<h2><a class="anchor" id="final-recommendations"></a>Final Recommendations</h2>  

* **Vehicle Strategy:** Focus more on smaller vehicles (Bike, Mini) due to reliability and higher success rates.
* **Cancellation Mitigation:** Introduce penalties for repeated cancellations by drivers/customers.
* **Payment Optimization:** Incentivize digital payments to reduce cash-related failures.
* **Service Quality:** Improve SUV & eBike service reliability through better driver onboarding.

---

<h2><a class="anchor" id="author--contact"></a>Author & Contact</h2>  

**ANKIT YADAV**
Data Analyst
📧 Email: *[ankit005.ac@gmail.com](mailto:ankit005.ac@gmail.com)*
🔗 LinkedIn: *\[https://www.linkedin.com/in/ankityadav05/]*
🐙 GitHub: *\[https://github.com/Ankit-workbook/]*



