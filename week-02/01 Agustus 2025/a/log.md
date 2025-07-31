## 📅 August 1, 2025

---

### 🧩 Project / Lab Title:
**Application Load Balancer with Cloud Armor**

📆 Date Completed:  
**August 1, 2025**

🔍 Objective:  
To learn how to secure a global Application Load Balancer by implementing a Cloud Armor security policy to explicitly deny traffic from a specific, known-bad IP address.

🔧 Tools/Services Used:
- Cloud Armor
- Cloud Load Balancing (Application Load Balancer)
- Compute Engine (Instance Templates, Managed Instance Groups)
- VPC Firewall Rules
- `gcloud` CLI

🧠 What I Did:
- Deployed a globally distributed web application using **Instance Templates** and **Managed Instance Groups (MIGs)** in multiple regions.
- Configured a global **Application Load Balancer** with a backend service, health check, and forwarding rule to serve traffic to the MIGs.
- Identified the IP address of a separate "testing" VM that would simulate a malicious actor.
- Created a new **Cloud Armor security policy**.
- Within the policy, I configured a rule with a high priority to **deny** traffic. The rule's condition was set to match the specific source IP address of my testing VM.
- I ensured a default, lower-priority rule was in place to **allow** all other traffic.
- **Attached the security policy** to the load balancer's backend service.
- From the testing VM, I attempted to access the web service and verified that I received an HTTP `403 (Forbidden)` error, confirming the denylist rule was effective.
- I also confirmed that traffic from other sources (like Cloud Shell) was still permitted.

🛡️ GRC / Compliance Relevance:  
✅ High  
IP denylisting with Cloud Armor is a direct and powerful GRC tool.
- **Incident Response:** This is a primary technique used during a security incident. Once a malicious IP is identified, security teams can use this to immediately block the threat at the network edge, preventing further damage.
- **Threat Mitigation:** Proactively blocking traffic from known malicious IP ranges or botnets is a key part of a defense-in-depth security posture.
- **Enforcing Access Policies:** For compliance, organizations may need to block access from specific countries or networks. Cloud Armor rules can enforce these geo-based or IP-based access policies.

🚩 Risks Identified:  
- **Accidental Blocking of Legitimate IPs:** The most common risk is human error—incorrectly typing an IP address or using too broad of a range (e.g., blocking a `/24` instead of a `/32`), which could deny service to legitimate users or an entire office.
- **Rule Priority Conflicts:** If a general `allow` rule has a higher priority (lower number) than a specific `deny` rule, the deny rule will never be evaluated. Proper ordering of policy rules is critical for them to function as intended.
- **Dynamic Attackers:** A simple IP denylist is ineffective against attackers who use large botnets or frequently change their IP addresses. It's a tool for specific, identified threats, not a comprehensive DDoS solution on its own.

✅ What I Learned:
- An **Application Load Balancer** is a Layer 7 load balancer that can inspect HTTP(S) traffic and make intelligent routing decisions.
- A **Cloud Armor policy** is a list of rules evaluated by **priority** (lowest number is highest priority). The first rule that matches a request's characteristics determines the action.
- A common and effective security pattern is to create specific `deny` rules with high priority and a final, default `allow` rule with the lowest priority.
- The `deny` action can be configured to return a specific HTTP error code, like `403 (Forbidden)`, `404 (Not Found)`, or `502 (Bad Gateway)`.
- Denylisting is a surgical tool used to block specific known threats at the edge of Google's network.

💭 Reflection:  
This lab built perfectly on the previous one. While the last lab was about throttling *excessive* traffic, this one was about completely blocking a *known bad actor*. It was very satisfying to configure a specific rule to block my own VM's IP and see the instant `403 Forbidden` error. This demonstrates a more surgical security response. It's easy to see how a security team, after identifying a threat from their logs, could immediately use this feature to neutralize it at the edge, protecting the entire application infrastructure behind it.

---

## 🏆 Leaderboard Status (as of August 1, 2025)

| Metric              | Value                    |
|---------------------|--------------------------|
| Arcade Username     | `ciril`                  |
| Global Arcade Games lvl 1 Rank         | **#5561**                 |
| Global Arcade Games lvl 1 XP           | **491,797,287 XP**      |
| Arcade Games lvl 1       | ✅ **Completed (12/12 Labs)** 🎉 |
| Trivia Week 1       | ✅ Completed (4/4 Labs)  |
| Badges Earned       | [🏅 Week 1 Trivia Badge](https://www.cloudskillsboost.google/public_profiles/c8fd48a4-987d-4216-9635-d49fa00793da/badges/17140064), [🏆 Level 1 Game Badge](https://www.cloudskillsboost.google/public_profiles/c8fd48a4-987d-4216-9635-d49fa00793da/badges/17245038)   |
| League Standing     | 5th – Silver League (980 pts) |
| Promotion Status    | 🟢 Gold League Promo |
