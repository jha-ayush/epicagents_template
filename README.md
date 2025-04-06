# EpicAgents Framework

<p align="center">
  <img src="https://i.imghippo.com/files/GH4101tzU.png" alt="EpicAgents Logo" width="120"/>
</p>

**Create, Customize & Deploy AI Chat Agents for Any Business Use Case**

EpicAgents is a modular, production-ready framework that powers branded AI assistants like **Navo** — tailored to answer business-specific customer or internal queries using structured data, with zero coding required for customization.

---

## 🎯 Why Do I Need EpicAgents for My Business?

For small businesses, it's hard to:
- Answer every customer or employee question fast
- Keep your website, SOPs, menus, and policies always accessible
- Avoid costly delays in customer service or internal operations

**EpicAgents fixes this** — by turning your official documents into real-time, 24/7 AI chat assistants that are fast, branded, and accurate.

### Use Cases:
- 🍽️ **Restaurants:** Menu, reservations, loyalty programs
- 🧾 **Internal Teams:** SOPs, HR policies, inventory, safety protocols
- 🛍️ **E-commerce:** Shipping, returns, product info
- 🧑‍💼 **HR Teams:** Employee handbooks, leave policies
- 🏨 **Hospitality:** Booking FAQs, internal training manuals
- 🏥 **Wellness clinics:** Service explanations, appointment guides

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
│   │   ├── customer_privacy.json
│   │   ├── loyalty_program.json
│   │   └── ordering_guide.json
│   └── internal_docs/
│       ├── employee_handbook.json
│       ├── health_safety_compliance.json
│       ├── inventory_management.json
│       ├── marketing_plan.json
│       └── standard_operating_procedures.json
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
FLASK_DEBUG=False
ADMIN_KEY=your-admin-token
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

## 📊 Redis Event Logs (Tracked)

| Event Name            | Logged When...                  |
|-----------------------|----------------------------------|
| `agent_reply`         | GPT-4 responds to a user        |
| `reset_chat`          | Chat is manually reset          |
| `export_pdf`          | Export to PDF is triggered      |
| `rate_limit_exceeded` | Too many rapid messages         |
| `access_blocked`      | User input blocked by filters   |

---

## 🔐 Built-in Protections

- 🚫 Profanity + PII filters
- ⏳ Rate-limiting and temporary bans
- 📎 Markdown formatting with brand styling
- 📊 Redis logs for every interaction
- 🧩 Modular agent switcher for customer/internal
- 📝 Clean response formatting (no IDs, no unnecessary labels)

---

## 🧩 Tech Stack

| Layer            | Tech Used                    |
|------------------|------------------------------|
| Backend          | Flask (Python)               |
| Frontend         | HTML + TailwindCSS + JS      |
| AI Engine        | OpenAI GPT-4 API             |
| Event Logging    | Redis                        |
| Hosting/CI/CD    | Render.com                   |

### 📦 Production Dependencies (Pinned & Clean)

```
Flask==3.0.3                  # Web framework
flask-cors==4.0.0             # CORS handling for cross-origin requests
Werkzeug==3.0.2               # WSGI utilities, Flask dependency
gunicorn==23.0.0              # Production WSGI server
python-dotenv==1.0.1          # Load environment variables from .env file
openai==0.28.1                # ✅ Legacy SDK compatible with ChatCompletion.create()
redis==5.0.8                  # Redis client for Python
python-json-logger==2.0.7     # Structured JSON logging
bleach==6.1.0                 # Sanitizes and cleans HTML inputs for security
black==24.3.0                 # Code formatter
pytest==8.0.2                 # Unit testing framework
```

---

## 🤝 Interested in Using EpicAgents?

Whether you're a local shop, a multi-location business, or a fast-growing company — EpicAgents can help you:

- Answer questions faster
- Automate repetitive information delivery
- Provide 24/7 instant support for customers and internal teams
- Ensure brand consistency across every conversation
- Scale operations without scaling costs

<p align="center">
  <img src="https://i.imghippo.com/files/Vq5956YiM.png" alt="Navo Logo" width="100"/>
</p>

### 🔗 [Visit epicagents.ai](https://epicagents.ai)  
We'll help you customize and deploy EpicAgents in minutes.

---

## 📄 License

This project is open for business.  
See the [LICENSE](LICENSE) file for terms.

Created with ❤️ by [SudoKodes LLC](https://epicagents.ai)  
For custom deployments: [admin@sudokode.co](mailto:admin@sudokode.co)
