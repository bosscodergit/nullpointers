# TrustAssess 🛡️📊

> **AI-Powered Soft-Skill Assessment, Behavioral Anti-Gaming & Organizational Analytics Platform**

TrustAssess is an intelligent behavioral evaluation platform built with Next.js 16, React 19, Tailwind CSS, Recharts, and Google Gemini AI. It transforms traditional workplace soft-skill evaluation through situational judgment tests (SJTs), grounded LLM rubric scoring, real-time telemetry-based anti-cheating detection, and an executive supervisor dashboard with an integrated HR AI advisor.

---
## 🔑 Demo Access & Test Credentials

You can test the entire platform without any manual registration using these pre-configured credentials:

### 1. Supervisor & HR Portal
- **Passkey**: `2026@null`
- **Authorized Name**: Any supervisor name (e.g. `Priya Sharma`, `Admin HR`)

### 2. Employee Assessment Portal
| Employee ID | Registered Email | Password | Role / Department |
| :--- | :--- | :--- | :--- |
| `emp1` | `arjun.mehta@gmail.com` | `Arjun@2026` *(or `password123`)* | Backend Engineer (Engineering) |
| `emp2` | `sanika@gmail.com` | `Sanika@2026` *(or `password123`)* | Frontend Engineer (Engineering) |
| `emp3` | `vikram.rao@gmail.com` | `Vikram@2026` *(or `password123`)* | Tech Lead (Engineering) |
| `emp4` | `ananya.deshmukh@gmail.com` | `Ananya@2026` *(or `password123`)* | Product Designer (Design) |
| `emp5` | `rahul.verma@gmail.com` | `Rahul@2026` *(or `password123`)* | Account Executive (Sales) |

---

## ✨ Key Features

### 1. Situational Judgment Tests (SJTs)
- Real-world workplace dilemmas mapped across 6 key functional departments: **Engineering**, **Sales**, **Marketing**, **Customer Success**, **Product**, and **Operations**.
- Candidates make tactical choices and write reasoned justifications for their actions.

### 2. 5-Dimensional Soft-Skill Rubric
Every decision and written rationale is scored on a standardized **1.0 to 5.0 scale** across 5 core competencies:
1. **Communication**: Clarity, diplomacy, active listening, and constructive conflict resolution.
2. **Accountability**: Ownership of outcomes, proactive issue escalation, and blameless post-mortems.
3. **Integrity**: Ethics under pressure, intellectual honesty, and adherence to commitments.
4. **Teamwork**: Cross-functional collaboration, unblocking peers, and empathy.
5. **Adaptability**: Resilience amid ambiguity, pivoting, and continuous learning.

### 3. Hybrid Scoring Engine (70 / 30 Model)
- **70% Multiple-Choice Alignment**: Standardized behavioral rating based on calibrated psychometric choices.
- **30% Free-Text Justification**: Evaluated via Google Gemini (with an offline deterministic NLP fallback) for concrete action verbs, depth, and evidence quotes.
- **Say-Do Consistency**: Automatically calculates divergence between chosen action and written justification.

### 4. Advanced Anti-Gaming & AI Cheating Detection
TrustAssess actively protects evaluation integrity using multi-signal telemetry and heuristic inspection:
- 📋 **Clipboard Paste Monitor**: Detects whether candidate pasted text directly from external chatbots.
- ⚡ **Typing Cadence Telemetry**: Flags unnatural typing bursts (> 18 characters/sec on responses over 80 characters).
- 🤖 **AI Slop & LLM Pattern Recognition**: Identifies stereotypical LLM boilerplate (`delve`, `foster open`, `crucial to`, `navigate this`, `ensure alignment`) and markdown bullet formats.
- ⚖️ **Say-Do Contradiction Circuit Breaker**: If option score and text score differ by >= 2.0, or if cheating signals are triggered, the system revokes the 30% text boost and routes the candidate to the Human Review Queue.

### 5. Supervisor & HR Analytics Dashboard
- **Cohort Performance Curves**: Aggregated score percentiles across teams and departments.
- **Review Alert Queue**: Highlights candidates flagged for low confidence, prompt injection attempts, or AI gaming.
- **Interactive Recharts**: Trait radar charts, departmental comparison bars, and strength/gap categorizations.

### 6. Built-in HR Advisor AI Chatbot
- Powered by Google Gemini 2.5/Flash.
- Natural-language interface for HR leaders to query team trends, ask about candidate strengths/gaps, and generate custom coaching recommendations.

### 7. Dual Database Architecture (Zero-Config Fallback)
- **Firebase Realtime Database & Firestore**: Cloud synchronization for enterprise production setups.
- **Offline Mock Persistence**: Full local state persistence using pre-seeded datasets so the application works out-of-the-box without requiring active cloud credentials.

---

## 🛠️ Tech Stack

| Domain | Technology / Library |
| :--- | :--- |
| **Framework** | Next.js 16 (App Router, Turbopack) |
| **UI & Styling** | React 19, Tailwind CSS v4 |
| **Data Visualization** | Recharts 3 (Radar, Bar, Line Charts) |
| **Generative AI** | Google Generative AI (Gemini Models), Groq API Fallback |
| **Database & Auth** | Firebase 13 (Realtime Database, Firestore, Auth) |
| **Language** | Modern JavaScript (ES Modules, Node.js 20+) |

---

## ⚡ Getting Started (Run Locally)

### 1. Prerequisites
- Node.js version **18.18.0** or higher (Node 20+ recommended).
- `npm` (comes with Node) or `pnpm` / `yarn`.

### 2. Clone the Repository
```bash
git clone https://github.com/your-username/trustassess.git
cd trustassess
