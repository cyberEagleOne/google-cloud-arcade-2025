## 📅 July 28, 2025

---

### 🧩 Project / Lab Title:
**Deploy Microsoft SQL Server to Compute Engine**

📆 Date Completed:  
**July 28, 2025**

🔍 Objective:  
To learn how to deploy a pre-configured Windows Server virtual machine with Microsoft SQL Server from the public images library, set Windows credentials, and connect to the instance using Remote Desktop Protocol (RDP) to verify the SQL Server installation.

🔧 Tools/Services Used:
- Google Cloud Console
- Compute Engine
- Remote Desktop Protocol (RDP)
- Microsoft SQL Server Management Studio (SSMS)

🧠 What I Did:
- Provisioned a new **Compute Engine** instance named `sqlserver-lab`.
- Instead of a standard OS, I selected a pre-configured public image: **SQL Server 2022 Web on Windows Server 2022 Datacenter**.
- After the instance was created, I used the **Set Windows password** feature to generate administrative credentials for the VM.
- I securely connected to the Windows VM's graphical interface using **Remote Desktop Protocol (RDP)**.
- Inside the RDP session, I launched **SQL Server Management Studio (SSMS)** with administrator privileges.
- I successfully connected to the local database engine, confirming that the SQL Server instance was deployed and running correctly.

🛡️ GRC / Compliance Relevance:  
✅ Moderate  
This lab touches on key GRC principles for Infrastructure as a Service (IaaS):
- **Software Licensing Compliance:** Deploying from the Google Cloud Marketplace or public images helps ensure that proper licenses for proprietary software like Windows Server and SQL Server are managed and accounted for.
- **Secure Baseline Configuration:** Using a pre-configured image from a trusted source (Google) provides a more secure starting point than building from scratch, as these images are typically hardened and maintained.
- **Access Control:** The process of setting a distinct Windows password and using RDP highlights the need for secure remote access management. In a production environment, this would be further secured using Identity-Aware Proxy (IAP) or a bastion host to avoid exposing RDP to the public internet.

🚩 Risks Identified:  
- **Public RDP Exposure:** By default, connecting via RDP over the internet exposes port 3389, making the VM a prime target for brute-force login attacks.
- **Credential Management:** The generated password must be stored securely. Losing it or having it compromised would grant an attacker full administrative access to the Windows Server and its database.
- **Patch Management:** While the initial image is up-to-date, the user is responsible for the ongoing patching of both the Windows OS and the SQL Server software to protect against future vulnerabilities.

✅ What I Learned:
- Compute Engine isn't just for Linux; it has first-class support for Windows Server and complex Microsoft applications.
- The **Public Images** library is a powerful feature for deploying full software stacks (like a database server) in a single step, saving significant configuration time.
- The Cloud Console provides integrated tools for managing VM-specific credentials, such as setting an initial **Windows password**.
- The standard method for managing a Windows Server in the cloud is through **Remote Desktop Protocol (RDP)**.
- It's critical to run administrative applications like SSMS with **"Run as administrator"** privileges within Windows to ensure they have the necessary permissions to function.

💭 Reflection:  
This was a great change of pace from the Linux-based labs. It was surprisingly easy to get a full-fledged Microsoft SQL Server running. The integration for setting the Windows password directly from the GCP console and then seamlessly connecting via RDP was very smooth. It really demonstrates the power of IaaS and how Google Cloud supports diverse, heterogeneous environments. I can easily see how a business heavily invested in the Microsoft ecosystem could migrate their workloads to GCP using this exact process.

---

## 🏆 Leaderboard Status (as of July 28, 2025)

| Metric              | Value                    |
|---------------------|--------------------------|
| Arcade Username     | `ciril`                  |
| Global Arcade Games lvl 1 Rank         | **#6159**                 |
| Global Arcade Games lvl 1 XP           | **169,478,393 XP**      |
| Arcade Games lvl 1       | ✅ Completed (5/12 Labs)  |
| Trivia Week 1       | ✅ Completed (4/4 Labs)  |
| Badges Earned       | 🏅 Week 1 Trivia Badge   |
| League Standing     | 5th – Bronze League (1406 pts)|
| Promotion Status    | 🟢 Silver League Promo |
