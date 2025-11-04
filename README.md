
# ⚡ **AgentForge**

### **The Free, Multi-Model AI Agent Workspace — Built on Base44**

**RAG • Agents • LLM Orchestration • Document Intelligence • Multi-Model Switching • Vector Search • Drag-Drop Agent Builder**

🔗 **Base44 Workspace:**
[https://app.base44.com/apps/6900d52013af49ef876418bf/editor/preview/Landing](https://app.base44.com/apps/6900d52013af49ef876418bf/editor/preview/Landing)

🔗 **Live Deployed App:**
[https://agent-forge-876418bf.base44.app](https://agent-forge-876418bf.base44.app)

---

# 🚀 Overview

**AgentForge** is a **full-stack AI operating system** designed for developers, analysts, startups, and enterprises.
It brings **RAG**, **Agent Execution**, **Multi-Model Chat**, **Document Intelligence**, **Embeddable Widgets**, and a **Luxury UI**—all built **100% free** using **Base44 + Hugging Face**.

✅ No backend configuration
✅ No infrastructure cost
✅ Entirely free model usage via HF Inference
✅ 100% Web + Cloud, runs instantly

---

# 🧠 Core Features

## ✅ **1. Multi-Model AI Chat Workspace**

* Switch instantly between models (Gemma, Llama, Mistral, Zephyr, Qwen, etc.)
* Temperature, max_tokens controls
* Context-aware chat
* Source-attached responses
* Luxury dual-column UI with conversation list

---

## ✅ **2. RAG Document Intelligence**

* Upload PDFs/docs
* Automatic chunking (2k–3k tokens)
* Embedding generation
* Vector search retrieval
* Source highlighting & contextual answers
* Per-document status, chunk count tracking

---

## ✅ **3. AI Agent Builder (Drag & Drop)**

Create advanced multi-step AI workflows:

🔹 Search
🔹 Webhook
🔹 Calculator
🔹 Database Query
🔹 Follow-up LLM Reasoning
🔹 Condition blocks
🔹 Flow branching

Store flows as reusable **AgentFlow** entities.

---

## ✅ **4. Model Manager + Tier System**

Add unlimited custom models:

* HF Models
* HF Spaces Predict
* Self-hosted / custom endpoint
* Tier tags: Economy / Standard / Premium
* Model tiles display: context window, latency, pricing tier

---

## ✅ **5. Team Workspaces**

* Team collaboration
* User roles
* Usage quota
* Billing simulation
* Usage analytics

---

## ✅ **6. Admin Dashboard**

* Total API calls
* Vector usage
* Document ingestion stats
* Model usage heatmaps
* Conversation metadata

---

## ✅ **7. Embedded Chat Widget**

Copy-paste HTML snippet to embed AgentForge chat in ANY website:

```html
<iframe 
  src="https://agent-forge-876418bf.base44.app/embed_chat?token={{YOUR_TOKEN}}" 
  width="420" 
  height="600">
</iframe>
```

---

# 🧩 System Architecture

## ✅ **1. Frontend (Base44 UI Engine)**

* React
* TypeScript
* Tailwind CSS
* Recharts
* Cloud Storage
* Real-time React Query patterns

---

## ✅ **2. Database Entities (8 Total)**

### **User**

* Email, name, role
* Team
* Profile photo
* API key

### **Team**

* Team name
* Billing plan
* Quota
* Members

### **Document**

* PDF/DOC file
* Owner
* Status (processing/ready)
* Chunk count

### **VectorChunk**

* Chunk ID
* Document
* Embedding vector
* Snippet text

### **Conversation**

* Model used
* Full message history
* Sources
* Timestamp

### **ModelConfig**

* Name
* Endpoint
* Context window
* Tier

### **AgentFlow**

* Steps array
* Owner
* Config

### **UsageRecord**

* Calls
* Tokens
* Team
* Model

---

# 🤖 AI / ML Models Used (Hugging Face)

## ✅ **Chat / Reasoning Models**

* `google/gemma-7b`
* `mistralai/Mistral-7B-Instruct`
* `meta-llama/Llama-3-8b`
* `HuggingFaceH4/zephyr-7b-beta`
* `Qwen/Qwen2-7B-Instruct`
* `tiiuae/falcon-7b`

---

## ✅ **Embeddings (RAG)**

* `sentence-transformers/all-MiniLM-L6-v2`
* `BAAI/bge-base-en`
* `intfloat/e5-base-v2`

---

## ✅ **Document Processing**

* HF Feature Extraction API
* Built-in tokenizer for chunking
* Local vector storage or Pinecone/Weaviate ready

---

## ✅ **Moderation**

* `facebook/roberta-hate-speech-detection`
* `openai-community/content-moderation`

---

# 🛠️ Backend Logic

## ✅ **1. chat_infer Workflow**

Steps:

1. Receive user message
2. Run moderation
3. If retrieval needed → embeddings → vector search
4. Assemble contextual prompt
5. Call HF Inference
6. Save conversation
7. Return result + sources

---

## ✅ **2. docs_ingest Workflow**

1. Upload file
2. Chunk document
3. Generate embeddings for each chunk
4. Store chunks
5. Update document metadata

---

## ✅ **3. agent_execute Workflow**

Executes structured JSON:

```json
{
  "action": "webhook",
  "params": {"url": "https://api.example.com", "payload": {}},
  "continue": true
}
```

Runs action → sends result back to LLM → loops until done.

---

# 🎨 UI/UX Design (Luxury Theme)

✅ Ivory / Charcoal / Gold palette
✅ Soft shadows (md & xl)
✅ Rounded-2xl cards
✅ 24px grid spacing
✅ Animated transitions
✅ Sticky model selection bar
✅ On-scroll fade reveals
✅ Hero section with 3 value cards

---

# 🧰 Tech Stack

## ✅ **Frontend / UI**

* React
* TypeScript
* Tailwind CSS
* React Query
* Recharts
* Lucide Icons
* Base44 Components

---

## ✅ **Backend / Logic**

* Base44 Server Workflows
* Base44 Database
* Optional external:
  ✅ Pinecone
  ✅ Weaviate
  ✅ Vercel Proxy

---

## ✅ **AI Integrations**

* Hugging Face Inference API
* Hugging Face Spaces Predict
* HF Embeddings API

**All used in free tier.**

---

# 🌐 API Connectors (Configured in Base44)

### ✅ HF_Inference

```
POST https://api-inference.huggingface.co/models/{{HF_MODEL}}
```

### ✅ HF_Spaces_Predict

```
POST https://huggingface.co/spaces/{{OWNER}}/{{SPACE}}/api/predict
```

### ✅ HF_Embeddings

```
POST https://api-inference.huggingface.co/pipeline/feature-extraction/{{MODEL}}
```

---

# 📦 Pages in the App

### ✅ Landing

Hero, features, call-to-action, model showcase.

### ✅ Dashboard

Usage charts, quick stats, model analytics.

### ✅ Workspace

Chat interface + context panel + conversation list.

### ✅ DocsUpload

Upload files, track ingestion, document status.

### ✅ ModelManager

Add/manage models, configure endpoints, tiers.

### ✅ AgentBuilder

Flow-based visual builder for AI agents.

### ✅ Admin

Team management + global analytics + usage limits.

---

# 📊 Usage Analytics

* API calls by model
* Tokens consumed
* Document count
* User activity
* Agent executions
* Vector chunk count

---

# 🧩 Embeddable Chat Widget

```html
<iframe 
  src="https://agent-forge-876418bf.base44.app/embed_chat?token={{YOUR_TOKEN}}" 
  width="420" 
  height="600">
</iframe>
```

---

# ✅ Future Enhancements (Roadmap)

* Memory system for agents
* Marketplace for flows
* API access for external apps
* Plugin ecosystem
* Real-time collaboration
* Prompt library

---**GitHub repository folder structure**, just tell me—I can generate all of them.
