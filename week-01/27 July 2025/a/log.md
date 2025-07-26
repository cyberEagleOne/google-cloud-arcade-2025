## 📅 July 27, 2025

---

### 🧩 Project / Lab Title:
**Getting Started with Cloud Shell and gcloud**

📆 Date Completed:  
**July 27, 2025**

🔍 Objective:  
To learn how to configure a Google Cloud development environment, create and manage VM instances, connect via SSH, configure firewall rules, and explore system logs using the gcloud CLI.

🔧 Tools/Services Used:
- Google Cloud Shell
- Compute Engine
- gcloud CLI
- Nginx
- Cloud Logging

🧠 What I Did:
- Set default region and zone (`us-west1`, `us-west1-a`) via `gcloud config`
- Defined and verified environment variables for Project ID and Zone
- Created a VM (`gcelab2`) using `gcloud compute instances create`
- Connected to the VM using `gcloud compute ssh`
- Installed and tested the Nginx web server inside the VM
- Updated firewall to allow HTTP traffic on tcp:80
- Verified firewall rule with `curl` and confirmed Nginx default page was served
- Used gcloud to explore and filter firewall rules and system logs
- Queried logs specific to the VM and the `gce_instance` resource type

🛡️ GRC / Compliance Relevance:  
✅ Medium  
The lab covers best practices for:
- Proper firewall configuration and exposure management
- Secure remote access via SSH
- Zone/region awareness for data residency and resource isolation
- Logging and monitoring for auditing and diagnostics

🚩 Risks Identified:  
- Enabling HTTP (tcp:80) publicly without TLS could expose the VM to unencrypted traffic risks
- SSH keys are generated automatically — secure storage and management is important

✅ What I Learned:
- How to configure and use Compute Engine with `gcloud` CLI
- Importance of zone/region selection for colocating resources
- Using tags and firewall rules to manage VM access
- How to monitor and filter logs using `gcloud logging read`
- Real-world cloud environment setup that simulates production deployments

💭 Reflection:  
This was my first real hands-on experience with Compute Engine and the gcloud CLI, and I feel way more comfortable creating VMs, updating firewall rules, and even navigating logs. This lab helped me bridge theory and practice for basic cloud infra management. It was also a great warm-up for more complex infra tasks!

---

## 🏆 Leaderboard Status (as of July 26, 2025)

| Metric              | Value                    |
|---------------------|--------------------------|
| Arcade Username     | `ciril`                  |
| Global Trivia week 1 Rank         | **#6689**                 |
| Global Trivia week 1 XP           | **26,785,714 XP**        |
| Trivia Week 1       | ✅ Completed (4/4 Labs)  |
| Arcade Games 1       | ✅ Completed (1/12 Labs)  |
| Badges Earned       | 🏅 Week 1 Trivia Badge   |
| League Standing     | 11th – Bronze League (832 pts)|
| Promotion Status    | 🟢 Needs to be at least top 10 to be promoted     |
