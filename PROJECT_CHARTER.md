# 📍 PROJECT_CHARTER.md – *SkimKnow: Your Knowledge Briefcase*

---

## 💡 Problem Statement

Information is power. Yet it seems to be scattered everywhere — in many places, in many forms — and we never seem to get enough of it. There's an inherent greed in knowing stuff, especially in not missing out, in not letting it slip through our fingers.

The result? Tabs that are never read or closed, countless "wanna read" documents, “someday I'll refer” videos and links that never saw the light of day... just overloading, uncomprehended pieces of knowledge. And we don’t seem to have time for all of it. 

What’s important, what’s redundant, what to miss and what not to miss – where do we find a balance in this rhythm?

That is where **SkimKnow** steps in — an intelligent knowledge synthesis system. It's your AI-powered content assistant, helping you merge, organize, and reduce overload by transforming scattered data into insightful summaries in various usable formats.

---

## ✨ Vision & Objective

**SkimKnow** is your smart briefcase for knowledge. It helps users:

- Import content from multiple sources (text, documents, links, videos, audio, images)
- Summarize them instantly using AI
- Store and organize summaries into folders
- Merge, tag, and search through knowledge easily

SkimKnow transforms scattered inputs into clean, structured, and editable summaries. It's not about consuming *more*, it's about consuming *cleverly*.

---

## 🗖️ Scope & Deliverables

### ✅ Phase 1: MVP

#### Input Modes
We allow users to input content through the following modes:

- **Paste-based text input**: Users can paste raw text directly into the UI.
- **Document upload**: Supports PDF and Word file uploads.
- **Drag-and-drop media**: Supports image (with OCR), and audio files.
- **Link input**: Accepts publicly accessible article or YouTube URLs for summarization.

These inputs form the foundation for processing content via the AI engine.

#### Summary Types & Output Formats
SkimKnow provides the following **output formats and summary types**, displayed as selectable **summary tabs** in the UI:

- ✍️ **Editable summaries** shown directly in the UI
- 📄 **Downloadable formats**: PDF and Word for export
- 📂 **Summary tabs** (selectable by user):
  - TL;DR
  - General Overview
  - Chronological Summary

Each summary tab represents a unique summarization strategy. Users can switch between views to suit their needs. The summaries are editable in-line for final tweaks before export.

#### File/Folder Management
- Create, Rename, Delete folders
- Drag-and-drop file reordering
- Move summaries across folders

#### Search
- Keyword-based search within stored summaries

---

### 🚀 Phase 2 (Planned Features)

#### Input Enhancements
- Google Drive import (Docs, Sheets, Slides)
- Chrome extension for browser tab summarization
- Batch file processing
- Email inbox integration for newsletters & subscriptions
- YouTube transcript auto-detection
- Image-to-summary (via OCR and captioning)
- Audio summarization with speaker tagging and timestamps

#### Output Enhancements
- Markdown, Flashcards, Excel, Infographics
- Timeline mode, Story mode, Dashboard mode
- Multi-format export: Image, JSON, Presentation
- Personalized Learning Mode (for Students & ADHD users)
- Export to Notion, Obsidian, OneNote

#### Organization & UX
- Smart merge of content
- Tag-based filtering and sorting
- Activity log, history, undo/redo
- Source preview and highlight sync (toggle original vs. summary)
- Fuzzy search, semantic search
- Custom folder colors and icons
- Favorites and pins

#### AI/LLM Capabilities
- Adaptive summary depth: Quick skim vs. Deep dive
- Hybrid LLM support with fallback options
- Real-time WebSocket updates for long-running summaries
- Model auto-selection based on file type & length
- Optional feedback to fine-tune summary quality
- Summarization style settings (professional, casual, visual)

---

## ✅ Success Criteria

- Supports 3–5 input types
- Summary is editable and downloadable
- Merge works across formats (e.g., PDF + Link)
- Summary quality supports use cases like revision and skimming
- UI adapts per summary type
- Output options align with neurodivergent-friendly formats

