## 📅 July 29, 2025

---

### 🧩 Project / Lab Title:
**Cloud Filestore: Qwik Start**

📆 Date Completed:  
**July 29, 2025**

🔍 Objective:  
To learn how to provision and use Cloud Filestore, Google Cloud's managed Network Attached Storage (NAS) service. The goal was to create a shared file system and mount it onto a Compute Engine VM, enabling file sharing between the VM and the storage service.

🔧 Tools/Services Used:
- Cloud Filestore
- Compute Engine
- Google Cloud Console
- SSH
- NFS (Network File System) client tools

🧠 What I Did:
- Provisioned a **Compute Engine** VM (`nfs-client`) to act as the client that would access the shared storage.
- Enabled the **Cloud Filestore API**.
- Created a new **Cloud Filestore instance** (`nfs-server`) of type Basic HDD, specifying its capacity and a file share name (`vol1`).
- Configured the instance's access control to allow connections from any client within the same VPC network.
- Connected to the `nfs-client` VM via **SSH**.
- On the client VM, I installed the `nfs-common` package, which provides the necessary tools to interact with NFS shares.
- Created a local directory (`/mnt/test`) to serve as the mount point.
- Executed the `sudo mount` command, using the Filestore instance's internal IP address, to attach the remote file share (`/vol1`) to the local mount point.
- Modified the file permissions on the mounted directory to allow read/write access.
- Created a test file on the mounted share and verified its existence and content, confirming that the VM could successfully write data to the Cloud Filestore instance.

🛡️ GRC / Compliance Relevance:  
✅ Moderate  
Cloud Filestore is relevant to GRC as it provides a centralized data management solution:
- **Centralized Data Governance:** Using a shared file system allows for centralized control and auditing of data access, which is easier to manage than data scattered across multiple VMs' local disks.
- **Data Durability and Availability:** As a managed service, Filestore provides a durable storage backend, which is a key component of business continuity and disaster recovery planning required by many compliance standards.
- **Secure Access Control:** Although configured permissively in the lab, real-world Filestore deployments rely on strict network-based access controls (VPC firewalls) to ensure only authorized systems can mount and access the file shares, enforcing the principle of least privilege.

🚩 Risks Identified:  
- **Overly Permissive Access:** The lab's configuration to "Grant access to all clients on the VPC network" is a significant security risk. In a production environment with multiple projects and tenants, this could allow unauthorized systems to access the file share.
- **Unencrypted Data in Transit:** Standard NFSv3, used by Filestore's basic tiers, does not encrypt data in transit. Any sensitive information transferred between the client VM and the Filestore instance could be intercepted on the network.
- **Insecure File Permissions:** Setting global read/write permissions (`chmod go+rw`) on the mount point is insecure and could lead to unauthorized data modification in a multi-user environment.

✅ What I Learned:
- **Cloud Filestore** is Google Cloud's fully managed **Network Attached Storage (NAS)** solution.
- It provides file-level storage and is accessed using the standard **NFS (Network File System)** protocol.
- The basic workflow is to create a Filestore instance (the server) and then `mount` its file share from a client machine (like a Compute Engine VM).
- The client machine needs the `nfs-common` package (on Debian/Ubuntu) to be able to mount NFS shares.
- Once mounted, the shared directory behaves exactly like a local folder on the client VM, but the data is persisted on the managed Filestore service.

💭 Reflection:  
This lab clearly demonstrated a classic and very practical use case in cloud computing: shared storage. It felt very intuitive, almost exactly like mounting a network drive on a local network. I can easily see how this would be essential for scenarios like hosting a website with shared content across multiple web servers, providing home directories for a team of users, or storing shared datasets for analysis. It’s a powerful example of GCP offering a familiar, traditional IT service in a highly available, managed, and scalable cloud format.

---

## 🏆 Leaderboard Status (as of July 29, 2025)

| Metric              | Value                    |
|---------------------|--------------------------|
| Arcade Username     | `ciril`                  |
| Global Arcade Games lvl 1 Rank         | **#6205**                 |
| Global Arcade Games lvl 1 XP           | **268,076,609 XP**      |
| Arcade Games lvl 1       | ✅ Completed (7/12 Labs)  |
| Trivia Week 1       | ✅ Completed (4/4 Labs)  |
| Badges Earned       | [🏅 Week 1 Trivia Badge](https://www.cloudskillsboost.google/public_profiles/c8fd48a4-987d-4216-9635-d49fa00793da/badges/17140064)   |
| League Standing     | 8th – Silver League (250 pts) |
| Promotion Status    | 🟢 Gold League Promo |
