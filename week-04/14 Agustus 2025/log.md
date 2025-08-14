## 📅 August 14, 2025

---

### 🧩 Project / Lab Title:
**Dataplex: Qwik Start - Console**

📆 Date Completed:  
**August 14, 2025**

🔍 Objective:  
To understand the fundamental concepts of Dataplex by creating its core logical constructs: a Lake, a Zone, and an Asset. The goal was to learn how Dataplex provides a unified data fabric to discover, manage, and govern data across distributed storage systems.

🔧 Tools/Services Used:
- Dataplex
- Cloud Storage
- Google Cloud Console

🧠 What I Did:
- Enabled the **Dataplex API** to begin using the service.
- Created a **Dataplex Lake**, which serves as a top-level logical domain to organize data, for example, by business unit.
- Within the lake, I added a **Zone**, a sub-domain used to categorize data further (e.g., by its processing stage like "raw-zone" or "curated-zone").
- I **attached an Asset** to the zone, which in this lab was a Cloud Storage bucket. This crucial step brought the bucket under Dataplex's management without moving or duplicating the actual data.
- I observed that Dataplex automatically begins harvesting technical metadata from the attached asset.
- To complete the lifecycle exercise, I detached the asset and then deleted the zone and the lake to clean up the environment.

🛡️ GRC / Compliance Relevance:  
✅ Critical  
Dataplex is a strategic GRC tool designed to address the challenges of data governance at scale.
- **Centralized Data Governance & Cataloging:** Dataplex creates a unified catalog and management plane over data that can be physically spread across Cloud Storage and BigQuery. This centralized view is essential for GRC teams to understand the entire data landscape and apply consistent policies.
- **Data Lineage and Provenance:** By enabling the creation of zones like "raw", "curated", and "product", Dataplex helps organizations build a clear data lineage. This is critical for data quality audits and proving the provenance of data used in regulatory reporting.
- **Scalable Policy Enforcement:** Security policies, such as IAM permissions, can be applied at the Lake or Zone level and are automatically inherited by the assets within. This allows for consistent and scalable enforcement of access controls, which is a core tenet of data governance.

🚩 Risks Identified:  
- **Poor Taxonomy Design:** An illogical or poorly planned structure of Lakes and Zones can lead to confusion, misapplied security policies, and ultimately undermine the data governance model it's meant to support.
- **Metadata Latency:** There is a delay between data changes in the source asset and the reflection of those changes in the harvested metadata. Relying on the Dataplex catalog for real-time, instantaneous data state can be risky.
- **IAM Misconfiguration:** As with any control plane, improper IAM permissions on the Dataplex resources themselves (Lakes, Zones) can lead to unauthorized users being able to alter the data governance structure or discover sensitive data assets.

✅ What I Learned:
- **Dataplex** is an intelligent "data fabric" that does not store data itself but provides a unified governance and management layer over existing data in Cloud Storage and BigQuery.
- It manages data **"in-place"** by discovering and harvesting its **metadata**.
- The core logical constructs are **Lakes**, **Zones**, and **Assets**.
- This architecture is a key enabler for building a **data mesh**, where different business domains can own and manage their data assets within a centrally governed framework.

💭 Reflection:gsp1115
This lab was a real eye-opener, shifting my perspective from managing individual data silos to governing a cohesive "data fabric." The concept of creating a logical map (Lakes and Zones) over physical data without needing to move it is incredibly powerful. Dataplex feels like the "IAM for data"—a central control plane for defining what data you have, where it is, and who can use it, regardless of its underlying storage. For any large organization struggling with data sprawl, this service seems absolutely essential for building a trustworthy and well-governed data platform.

---

## 🏆 Leaderboard Status (as of August 14, 2025)

| Metric                              | Value                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| :---------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Arcade Username                     | `ciril`                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **---COMPLETED---** |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Arcade Games lvl 1 (Infrastructure) | ✅ **Finished (12/12 Labs)** 🎉                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Trivia Week 1 (July)                | ✅ **Finished (4/4 Labs)** 🎉                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Trivia Week 2 (July)                | ✅ **Finished (3/3 Labs)** 🎉                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Trivia Week 1 (August)              | ✅ **Finished (4/4 Labs)** 🎉                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **---IN PROGRESS---** |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Arcade Games lvl 1 (App Design)     | ✅ Completed (1/12 Labs)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Secure Data Lake Quest              | ✅ Completed (3/4 Labs)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **---OVERALL---** |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Badges Earned                       | [🏅 Week 1 Trivia Badge](https://www.cloudskillsboost.google/public_profiles/c8fd48a4-987d-4216-9635-d49fa00793da/badges/17140064), [🏆 Level 1 Game Badge](https://www.cloudskillsboost.google/public_profiles/c8fd48a4-987d-4216-9635-d49fa00793da/badges/17245038), [🏅 Week 2 Trivia Badge](https://www.cloudskillsboost.google/public_profiles/c8fd48a4-987d-4216-9635-d49fa00793da/badges/17274275), [🏅 August Week 1 Trivia Badge](https://www.cloudskillsboost.google/public_profiles/c8fd48a4-987d-4216-9635-d49fa00793da/badges/17423679) |
| League Standing                     | 11th – Gold League (140 pts)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Promotion Status                    | ⚪️ Stable                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
