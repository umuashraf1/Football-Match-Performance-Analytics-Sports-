# Football-Match-Performance-Analytics-Sports-
This  repository  is on Capstone Project for group 3, Hagital Data Engineering Boothcamp

## **Team**
1. Ganiyat Adebayo
2. Taiwo Ayeni
3. Adetona Oluwasemilore

## **Project Overview**

The **Football Match Performance Analytics** project focuses on building an end-to-end analytics pipeline for football matches. It involves extracting live match and player data, processing the data to generate insights, storing it in a structured database, and visualizing the results in **Grafana**.

---

## **Data Source**

* **API Provider:** [API-Football](https://www.football-data.org))
* **Authentication:** Requires a free API key
* **Data Retrieved:**

  * Match fixtures & results
  * Player stats
  * League standings
  * Team performance data

---

## **Deliverables**

### **1. Python ETL Script**

* Fetches match and player statistics from **API-Football**.
* Cleans and transforms data.
* Calculates:

  * **Possession %**
  * **Pass accuracy**
  * **Player performance scores**.

### **2. PostgreSQL Schema**

Database designed to store football data efficiently.

**Tables:**

* **teams** → team details
* **matches** → match fixtures & results
* **players** → player details
* **stats** → performance metrics

### **3. Grafana Dashboard**

Three primary dashboards were created:

#### **a) League Standings**

Shows the latest positions, points, wins, draws, and losses.

![League Standings] <img width="1366" height="768" alt="league standing (grafana)" src="https://github.com/user-attachments/assets/3b3e58a2-2f64-4cb0-8c5e-0342bead4edd" />


🔗 **Live Dashboard:** [League Standings](http://localhost:3000/dashboard/snapshot/lvo56F1EunZMyQIvNjCb89H8KpgGA9rO)

---

#### **b) Player Performance Heatmaps**

Visualizes player performance scores based on position and activity.

![Player Performance]<img width="1288" height="565" alt="player performance board(grafana)" src="https://github.com/user-attachments/assets/bc759198-3d66-4ec5-bf2d-0930f08e0db2" />


🔗 **Live Dashboard:** [Player Performance](http://localhost:3000/dashboard/snapshot/QUNYvMHTmIFlZVHgByyzxRzYLBFzfBJN)

---

#### **c) Match Outcome Predictions**

Displays probability-based match result predictions.

![Match Outcome Predictions]<img width="1304" height="572" alt="match outcome prediction (grafana)" src="https://github.com/user-attachments/assets/5b6727d0-0490-447f-bf5b-d2b33f56dc15" />

🔗 **Live Dashboard:** [Match Outcome Predictions](http://localhost:3000/dashboard/snapshot/zc0SAllWsWBwUXNVxEULv4V2EteUxqKo)

---

## **Implementation Workflow**

1. **Data Extraction** → football-api.org API.
2. **Data Transformation** → Python ETL pipeline.
3. **Data Storage** → PostgreSQL database.
4. **Data Visualization** → Grafana dashboards.

---

## **Challenges and Solutions**
1. API Limitations

Issue: The initial API (API-Football) restricted access to detailed player stats due to free subscription limits.

Solution: Switched to football-data.org, which provided wider coverage for matches, players, and standings.

2. Data Transformation Complexity

Issue: Calculating possession %, pass accuracy, and performance scores required aggregating multiple datasets.

Solution: Built custom Python functions to clean, normalize, and merge datasets for accurate analysis.

3. Grafana Integration

Issue: Grafana works best with real-time or structured data, while our API data was fetched in batches.

Solution: Created optimized PostgreSQL views and queries to simulate real-time match stats for smooth dashboard visualization.

4. Team Collaboration

Issue: Out of the entire group, only three members actively contributed to the project.

Solution: Maintained smooth collaboration through Discord and we also introduced Whatsapp group call and chat.

Lessons Learned

API Selection Matters – Free APIs often have data limitations; switching to a better API early saves time.

Data Transformation is Crucial – Clean, structured data leads to better insights and smoother dashboards.

Grafana Needs Optimized Data – Pre-aggregating stats in PostgreSQL makes dashboards load faster and look cleaner.

Collaboration is Key – Clear role assignments improved efficiency and avoided duplication of tasks.

## **Next Steps**

* Automate ETL jobs using **Airflow** .


---

## **Project Status**

✅ Data pipeline working.
✅ PostgreSQL database live.
✅ Grafana dashboards created.
🚀 Next phase: Authomate with Airflow.


