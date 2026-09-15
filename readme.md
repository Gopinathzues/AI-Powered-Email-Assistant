# 🤖 AI-Powered Email Assistant

An automated workflow tool built with Node.js that converts incoming emails into organized schedule updates and instant mobile alerts. The script scans inbox messages, extracts event details using the Gemini API, schedules them directly in Google Calendar, and sends real-time summaries to WhatsApp.

---

## ⚡ Key Features

* **Smart Extraction:** Uses Google Gemini AI to parse dates, times, and topics from natural language email bodies.
* **Calendar Sync:** Automatically schedules events via Google Calendar API using OAuth 2.0.
* **Instant Alerts:** Sends real-time event updates to WhatsApp via Twilio.
* **Interactive CLI:** Filter emails dynamically by sender, subject keyword, start date, and fetch limits.

---

## 🛠️ Tech Stack

* **Runtime:** Node.js
* **Email Parsing:** IMAP
* **AI Engine:** Google Gemini API
* **Integrations:** Google Calendar API, Twilio WhatsApp API

---

## 📁 Repository Structure

```text
AI-Powered-Email-Assistant/
├── config/                  # OAuth keys & tokens (Git ignored)
├── utils/                   # Helper modules (Email, Calendar, Twilio)
├── .env                     # API credentials and environment variables
├── emailManagement.js       # Main application pipeline
└── README.md

🚀 Getting Started
1. Installation
Bash
git clone [https://github.com/Gopinathzues/AI-Powered-Email-Assistant.git](https://github.com/Gopinathzues/AI-Powered-Email-Assistant.git)
cd AI-Powered-Email-Assistant
npm install

2. Environment Setup
Place your Google OAuth client secrets in config/credentials.json.

Create a .env file in the root directory:

Code snippet
IMAP_USER=your_email@gmail.com
IMAP_PASSWORD=your_app_password
GEMINI_API_KEY=your_gemini_api_key
TWILIO_ACCOUNT_SID=your_twilio_sid
TWILIO_AUTH_TOKEN=your_twilio_auth_token
TWILIO_WHATSAPP_NUMBER=whatsapp:+14155238886
MY_WHATSAPP_NUMBER=whatsapp:+your_number

3. Run
Bash
node emailManagement.js
