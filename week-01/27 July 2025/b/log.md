## 📅 July 27, 2025

---

### 🧩 Project / Lab Title:
**Cloud Storage: Qwik Start - Cloud Console**

📆 Date Completed:  
**July 27, 2025**

🔍 Objective:  
To learn how to create a Cloud Storage bucket, upload and organize data using folders, manage access permissions, and make objects publicly accessible through the Google Cloud Console.

🔧 Tools/Services Used:
- Google Cloud Console
- Cloud Storage

🧠 What I Did:
- Created a Cloud Storage **bucket** with a globally unique name(my ID Projects).
- Uploaded a file (`kitten.png`) into the bucket as an **object**.
- Made the object **publicly accessible** by assigning the `Storage Object Viewer` role to `allUsers`.
- Created a folder (`folder1`) and a **nested subfolder** (`folder2`) inside the bucket.
- Uploaded files inside the folders to simulate organizing assets.
- Deleted folders and verified cleanup to manage bucket contents.

🛡️ GRC / Compliance Relevance:  
✅ Moderate  
Understanding how to control object-level access, manage public permissions, and structure cloud data is essential in maintaining compliance and governance policies related to:
- Data classification
- Secure access management
- Least privilege principles

🚩 Risks Identified:  
- Public sharing of objects without proper access control may lead to unintentional exposure of sensitive files.

✅ What I Learned:
- A **bucket** is a globally named container that stores objects (files).
- An **object** is a file and its metadata stored in Cloud Storage.
- Bucket names must follow global DNS-like naming rules and be unique.
- Access control is handled via roles, such as `Storage Object Viewer`, and principals like `allUsers`.
- Folders in Cloud Storage are logical — they help organize objects via naming (e.g. `folder1/folder2/file.png`).
- Objects can be **made public** via IAM settings, and then shared through a public URL like:  
  `https://storage.googleapis.com/[BUCKET_NAME]/[OBJECT_NAME]`.

💭 Reflection:  
This lab was very practical. It felt like setting up my own personal drive, but with enterprise-grade control and scalability. I could clearly imagine how this could be useful for hosting portfolios, sharing assets, or storing logs securely. Definitely a foundational skill to master early.

---

## 🏆 Leaderboard Status (as of July 27, 2025)

| Metric              | Value                    |
|---------------------|--------------------------|
| Arcade Username     | `ciril`                  |
| Global Arcade Games lvl 1 Rank         | **#6563**                 |
| Global Arcade Games lvl 1 XP           | **58,035,714 XP**        |
| Arcade Games lvl 1       | ✅ Completed (2/12 Labs)  |
| Trivia Week 1       | ✅ Completed (4/4 Labs)  |
| Badges Earned       | 🏅 Week 1 Trivia Badge   |
| League Standing     | 10th – Bronze League (981 pts)|
| Promotion Status    | 🟢 Silver League Promo |
