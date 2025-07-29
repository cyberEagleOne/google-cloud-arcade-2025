## 📅 July 29, 2025

---

### 🧩 Project / Lab Title:
**Set Up Network Load Balancers**

📆 Date Completed:  
**July 29, 2025**

🔍 Objective:  
To configure a high-availability setup by deploying a Layer 4 (L4) passthrough Network Load Balancer. The goal was to distribute TCP traffic across a group of backend Apache web server instances running on Compute Engine VMs.

🔧 Tools/Services Used:
- Google Cloud Shell
- `gcloud` CLI
- Compute Engine
- Cloud Load Balancing (Network Load Balancer)
- VPC Firewall Rules

🧠 What I Did:
- Created three identical **Compute Engine** VM instances (`www1`, `www2`, `www3`), each running an Apache web server configured via a **startup script**.
- Applied a common tag (`network-lb-tag`) to all instances for easy management.
- Configured a **VPC firewall rule** to allow HTTP traffic on port 80 specifically to instances with that tag.
- Provisioned a **static external IP address** to serve as the public entry point for the load balancer.
- Created a legacy **HTTP health check** to monitor the availability of the backend web servers.
- Set up a **target pool**, which grouped the three VM instances together and associated them with the health check.
- Deployed a **forwarding rule** to direct incoming traffic from the static public IP on port 80 to the target pool.
- Verified the setup by repeatedly sending `curl` requests to the load balancer's IP and observing the traffic being distributed in a round-robin fashion across the three backend servers.

🛡️ GRC / Compliance Relevance:  
✅ High  
Load balancing is a cornerstone of GRC because it directly supports key compliance and security principles:
- **High Availability & Business Continuity:** By distributing traffic, a load balancer prevents a single server failure from causing a total service outage. This is a fundamental requirement for most compliance standards (e.g., ISO 27001, SOC 2).
- **Network Security:** The use of firewall rules and tags demonstrates network segmentation and the principle of least privilege, ensuring that only legitimate, allowed traffic can reach the application servers.
- **Auditable Infrastructure:** Defining the entire load balancer configuration via `gcloud` commands creates a repeatable and auditable trail for how the production environment is structured and secured.

🚩 Risks Identified:  
- **Single Region Deployment:** All components in this lab were deployed in a single region (`us-east4`). While this setup is resilient to a VM failure, it is not resilient to a full regional outage.
- **Unencrypted Traffic:** The lab uses a passthrough load balancer for HTTP traffic on port 80, meaning all data transmitted is unencrypted. This is a significant security risk and would not be compliant for applications handling any sensitive information.
- **Health Check Misconfiguration:** An improperly tuned health check could falsely mark healthy instances as down, leading to reduced capacity or even a full outage if all instances are removed from the pool.

✅ What I Learned:
- A **Network Load Balancer** is a Layer 4 service that distributes traffic based on IP and port data, without inspecting the packet content (passthrough).
- The essential components of this type of load balancer are a **Forwarding Rule** (the frontend) and a **Target Pool** (the backend).
- **Health checks** are critical for ensuring that traffic is only sent to healthy, responsive instances.
- **Tags** are a powerful and efficient way to apply network configurations, like firewall rules, to groups of VMs.
- Startup scripts are an effective method for automating instance initialization and software installation.

💭 Reflection:  
This lab provided a fantastic, hands-on understanding of how to build a scalable and resilient application frontend. It moved beyond a single server and into a fleet architecture. The process of connecting the different components—the public IP, the forwarding rule, the health check, the target pool, and the instances—made the entire data flow very clear. Watching the `curl` command return responses from different servers was a very satisfying confirmation that the system was working as designed. This is a foundational pattern for almost any web service.

---

## 🏆 Leaderboard Status (as of July 29, 2025)

| Metric              | Value                    |
|---------------------|--------------------------|
| Arcade Username     | `ciril`                  |
| Global Arcade Games lvl 1 Rank         | **#6277**                 |
| Global Arcade Games lvl 1 XP           | **234,577,850 XP**      |
| Arcade Games lvl 1       | ✅ Completed (6/12 Labs)  |
| Trivia Week 1       | ✅ Completed (4/4 Labs)  |
| Badges Earned       | [🏅 Week 1 Trivia Badge](https://www.cloudskillsboost.google/public_profiles/c8fd48a4-987d-4216-9635-d49fa00793da/badges/17140064)   |
| League Standing     | 12th – Silver League (30 pts) |
| Promotion Status    | 🟢 Needs to be at least top 10 to be promoted to Gold          |
