## 📅 July 28, 2025

---

### 🧩 Project / Lab Title:
**Cloud Storage: Qwik Start - CLI/SDK**

📆 Date Completed:  
**July 28, 2025**

🔍 Objective:  
To learn how to manage Cloud Storage resources programmatically using the `gcloud` and `gsutil` command-line tools in Cloud Shell. This includes creating buckets, uploading/downloading objects, organizing data into folders, and managing public access permissions via the command line.

🔧 Tools/Services Used:
- Google Cloud Shell
- `gcloud` CLI
- `gsutil` CLI
- Cloud Storage

🧠 What I Did:
- Activated **Cloud Shell** and authenticated my session.
- Created a globally unique Cloud Storage bucket using the `gcloud storage buckets create gs://[BUCKET_NAME]` command.
- Used `curl` to download an image (`ada.jpg`) to the Cloud Shell instance.
- Uploaded the image from Cloud Shell into the bucket as an object with `gcloud storage cp`.
- Copied the object into a new logical folder (`image-folder/`) within the same bucket.
- Listed the contents of the bucket (`gcloud storage ls`) and viewed detailed object metadata (`gcloud storage ls -l`).
- Made the object **publicly readable** by applying an Access Control List (ACL) change with `gsutil acl ch -u AllUsers:R`.
- Verified public access by opening the public URL.
- **Revoked public access** using `gsutil acl ch -d AllUsers` and deleted the object with `gcloud storage rm`.

🛡️ GRC / Compliance Relevance:  
✅ Moderate  
Using the CLI for storage management is fundamental to **Governance, Risk, and Compliance (GRC)** automation. It enables:
- **Scripted deployments:** Ensuring storage resources are created consistently according to security policies.
- **Auditable changes:** Every command executed via the CLI can be logged, providing a clear audit trail for compliance checks.
- **Automated access control:** Scripts can programmatically grant and revoke permissions, enforcing the principle of least privilege at scale and reducing human error.

🚩 Risks Identified:  
- **Scripting Errors:** A typo in a script could apply incorrect permissions (e.g., making an entire bucket public instead of a single object), leading to a large-scale data breach.
- **Credential Management:** Scripts running commands often rely on service account keys. If these keys are exposed, an attacker could gain programmatic control over storage resources.

✅ What I Learned:
- The `gcloud storage` command group is the modern tool for most bucket and object operations.
- The legacy `gsutil` tool is still necessary for certain fine-grained controls, like managing **Access Control Lists (ACLs)**.
- The principal `AllUsers` is a special identifier used to grant access to anyone on the public internet.
- You can create "folders" in Cloud Storage from the CLI by simply including the folder name and a trailing `/` in the destination path of a copy command (e.g., `gs://[BUCKET]/[FOLDER]/`).
- Commands for core actions include:
  - Create Bucket: `gcloud storage buckets create`
  - Copy/Upload/Download: `gcloud storage cp`
  - List Contents: `gcloud storage ls`
  - Modify ACLs: `gsutil acl ch`
  - Delete Object: `gcloud storage rm`

💭 Reflection:  
This lab was an excellent step up from the Cloud Console. Working with the CLI felt much more efficient and powerful. I can now see how cloud operations are automated in the real world. A single script could set up storage for a new application, upload assets, and configure permissions in seconds. This moves beyond simple "cloud drive" usage and into true infrastructure management. Mastering the CLI is clearly non-negotiable for serious cloud work.

---

## 🏆 Leaderboard Status (as of July 28, 2025)

| Metric              | Value                    |
|---------------------|--------------------------|
| Arcade Username     | `ciril`                  |
| Global Arcade Games lvl 1 Rank         | **#6424**                 |
| Global Arcade Games lvl 1 XP           | **73,136,385 XP**        |
| Arcade Games lvl 1       | ✅ Completed (3/12 Labs)  |
| Trivia Week 1       | ✅ Completed (4/4 Labs)  |
| Badges Earned       | 🏅 Week 1 Trivia Badge   |
| League Standing     | 10th – Bronze League (1014 pts)|
| Promotion Status    | 🟢 Silver League Promo |
