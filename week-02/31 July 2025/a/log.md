## 📅 July 31, 2025

---

### 🧩 Project / Lab Title:
**Cloud IAM: Qwik Start**

📆 Date Completed:  
**July 31, 2025**

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
- As the "Viewer", I verified that I could see resources like Compute Engine instances but was correctly denied permission when attempting to create, modify, or delete anything.
- I switched back to my "Owner" account and removed the Viewer role from the second user, effectively **revoking their access**.
- Finally, I confirmed as the second user that all access to the project's resources was now gone, demonstrating a complete access control lifecycle.

🛡️ GRC / Compliance Relevance:  
✅ Critical  
This lab is the absolute foundation of Governance, Risk, and Compliance (GRC) in the cloud. All security controls depend on a correctly configured IAM policy.
- **Principle of Least Privilege (PoLP):** The lab is a direct, practical demonstration of PoLP, a core requirement for nearly all security frameworks (PCI-DSS, ISO 27001, SOC 2, HIPAA). The Viewer role grants only the minimum necessary access.
- **Segregation of Duties (SoD):** Using an Owner (can change permissions) and a Viewer (cannot) is a textbook example of SoD, preventing single users from having excessive, unchecked power.
- **Access Control & Auditing:** The entire process of adding, testing, and removing user access is what auditors examine during access reviews to ensure policies are being enforced correctly.

🚩 Risks Identified:  
- **Privilege Creep:** The primary risk in IAM is assigning overly broad roles (e.g., giving a user Project Editor when they only need Compute Viewer). This violates the principle of least privilege and expands the potential attack surface.
- **Stale Permissions:** Failing to revoke access for users who no longer need it is a common vulnerability that creates unnecessary security gaps.
- **Role Misconfiguration:** Granting a predefined role without fully understanding the permissions it contains can lead to unintentional exposure of sensitive resources or capabilities.

✅ What I Learned:
- Cloud IAM policies are built on three core components: the **Principal** (who), the **Role** (what they can do), and the **Resource** (the object they can do it on).
- The **Owner** role is the highest-level primitive role, granting full administrative control over a project and its IAM policy.
- The **Viewer** role provides read-only access, which is ideal for auditing, monitoring, or team members who only need to see the state of resources.
- IAM changes are applied almost instantly.
- Using an **Incognito window** is a very effective technique for testing different permission levels without having to constantly log in and out.

💭 Reflection:  
This lab felt like being given the keys to the kingdom and then learning how to responsibly give out spare keys. While other labs are about building things, this was about securing them. Actually seeing the "Permission Denied" errors as the Viewer user was a simple but powerful lesson in how the principle of least privilege works in practice. It's incredibly clear that a single mistake in IAM could undermine all other security efforts. This is without a doubt one of the most critical services to master.

---

## 🏆 Leaderboard Status (as of July 31, 2025)

| Metric              | Value                    |
|---------------------|--------------------------|
| Arcade Username     | `ciril`                  |
| Global Arcade Games lvl 1 Rank         | **#6627**                 |
| Global Arcade Games lvl 1 XP           | **293,889,228 XP**      |
| Arcade Games lvl 1       | ✅ Completed (8/12 Labs)  |
| Trivia Week 1       | ✅ Completed (4/4 Labs)  |
| Badges Earned       | [🏅 Week 1 Trivia Badge](https://www.cloudskillsboost.google/public_profiles/c8fd48a4-987d-4216-9635-d49fa00793da/badges/17140064)   |
| League Standing     | 15th – Silver League (280 pts)|
| Promotion Status    | ⚪️ Stable                |
