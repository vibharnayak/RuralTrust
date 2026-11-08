e · MD
# 🌾 RuralTrust
 
### AI-Powered Rural Employment Platform
 
*Every Skill Deserves an Opportunity. Every Worker Deserves Trust.*
 
 
---
 
## 📌 Problem Statement 
 
> **Rural youth cannot find work that fits, and small employers cannot find them.**
 
Job information in rural areas is scattered across WhatsApp groups, local agents and personal networks. Workers face fake listings and unclear salary terms, language and digital-literacy barriers make online platforms hard to use, and poor matches often lead to early job exits.
 
## 💡 Our Solution
 
**RuralTrust** is one unified platform that connects rural workers and small employers, with trust built in from the start.
 
| Pillar | What it does |
|---|---|
| 🗣️ **Voice access** | Workers can register, search, listen to job details and apply using voice, alongside a simple text mode. |
| 🪪 **Universal Skill Passport** | A digital skill profile for people who may not have a formal CV. |
| 🤖 **AI job matching** | Recommends jobs by skills, location, salary, experience and availability. |
| 🛡️ **Employer verification and risk screening** | Flags suspicious listings for admin review. |
| 📋 **Job Reality Check** | Compares advertised and agreed terms and keeps wage and complaint records. |
| 📈 **Retention intelligence** | Follow-ups at Day 7, 30, 60 and 90. |
 
---
 
## 🚦 Project Status
 
This repository describes the **proposed design** of RuralTrust. Features are listed below with their current status so nothing is overstated.
 
| Feature | Status |
|---|---|
| Worker, Employer and Admin portals | 🔴 Planned |
| Smart Mode (text-based search and apply) | 🔴 Planned |
| Voice-assisted mode (Kannada demo) | 🔴 Planned |
| Additional languages | 🔴 Planned |
| Universal Skill Passport | 🔴 Planned |
| AI job matching | 🔴 Planned |
| Employer verification and risk screening | 🔴 Planned |
| Job Reality Check and worker protection | 🔴 Planned |
| Employment retention follow-ups | 🔴 Planned |
| Assisted Access Portal (service centres) | 🔴 Planned |
 
**Legend:** 🟢 Implemented · 🟡 In development · 🔴 Planned
 
> Update this table as each feature moves from planned to in development to implemented.
 
> ⚠️ **Demo data notice:** Any names, salaries, counts and charts used in demos or presentations are **sample data for illustration only**. They are not real users, employers or outcomes.
 
---
 
## ✨ Key Features
 
### 🗣️ Multilingual Voice-Assisted Employment
- Choose a preferred language
- Register with voice guidance
- Search for jobs by speaking
- Listen to job descriptions and salary details
- Apply through guided voice assistance
- Check application status
**Kannada** is the planned demo language. Broader multilingual support is a development goal.
 
### 🪪 Universal Skill Passport
Education and qualifications, work experience, practical and vocational skills, projects and training, self-declared skills with supporting evidence, and skill assessment status.
 
### 🤖 AI-Powered Job Matching
Worker Profile → AI Matching → Suitable Jobs → Apply
 
Matching considers skills and qualifications, location and travel distance, salary expectations, experience, and availability and job requirements.
 
### 🛡️ Employer Verification and Fraud Risk Detection
- Employer identity and business detail submission
- Verification status: **Verified**, **Pending Review** or **Flagged**
- Duplicate or suspicious listing detection
- Recruitment-fee warnings
- Salary and job-description inconsistency checks
- Admin review of flagged listings
> **Important:** a risk flag means *"needs human review"*, **not** confirmed fraud.
 
### 📋 Job Reality Check and Worker Protection
Record and compare advertised and agreed salary, working hours, location, employment conditions and terms, plus wage records, complaints and supporting evidence.
 
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
    U["Worker, Employer, Admin"] --> F["React Frontend"]
    F --> B["Node.js Backend"]
    B --> D[("PostgreSQL Database")]
    B --> A["Python AI Services"]
    A --> R["Results"]
```
 
**In words:** Workers, employers and admins use the React frontend. It calls the Node.js backend, which stores data in PostgreSQL and calls the Python AI services for job matching, skill extraction and risk screening. Results are returned to the user. Voice and language features use speech-to-text, text-to-speech and translation APIs, and maps use OpenStreetMap.
 
## 🛠️ Tech Stack (Proposed)
 
| Layer | Technology |
|---|---|
| Frontend | React.js, Tailwind CSS |
| Backend | Node.js, Express.js |
| Database | PostgreSQL |
| AI services | Python, FastAPI |
| AI capabilities | Job matching, skill extraction, risk screening |
| Voice and language | Speech-to-text, text-to-speech, translation APIs |
| Maps | OpenStreetMap |
| Authentication | JWT, role-based access control (RBAC) |
 
---
 
## 🖼️ Screenshots
 
Screenshots of the working prototype will be added here once the interface is ready.
 
<!-- Add images like this once they exist in docs/screenshots/:
![Worker dashboard](docs/screenshots/worker-dashboard.png)
-->
 
---
 
## 🚀 Getting Started (Planned Setup)
 
> **Note:** The commands below are the **planned** setup instructions. They will work once the code for each service is added to this repository. Adjust them to match the final folder layout.
 
### Prerequisites
- Node.js 18 or later
- Python 3.10 or later
- PostgreSQL 14 or later
### 1. Clone the repository
```bash
git clone https://github.com/vibharnayak/ruraltrust.git
cd ruraltrust
```
 
### 2. Configure environment variables
Create a `.env` file in each service folder. Never commit real secrets.
 
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
 
## 📁 Planned Project Structure
 
```
ruraltrust/
├── frontend/       # React + Tailwind CSS
├── backend/        # Node.js + Express API
├── ai-services/    # Python + FastAPI (matching, skill extraction, risk screening)
├── database/       # PostgreSQL schema and migrations
├── docs/           # Presentation, diagrams and screenshots
├── LICENSE
└── README.md
```
 
---
 
## 🤝 Responsible Design Principles
 
- **Human in the loop:** risk flags go to an admin for review; nothing is labelled fraud automatically.
- **Transparency:** matching results and flags should be explainable to workers and employers.
- **Accessibility first:** voice and local-language support so digital literacy is not a barrier.
- **Privacy:** collect only what is needed, protect worker and employer data, and keep secrets out of the repository.
- **Honest reporting:** no invented statistics, partnerships or outcomes.
## 🗺️ Roadmap
 
- [ ] Core Worker, Employer and Admin portals
- [ ] Voice flow in Kannada (demo language)
- [ ] Skill Passport and AI job matching
- [ ] Employer verification and risk screening
- [ ] Job Reality Check with wage and complaint records
- [ ] Day 7, 30, 60 and 90 retention follow-ups
- [ ] Additional languages
- [ ] Assisted Access Portal for service centres
## 📄 License
 
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
 
---
 
**RuralTrust**
*Connecting Skills. Creating Opportunities. Building Trust.*
