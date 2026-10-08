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
* **Testing:** Jest (Unit tests for extraction logic)

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

git clone https://github.com/Gopinathzues/AI-Powered-Email-Assistant.git
cd AI-Powered-Email-Assistant
npm install

2. Environment Setup
Important: Never commit your .env or config/credentials.json files to version control.

Place your Google OAuth client secrets in config/credentials.json.

Create a .env file in the root directory with the following variables:

# Google OAuth
GOOGLE_CLIENT_ID=your_client_id
GOOGLE_CLIENT_SECRET=your_client_secret
GOOGLE_REFRESH_TOKEN=your_refresh_token

# IMAP Email Access
IMAP_USER=your_email@gmail.com
IMAP_PASSWORD=your_app_password

# Twilio WhatsApp
TWILIO_ACCOUNT_SID=your_sid
TWILIO_AUTH_TOKEN=your_token
TWILIO_WHATSAPP_NUMBER=whatsapp:+14155238886
TARGET_WHATSAPP_NUMBER=whatsapp:+1234567890
3. Run the Assistant

node emailManagement.js
You will be prompted to filter emails by sender, keyword, or date range.

⚠️ Security Note
OAuth Tokens: Refresh tokens are stored in config/credentials.json and should never be committed.
API Keys: Ensure all API keys in .env are rotated regularly.
Email Passwords: Use an App Password (not your main password) for IMAP access if using Gmail.

📈 Performance
Extraction Accuracy: High accuracy on standard calendar invites (dates, times, titles).
Latency: ~2-3 seconds per email for extraction + calendar creation + WhatsApp alert.
Scalability: Designed for single-user personal automation; not optimized for high-volume enterprise inboxes.

🤝 Future Enhancements
Support for Outlook/Exchange IMAP
Natural language query for calendar events ("What do I have tomorrow?")
Multi-recipient WhatsApp alerts
Error handling for duplicate calendar events

Author
Gopinath M

---
