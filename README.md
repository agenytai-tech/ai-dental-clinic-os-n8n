🦷 AI Dental Clinic Operating System (n8n + Supabase + Meta Cloud API)

Built by EGENYT Twins | AI Automation Engineers

An end-to-end, production-ready AI Clinic Operating System engineered over 2+ months to automate patient inquiries, voice notes, appointment bookings, 24h/3h reminders, autonomous waitlist cascading, Google Maps reputation management, and live Google Sheets syncing.

🚀 Key System Capabilities (7 Integrated Workflows)

Workflow File

Core Function

GitHub_1_Dental_Clinic_Main_Workflow.json

Multi-Modal AI Receptionist: Handles text & Egyptian Arabic voice notes (OpenAI Whisper), 6-second message buffering, OpenAI + Gemini 2.5 Flash Fallback, strict Supabase Vector RAG grounding, 1-click Google Calendar + Google Maps GPS confirmations, Telegram doctor alerts, and 1–5 star rating triage.

GitHub_2_Dental_Reminder_24h.json

24-Hour Official Meta Reminder: Automatically sends the dental_appointment_reminder template 24 hours prior to the visit with one-time decision locking (CONFIRM_APPT / CANCEL_APPT).

GitHub_3_Dental_Reminder_3h.json

3-Hour Final Attendance Check: Sends same-day attendance confirmation 3 hours before the appointment to eliminate no-shows.

GitHub_4_Dental_Waitlist_Dispatcher.json

Autonomous Waitlist Engine (15-Min Cascade): Instantly notifies the next waiting patient when a slot is cancelled and waits 15 minutes; if unclaimed, it expires the offer and automatically cascades to the next patient in line.

GitHub_5_Dental_Google_Sheets_Live_Sync.json

Real-Time Google Sheets Mirror: Syncs every booking, rescheduling, attendance confirmation, cancellation, waitlist promotion, and patient rating directly to Google Sheets by Booking ID.

GitHub_6_Dental_RAG_Knowledge_Base.json

Dynamic Google Drive RAG Pipeline: Watches the clinic's official Google Doc for price or schedule updates and automatically refreshes embeddings in the Supabase documents vector store.

GitHub_7_Dental_Error_Notifications.json

24/7 Error Monitoring Guard: Captures any workflow execution failure and dispatches instant diagnostic alerts via Telegram and Gmail.

🛠️ Tech Stack & Architecture

Orchestration: n8n (Self-Hosted / Cloud)

Messaging API: Meta Official WhatsApp Cloud API (v21.0) + Interactive Lists & Templates

LLM & Fallbacks: OpenAI (gpt-4.1-mini) + Google Gemini (gemini-2.5-flash)

Voice AI: OpenAI Whisper (whisper-1) for Arabic dialect speech-to-text

Database & Vector Store: Supabase (PostgreSQL + pgvector + Row-Level Security)

Notifications & Sync: Telegram Bot API, Google Sheets API, Google Calendar Links, Gmail API

⚙️ Quick Setup Guide

Database Setup (Supabase):
Create the required tables (appointments, waitlist, whatsapp_message_buffer, whatsapp_chat_histories, patient_sessions, whatsapp_message_logs, and documents) in your Supabase SQL Editor.

Import Workflows into n8n:
Import the 7 .json files into your n8n instance.

Configure Credentials:
Replace the placeholder variables inside Clinic Config & Parse Meta (YOUR_META_PERMANENT_ACCESS_TOKEN, YOUR_WHATSAPP_PHONE_NUMBER_ID, YOUR_TELEGRAM_BOT_TOKEN, YOUR_TELEGRAM_CHAT_ID) and connect your Supabase, Postgres, OpenAI, Gemini, and Google credentials.

Activate Workflows:
Turn all 7 workflows to Active and connect your Meta Webhook URL.

🤝 Built by EGENYT Twins

Looking to implement a custom AI Operating System or WhatsApp Automation for your clinic or enterprise?
Connect with EGENYT Twins on LinkedIn or reach out for a live demo!
