# 🤖 EpicAgents Framework

**Train and deploy custom AI agents using your business docs**  
EpicAgents is a modular framework for building AI-powered agents that answer questions based on structured documents like FAQs, menus, policies, SOPs, and more — no code required.

---

## 🔗 Live Agent Examples

| Agent Type        | Demo URL                                      |
|-------------------|-----------------------------------------------|
| 🍽️ Navo (Customer) | [epicagents.ai](https://epicagents.ai)        |
| 🛡️ Zyra (Internal)  | [epicagents.ai](https://epicagents.ai)        |

---

## 🧠 What You Can Build

| Use Case              | Example Agent |
|------------------------|----------------|
| 🧾 Menu or Product Guide | Navo (Food Delights) |
| 📘 Employee Handbook     | Zyra (Internal Docs) |
| 📦 SOPs & Processes      | Zyra |
| 🎓 Onboarding Agent      | Zyra |
| 📣 FAQ & Policy Chatbot  | Navo / Zyra |

---

## ✨ Features

| Feature                     | Description |
|----------------------------|-------------|
| ⚙️ Modular Agent Design      | Use the same framework for different agents |
| 🧠 GPT-4 Integration         | Context-aware AI from OpenAI |
| 💡 Sticky Welcome Message   | Brand-first, user-friendly onboarding |
| 🎨 Tailwind UI Widget       | Responsive, mobile-optimized, modern |
| 📄 Markdown Reply Support   | Bold, italics, lists, and clean layout |
| 📤 PDF Export               | Save chat transcripts |
| 🔁 Redis Logging (Optional) | Analytics-ready event logs |
| 🔐 Secure `.env` Setup      | API keys & config separation |

---

## 🧩 Folder Structure Template

```
📁 epicagents_agentname/
├── assets/
│   ├── agent_avatar.png
│   └── epic_agents_logo.png
├── data/
│   ├── menu.json
│   ├── faqs.json
│   └── ...
├── app.py
├── index.html
├── requirements.txt
└── .env
```

---

## 🚀 Setup Guide

### 1. Clone the Agent Repo

```bash
git clone https://github.com/your-org/epicagents_agentname.git
cd epicagents_agentname
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Create `.env` File

```env
OPENAI_API_KEY=your-key-here
USE_REDIS=True
REDIS_URL=redis://your-redis-url
FLASK_ENV=production
```

### 4. Run the Flask App

```bash
python app.py
```

---

## 🛠️ Creating New Agents

1. **Fork or clone this repo as a base**
2. **Customize `agentConfig` in the frontend**
3. **Replace avatar and data files**
4. **Update the README with specific agent info**
5. **Deploy to Render or your preferred platform**

---

## 🌐 Hosting & Deployment

- 🟩 **Backend**: Flask app (Render, Railway, etc.)
- 🟨 **Frontend**: HTML+Tailwind widget embedded in any site
- 🟥 **Logging (optional)**: Redis-compatible, secure and private

---

## 🧠 Powered by EpicAgents  
Built by [EpicAgents](https://epicagents.ai), subsidiary of SudoKodes LLC  
Contact: [admin@sudokode.co](mailto:admin@sudokode.co)

---

## 📣 Want Custom Agents?

Need help building agents for your business or team?  
**Contact us today → [admin@sudokode.co](mailto:admin@sudokode.co)**
