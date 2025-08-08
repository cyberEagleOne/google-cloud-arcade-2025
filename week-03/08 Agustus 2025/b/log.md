## 📅 August 8, 2025

---

### 🧩 Project / Lab Title:
**Getting Started with Liquid to Customize the Looker User Experience**

📆 Date Completed:  
**August 8, 2025**

🔍 Objective:  
To learn how to use the **Liquid** templating language within Looker's LookML layer to create dynamic, interactive, and visually customized user experiences in data explorations and dashboards.

🔧 Tools/Services Used:
- Looker
- LookML (Looker's data modeling language)
- Liquid templating language

🧠 What I Did:
- Entered Looker's **Development Mode** to edit the underlying LookML code for a data model.
- Modified a dimension by adding a `link` parameter. Within this parameter, I used **Liquid syntax** (e.g., `{{ value }}`) to dynamically insert the dimension's value into a URL, effectively creating a custom link for each row of data (for example, to perform a Google search).
- I also experimented with creating links that navigate to other Looker dashboards, passing the current value as a filter to create interactive drill-down paths.
- Next, I used the `html` parameter on a dimension or measure. Inside this, I wrote Liquid conditional logic (`{% if ... %}`) combined with HTML tags to change how data was displayed. For example, I color-coded numerical values based on whether they were above or below a certain threshold.
- I saved and validated my LookML code and then explored the data in Looker to see my custom links and conditional HTML formatting in action.

🛡️ GRC / Compliance Relevance:  
✅ Low  
This feature is primarily for enhancing User Experience (UX), but it has indirect GRC applications:
- **Data Clarity for Compliance:** Using Liquid to conditionally highlight data that falls outside of compliance thresholds (e.g., coloring a transaction red if it exceeds a certain limit) can make compliance-related dashboards much more effective for oversight.
- **Governed Navigation:** By creating pre-defined `link` parameters, data governors can guide users to sanctioned reports and external resources, ensuring a more controlled and consistent data analysis experience.

🚩 Risks Identified:  
- **Broken Logic:** An error in the Liquid syntax within an `html` or `link` parameter can lead to broken links or improperly rendered data, which can confuse users and reduce trust in the dashboard.
- **Over-Customization:** Excessive use of custom colors, fonts, and HTML can make reports cluttered and less readable, defeating the purpose of data visualization.
- **Maintenance Overhead:** Heavily customized LookML can be more difficult to maintain and debug over time compared to standard LookML.

✅ What I Learned:
- **Liquid** is a powerful templating language that can be used directly within **LookML** to inject dynamic logic into dimensions, measures, and other objects.
- The `{{ value }}` syntax is used to reference the raw data value of a field.
- The **`link` parameter** allows for the creation of dynamic hyperlinks on a per-row basis, perfect for linking to external tools or other Looker content.
- The **`html` parameter** gives complete control over the rendering of a data point, enabling powerful conditional formatting using HTML and Liquid's `if/else` logic.

💭 Reflection:  
This lab was a fantastic glimpse into the power of Looker beyond simple charts and tables. Using Liquid felt like I was "programming" my data model to be smarter and more helpful to the end-user. The ability to create a custom, data-driven link for every row is an incredibly practical feature that can turn a static report into an actionable workflow. Similarly, using HTML to color-code results makes identifying important data points instantaneous. This lab shows how Looker can be used to build not just dashboards, but true custom data applications.

---

## 🏆 Leaderboard Status (as of August 8, 2025)

| Metric                              | Value                                                                                                                                                                                                                                                                                             |
| :---------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Arcade Username                     | `ciril`                                                                                                                                                                                                                                                                                           |
| **---COMPLETED---** |                                                                                                                                                                                                                                                                                                   |
| Arcade Games lvl 1 (Infrastructure) | ✅ **Finished (12/12 Labs)** 🎉                                                                                                                                                                                                                                                                   |
| Trivia Week 1                       | ✅ **Finished (4/4 Labs)** 🎉                                                                                                                                                                                                                                                                     |
| Trivia Week 2                       | ✅ **Finished (3/3 Labs)** 🎉                                                                                                                                                                                                                                                                     |
| **---IN PROGRESS---** |                                                                                                                                                                                                                                                                                                   |
| Arcade Games lvl 1 (App Design)     | ✅ Completed (1/12 Labs)                                                                                                                                                                                                                                                                          |
| Trivia August Week 1                | ✅ Completed (2/4 Labs)                                                                                                                                                                                                                                                                           |
| Global Trivia Aug W1 Rank           | **#4761** |
| Global Trivia Aug W1 XP             | **42,686,229 XP** |
| **---OVERALL---** |                                                                                                                                                                                                                                                                                                   |
| Badges Earned                       | [🏅 Week 1 Trivia Badge](https://www.cloudskillsboost.google/public_profiles/c8fd48a4-987d-4216-9635-d49fa00793da/badges/17140064), [🏆 Level 1 Game Badge](https://www.cloudskillsboost.google/public_profiles/c8fd48a4-987d-4216-9635-d49fa00793da/badges/17245038), [🏅 Week 2 Trivia Badge](https://www.cloudskillsboost.google/public_profiles/c8fd48a4-987d-4216-9635-d49fa00793da/badges/17274275) |
| League Standing                     | 17th – Silver League (254 pts)                                                                                                                                                                                                                                                                   |
| Promotion Status                    | ⚪️ Stable                                                                                                                                                                                                                                                                                       |
