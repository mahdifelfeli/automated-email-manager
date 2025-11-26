# 📧 AI Smart Email Assistant (n8n + Gemini)

## 🚀 Overview
This project is an autonomous **AI Agent** built with **n8n** that manages incoming emails intelligently. Unlike simple auto-responders, this agent uses **Google Gemini** to understand the context, checks my real-time availability via **Google Calendar**, and aligns responses with my personal objectives stored in **Google Sheets**.

## 🧠 Key Features
* **Contextual Understanding:** Uses LLM (Gemini) to categorize emails into `Work` or `Personal`.
* **Calendar Integration (Tool Calling):** Automatically checks Google Calendar for free slots before proposing meeting times.
* **Goal Alignment (RAG):** Consults a knowledge base (Google Sheet) to ensure responses align with defined personal/business goals.
* **Draft Generation:** Creates ready-to-send drafts in Gmail with appropriate labels.

## 🛠️ Tech Stack
* **Orchestration:** [n8n](https://n8n.io/)
* **Model:** Google Gemini (PaLM)
* **Integrations:** Gmail API, Google Calendar API, Google Sheets API
* **Techniques:** Function Calling, Structured Output Parsing (JSON).

## ⚙️ How to Setup

### 1. Prerequisites
You need a Google Sheet to act as the "Goals" database.
1.  Create a new Google Sheet.
2.  Add a column header named **Goals** (A1).
3.  List your goals in the rows below it.

### 2. Import Workflow
1.  Download the `workflow.json` file from this repository.
2.  Open your n8n instance.
3.  Go to **Workflows** > **Import from File** and select the JSON file.

### 3. Configure Credentials
You will need to set up the following credentials in n8n:
* Gmail OAuth2
* Google Calendar OAuth2
* Google Sheets OAuth2
* Google Gemini (PaLM) API Key

### 4. Update Node IDs
* In the **"Goals"** node, select your created Google Sheet.
* In the **"CA"** (Calendar) node, ensure the calendar ID matches your account.

---
*Created by [Your Name]*
