# AI-personilized-chatbot

# 🤖 Telegram AI Voice Assistant – Chat, Transcribe & Automate (n8n Workflow)

This workflow turns a Telegram bot into a personal AI assistant capable of:

Handling text OR voice messages

Transcribing voice messages via Deepgram

Using Google Gemini AI to respond intelligently

Remembering previous context through memory

Creating Google Calendar events automatically

Sending responses back to Telegram

Sending optional email alerts

# 📌 Features
Feature	Description
🎙️ Voice-to-Text	Voice messages are downloaded & transcribed using Deepgram
💬 Text-AI Chat	Personal AI replies via Google Gemini
🧠 Memory Support	Saves conversation memory for smarter responses
📅 Auto Calendar Events	Detects tasks & creates Google Calendar events
📧 Email Alerts	Sends email notifications when needed
🤖 Telegram Bot	Works fully inside Telegram

# 🧩 Workflow Breakdown

1️⃣ Telegram Trigger – Listens for incoming messages
2️⃣ Switch Node – Detects whether message is text or voice
3️⃣ get voice – Gets voice file from Telegram
4️⃣ download voice – Downloads audio
5️⃣ HTTP Request (Deepgram) – Converts speech → text
6️⃣ Edit Fields – Prepares data to send to AI
7️⃣ personal AI (Gemini) – Processes text and decides:

response

memory to store

tasks to create
8️⃣ Simple Memory – Stores conversation memory
9️⃣ Create Events (Google Calendar) – Creates tasks automatically
🔟 send email – Sends notification email
1️⃣1️⃣ Text Response – Replies back to Telegram

# 🛠️ Requirements

To run this workflow you need:

n8n (Cloud or Self-hosted)

Telegram Bot Token

Deepgram API Key

Google Gemini API Key

Google Calendar Credentials

Gmail Credentials (optional)

# 🔧 Setup Instructions

1️⃣ Import this workflow JSON into n8n
2️⃣ Add credentials:

Telegram API (BotFather token)

Deepgram API Key

Google Gemini Model

Gmail (optional)

Calendar OAuth credentials

3️⃣ Update variables:

Calendar ID in "Create Events"

Email recipient in "send email"

Your Telegram Bot Webhook URL (or use polling)

4️⃣ Click Execute Workflow → Send a message / audio to test

# 🧠 How AI Works

The personal AI node contains an instruction prompt that determines:

how the bot should respond

what to save in memory

when to trigger email or calendar actions

Customize it to make your AI:

behave like a personal assistant

take notes

manage reminders

act as a chatbot

# 🐞 Troubleshooting
Issue	Fix
Bot not responding	Ensure Telegram webhook is configured & workflow is active
Voice not transcribing	Check Deepgram key + supported audio format
Calendar not creating events	Verify calendar OAuth + event mapping
Gemini responses empty	Update Chat Model prompt
