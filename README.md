#  VELKA MAMA Restaurant – AI Telegram Automation Bot

An AI-powered Telegram bot built using **n8n**, **Google Gemini**, and **Google Sheets** to automate food ordering, inventory management, FAQs, and customer interaction for restaurants.

This project demonstrates a **real-world automation system** combining AI agents, workflow orchestration, and cloud services.

---

##  Key Features

-  AI-powered conversational Telegram bot
-  Context-aware conversation memory
-  Automated food ordering system
-  Real-time inventory checking
-  Orders stored automatically in Google Sheets
-  FAQ handling (delivery, location, contact info)
-  Built using n8n (low-code automation)

---

## 🎥 Demo

![Demo Video](https://youtu.be/BZku93-37P8?si=o-uXgTpjeC89ITMk)


##  System Architecture

```
Telegram User
     ↓
Telegram Trigger (n8n)
     ↓
AI Agent (Gemini + Memory)
     ↓
Google Sheets (Inventory / Orders / FAQ)
     ↓
Telegram Response
```

---

##  Tech Stack

- **Automation Platform:** n8n
- **AI Model:** Google Gemini Chat Model
- **Messaging:** Telegram Bot API
- **Database:** Google Sheets
- **Deployment:** Docker + ngrok

---

##  Screenshots

> Add screenshots inside the `screenshots/` folder

- Telegram chat demo
- n8n workflow canvas
- Google Sheets order log

---

##  Setup & Installation

 For full setup instructions, see:
 **[setup-guide.md](setup-guide.md)**

Quick summary:

1. Create Telegram bot via BotFather
2. Prepare Google Sheets (Inventory, Orders, FAQ)
3. Import workflow into n8n
4. Configure credentials (Telegram, Google, Gemini)
5. Activate workflow and start chatting

---

##  How to Test

1. Start n8n
2. Run ngrok
3. Open Telegram
4. Send `hello` to bot
5. Try: “what food items do you have?”
6. Try: “I want 2 Morog Polao”


#  Example User Commands

```
hello
what food items do you have?
I want to order
Morog Polao
2 plates
confirm order
Do you have home delivery?
```

---

## 📂 Repository Structure

```
VELKA-MAMA-Telegram-Bot/
├── README.md
├── setup-guide.md
├── workflow/
│   └── velka_mama_n8n_workflow.json
├── screenshots/
│   ├── bot-chat.png
│   ├── workflow.png
│── google-sheet/
     └── Food Delivery System
```

---

##  Security Notes

- ❌ Do not commit API keys or bot tokens
- ✅ Use n8n credential manager
- 🔒 Restrict Google API access properly

---

##  Future Enhancements

- Payment gateway integration
- Delivery address handling
- Admin notification system
- Order tracking & status updates
- Database backend (instead of Sheets)

---

##  Author

**Shahriar Alom Masud**  
B.Sc(Enng.) in IoT & Robotics Engineering,
 University of Frontier Technology, Bangladesh

---
