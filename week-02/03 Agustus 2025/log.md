## 📅 August 3, 2025

---

### 🧩 Project / Lab Title:
**Redacting Critical Data with Sensitive Data Protection**

📆 Date Completed:  
**August 3, 2025**

🔍 Objective:  
To learn how to use the Sensitive Data Protection service (Cloud DLP API) to automatically discover, classify, and de-identify sensitive information within both text strings and images.

🔧 Tools/Services Used:
- Sensitive Data Protection (Cloud DLP API)
- Cloud Shell
- `curl` command
- JSON

🧠 What I Did:
- Enabled the **Cloud Data Loss Prevention (DLP) API**.
- Using `curl` in Cloud Shell, I sent an API request to the `content.inspect` endpoint to scan a string of text for sensitive data. I analyzed the JSON response which identified the `infoType` (e.g., `EMAIL_ADDRESS`) and its location.
- I then used the `content.deidentify` endpoint to programmatically **redact** and **mask** the sensitive information found in the text string, turning it into non-sensitive data.
- The most impressive part was working with images. I sent a request to the `image.redact` endpoint, providing an image containing visible text with sensitive information.
- The API performed Optical Character Recognition (OCR), identified the sensitive `infoTypes` within the image's text, and returned a new version of the image with the sensitive data blacked out.

🛡️ GRC / Compliance Relevance:  
✅ Critical  
Sensitive Data Protection is a purpose-built GRC tool that directly addresses major compliance and data privacy requirements.
- **Data Discovery & Classification:** A foundational requirement for regulations like GDPR and CCPA is knowing what sensitive data you have and where it is. The "inspect" functionality automates this critical task across data stores like Cloud Storage and BigQuery.
- **Privacy by Design:** The de-identification features (redaction, masking, tokenization) are the technical controls needed to implement "Privacy by Design." Applications can be built to automatically sanitize user-generated content or logs, minimizing the risk of storing PII.
- **Data Minimization:** By redacting or masking data that is not essential for a given business process, organizations can adhere to the principle of data minimization, a key tenet of modern privacy laws. This helps reduce the "blast radius" in case of a data breach.

🚩 Risks Identified:  
- **False Negatives:** No automated scanner is perfect. There's a risk that the DLP API might miss certain instances of sensitive data, especially if it's in a non-standard format, leading to a false sense of security.
- **Cost at Scale:** Running inspection and de-identification jobs across petabytes of data can be costly. Proper planning is required to scope jobs effectively and manage the associated costs.
- **Performance Impact:** For real-time redaction use cases, the latency of the API call must be factored into the application's overall performance.

✅ What I Learned:
- **Sensitive Data Protection (Cloud DLP)** is a powerful managed service that uses pre-trained ML models to find and protect sensitive data.
- It can identify a vast library of built-in **`infoTypes`**, from email addresses and phone numbers to national identification numbers from many countries.
- It offers various **de-identification techniques**, including **redaction** (removing data), **masking** (replacing with symbols), and **tokenization** (replacing with a non-sensitive token).
- A key capability is its ability to process **images**, using OCR to find and redact text directly within a picture.

💭 Reflection:  
This lab was genuinely impressive. The ability of a single API call to not only find an email address in a sentence but to also read text from an image and black out the sensitive parts is a "wow" moment. It showcases the power and accessibility of Google's AI/ML services. This tool is a massive asset for any company handling user data, as it provides a practical and automated way to enforce data privacy policies and reduce risk without needing to build a complex data-scanning engine from scratch. It's a perfect example of how the cloud can simplify sophisticated compliance and security challenges.

---

## 🏆 Leaderboard Status (as of August 3, 2025)

| Metric                      | Value                                                                                                                                                                                                                                                                                             |
| :-------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Arcade Username             | `ciril`                                                                                                                                                                                                                                                                                           |
| **---COMPLETED---** |                                                                                                                                                                                                                                                                                                   |
| Arcade Games lvl 1          | ✅ **Finished (12/12 Labs)** 🎉                                                                                                                                                                                                                                                                   |
| Trivia Week 1               | ✅ **Finished (4/4 Labs)** 🎉                                                                                                                                                                                                                                                                     |
| Trivia Week 2               | ✅ **Finished (3/3 Labs)** 🎉                                                                                                                                                                                                                                                                     |
| **---IN PROGRESS---** |                                                                                                                                                                                                                                                                                                   |
| Trivia Week 3               | ✅ Completed (1/4 Labs)                                                                                                                                                                                                                                                                           |
| Global Trivia Week 3 Rank   | **#8860** |
| Global Trivia Week 3 XP     | **79,881,656 XP** |
| **---OVERALL---** |                                                                                                                                                                                                                                                                                                   |
| Badges Earned               | [🏅 Week 1 Trivia Badge](https://www.cloudskillsboost.google/public_profiles/c8fd48a4-987d-4216-9635-d49fa00793da/badges/17140064), [🏆 Level 1 Game Badge](https://www.cloudskillsboost.google/public_profiles/c8fd48a4-987d-4216-9635-d49fa00793da/badges/17245038), [🏅 Week 2 Trivia Badge](https://www.cloudskillsboost.google/public_profiles/c8fd48a4-987d-4216-9635-d49fa00793da/badges/17274275) |
| League Standing             | 6th – Silver League (1544 pts)                                                                                                                                                                                                                                                                    |
| Promotion Status            | 🟢 Gold League Promo                                                                                                                                                                                                                                                                              |
