<div align="center">

# 🗂️ Social-Media-Assistant-Agent
### An Intelligent, Multi-Modal Automation & Content Generation Pipeline

[![n8n](https://img.shields.io/badge/Orchestrator-n8n-FF6D5A?style=for-the-badge&logo=n8n&logoColor=white)](https://n8n.io/)
[![OpenAI](https://img.shields.io/badge/AI_Engine-OpenAI_GPT--4o-412991?style=for-the-badge&logo=openai&logoColor=white)](https://openai.com/)
[![Google Drive](https://img.shields.io/badge/Storage-Google_Drive-4285F4?style=for-the-badge&logo=googledrive&logoColor=white)](https://drive.google.com/)
[![Status](https://img.shields.io/badge/Build-Production_Ready-emerald?style=for-the-badge)]()

<p align="center">
  A sophisticated end-to-end automation system designed to capture raw voice & text inputs, orchestrate generative AI post drafting, manage asset storage, and execute social media publication.
</p>

</div>

---

## 🏛️ Architecture Overview

The pipeline leverages an event-driven architecture built on **n8n**, orchestrating modular agents for transcription, visual composition, state management, and API-based social publishing.

<div align="center">

| Gateway Stage | AI Processing | Data Storage | Publishing Layer |
| :---: | :---: | :---: | :---: |
| <b>Messenger Webhook</b> | <b>OpenAI Whisper</b> <br><i>(Audio Transcribe)</i> | <b>Google Drive</b> <br><i>(Media Assets)</i> | <b>Facebook API</b> <br><i>(Live Post)</i> |
| <b>Action Switch</b> | <b>GPT-4o Agent</b> <br><i>(Text Generation)</i> | <b>Google Sheets</b> <br><i>(Row Database)</i> | <b>Instagram API</b> <br><i>(In Development)</i> |

</div>

---

## 📸 Workflow Design

<div align="center">
  <img src="screenshots/workflow-overview.png" alt="System Workflow Diagram" width="100%" style="border-radius: 8px; border: 1px solid #30363d;">
</div>

---

## 🗝️ Core Capabilities

| Capability | Technical Description |
| :--- | :--- |
| **Multi-Modal Processing** | Native handling of speech-to-text via OpenAI Whisper & structured text parsing. |
| **Agentic Content Engine** | Custom OpenAI Assistant nodes for contextual copywriting and prompt-driven image synthesis. |
| **Interactive Feedback Loop** | Webhook-driven response mechanisms enabling real-time human-in-the-loop review (*Approve* vs. *Regenerate*). |
| **Persistent Asset Pipeline** | Automatic upload, public link generation, and structured audit-logging in Google Suite. |
| **Multi-Channel Distribution** | Dynamic payload routing to platform Graph APIs (*Facebook & Instagram*). |

---

## 🧱 Module Hierarchy

### 1. Webhook & Inbound Gateway
- **`Messenger Webhook`**: Event listener capturing incoming payloads.
- **`Route User Action`**: Stateful switch node determining operational context (initial prompt, revision, or publication command).

### 2. Audio Processing Engine
- **`Download Audio & Transcribe`**: Downloads incoming binary audio streams and processes them through OpenAI's transcription engine.

### 3. Primary Generation Pipeline
- **`Post Generator Agent`**: Synthesizes transcripts or text prompts into high-converting social media copy.
- **`Generate Post Image`**: Generates high-resolution social graphics matched to post context.
- **`Cloud Persistence`**: Stores media in Google Drive, acquires public direct links, and logs metadata to Google Sheets.

### 4. Revision & Iteration Engine
- **`Post Regenerator Agent`**: Executes context-aware rewrites when a draft is rejected by the user.
- **`State Synchronizer`**: Overwrites and syncs modified post drafts in Google Sheets seamlessly.

### 5. Publishing Core
- **`Route Social Platform`**: Routes approved content based on designated social channels.
- **`Facebook Graph API`**: Direct production publishing.
- **`Instagram Graph API`**: *[Under Active Integration]* Reserved node architecture for Instagram media publishing.

---

## 💎 Integration Stack

* **Orchestration**: `n8n`
* **Intelligence Layer**: `OpenAI (GPT-4o, Whisper, DALL-E 3)`
* **Database & Cloud Storage**: `Google Sheets API`, `Google Drive API`
* **Social Graph Protocols**: `Facebook Graph API`, `Instagram Graph API`

---

## ⚡ Quick Start & Deployment

1. **Clone Repository**
   ```bash
   git clone [https://github.com/YOUR-USERNAME/Social-Media-Assistant-Agent.git](https://github.com/YOUR-USERNAME/Social-Media-Assistant-Agent.git)