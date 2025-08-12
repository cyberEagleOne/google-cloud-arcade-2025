## 📅 August 12, 2025

---

### 🧩 Project / Lab Title:
**Cloud IAM: Qwik Start**

📆 Date Completed:  
**August 12, 2025**

🔍 Objective:  
To understand the fundamental principles of Cloud Identity and Access Management (IAM) by granting and revoking roles for different users. The goal was to experience firsthand the difference in permissions between a Project Owner and a Viewer role.

🔧 Tools/Services Used:
- Google Cloud Console
- Cloud IAM & Admin
- Incognito Mode (for multi-user testing)

🧠 What I Did:
- As the default **Project Owner**, I navigated to the **IAM & Admin** section of the Cloud Console.
- I added a second user account (a new **principal**) to the project's IAM policy.
- I assigned the predefined **Viewer** (`roles/viewer`) role to this second user, intentionally granting them limited, read-only permissions.
- Using an **Incognito window**, I logged in with the second user's credentials to simulate a different person accessing the project.
- As the "Viewer", I verified that I could see resources but was correctly denied permission when attempting to create, modify, or delete anything.
- I switched back to my "Owner" account and removed the Viewer role from the second user, effectively **revoking their access**.

🛡️ GRC / Compliance Relevance:  
✅ Critical  
This lab is the absolute foundation of Governance, Risk, and Compliance (GRC) in any cloud environment, especially for a data lake which holds an organization's most valuable data.
- **Principle of Least Privilege (PoLP):** This is a direct demonstration of PoLP. For a data lake, this means data scientists might only have read access to certain datasets, while data engineers have write access, and no one has delete permissions on raw data buckets.
- **Segregation of Duties (SoD):** Using different roles prevents a single user from having excessive power. An analyst who can read data should not also be able to change the permissions on that data.
- **Access Control & Auditing:** The entire process of managing IAM roles is the primary subject of access control audits for compliance frameworks like SOC 2, HIPAA, and GDPR.

🚩 Risks Identified:  
- **Over-permissioning (Privilege Creep):** The biggest risk is assigning overly broad roles (e.g., Project Editor) to users or services that only need read access to a specific Cloud Storage bucket or BigQuery dataset.
- **Stale Permissions:** Failure to remove permissions for users who no longer need them leaves a security vulnerability and an open door into the data lake.

✅ What I Learned:
- Cloud IAM policies are built on three core components: the **Principal** (who), the **Role** (what they can do), and the **Resource** (e.g., a specific Cloud Storage bucket).
- The **Owner** role is the most powerful, with full administrative rights, including managing IAM policies.
- The **Viewer** role provides read-only access, which is ideal for auditors or stakeholders who need visibility without the ability to make changes.
- Using an **Incognito window** is a very effective technique for testing different permission levels.

💭 Reflection:  
Mengerjakan kembali lab fundamental ini dalam konteks membangun *data lake* yang aman benar-benar menekankan pentingnya memulai dengan model perizinan yang kuat. Sebelum data apa pun dimasukkan, mendefinisikan siapa yang dapat membaca, menulis, dan mengelola bucket Cloud Storage dan dataset BigQuery adalah langkah pertama yang paling krusial. Satu kesalahan konfigurasi IAM dapat merusak keamanan seluruh data lake, terlepas dari kontrol keamanan lainnya yang ada.

---

## 🏆 Leaderboard Status (as of August 12, 2025)

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
| Secure Data Lake Quest              | ✅ Completed (1/4 Labs)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **---OVERALL---** |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Badges Earned                       | [🏅 Week 1 Trivia Badge](https://www.cloudskillsboost.google/public_profiles/c8fd48a4-987d-4216-9635-d49fa00793da/badges/17140064), [🏆 Level 1 Game Badge](https://www.cloudskillsboost.google/public_profiles/c8fd48a4-987d-4216-9635-d49fa00793da/badges/17245038), [🏅 Week 2 Trivia Badge](https://www.cloudskillsboost.google/public_profiles/c8fd48a4-987d-4216-9635-d49fa00793da/badges/17274275), [🏅 August Week 1 Trivia Badge](https://www.cloudskillsboost.google/public_profiles/c8fd48a4-987d-4216-9635-d49fa00793da/badges/17423679) |
| League Standing                     | 15th – Silver League (672 pts)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Promotion Status                    | ⚪️ Stable                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
