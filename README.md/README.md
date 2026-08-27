# 🗂️ Social-Media-Assistant-Agent

### An Autonomous AI-Powered Content Creation & Publishing Workflow built with n8n

<p align="center">

[![n8n](https://img.shields.io/badge/Orchestrator-n8n-FF6D5A?style=for-the-badge\&logo=n8n\&logoColor=white)](https://n8n.io/)
[![OpenAI](https://img.shields.io/badge/AI-OpenAI-412991?style=for-the-badge\&logo=openai\&logoColor=white)](https://openai.com/)
[![Google Drive](https://img.shields.io/badge/Storage-Google_Drive-4285F4?style=for-the-badge\&logo=googledrive\&logoColor=white)](https://drive.google.com/)
[![Meta](https://img.shields.io/badge/API-Meta_Graph_API-0866FF?style=for-the-badge\&logo=facebook\&logoColor=white)
](https://developers.facebook.com/)
[![Status](https://img.shields.io/badge/Status-Production_Ready-22C55E?style=for-the-badge)

</p>

---

## 📖 Overview

**Social-Media-Assistant-Agent** is a complete AI automation workflow built with **n8n** that transforms simple text prompts or voice notes into production-ready social media posts.

The workflow automates the entire content pipeline:

* 🎤 Speech-to-Text with OpenAI Whisper
* ✍️ AI Copywriting using GPT-4o
* 🎨 AI Image Generation
* ☁️ Google Drive Storage
* 📊 Google Sheets Database
* 💬 Human Approval Loop
* 🚀 Facebook Publishing
* 📱 Instagram Publishing *(Coming Soon)*

---

# 📸 Workflow Overview

![Workflow Overview](Screenshots/Social-Media-Assistant-Agent.jpeg)

---

# 🏗️ Architecture

| Layer              | Technology         |
| ------------------ | ------------------ |
| User Interface     | Meta Messenger     |
| Orchestration      | n8n                |
| Speech Recognition | OpenAI Whisper     |
| AI Copywriting     | GPT-4o             |
| Image Generation   | OpenAI Images      |
| Database           | Google Sheets      |
| Cloud Storage      | Google Drive       |
| Publishing         | Facebook Graph API |

---

# ⚙️ Features

## 🎤 Speech-to-Text

Automatically transcribes incoming voice notes into clean text using OpenAI Whisper.

---

## ✍️ AI Copywriting

Generates platform-optimized captions including:

* Hooks
* Storytelling
* Calls-to-Action
* Hashtags
* Emojis

---

## 🎨 AI Image Generation

Creates context-aware AI images matching the generated content.

---

## ☁️ Asset Management

Automatically uploads generated images to Google Drive and creates shareable links.

---

## 📊 Content Database

Stores every generated post inside Google Sheets including:

* Caption
* Image URL
* Status
* Timestamp

---

## 🔄 Human-in-the-Loop Approval

Users can review generated posts before publishing.

Supported actions:

* ✅ Approve
* 🔄 Regenerate

Rejected posts are automatically regenerated while preserving workflow state.

---

## 🚀 Facebook Publishing

Publishes approved content directly using the Facebook Graph API.

---

## 📱 Instagram Integration

Instagram publishing pipeline is currently under development.

---

# 🔄 Workflow Lifecycle

```text
User (Voice/Text)
        │
        ▼
Messenger Webhook
        │
        ▼
Route User Action
        │
        ├─────────────── New Post ───────────────┐
        │                                        │
        ▼                                        │
Whisper Speech-to-Text                           │
        │                                        │
        ▼                                        │
GPT-4o Content Generator                         │
        │                                        │
        ▼                                        │
AI Image Generation                              │
        │                                        │
        ▼                                        │
Google Drive Upload                              │
        │                                        │
        ▼                                        │
Google Sheets Logging                            │
        │                                        │
        ▼                                        │
Messenger Review                                 │
        │                                        │
   ┌────┴────┐                                   │
   │         │                                   │
Approve   Regenerate                             │
   │         │                                   │
   ▼         ▼                                   │
Facebook   Rewrite + New Image                   │
```

---

# 📂 Repository Structure

```text
Social-Media-Assistant-Agent
│
├── README.md
│
├── workflow
│   └── Social-Media-Assistant-Agent.json
│
├── Screenshots
│   └── Social-Media-Assistant-Agent.png
│
└── assets
```

---

# 🔌 Integrations

* ✅ n8n
* ✅ OpenAI GPT-4o
* ✅ OpenAI Whisper
* ✅ OpenAI Image Generation
* ✅ Google Drive API
* ✅ Google Sheets API
* ✅ Meta Messenger Webhooks
* ✅ Facebook Graph API
* 🚧 Instagram Graph API

---

# 🎯 Use Cases

Perfect for:

* Personal Brands
* Content Creators
* Marketing Agencies
* Small Businesses
* E-commerce Stores
* Corporate Communications
* Podcast Repurposing
* Video Content Automation

---

# 🚀 Installation

## 1. Clone Repository

```bash
git clone https://github.com/omar-n8n/Social-Media-Assistant-Agent.git
```

---

## 2. Import Workflow

Open your **n8n** instance.

Navigate to:

```
Workflows
→ Import from File
```

Import:

```
workflow/Social-Media-Assistant-Agent.json
```

---

## 3. Configure Credentials

Configure the following credentials:

* OpenAI API
* Google Drive OAuth
* Google Sheets OAuth
* Meta Developer Credentials
* Facebook Page Token

---

## 4. Activate Workflow

Enable the workflow to start receiving Messenger requests.

---

# 📦 Requirements

* n8n (Cloud or Self-hosted)
* OpenAI API Key
* Google Cloud Project
* Google Drive API
* Google Sheets API
* Meta Developer Account
* Facebook Graph API Access

---

# 📈 Roadmap

* [x] Speech-to-Text
* [x] AI Copywriting
* [x] AI Image Generation
* [x] Google Drive Integration
* [x] Google Sheets Logging
* [x] Human Approval Workflow
* [x] Facebook Publishing
* [ ] Instagram Publishing
* [ ] Scheduled Posts
* [ ] Analytics Dashboard
* [ ] Multi-Platform Publishing
* [ ] LinkedIn Integration
* [ ] Telegram Integration
* [ ] WhatsApp Integration

---

# 💡 Tech Stack

* n8n
* OpenAI GPT-4o
* OpenAI Whisper
* OpenAI Images
* Google Drive
* Google Sheets
* Meta Graph API
* Messenger Webhooks
* REST APIs

---

# 📄 License

This repository is intended for educational and portfolio purposes.

Feel free to explore the workflow architecture and adapt it for your own automation projects.

---

# 👨‍💻 Author

## Omar Ali Osman

**AI Automation Developer**

I build intelligent AI automation systems using:

* AI Agents
* n8n
* OpenAI APIs
* API Integrations
* Workflow Automation
* Webhooks

### Connect with me

**GitHub**

https://github.com/omar-n8n

**LinkedIn**

https://www.linkedin.com/in/omar-ali-007000379/

---

<div align="center">

### ⭐ If you found this project useful, consider giving it a Star!

**Built with ❤️ using n8n & OpenAI**

</div>
