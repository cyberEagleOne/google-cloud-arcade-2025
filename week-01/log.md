# 🗓️ Week 01 Log (22 – 28 July 2025)

Welcome to my first official week in the Google Cloud Arcade 2025!  
This week I completed 3 labs to kickstart my learning journey toward Cloud Security and GRC 🎯

---

## ✅ Completed Labs

---

### 🧩 Project / Lab Title:
**A Tour of Google Cloud Hands-on Labs (GSP282)**

📆 Date Completed:  
**July 22, 2025**

🔍 Objective:  
To explore how Google Cloud Skills Boost labs work, understand lab time limits, and navigate temporary project environments.

🔧 Tools/Services Used:
- Google Cloud Skills Boost
- Cloud Console
- Cloud Shell

🧠 What I Did:
- Launched the introductory lab
- Learned how lab time & credentials work
- Explored the interface of Cloud Console
- No technical config yet — focus was orientation

🛡️ GRC / Compliance Relevance:
Understanding sandbox environments is essential in GRC & audit contexts — this was the foundation.

🚩 Risks Identified:  
None — just exploration.

✅ What I Learned:
- Lab structure, temporary access, and time limits
- Safe lab environments mimic safe production systems

📂 Screenshots / Evidence:  


💭 Reflection:  
A nice warm-up. It helped me feel prepared and less intimidated for future hands-on labs.

---

### 🧩 Project / Lab Title:
**Entity and Sentiment Analysis with the Natural Language API**

📆 Date Completed:  
**July 23, 2025**

🔍 Objective:  
Analyze entities and sentiments in text using Google Cloud's Natural Language API.

🔧 Tools/Services Used:
- Natural Language API
- Cloud Shell / CLI
- gcloud + curl

🧠 What I Did:
- Enabled the API and authenticated via service account
- Used `curl` and `gcloud` to send text analysis requests
- Explored sentiment scoring and entity labeling

🛡️ GRC / Compliance Relevance:
Moderate — understanding automated text analysis helps in compliance tools like DLP or auto-tagging sensitive content.

🚩 Risks Identified:  
None — the API was used in a secure lab environment.

✅ What I Learned:
- How to use Natural Language API via command line
- What entity types and sentiment scores represent
- JSON response structure for NLP analysis

📂 Screenshots / Evidence:  


💭 Reflection:  
My first exposure to using APIs through CLI! It was exciting to see how machine learning can detect meaning and tone.

---

### 🧩 Project / Lab Title:
**Create and Test a Document AI Processor**

📆 Date Completed:  
**July 24, 2025**

🔍 Objective:  
To use Document AI to process a form-based PDF and extract key-value data using OCR and AI.

🔧 Tools/Services Used:
- Document AI API
- Compute Engine (VM)
- IAM & Service Account
- Python Client SDK

🧠 What I Did:
- Enabled the API and created a Form Parser processor
- Uploaded a handwritten form and tested parsing accuracy
- Authenticated via service account and ran Python script
- Parsed key-value fields with confidence scoring

🛡️ GRC / Compliance Relevance:
✅ High  
Document parsing like this is essential in compliance workflows, e.g., extracting PII from forms or automating audits.

🚩 Risks Identified:  
None in the lab — but in real world, document parsing needs secure input handling.

✅ What I Learned:
- How to authenticate with service account using `key.json`
- Use of `curl` to POST base64 PDFs to the API
- Running Document AI with Python client and parsing output
- Confidence scores can indicate data reliability

📂 Screenshots / Evidence:  


💭 Reflection:  
This felt like real-world work. Seeing a raw PDF get turned into structured data automatically was awesome!

---

## 🏆 Leaderboard Status (as of July 24, 2025)

| Metric              | Value               |
|---------------------|---------------------|
| Arcade Username     | `ciril`             |
| Global Rank         | **#8469**           |
| Global XP           | **47,022,890 XP**   |
| Trivia Week 1       | ✅ Completed        |
| Badges Earned       | _None yet_ (ongoing) |
| Labs Completed      | 3 Total ✅          |

---

## 💭 Weekly Reflection

I started from zero and already learned how APIs, cloud environments, and security credentials work together. The Python script part was challenging but fun, and I love how hands-on this journey feels already. Looking forward to earning my first badge next week!

