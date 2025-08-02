## 📅 August 2, 2025

---

### 🧩 Project / Lab Title:
**Analyze Findings with Security Command Center**

📆 Date Completed:  
**August 2, 2025**

🔍 Objective:  
To learn how to operationalize security data by exporting findings from Security Command Center (SCC) into a continuous pipeline using Pub/Sub, and then ingesting that data into BigQuery for advanced, SQL-based analysis.

🔧 Tools/Services Used:
- Security Command Center (SCC)
- Pub/Sub
- BigQuery
- Google Cloud Console

🧠 What I Did:
- Explored the **Security Command Center (SCC)** dashboard to view and filter pre-existing security findings.
- Created a **Pub/Sub topic** to act as a messaging queue for exporting findings.
- Configured a **Continuous Export** in SCC to automatically send all new security findings to the newly created Pub/Sub topic in real-time.
- Created a **BigQuery dataset** to store the findings for analysis.
- Set up a **BigQuery subscription** to the Pub/Sub topic. This automatically created a table and began ingesting the findings from the Pub/Sub stream into BigQuery.
- Navigated to the BigQuery workspace and confirmed that the findings data was populating the table.
- Wrote and executed **SQL queries** against the findings data in BigQuery to perform custom analysis, such as counting the number of findings by severity or category.

🛡️ GRC / Compliance Relevance:  
✅ Critical  
This lab demonstrates a mature GRC practice: operationalizing security data for continuous monitoring and response.
- **Continuous Compliance Monitoring:** The SCC-to-BigQuery pipeline allows for the creation of dashboards and scheduled queries that continuously monitor the organization's compliance posture against security benchmarks and regulations.
- **Automated Incident Response (SOAR):** Exporting findings to Pub/Sub is the foundational step for Security Orchestration, Automation, and Response. A high-severity finding can trigger a Cloud Function to automatically remediate the issue (e.g., isolate a VM, revert a firewall rule).
- **Centralized Auditing & Reporting:** This pipeline enables the aggregation of security data into a central data warehouse (BigQuery). From there, custom reports can be generated for auditors, and the data can be integrated with enterprise-wide SIEM tools like Splunk or Chronicle.

🚩 Risks Identified:  
- **Incomplete Data Pipeline:** A misconfiguration in the export filter (in SCC), the Pub/Sub topic permissions, or the BigQuery subscription could break the data flow, leading to a critical blind spot where new security findings are not being analyzed.
- **Data Access Control:** The exported findings in the BigQuery dataset are sensitive. Improper IAM permissions on the dataset could allow unauthorized users to view the organization's security weaknesses.
- **Alert Fatigue:** Exporting all findings, including low-severity or informational ones, without proper filtering can create a noisy dataset. This can lead to "alert fatigue" where analysts may overlook critical alerts amongst the noise.

✅ What I Learned:
- **Security Command Center** is not just a dashboard; its findings can be programmatically accessed and exported.
- The standard pattern for creating a security data analysis pipeline is **SCC → Pub/Sub → BigQuery**.
- **Continuous Exports** in SCC allow for real-time streaming of findings as they are generated.
- **Pub/Sub** acts as a scalable, asynchronous messaging buffer between SCC and downstream services.
- **BigQuery** can subscribe directly to a Pub/Sub topic, making it easy to build a data lake for long-term security data retention and complex SQL analysis.

💭 Reflection:  
This lab was incredibly powerful. It showed me how to go beyond just passively looking at a security dashboard. Building the pipeline to get findings into BigQuery felt like I was creating a true security data platform. The ability to run SQL queries on security findings unlocks endless possibilities for custom dashboards, trend analysis, and automation. This is how I imagine a real Security Operations Center (SOC) would work—transforming raw security events into actionable intelligence and building automated responses. It’s a perfect example of how different GCP services can be composed to create a solution that is far greater than the sum of its parts.

---

## 🏆 Leaderboard Status (as of August 2, 2025)

| Metric                      | Value                                                                                                                                                             |
| --------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Arcade Username             | `ciril`                                                                                                                                                           |
| **---COMPLETED---** |                                                                                                                                                                   |
| Arcade Games lvl 1          | ✅ **Finished (12/12 Labs)** 🎉                                                                                                                                   |
| Trivia Week 1               | ✅ **Finished (4/4 Labs)** 🎉                                                                                                                                     |
| **---IN PROGRESS---** |                                                                                                                                                                   |
| Trivia Week 2               | ✅ Completed (2/3 Labs)                                                                                                                                           |
| Global Trivia Week 2 Rank   | **#8798** |
| Global Trivia Week 2 XP     | **48,483,791 XP** |
| **---OVERALL---** |                                                                                                                                                                   |
| Badges Earned               | [🏅 Week 1 Trivia Badge](https://www.cloudskillsboost.google/public_profiles/c8fd48a4-987d-4216-9635-d49fa00793da/badges/17140064), [🏆 Level 1 Game Badge](https://www.cloudskillsboost.google/public_profiles/c8fd48a4-987d-4216-9635-d49fa00793da/badges/17245038) |
| League Standing             | 7th – Silver League (1290 pts)                                                                                                                                    |
| Promotion Status            | 🟢 Gold League Promo                                                                                                                                              |
