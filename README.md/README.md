<div align="center">

# 🗂️ Social Media Assistant Agent
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

### System Flow Diagram

```text
                  ┌────────────────────────┐
                  │   Incoming Webhook     │
                  └───────────┬────────────┘
                              │
               ┌──────────────┴──────────────┐
               ▼                             ▼
     ┌───────────────────┐         ┌───────────────────┐
     │   Voice Pipeline  │         │   Text Pipeline   │
     │ (Whisper Engine)  │         │ (Context Parsing) │
     └─────────┬─────────┘         └─────────┬─────────┘
               │                             │
               └──────────────┬──────────────┘
                              ▼
                 ┌─────────────────────────┐
                 │  Agentic Drafting & AI  │
                 │    Image Generation     │
                 └────────────┬────────────┘
                              │
               ┌──────────────┴──────────────┐
               ▼                             ▼
     ┌───────────────────┐         ┌───────────────────┐
     │   Google Drive    │         │   Google Sheets   │
     │  (Asset Hosting)  │         │ (State Logging)   │
     └─────────┬─────────┘         └─────────┬─────────┘
               │                             │
               └──────────────┬──────────────┘
                              ▼
                 ┌─────────────────────────┐
                 │  Social Graph Publishing│
                 └─────────────────────────┘
📸 Workflow Design🗝️ Core CapabilitiesCapabilityTechnical DescriptionMulti-Modal ProcessingNative handling of speech-to-text via OpenAI Whisper & structured text parsing.Agentic Content EngineCustom OpenAI Assistant nodes for contextual copywriting and prompt-driven image synthesis.Interactive Feedback LoopWebhook-driven response mechanisms enabling real-time human-in-the-loop review (Approve vs. Regenerate).Persistent Asset PipelineAutomatic upload, public link generation, and structured audit-logging in Google Suite.Multi-Channel DistributionDynamic payload routing to platform Graph APIs (Facebook & Instagram).🧱 Module Hierarchy1. Webhook & Inbound GatewayMessenger Webhook: Event listener capturing incoming payloads.Route User Action: Stateful switch node determining operational context (initial prompt, revision, or publication command).2. Audio Processing EngineDownload Audio & Transcribe: Downloads incoming binary audio streams and processes them through OpenAI's transcription engine.3. Primary Generation PipelinePost Generator Agent: Synthesizes transcripts or text prompts into high-converting social media copy.Generate Post Image: Generates high-resolution social graphics matched to post context.Cloud Persistence: Stores media in Google Drive, acquires public direct links, and logs metadata to Google Sheets.4. Revision & Iteration EnginePost Regenerator Agent: Executes context-aware rewrites when a draft is rejected by the user.State Synchronizer: Overwrites and syncs modified post drafts in Google Sheets seamlessly.5. Publishing CoreRoute Social Platform: Routes approved content based on designated social channels.Facebook Graph API: Direct production publishing.Instagram Graph API: [Under Active Integration] Reserved node architecture for Instagram media publishing.💎 Integration StackOrchestration: n8nIntelligence Layer: OpenAI (GPT-4o, Whisper, DALL-E 3)Database & Cloud Storage: Google Sheets API, Google Drive APISocial Graph Protocols: Facebook Graph API, Instagram Graph API⚡ Quick Start & DeploymentClone RepositoryBashgit clone [https://github.com/YOUR-USERNAME/Social-Media-Assistant-Agent.git](https://github.com/YOUR-USERNAME/Social-Media-Assistant-Agent.git)
Import WorkflowNavigate to your n8n Dashboard ➔ Workflows ➔ Import from File.Select workflow/Social-Media-Assistant-Agent.json.Configure Environment Credentials
Ensure the following connections are authenticated in your n8n environment:OpenAI API KeyGoogle Drive OAuth2 / Service AccountGoogle Sheets OAuth2 / Service AccountFacebook Graph API Access Token🗓️ Deployment Roadmap[x] Speech-to-Text transcription & automated copywriting pipeline[x] Automated Facebook Graph API publishing engine[x] Interactive user approval & regeneration feedback loops[ ] Instagram Graph API Media Deployment (In Active Progress)[ ] Analytics dashboard for tracking published post performance