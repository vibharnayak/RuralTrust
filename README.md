# RuralTrust

### AI-Powered Rural Employment Platform
 
*Every Skill Deserves an Opportunity. Every Worker Deserves Trust.*
 
**Hackathon Problem Statement 8.2** · Theme: Rural Employment, Accessibility, Artificial Intelligence and Worker Protection · Status: Under Development
 
---
 
## 📌 Problem Statement 8.2
 
> **Rural youth cannot find work that fits, and small employers cannot find them.**
 
Job information in rural areas is scattered across WhatsApp groups, local agents and personal networks. Workers face fake listings and unclear salary terms, language and digital-literacy barriers make online platforms hard to use, and poor matches often lead to early job exits.
 
## 💡 Our Solution
 
**RuralTrust** is one unified platform that connects rural workers and small employers, with trust built in from the start.
 
| Pillar | What it does |
|---|---|
| 🗣️ **Voice access** | Workers can register, search, listen to job details and apply using voice, alongside a simple text mode. |
| 🪪 **Universal Skill Passport** | A digital skill profile for people who may not have a formal CV. |
| 🤖 **AI job matching** | Recommends jobs by skills, location, salary, experience and availability. |
| 🛡️ **Employer verification & risk screening** | Flags suspicious listings for admin review. |
| 📋 **Job Reality Check** | Compares advertised vs agreed terms and keeps wage and complaint records. |
| 📈 **Retention intelligence** | Follow-ups at Day 7, 30, 60 and 90. |
 
---
 
## 🚦 Project Status
 
> This section is honest by design. Please keep it updated as work progresses.
 
| Feature | Status |
|---|---|
| Worker, Employer and Admin portals | 🟡 In development |
| Smart Mode (text-based search & apply) | 🟡 In development |
| Voice-assisted mode (Kannada demo) | 🟡 In development |
| Additional languages | 🔴 Planned |
| Universal Skill Passport | 🟡 In development |
| AI job matching | 🟡 In development |
| Employer verification & risk screening | 🟡 In development |
| Job Reality Check & worker protection | 🔴 Planned |
| Employment retention follow-ups | 🔴 Planned |
| Assisted Access Portal (service centres) | 🔴 Planned |
 
**Legend:** 🟢 Implemented · 🟡 In development · 🔴 Planned
 
> ⚠️ **Demo data notice:** All names, salaries, counts and charts in the demo and presentation are **sample data for illustration only**. They are not real users, employers or outcomes.
 
---
 
## ✨ Key Features
 
### 🗣️ Multilingual Voice-Assisted Employment
- Choose a preferred language
- Register with voice guidance
- Search for jobs by speaking
- Listen to job descriptions and salary details
- Apply through guided voice assistance
- Check application status
**Kannada** is the demo language. Broader multilingual support is a development goal.
 
### 🪪 Universal Skill Passport
Education and qualifications · work experience · practical and vocational skills · projects and training · self-declared skills with supporting evidence · skill assessment status.
 
### 🤖 AI-Powered Job Matching
Worker Profile → AI Matching → Suitable Jobs → Apply
 
Matching considers skills and qualifications, location and travel distance, salary expectations, experience, and availability and job requirements.
 
### 🛡️ Employer Verification & Fraud Risk Detection
- Employer identity and business detail submission
- Verification status: **Verified / Pending Review / Flagged**
- Duplicate or suspicious listing detection
- Recruitment-fee warnings
- Salary and job-description inconsistency checks
- Admin review of flagged listings
> **Important:** a risk flag means *"needs human review"*, **not** confirmed fraud.
 
### 📋 Job Reality Check & Worker Protection
Record and compare advertised vs agreed salary, working hours, location, employment conditions and terms, plus wage records, complaints and supporting evidence.
 
### 📈 Employment Retention Intelligence
| Checkpoint | Purpose |
|---|---|
| Day 7 | Initial employment check |
| Day 30 | Job satisfaction and payment check |
| Day 60 | Employment stability check |
| Day 90 | Retention outcome |
 
