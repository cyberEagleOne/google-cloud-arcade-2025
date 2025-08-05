## 📅 August 5, 2025

---

### 🧩 Project / Lab Title:
**Speech to Text Transcription with the Cloud Speech API**

📆 Date Completed:  
**August 5, 2025**

🔍 Objective:  
To learn the fundamentals of the Cloud Speech-to-Text API by sending an audio file for transcription, configuring the API request for different languages, and interpreting the transcribed text from the API's response.

🔧 Tools/Services Used:
- Cloud Speech-to-Text API
- Cloud Storage
- Cloud Shell
- `curl` command
- JSON

🧠 What I Did:
- Enabled the **Cloud Speech-to-Text API** for my project.
- Created an **API Key** to securely authenticate my requests.
- Uploaded a sample audio file to a **Cloud Storage bucket**, which is a common and efficient way to provide audio sources to the API.
- Constructed a `request.json` file in Cloud Shell. This file contained the `config` object (specifying `encoding`, `sampleRateHertz`, and `languageCode`) and the `audio` object (pointing to the audio file's `uri` in Cloud Storage).
- Used the `curl` command to make a POST request to the Speech-to-Text API endpoint, passing the JSON request file.
- Analyzed the JSON response returned by the API to extract the transcribed text and its associated confidence score.
- Demonstrated the API's multilingual capabilities by modifying the `languageCode` in the request file and transcribing an audio file in a different language.

🛡️ GRC / Compliance Relevance:  
✅ High  
The Speech-to-Text API processes conversational data, which is often highly sensitive, making its use a significant GRC concern.
- **Data Privacy (PII/PHI):** Audio from sources like customer service calls or medical dictations can contain Personally Identifiable Information (PII) or Protected Health Information (PHI). Transcribing this data requires strict adherence to privacy regulations like GDPR, CCPA, and HIPAA.
- **E-Discovery and Legal Compliance:** Transcriptions of official communications (e.g., voicemails, meeting recordings) can become legal records subject to e-discovery. The accuracy and secure storage of these transcriptions are critical.
- **Access Control & Auditing:** As with any service handling sensitive data, it's crucial to use IAM to restrict who can submit audio and access transcriptions, and to maintain detailed audit logs of all API interactions.

🚩 Risks Identified:  
- **Transcription Inaccuracy:** The API's accuracy can be affected by poor audio quality, background noise, strong accents, or specialized terminology. Relying solely on automated transcripts for critical decisions (legal, medical) without human review is risky.
- **Sensitive Data Exposure:** If the original audio or the resulting text transcripts are stored in an insecure bucket or database, this could lead to a breach of highly sensitive conversational data.
- **Cost Overruns:** The API is priced per minute of audio processed. Transcribing large volumes of audio without monitoring and cost controls can lead to significant, unexpected expenses.

✅ What I Learned:
- The **Cloud Speech-to-Text API** is a powerful ML service that converts spoken audio to written text.
- API requests are made via a **JSON payload** that specifies the `config` (how to process the audio) and the `audio` source.
- The `config` object's `languageCode` parameter is essential for telling the API which language model to use for transcription.
- Providing audio via a **Cloud Storage URI** (`gs://...`) is an efficient method for processing audio files, especially large ones.
- The API's ability to handle over 80 languages makes it a versatile tool for building global applications.

💭 Reflection:  
This was another fantastic dive into Google's AI/ML APIs. It’s remarkable how a process as complex as speech recognition can be accessed through a straightforward API call. The lab did a great job of demystifying the process by having me build the JSON request manually. I can clearly see how this technology powers everyday applications like voice assistants, automated customer service bots, and real-time captioning services. It's a powerful tool for converting unstructured audio data into valuable, searchable text.

---

## 🏆 Leaderboard Status (as of August 5, 2025)

| Metric                              | Value                                                                                                                                                                                                                                                                                             |
| :---------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Arcade Username                     | `ciril`                                                                                                                                                                                                                                                                                           |
| **---COMPLETED---** |                                                                                                                                                                                                                                                                                                   |
| Arcade Games lvl 1 (Infrastructure) | ✅ **Finished (12/12 Labs)** 🎉                                                                                                                                                                                                                                                                   |
| Trivia Week 1                       | ✅ **Finished (4/4 Labs)** 🎉                                                                                                                                                                                                                                                                     |
| Trivia Week 2                       | ✅ **Finished (3/3 Labs)** 🎉                                                                                                                                                                                                                                                                     |
| **---IN PROGRESS---** |                                                                                                                                                                                                                                                                                                   |
| Arcade Games lvl 1 (App Design)     | ✅ Completed (1/12 Labs)                                                                                                                                                                                                                                                                          |
| Global App Design Lvl 1 Rank        | **#604** |
| Global App Design Lvl 1 XP          | **39,387,388 XP** |
| **---OVERALL---** |                                                                                                                                                                                                                                                                                                   |
| Badges Earned                       | [🏅 Week 1 Trivia Badge](https://www.cloudskillsboost.google/public_profiles/c8fd48a4-987d-4216-9635-d49fa00793da/badges/17140064), [🏆 Level 1 Game Badge](https://www.cloudskillsboost.google/public_profiles/c8fd48a4-987d-4216-9635-d49fa00793da/badges/17245038), [🏅 Week 2 Trivia Badge](https://www.cloudskillsboost.google/public_profiles/c8fd48a4-987d-4216-9635-d49fa00793da/badges/17274275) |
| League Standing                     | 5th – Silver League (1706 pts)                                                                                                                                                                                                                                                                    |
| Promotion Status                    | 🟢 Gold League Promo                                                                                                                                                                                                                                                                              |
