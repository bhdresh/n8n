# 🕵️‍♂️ AI-Powered Phishing Domain Detection with n8n, CZDS & Telegram

This project is an automated phishing detection pipeline built on [n8n](https://n8n.io/) that uses AI agents, domain intelligence tools, and real-time messaging to identify and report potential phishing domains derived from CZDS zone files.

---

## 🚀 Features

- 🔍 **CZDS Monitoring**: Automatically parses daily TLD zone files to find domains matching sensitive keywords.
- 🧠 **AI Analysis**: Uses an integrated LangChain agent backed by Ollama (LLM) and OpenAI Vision to analyze both content and visual similarity.
- 🔐 **Recon Tools**: WHOIS, NSLookup, and SSL certificate analysis via `nmap`.
- 📸 **Visual Matching**: Screenshots captured and analyzed using OpenAI Vision to compare against original website layout.
- 📊 **Scoring System**: Assigns confidence score (1–10) and urgency for action.
- 📬 **Real-Time Alerts**: Sends phishing verdicts, screenshots, and explanation directly to Telegram.
- ♻️ **Fully Automated & Scheduled**: Runs daily with no manual input.

---

## 🧠 How It Works

1. **Monitor Keyword**: You provide a brand keyword + original website URL.
2. **Zone File Parsing**: Extracts potential domains from CZDS files.
3. **Website & Domain Recon**:
    - WHOIS lookup
    - NS record resolution
    - SSL certificate inspection
    - Visual screenshot and description
4. **AI Agent Evaluation**:
    - Compares original and suspicious domains.
    - Analyzes similarity, impersonation, SSL type, and content clues.
5. **Verdict & Reporting**:
    - Score from 1–10 with urgency level
    - Final phishing verdict with justification
    - Sends results and images to Telegram
    - Stores phishing domain in a report file

---

## 📦 Tech Stack

| Tool            | Purpose                               |
|-----------------|----------------------------------------|
| `n8n`           | Workflow orchestration (low-code)      |
| `LangChain`     | AI agent with custom prompt            |
| `Ollama`        | Local LLM model (e.g., Qwen2.5:32b)    |
| `OpenAI Vision` | Visual similarity analysis             |
| `urlscan.io`    | Website screenshot + metadata          |
| `nmap`          | SSL certificate check via CLI          |
| `Telegram API`  | Real-time alerting                     |
| `CZDS`          | Central Zone Data Service from ICANN   |

---

## 📸 Demo

📹 **Watch the demo video here**: [👉 Click to view](https://youtu.be/cCaZOshBdnY)

---

