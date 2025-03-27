# 🤖 EpicAgents Framework

**Create, Customize & Deploy AI Chat Agents for Any Business Use Case**

EpicAgents is a modular, production-ready framework that powers branded AI assistants like **Navo** — tailored to answer business-specific customer or internal queries using structured data, with zero coding required for customization.

---

## 🔧 Features

| Feature                      | Description |
|-----------------------------|-------------|
| 🧱 Modular Frontend & Backend | Built with Flask, TailwindCSS, and JS for reuse across agents |
| 🧠 GPT-4 Powered             | High-quality conversational support via OpenAI API |
| 📁 Structured JSON Support   | Feed business data (e.g., FAQs, Policies, Menus, SOPs) |
| 🗂️ Multi-Agent Ready         | Easily spin up different agents (e.g., customer vs. internal) |
| 📊 Redis Event Logging       | Tracks queries, resets, exports for insights |
| 📤 Export to PDF             | Customers can download chat history |
| 🎨 Fully Branded             | Custom logos, names, tones, colors for every agent |
| 📱 Mobile Optimized          | Responsive UI, sleek dark theme |
| 🔁 Prompt System             | Configurable tone, formatting, and context injection |
| 🌐 CORS & Deployment Ready   | Flask backend deploys easily on Render or similar platforms |

---

## 📁 Directory Structure

```
epicagents/
│
├── assets/
│   ├── epic_agents_logo.png
│   ├── navo_logo_01.jpg
│   └── navo_logo_01_transparent.jpg
│
├── data/
│   ├── customer_docs/
│   │   ├── menu.json
│   │   ├── faqs.json
│   │   └── ...
│   └── internal_docs/
│       ├── employee_handbook.json
│       ├── sop.json
│       └── ...
│
├── templates/
│   ├── index_customer.html
│   └── index_internal.html
│
├── .env
├── .gitignore
├── app.py
├── LICENSE
├── README.md
└── requirements.txt
```

---

## 🚀 Running Locally

1. **Clone the Repo**
```bash
git clone https://github.com/your-org/epicagents.git
cd epicagents
```

2. **Install Python Dependencies**
```bash
pip install -r requirements.txt
```

3. **Set up Environment Variables**
Create a `.env` file in the root:
```
OPENAI_API_KEY=your-key-here
USE_REDIS=True
REDIS_URL=redis://your-redis-url
```

4. **Run the App**
```bash
python app.py
```

---

## 🔀 Agent Switching Logic

- `GET /ask-customer/` → Loads customer-facing structured data from `customer_docs`
- `GET /ask-internal/` → Loads internal-use structured data from `internal_docs`

Use corresponding frontends:  
- `index_customer.html` for public user interactions  
- `index_internal.html` for internal teams or admin users

---

## ✨ Live Demo

Visit: [https://epicagents.ai](https://epicagents.ai)  
Try both Showcase 1 (Customer Docs) and Showcase 2 (Internal Docs)

---

## 🧠 Powered by GPT-4  
Created with ❤️ by [SudoKodes LLC](https://epicagents.ai)  
For custom deployments: [admin@sudokode.co](mailto:admin@sudokode.co)
