# AI & Lead Automation Blueprints

A collection of production-ready automation workflows built with **n8n** and **Make.com**.

---

### 1. AI Chatbot & CRM Support Agent (n8n)
An n8n workflow using an AI Agent node connected to OpenAI, Vector Knowledge Search, Typebot webhooks, and HubSpot CRM.

![AI Chatbot Integration](Ai%20chatbot%20integration.png)

* **Trigger:** Typebot Webhook
* **AI Engine:** OpenAI Model + Conversation Memory + Knowledge Base Search
* **CRM Actions:** Search HubSpot CRM Contacts & Create Support Tickets
* **Output:** Instant personalized AI response returned to the user

---

### 2. Automated Lead Enrichment & Outreach (Make.com)
A Make.com scenario that extracts lead domains, enriches them, uses Google Gemini AI to draft customized outreach emails, and logs execution in Google Sheets.

![Make.com Leads Scraper](make.com%20leads%20scraper.png)

* **Source:** Domain Search via HTTP
* **Processing:** Data iteration & Google Sheets logging
* **AI Personalization:** Google Gemini AI response generation
* **Outreach:** Automated Gmail dispatch & row updates
