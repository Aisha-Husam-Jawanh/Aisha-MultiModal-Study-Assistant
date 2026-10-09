# 🤖 Multi-Modal AI Study Assistant Bot

[![Try Bot on Telegram](https://img.shields.io/badge/Telegram-Try%20Bot%20Live-2CA5E0?style=for-the-badge&logo=telegram)](https://t.me/Aisha_Study_Bot)

An automated multi-modal study assistant built using **n8n**, **OpenAI API**, and **Telegram API**. It seamlessly ingests study materials across multiple modalities (Text, PDFs, Book Images via OCR, and Voice Notes via Whisper) and automatically returns comprehensive summaries alongside 10 interactive revision questions with model answers.

---

## 📐 Workflow Architecture

![n8n Workflow Architecture](Screenshot%202026-10-09%20142355.png)

---

## ✨ Key Features & Capabilities

- **🔀 Multi-Modal Routing:** Intelligent `Switch` routing node that processes incoming Telegram messages based on content type:
  - **PDF Documents:** Extract text automatically using PDF parsing nodes.
  - **Images & Book Pages:** High-accuracy OCR & vision processing for handwritten/printed book photos.
  - **Voice Notes:** Audio transcription utilizing OpenAI's Whisper model.
  - **Plain Text:** Direct study material intake.
- **📚 Smart Summary & Quiz Generation:** Prompt-engineered processing to produce structured bullet-point summaries and 10 targeted Multiple Choice Questions (MCQs) with full answer keys.
- **⚡ Automated Delivery:** Formatted response splitting and immediate dispatch back to the user via Telegram Bot API.

---

## 🛠️ Built With

- **n8n:** Workflow Orchestration & Node Routing
- **OpenAI API:** GPT-4o Vision & Audio Transcription (Whisper)
- **Telegram Bot API:** User Interface & Media Webhooks
- **JSON:** Exportable Workflow Definition

---

## 🚀 How to Import into n8n

1. Clone or download this repository.
2. Locate the `workflow.json.json` file in the repository root.
3. In your n8n workspace, click **Import from file** and select `workflow.json.json`.
4. Configure your Telegram Bot credentials and OpenAI API keys in the respective nodes.
