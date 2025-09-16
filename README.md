<p align="center">
  <img src="/image" alt="AI Agent Workflow Banner" width="800">
</p>
# Personal-Assistant-with-n8n
AI-powered Personal Assistant Workflow 🤖 – A smart assistant that works inside Telegram, supports text &amp; voice inputs, and can manage emails, schedule calendar events, handle contacts via Google Sheets, solve calculations, and answer general queries.
# 🤖 AI Agent Workflow – Personal Assistant  

This project is an **AI-powered Personal Assistant Workflow** that can:  
- 📩 Read, write, and reply to emails  
- 📅 Create, update, and manage calendar events  
- 📇 Manage contacts via Google Sheets  
- 🧮 Solve calculations  
- 🌍 Answer general knowledge questions  
- 🎙 Handle both **text & voice inputs** through a Telegram bot  

---

## 🚀 Features  

### 🔹 Input Handling  
- **Text Input:** Directly processed by AI.  
- **Voice Input:** Goes through a **Transcription Node** → converted to text → processed by AI.  

---

### 🔹 Email Management  
The AI routes your request to the **Email Node** when it detects keywords like `send`, `reply`, `unread mails`.  

✅ Send Emails  
✅ Reply to Emails  
✅ Delete Emails  
✅ View Unread Emails  
✅ Get Access to All Mails  

**Example:**  
```text
User: Write an email to John saying I will be late for the meeting.
AI → Sends the mail through Email Node.
