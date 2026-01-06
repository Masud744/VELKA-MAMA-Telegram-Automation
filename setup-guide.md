# 🍽️ VELKA MAMA Restaurant – Telegram Automation Bot (n8n)

An AI-powered Telegram automation system built using **n8n**, **Google Gemini AI**, and **Google Sheets**.
This bot helps a restaurant automate food ordering, inventory checking, FAQs, and order storage via Telegram.

---

## 🚀 Features

- 🤖 AI-powered Telegram chatbot
- 📋 Food menu & inventory checking
- 🛒 Order placement & confirmation
- 📊 Orders stored automatically in Google Sheets
- 🧠 Conversation memory per user
- ❓ FAQ handling (delivery, location, contact)
- ⚙️ Fully automated using n8n

---

## 🧱 Tech Stack

- **Automation:** n8n
- **Messaging:** Telegram Bot API
- **AI Model:** Google Gemini Chat Model
- **Database:** Google Sheets
- **Deployment:** Docker + ngrok

---

## 📦 Prerequisites

- Telegram account
- Google account
- Docker installed
- n8n basic knowledge
- ngrok account (free)

---

## 🤖 Step 1: Create Telegram Bot

1. Open Telegram and search **@BotFather**
2. Run `/start`
3. Run `/newbot`
4. Set bot name: `VELKA_MAMA_BOT`
5. Set username (must end with `bot`)
6. Copy and save the **Bot Token**

---

## 🧾 Step 2: Prepare Google Sheets

Create a spreadsheet named:

```
Food Delivery System
```

### Inventory Sheet

| Food Item     | Available Quantity |
| ------------- | ------------------ |
| Morog Polao   | 12                 |
| Chicken Polao | 18                 |
| Beef Tehari   | 15                 |

### Orders Sheet

| Customer Name | Food Item | Quantity Ordered | Order Date | Status |

### FAQ Sheet

| Question | Answer |

---

## 🔑 Step 3: Google Sheets API Setup

1. Go to Google Cloud Console
2. Create a new project
3. Enable **Google Sheets API**
4. Configure OAuth consent screen
5. Create OAuth credentials
6. Use credentials in n8n

---

## 🐳 Step 4: Run n8n (Docker)

```bash
docker run -it --rm -p 5678:5678 -v n8n_data:/home/node/.n8n n8nio/n8n
```

Open browser:

```
http://localhost:5678
```

---

## 🌐 Step 5: Run ngrok

```bash
ngrok http 5678
```

Copy the HTTPS URL and use it in n8n webhook settings.

---

## 🔗 Step 6: Import Workflow

1. Open n8n UI
2. Click **Import**
3. Upload `velka_mama_n8n_workflow.json`
4. Save and activate workflow

---

## 🧠 Step 7: Workflow Overview

Nodes used:

- Telegram Trigger
- AI Agent
- Google Gemini Chat Model
- Simple Memory
- Google Sheets (Inventory, Orders, FAQ)
- Telegram Send Message

---

## 🧪 Step 8: Test Bot

Example commands:

```
hello
what food items do you have?
I want to order
Morog Polao
2 plates
confirm order
```

Orders will be saved automatically.

---

## 📂 Recommended Repository Structure

```
VELKA-MAMA-Telegram-Bot/
├── README.md
├── setup-guide.md
├── workflow/
│   └── velka_mama_n8n_workflow.json
├── screenshots/
│   ├── bot-chat.png
│   ├── workflow.png
│
```

---

## 🛡️ Security Notes

- Never commit API keys
- Use n8n credential manager
- Restrict Google API access

---

## 📈 Future Enhancements

- Delivery address handling
- Payment integration
- Admin order notification
- Order tracking system
- Database backend

---

## 👨‍💻 Author

**Shahriar Alom Masud**  
IoT & Automation Enthusiast

---

⭐ If you like this project, please star the repository!
