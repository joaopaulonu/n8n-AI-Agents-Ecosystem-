# 🤖 n8n AI Agents Ecosystem - Low-Code Automation

![Platform](https://img.shields.io/badge/Platform-n8n-FF6D5A)
![AI Model](https://img.shields.io/badge/AI--Model-Google%20Gemini-4285F4)
![Category](https://img.shields.io/badge/Category-AI%20%26%20Automation-blueviolet)
![Status](https://img.shields.io/badge/Status-Completed-success)
![Workflow](https://img.shields.io/badge/Workflow-Agentic-green)

---

## 📄 Overview

This repository showcases a suite of **4 advanced AI Agents** developed during an intensive week of automation training using **n8n**.

The ecosystem ranges from automated lead nurturing to complex multi-agent orchestration and intelligent document processing (OCR). Each workflow was engineered to solve real-world business challenges, leveraging Large Language Models (LLMs) for logical decision-making, structured data extraction, and multimodal interaction.

---

## 🧠 What is n8n?

**n8n** is a "fair-code" workflow automation tool that allows for deep integration between various apps and services through a visual interface. Unlike purely no-code tools, n8n enables advanced logic via JavaScript and, crucially, provides native nodes for **Agentic AI (LangChain)**.

### Key capabilities demonstrated in this project:
- Building complex workflows with branching logic (If/Else, Switch).
- Integrating AI with short-term and long-term memory.
- Connecting agents to external tools (Google Sheets, Gmail, Telegram, APIs).
- Processing real-time data through Webhooks and Triggers.

---

## 🚀 Developed Agents

### 1. Sales Email Response Agent
Automates initial lead intake by filtering and answering inquiries.
- **Trigger:** `Gmail Trigger` (On Message Received).
- **AI Core:** `AI Agent` powered by **Google Gemini**.
- **Memory:** `Simple Memory` to maintain context across email threads.
- **Key Feature:** Automatically replies using the original message ID to keep conversations organized and professional.

### 2. Refund Analyst Agent
A structured system for processing refund requests by cross-referencing form data with internal records.
- **Trigger:** `Webhook` receiving POST requests from **Tally** forms.
- **Tools:** **Google Sheets** tool to query the "Customer Base" spreadsheet.
- **Intelligence:** Performs sentiment analysis and generates **Structured Output (JSON)**.
- **Logic:** Uses specific JSON fields (value, satisfaction level, timeframes) to drive automated decision-making.

### 3. Multi-Agent Orchestration System
An advanced architecture featuring a "Main Agent" that routes tasks to department-specific specialists.
- **Trigger:** `Telegram Trigger` (Supports both text and voice).
- **Multimodality:** Converts voice notes to text using Gemini's `Transcribe a recording`.
- **Architecture:** The **Orchestrator Agent** evaluates user intent and calls specialized Sub-workflows:
  - 💰 **Financial Agent**
  - 🤝 **CS (Customer Success) Agent**
  - 🛠️ **Support Agent**

### 4. Invoice Processing Agent (OCR)
Focuses on automated data extraction and document classification.
- **Flow:** Downloads attachments via Gmail, uses `Split Out` and `Loop` for batch processing.
- **Analysis:** `Analyze document` node (Gemini/GPT-4o) to extract Vendor, Amount, Date, and Taxes.
- **Storage:** Classifies documents as "Personal" or "Corporate", saves files to specific **Google Drive** folders, and logs metadata in **Google Sheets**.

---

## 🛠️ Technologies & Tools

| Category | Detail |
| :--- | :--- |
| **Automation Platform** | n8n |
| **AI Models** | Google Gemini / GPT-4o |
| **Communication** | Gmail, Telegram |
| **Data & Storage** | Google Sheets, Google Drive |
| **Data Formats** | Structured JSON |
| **Processing** | OCR, Audio Transcription, Loops |

---

## 💡 Concepts Covered

- **Agentic Workflows:** Autonomous agents that decide which tools to use for task completion.
- **Structured Output:** Forcing LLMs to return JSON for reliable downstream automation.
- **Human-in-the-loop:** Architecture ready for human validation before critical actions.
- **RAG (Retrieval-Augmented Generation):** Connecting external knowledge bases to AI prompts.

---

## 🚀 How to Run the Projects

1. Install **n8n** (via Docker or the Desktop app).
2. Import the `.json` workflow files provided in this repository.
3. Configure **Credentials** for the required services:
   - Google Cloud Console (Gmail, Sheets, Drive APIs).
   - Telegram Bot API.
   - AI Provider API Keys (Google Gemini or OpenAI).
4. Activate the Workflows and test by sending an email or a Telegram message.

---

## 📬 Contact Me

<div align="center"> 
  <a href="https://www.linkedin.com/" target="_blank"><img src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white"></a>
  <a href="https://github.com/" target="_blank"><img src="https://img.shields.io/badge/-Github-181717?style=for-the-badge&logo=github&logoColor=white"></a>
  <a href="mailto:your-email@example.com"><img src="https://img.shields.io/badge/-Gmail-%23333?style=for-the-badge&logo=gmail&logoColor=white"></a>
</div>
