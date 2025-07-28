## 📅 July 28, 2025

---

### 🧩 Project / Lab Title:
**Rent-a-VM to Process Earthquake Data**

📆 Date Completed:  
**July 28, 2025**

🔍 Objective:  
To deploy a Compute Engine instance, install software, ingest external data, run a transformation script on the VM, and publish the results to the web using Cloud Storage.

🔧 Tools/Services Used:
- Google Cloud Console
- Compute Engine
- Secure Shell (SSH)
- Cloud Storage
- `git`
- `gsutil`

🧠 What I Did:
- Created a **Debian Compute Engine VM** and configured its **Access Scopes** to allow full access to all Cloud APIs, enabling it to interact with other services.
- Connected to the instance via **browser-based SSH**.
- Installed required software packages, including `git` and Python libraries (`matplotlib`, `numpy`, `basemap`), using `apt-get` and `pip`.
- Cloned a GitHub repository (`training-data-analyst`) to fetch data processing scripts.
- Executed an `ingest.sh` script to download raw earthquake data from the USGS.
- Ran a Python script (`transform.py`) to process the raw data and generate a visual map (`earthquakes.png`).
- Created a new **Cloud Storage bucket** with fine-grained access control.
- Used the `gsutil cp` command from within the VM to copy the processed files to the Cloud Storage bucket.
- Made the output files **publicly accessible** by editing their permissions in the Cloud Console to grant the `Reader` role to the `allUsers` principal.

🛡️ GRC / Compliance Relevance:  
✅ Moderate  
This lab demonstrates a basic data processing pipeline, which is highly relevant to GRC:
- **Infrastructure Security:** Provisioning a VM with specific IAM access scopes is a critical security control. Granting overly permissive access (as done in the lab for simplicity) is a significant risk that GRC policies aim to prevent.
- **Data Governance:** The process of ingesting data to a specific region, transforming it, and storing it touches upon data residency and sovereignty requirements.
- **Change Management:** Installing software on a VM is a configuration change that must be tracked and audited to maintain a compliant state.

🚩 Risks Identified:  
- **Overly Permissive VM Access:** Setting "Allow full access to all Cloud APIs" on the VM creates a significant security risk. If the VM were compromised, the attacker could leverage its identity to access or damage any service within the project.
- **Untrusted Software:** Installing packages from default repositories using `apt-get` or `pip` could introduce vulnerabilities if not managed through a secure, private artifact repository.

✅ What I Learned:
- A complete workflow for data processing: **Ingest (git) -> Process (Python on VM) -> Store (gsutil) -> Publish (Public URL)**.
- **Access Scopes** are essential for allowing a Compute Engine instance to interact with other Google Cloud services on your behalf.
- A VM can act as a temporary, powerful workstation for specific tasks, while Cloud Storage provides a durable, scalable location for the results.
- The `gsutil` command can be used directly from a properly configured VM to manage Cloud Storage objects.
- How to make individual objects in a bucket public while keeping the rest private, using fine-grained access controls.

💭 Reflection:  
This was a fantastic, practical lab that connected multiple core services. It moved beyond just storing files and showed how to use compute power to actively *do something* with data. The "aha!" moment was using `gsutil` from the VM's command line; it really clarified how different GCP services are designed to work together seamlessly. This feels like a true building block for creating real-world applications on the cloud.

---

## 🏆 Leaderboard Status (as of July 28, 2025)

| Metric              | Value                    |
|---------------------|--------------------------|
| Arcade Username     | `ciril`                  |
| Global Arcade Games lvl 1 Rank         | **#6383**                 |
| Global Arcade Games lvl 1 XP           | **96,585,421 XP**        |
| Arcade Games lvl 1       | ✅ Completed (4/12 Labs)  |
| Trivia Week 1       | ✅ Completed (4/4 Labs)  |
| Badges Earned       | 🏅 Week 1 Trivia Badge   |
| League Standing     | 7th – Bronze League (1279 pts)|
| Promotion Status    | ⚪️ Stable                |
