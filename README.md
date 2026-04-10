# 🤖 IT Helpdesk AI System

An intelligent IT support system that automatically answers employee questions using AI, logs all interactions, and escalates complex issues to human agents via Slack.

---

## 🏗️ System Architecture

User → Chatbot (GitHub Pages)
↓
Make.com Webhook
↓
Pinecone (Vector Search)
↓
Claude API (Response Generation)
↓
Airtable (Ticket Logging)
↓
Google Sheets (Sync) → Looker Studio (Dashboard)
↓
Make.com (Escalation Trigger)
↓
Slack #it-helpdesk-escalations

---

## ⚙️ Tech Stack

| Component | Tool |
|---|---|
| Frontend Chatbot | HTML/CSS/JS (GitHub Pages) |
| Automation | Make.com |
| Vector Database | Pinecone |
| AI Model | Claude API (Anthropic) |
| Ticket Logging | Airtable |
| Data Sync | Google Apps Script |
| Dashboard | Looker Studio |
| Notifications | Slack |

---

## 🔄 How It Works

1. **User submits a question** via the chatbot interface
2. **Make.com receives** the question via webhook
3. **Pinecone searches** the knowledge base for similar FAQs
4. **If similarity score ≥ 0.6:** Claude generates a response → Status = `Resolved`
5. **If similarity score < 0.6:** Claude acknowledges the limitation → Status = `Escalated`
6. **Airtable logs** the ticket with all metadata
7. **Google Apps Script** syncs Airtable data to Google Sheets every hour
8. **Looker Studio** displays real-time metrics from Google Sheets
9. **Make.com monitors** Airtable and sends Slack notification for escalated tickets

---

## 📊 Dashboard Metrics

- Total Tickets
- Escalated Tickets
- Resolved Tickets
- Average Confidence Score
- Ticket Volume Over Time
- Performance by Category
- Issues Needing Attention

---

## 🚀 Getting Started

### Prerequisites
- Make.com account
- Pinecone account
- Anthropic API key
- Airtable account
- Google account (Sheets + Looker Studio)
- Slack workspace

### Configuration
1. Clone this repository
2. Update `index.html` with your Make.com webhook URL
3. Configure Make.com scenario with your API keys
4. Set up Pinecone index with your FAQ embeddings
5. Configure Airtable base with the Tickets table
6. Set up Google Apps Script sync
7. Connect Looker Studio to Google Sheets

---

## 📝 Adding New FAQs

See [FAQ_GUIDE.md](FAQ_GUIDE.md) for instructions on adding new knowledge base entries.

---

## 🔧 Troubleshooting

See [TROUBLESHOOTING.md](TROUBLESHOOTING.md) for common issues and solutions.

---

## 👩‍💻 Built by

**Maggie** — AI Automation Specialist  
[LinkedIn](https://linkedin.com/in/tu-perfil) | [Upwork](https://upwork.com/tu-perfil)