---

## ❌ Constraints (Phase 1)

| Area             | Constraint                                                              |
|------------------|-------------------------------------------------------------------------|
| File Input       | 1 file per input type per session                                       |
| Merge Limit      | 3–5 items maximum for merged output                                     |
| Infra            | Free-tier only: FastAPI, PostgreSQL, Redis, Gemini Flash                |
| Storage          | Only parsed content is stored (not original files)                      |
| Upload Limits    | Large files may be partially processed due to token/memory constraints  |
| Solo Development | Solo build effort; tight prioritization needed                          |

---

## 💼 Stakeholders & Roles

| Stakeholder        | Role                                                                 |
|--------------------|----------------------------------------------------------------------|
| Kiran Ruba         | Product Owner, Architect, Full-stack Developer                       |
| Users              | Students, Researchers, Knowledge workers, Neurodivergent learners    |
| Recruiters         | Evaluators for product/system design, practical utility              |
| Startups/Employers | Potential employers/investors for technical and visionary depth      |

---

## ⏳ Timeline & Phase Breakdown

| Week | Timeline | Milestone |
|------|----------|-----------|
| W1   | July 14 | Finish all pre-dev documentation:<br>`PROJECT_CHARTER.md`, `SRS.md`, `FEASIBILITY.md`, `ARCHITECTURE.md`, `API_DESIGN.md`, `UI_FLOW.md`, `README.md`, `BUSINESS_OVERVIEW.md`, `COMPETITIVE_LANDSCAPE.md`  |
| W2 | July 21 | Set up basic front-end + backend:<br>- Textbox input (Paste Mode)<br>- Basic backend API<br>- Integration with Gemini LLM<br>- Show editable inline summary |
| W3 | July 28 | Implement file-folder structure (UI + backend):<br>- Basic folder view<br>- Setup DB and file schema<br>- Store metadata in DB |
| W4 | Aug 04 | Implement login screen + backend auth logic<br>- Secure password storage<br>- Authenticated routes |
| W5 | Aug 11 | Implement file upload (frontend):<br>- PDF/Word support<br>- Drag-and-drop<br>- File selector |
| W6 | Aug 18 | Implement backend file handling:<br>- File parsing + extraction using third-party libs<br>- Store only extracted content<br>- Add gzip compression + preview thumbnails |
| W7+ | Aug 20+ | Expand to multiple formats, refine UI by summary type, prepare demo, deploy MVP |

---

## 📁 GitHub Documentation Plan

| File Name                 | Purpose                                                                  | Status         	|
|---------------------------|--------------------------------------------------------------------------|--------------------|
| `PROJECT_CHARTER.md`      | High-level overview: problem, vision, scope, timeline                    | ✅ Finalized 		|
| `SRS.md`                  | Software Requirements Spec: functional & non-functional requirements     | ✅ Finalized 		|
| `FEASIBILITY.md`          | Tech, cost, timeline, risk analysis for Phase 1                          | 🛠️ In Progress		|
| `ARCHITECTURE_OVERVIEW.md`| System design, backend structure, LLM routing, UI architecture           | 🚧 Pending  	    |
| `API_DESIGN.md`           | REST API contracts: endpoints, formats, error codes                      | 🚧 Pending   		|
| `UI_FLOW.md`              | UI wireframes, interaction states, component structure                   | 🚧 Pending		    |
| `README.md`               | Setup guide, installation, core philosophy                               | 🛠️ Drafted  		|
| `COMPETITIVE_LANDSCAPE.md`| Competitor analysis by category and positioning                          | ✅ Finalized 		|
| `BUSINESS_OVERVIEW.md`    | Business model, monetization, market, user segments                      | ✅ Finalized 		|

---

### ✅ Status: Finalized
This document serves as the living charter of the SkimKnow project.


