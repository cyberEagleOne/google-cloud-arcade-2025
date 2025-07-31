## 📅 August 1, 2025

---

### 🧩 Project / Lab Title:
**Rate Limiting with Cloud Armor**

📆 Date Completed:  
**August 1, 2025**

🔍 Objective:  
To learn how to protect a global HTTP(S) Load Balancer from denial-of-service (DoS) attacks and other abusive traffic by configuring and applying a Cloud Armor rate-limiting policy.

🔧 Tools/Services Used:
- Cloud Armor
- Cloud Load Balancing (Global HTTP(S) Load Balancer)
- Compute Engine (Instance Templates, Managed Instance Groups)
- VPC Firewall Rules
- `gcloud` CLI

🧠 What I Did:
- Set up a resilient, globally distributed web service by creating two **Managed Instance Groups (MIGs)** in different regions, based on a common **Instance Template**.
- Configured a global **HTTP(S) Load Balancer** to distribute traffic to these MIGs. This involved setting up a backend service, health check, URL map, and a global forwarding rule with a public IP.
- Deployed a separate VM to act as a stress-testing client.
- From the client VM, I simulated a high-traffic scenario to confirm the load balancer was working correctly.
- Created a **Cloud Armor security policy**.
- Inside the policy, I defined a new **rate-limiting rule** to throttle requests from any single IP address to a specific rate (e.g., 10 requests per minute).
- **Attached the Cloud Armor policy** to the load balancer's backend service.
- Ran the stress test again and verified that after exceeding the rate limit, Cloud Armor correctly blocked subsequent requests from my client VM, returning an HTTP `429 (Too Many Requests)` error.

🛡️ GRC / Compliance Relevance:  
✅ High  
Cloud Armor is a primary tool for meeting security and availability compliance requirements.
- **Denial of Service (DoS) Mitigation:** Protecting services from DoS attacks is a fundamental control for ensuring service availability, a core tenet of the CIA (Confidentiality, Integrity, Availability) security triad and a requirement for frameworks like SOC 2 and ISO 27001.
- **Resource & Cost Governance:** Rate limiting prevents abusive bots or attackers from consuming excessive compute resources, which helps in managing operational costs and ensuring fair use of the platform for legitimate users.
- **Threat Intelligence and Incident Response:** Cloud Armor logs provide detailed visibility into blocked traffic, which is invaluable for security monitoring, identifying attack patterns, and informing incident response procedures.

🚩 Risks Identified:  
- **Blocking Legitimate Traffic:** Setting a rate limit that is too strict can inadvertently block legitimate users or automated services with bursty traffic patterns, causing a self-inflicted denial of service. Careful tuning and analysis are required.
- **IP-Based Evasion:** While effective against simple attacks, IP-based rate limiting can be bypassed by sophisticated attackers using large, distributed botnets (DDoS). This would require more advanced Cloud Armor features like Adaptive Protection.
- **Policy Misconfiguration:** Applying the wrong rule or attaching the policy to the wrong backend service could leave the application unprotected or cause unintended blocking of valid traffic.

✅ What I Learned:
- **Cloud Armor** is Google's distributed denial-of-service (DDoS) mitigation and Web Application Firewall (WAF) service that operates at the edge of Google's network.
- It protects applications served by the **global HTTP(S) Load Balancer**.
- A Cloud Armor **security policy** is a container for a set of rules that are evaluated in priority order.
- **Rate limiting** is a specific rule type that allows you to throttle requests based on a key (like the source IP address) over a configurable time interval.
- When a client is throttled, Cloud Armor can be configured to return a specific HTTP error code, typically `429 (Too Many Requests)`.
- Policies are applied by attaching them to one or more **backend services**.

💭 Reflection:  
This lab was an excellent, hands-on demonstration of network edge security. It felt like I was setting up a digital bouncer for my application. The most impactful moment was running the stress test and watching it fail after the Cloud Armor policy was applied—it was a powerful and immediate confirmation that the protection was active. It clearly shows how to defend against volumetric attacks before they even reach your VPC network, saving resources and ensuring application availability. This is an absolutely essential skill for any public-facing service deployed on Google Cloud.

---

## 🏆 Leaderboard Status (as of August 1, 2025)

| Metric              | Value                    |
|---------------------|--------------------------|
| Arcade Username     | `ciril`                  |
| Global Arcade Games lvl 1 Rank         | **#5695**                 |
| Global Arcade Games lvl 1 XP           | **470,432,382 XP**      |
| Arcade Games lvl 1       | ✅ Completed (11/12 Labs) |
| Trivia Week 1       | ✅ Completed (4/4 Labs)  |
| Badges Earned       | [🏅 Week 1 Trivia Badge](https://www.cloudskillsboost.google/public_profiles/c8fd48a4-987d-4216-9635-d49fa00793da/badges/17140064)   |
| League Standing     | 5th – Silver League (790 pts) |
| Promotion Status    | 🟢 Gold League Promo |