---
 
## 🧩 Four Platform Experiences
 
| Portal | Purpose |
|---|---|
| 👷 **Worker Portal** | Find jobs, manage skills, track applications |
| 🏪 **Employer Portal** | Post vacancies, discover candidates |
| 🧑‍💼 **Admin Portal** | Verify employers, review flagged jobs, manage complaints |
| 🎧 **Assisted Access Portal** | Help workers register and apply through participating service centres |
 
---
 
## 🏗️ Architecture
 
```mermaid
flowchart LR
    U["Worker / Employer / Admin"] --> F["React Frontend<br/>(Tailwind CSS)"]
    F --> B["Node.js Backend<br/>(Express.js, JWT + RBAC)"]
    B --> D[("PostgreSQL")]
    B --> A["Python AI Services<br/>(FastAPI)"]
    A --> R["Results<br/>Matches · Risk flags · Skill insights"]
    B -.-> V["Speech-to-text · Text-to-speech · Translation APIs"]
    F -.-> M["OpenStreetMap"]
```
 
## 🛠️ Tech Stack (Proposed)
 
| Layer | Technology |
|---|---|
| Frontend | React.js, Tailwind CSS |
| Backend | Node.js, Express.js |
| Database | PostgreSQL |
| AI services | Python, FastAPI |
| AI capabilities | Job matching, skill extraction, risk screening |
| Voice & language | Speech-to-text, text-to-speech, translation APIs |
| Maps | OpenStreetMap |
| Authentication | JWT, role-based access control (RBAC) |
 
---
 
## 🚀 Getting Started
 
> Replace the commands below with the ones that match your actual repository layout.
 
### Prerequisites
- Node.js 18+
- Python 3.10+
- PostgreSQL 14+
### 1. Clone the repository
```bash
git clone https://github.com/vibharnayak/ruraltrust.git
cd ruraltrust
```
 
### 2. Configure environment variables
Create a `.env` file in each service folder (never commit real secrets):
 
```env
# backend/.env
PORT=5000
DATABASE_URL=postgresql://user:password@localhost:5432/ruraltrust
JWT_SECRET=change_me
AI_SERVICE_URL=http://localhost:8000
 
# ai-services/.env
# Add keys for the speech and translation providers you choose
```
 
### 3. Run the services
```bash
# Frontend
cd frontend && npm install && npm run dev
 
# Backend
cd backend && npm install && npm start
 
# AI services
cd ai-services && pip install -r requirements.txt && uvicorn main:app --reload
```
 
---
 
## 📁 Suggested Project Structure
 
```
ruraltrust/
├── frontend/       # React + Tailwind CSS
├── backend/        # Node.js + Express API
├── ai-services/    # Python + FastAPI (matching, skill extraction, risk screening)
├── database/       # PostgreSQL schema and migrations
├── docs/           # Presentation and diagrams
└── README.md
```
 
---
 
## 🤝 Responsible Design Principles
 
- **Human in the loop:** risk flags go to an admin for review; nothing is labelled fraud automatically.
- **Transparency:** matching and flags should be explainable to workers and employers.
- **Accessibility first:** voice and local-language support so digital literacy is not a barrier.
- **Privacy:** collect only what is needed, protect worker and employer data, and keep secrets out of the repository.
- **Honest reporting:** no invented statistics, partnerships or outcomes.
## 🗺️ Roadmap
 
- [ ] Complete core Worker, Employer and Admin portals
- [ ] Voice flow in Kannada (demo language)
- [ ] Skill Passport and AI job matching
- [ ] Employer verification and risk screening
- [ ] Job Reality Check and wage/complaint records
- [ ] Day 7 / 30 / 60 / 90 retention follow-ups
- [ ] Additional languages
- [ ] Assisted Access Portal for service centres
## 📄 License
 
Distributed under the MIT License. See `LICENSE` for details. *(Change this if you choose a different license.)*
 
---
 
**RuralTrust**
*Connecting Skills. Creating Opportunities. Building Trust.*
