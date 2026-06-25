# 🚀 AI-Powered Content Creator Agent (n8n)

## 📌 Project Overview

This project demonstrates a **no-code AI-powered content creation agent** built using **n8n**. The workflow automates the entire content pipeline — from identifying topics to generating platform-specific content — enabling fast, scalable, and high-quality content creation without manual effort.

---

## 🎯 Objective

To design and implement an automated workflow that:

* Fetches trending topics from Google Sheets
* Performs real-time research using Tavily API
* Generates AI-powered content for:

  * LinkedIn
  * X (Twitter)
  * Blog Summary
* Updates results back into Google Sheets

---

## ⚙️ Tech Stack

* **n8n** – Workflow automation platform
* **Google Sheets API** – Input & output storage
* **Tavily API** – Real-time web research
* **Google Gemini API** – AI content generation

---

## 🔑 APIs Used

* Tavily Search API
* Google Gemini API

> ⚠️ Note: API keys are not included for security reasons.

---

## 📊 Input Source (Google Sheets)

The workflow uses a structured Google Sheet with the following columns:

| Column Name    | Description                |
| -------------- | -------------------------- |
| Topic          | Content topic              |
| Status         | Pending / Completed        |
| Linkedin_post  | Generated LinkedIn content |
| X_post         | Generated Twitter content  |
| Blog_summary   | Generated blog summary     |
| Published_Date | Timestamp                  |

---

## 🔄 Workflow Architecture

### Step-by-Step Flow:

1. **Google Sheets Node**

   * Fetch rows where `Status = Pending`

2. **Tavily API (HTTP Request)**

   * Perform real-time research on the topic

3. **Split Out Node**

   * Split multiple search results

4. **Function Node**

   * Aggregate and clean research content

5. **Gemini AI Nodes (3 Separate Nodes)**

   * Generate platform-specific content:

     * LinkedIn Post (professional tone)
     * X Post (short & engaging)
     * Blog Summary (150–200 words)

6. **Google Sheets Update Node**

   * Update:

     * Generated content
     * Status → Completed
     * Published_Date → Timestamp

---

## 🧠 Prompt Design

### 🔹 LinkedIn Prompt

* Professional tone
* 120–150 words
* Includes hashtags

### 🔹 X (Twitter) Prompt

* Under 280 characters
* Concise and engaging
* Includes hashtags

### 🔹 Blog Summary Prompt

* 150–200 words
* Informative and structured

---

## ✅ Sample Input

```
Topic: AI Agents in Business  
Status: Pending
```

---

## ✅ Sample Output

### LinkedIn Post

AI agents are transforming modern businesses by automating repetitive tasks, improving efficiency, and enabling smarter decision-making...

### X Post

AI agents are reshaping businesses by automating tasks and boosting efficiency 🚀 #AI #Automation

### Blog Summary

AI agents are rapidly becoming a core component of modern enterprises. They help streamline workflows, reduce operational costs, and improve productivity...

---

## 🧪 Testing & Validation

* Workflow tested with multiple topics
* Outputs verified for:

  * Accuracy
  * Relevance
  * Formatting

---

## 📸 Workflow Screenshot

![Workflow png](./workflow%20screenshot.png)

---

## 📁 Files Included

* `workflow.json` – Exported n8n workflow
* `README.md` – Project documentation
* Workflow screenshot

---

## 🎉 Conclusion

This project successfully demonstrates how **no-code automation + AI** can be combined to build a scalable content creation system. It highlights real-world applications in marketing, education, and digital content strategies.

---

## 💡 Future Improvements

* Auto-posting to LinkedIn/X
* Scheduling system
* Content personalization
* Multi-language support

---

## 🙌 Author

**Swarup Karthik S**
B.Tech AI & DS
--------------
