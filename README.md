# 🛡️ SafeSpace Copilot

> **An AI-powered workplace wellbeing and psychological safety agent built for Microsoft 365**

![Microsoft Copilot Studio](https://img.shields.io/badge/Microsoft-Copilot%20Studio-0078D4?style=flat&logo=microsoft)
![No Code](https://img.shields.io/badge/Built%20With-No%20Code-brightgreen?style=flat)
![SharePoint](https://img.shields.io/badge/Microsoft-SharePoint-0078D4?style=flat&logo=microsoft-sharepoint&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=flat)
![Agents League Hackathon](https://img.shields.io/badge/Microsoft%20365-AgentsLeague%20Hackathon%202026-purple?style=flat)

---

## 🌿 What is SafeSpace Copilot?

SafeSpace Copilot is a **fully no-code** conversational AI agent built in **Microsoft Copilot Studio**, grounded in **SharePoint** knowledge, and designed for **Microsoft Teams** deployment. It gives every employee a private, intelligent, and anonymous wellbeing companion — without ever leaving Microsoft 365.

**The problem it solves:** Most enterprise tools are built for productivity, not people. Burnout, psychological unsafety, and fear of reporting go unaddressed because employees lack a private, always-available, judgment-free resource. SafeSpace Copilot fills that gap — built entirely through Copilot Studio's visual no-code interface, powered by Microsoft's AI agent framework.

---

## 🎬 Demo Video

▶️ **[Watch the full demo on YouTube](#)**


> 📌 Demo recorded using the Microsoft Copilot Studio built-in test panel,
> showcasing all 4 features in a live working agent.

---

## ✨ Core Features

| Feature | Description |
|---|---|
| 🌿 **Wellbeing Check-In** | Anonymous mood rating 1–5 with compassionate, tailored responses and support options |
| 📋 **HR Policy Q&A** | Natural language answers grounded in real SharePoint HR documents via Generative AI |
| 🚨 **Safe Concern Reporting** | Trauma-informed, 3-step anonymous reporting flow with dignity-first design |
| 🧘 **Wellness Tips** | Box breathing, 5-4-3-2-1 grounding technique, and self-compassion prompts |

---

## 🏗️ Architecture

```
┌─────────────────────────────────────────────────┐
│            Employee / HR Manager                │
│    (Microsoft Teams · Copilot Studio Test Panel)│
└──────────────────┬──────────────────────────────┘
                   │
                   ▼
┌─────────────────────────────────────────────────┐
│         SafeSpace Copilot Agent                 │
│    Microsoft Copilot Studio (No-Code Build)     │
│                                                 │
│  ┌─────────────┐  ┌──────────┐  ┌───────────┐  │
│  │  Wellbeing  │  │HR Policy │  │  Safe     │  │
│  │  Check-In   │  │  Q&A     │  │ Reporting │  │
│  └─────────────┘  └──────────┘  └───────────┘  │
│            ┌──────────────┐                     │
│            │ Wellness     │                     │
│            │ Tips         │                     │
│            └──────────────┘                     │
└───────────┬─────────────────────┬───────────────┘
            │                     │
            ▼                     ▼
┌────────────────────┐  ┌────────────────────────┐
│    SharePoint      │  │  Microsoft 365 Platform │
│  HR Policy Docs    │  │  Entra ID · Azure AI    │
│  Knowledge Base    │  │  (via Copilot Studio)   │
└────────────────────┘  └────────────────────────┘
```

![[Architecture Diagram](https://claude.ai/public/artifacts/bc864565-0178-45d4-96ad-12fb3e1b5fcb)]

---

## 🔧 Technologies Used

| Technology | Role |
|---|---|
| **Microsoft Copilot Studio** | No-code agent builder — all 5 topics built using visual node editor |
| **SharePoint Online** | HR policy knowledge base — source for all generative AI answers |
| **Microsoft Entra ID** | Authentication and identity management |
| **Azure AI Language** | Natural language understanding (built into Copilot Studio) |
| **Microsoft Teams** | Target deployment channel for enterprise rollout |

> 💡 **This is a fully no-code project.** Every topic, condition, message, and
> redirect was built using Copilot Studio's visual conversation editor —
> no scripting or development environment required.

---

## 🧠 Domain Expertise Behind the Design

SafeSpace Copilot is built at the intersection of technology and human science:

| Domain | How It Shapes SafeSpace |
|---|---|
| **Human Resource Management** | HR policy access, anonymous reporting, employee lifecycle awareness |
| **Psychology** | Trauma-informed conversation design, mood-responsive empathy flows |
| **Criminology & Criminal Justice** | Ethical anonymous reporting structure, harm prevention, dignity-first principles |
| **Library & Information Science** | Structured knowledge retrieval and SharePoint document architecture |
| **AI & Continuous Learning** | Microsoft AI Skills Fest, Salesforce Agentforce, Google DeepMind community |

---

## 🚀 Setup & Run Instructions

### Prerequisites
- Microsoft 365 account (Education, Business, or Enterprise)
- Access to [Microsoft Copilot Studio](https://copilotstudio.microsoft.com)
- SharePoint site for HR documents

---

### Step 1 — Create SharePoint Knowledge Base

1. Go to [office.com](https://office.com) → open **SharePoint**
2. Click **+ Create site** → **Team site** → name it `SafeSpace HR Hub`
3. Go to **Documents** → click **+ New** → **Word document**
4. Add your HR policy content (leave, sick leave, remote work, reporting policies)
5. Save — copy the SharePoint site URL for the next step

---

### Step 2 — Create the Agent in Copilot Studio

1. Go to [copilotstudio.microsoft.com](https://copilotstudio.microsoft.com)
2. Click **Create** → **New Agent**
3. Name: `SafeSpace Copilot`
4. Description: *"A confidential workplace wellbeing and HR support agent"*
5. Under **Knowledge** → **Add knowledge** → select **SharePoint**
6. Paste your SharePoint site URL → click Add
7. Enable **Generative answers**

---

### Step 3 — Build the 5 Topics (No-Code Visual Editor)

All topics are built using Copilot Studio's visual node editor. Build in this order:

| Order | Topic | Key Nodes Used |
|---|---|---|
| 1st | Wellbeing Check-In | Question, Condition Group, Message, Redirect |
| 2nd | HR Policy Q&A | Question, Generative Answers, Condition Group |
| 3rd | Safe Reporting | Question (×4), Condition Group (×2), Message |
| 4th | Wellness Tips | Message (×3), Question, Condition Group |
| 5th (last) | Greeting | Question, Condition Group, Redirect (×4) |

> See `/docs/step-by-step-build-guide.md` for the complete no-code build instructions.

---

### Step 4 — Test the Agent

1. Click **Test** (top right in Copilot Studio) to open the test panel
2. Run these conversations to verify everything works:

| Type this | Expected response |
|---|---|
| `hello` | Welcome message with 4 buttons |
| `I want to check in` | Mood rating 1–5 buttons appear |
| `annual leave policy` | SharePoint-grounded HR answer |
| `I need to report something` | Trauma-informed consent flow |
| `give me a wellness tip` | Box breathing exercise |

---

### Step 5 — Deploy to Microsoft Teams

1. Click **Publish** → confirm
2. Go to **Channels** → **Microsoft Teams** → Turn on Teams
3. Install the SafeSpace Copilot app in Teams
4. Share with your organisation

> 💡 **Note:** Deployment to Microsoft Teams requires a paid or full Microsoft 365
> licence. This project was built and demonstrated using the Copilot Studio
> built-in test panel, which fully showcases all agent capabilities.
> The build is production-ready for Teams deployment with the appropriate licence.

---

## 💬 Sample Conversations

**Wellbeing Check-In:**
> `User:` I want to check in
> `SafeSpace:` *"Thank you for taking a moment for yourself. This check-in is completely anonymous. How are you feeling today?"*
> `User:` 😔 1 - Really struggling
> `SafeSpace:` *"Thank you for trusting SafeSpace with that. You are not alone..."*

**HR Policy Q&A:**
> `User:` How many days of annual leave do I have?
> `SafeSpace:` *"Based on the HR policy: Full-time employees receive 20 days of paid annual leave per year..."*

**Safe Reporting:**
> `User:` I need to report something
> `SafeSpace:` *"It takes courage to speak up. Your identity will not be shared. Are you ready to proceed?"*
> `User:` ✅ Yes, let's continue
> `SafeSpace:` *"Step 1 of 3: What type of concern would you like to raise?"*

**Wellness Tip:**
> `User:` Give me a wellness tip
> `SafeSpace:` *"Breathe IN for 4 counts... HOLD for 4... OUT for 4... HOLD for 4. Repeat 3 times. You are doing better than you think. 💙"*

---

## 📁 Repository Structure

```
safespace-copilot/
│
├── README.md                           ← This file
├── architecture.png                    ← Architecture diagram
│
├── docs/
│   ├── project-description.md          ← Hackathon submission description
│   ├── conversation-flows.md           ← Full conversation scripts
│   ├── step-by-step-build-guide.md     ← Complete no-code build guide
│   └── architecture-diagram.html       ← Interactive architecture diagram
│
└── screenshots/
    └── (Copilot Studio test panel screenshots)
```

---

## 🗺️ Roadmap

- [ ] Full Microsoft Teams deployment (with enterprise M365 licence)
- [ ] Power BI dashboard for anonymised wellbeing trends
- [ ] Multilingual support
- [ ] Manager coaching prompts via Outlook
- [ ] Employee Assistance Programme (EAP) referral integration

---

## 👩‍💻 About the Builder

Built by a multidisciplinary learner and innovator with expertise across HR, Psychology, Criminology, Library Science, Commerce, and AI.

**Certifications & Community:**
- 🌟 Salesforce Triple Star Ranger — 400+ badges
- 🤖 Salesforce Agentforce Innovator
- 🧠 Google DeepMind Research Foundation — Tri AI Lagos Cohort 10
- 📚 Microsoft AI Skills Fest Participant
- 🎓 Microsoft Recruit Badge — AI Skill Navigator
- 🧘 Yoga practitioner — 2100+ Duolingo streak — 1300+ Apple Books reading streak

---

## 📄 License

MIT License — open for learning, adaptation, and enterprise use.

---

*SafeSpace Copilot · Enterprise Agents Track · Microsoft 365 Copilot Hackathon 2026*
