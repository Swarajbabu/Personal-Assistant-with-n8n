![AI Agent Workflow](https://github.com/Swarajbabu/Personal-Assistant-with-n8n/blob/main/Image.png?raw=true)
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

✅ Send Emails ✅ Reply to Emails ✅ Delete Emails ✅ View Unread Emails ✅ Get Access to All Mails  

**Example:**  
```text
User: Write an email to John saying I will be late for the meeting.
AI → Sends the mail through Email Node.
```
---
### 🔹 Calendar Management 
The AI routes your request to the **Calendar Node** when it detects keywords like `creat`, `workshaving`, `Events`.  

✅ Create Events
✅ Update Events
✅ Delete Events
✅ View All Events 

**Example:**  
```text
User: Create a calendar event tomorrow from 9 to 10 for my class.
AI → Adds the event to Google Calendar → You get a reminder.
```
---
### 🔹 Contact Database (Google Sheets)

Uses a Google Sheet as a simple contact database.

✅ Add Contacts
✅ Edit Contacts
✅ Delete Contacts
✅ Search by Name, Email, or Phone

**Example:**  
```text
User: Send a mail to Ramesh.
AI → Looks up Ramesh’s email in Google Sheet → Sends the mail.
```
---
## ⚙️ Setup Process  

To run this project, follow these steps:  

1. **Open N8N**  
   - Go to the [N8N website](https://n8n.io/) and log in.  
   - Create a **new workflow** (worksheet).  

2. **Import JSON Files**  
   - In the workflow editor, click on the **three dots (⋮)** menu.  
   - Select **Import → From File**.  
   - Import the JSON files **one by one** (you cannot upload all four at once).  
   - After importing all four JSON files, the workflow will show all the connected **agents and nodes**.  

3. **Create an OpenAI API Key**  
   - Go to [OpenAI](https://platform.openai.com/) and generate an **API key**.  
   - Add this key to the **OpenAI Node** inside N8N so the AI can process inputs.  

4. **Set Up a Local Memory Node**  
   - Add a **Memory Node** in N8N.  
   - This acts as simple **local memory**, so the assistant can **remember context** across inputs.  

5. **Define System Prompts**  
   - The AI needs **prompts** to understand your intent (keywords like *send*, *create*, *delete*).  
   - Use the **System Prompt Generator** ([System Prompt Generator](https://chatgpt.com/g/g-8qIKJ1ORT-system-prompt-generator)).  
   - Describe your idea there → it will generate a **system prompt** for you.  
   - Add this generated prompt in the **AIAgent Node** under *System Instructions*.  

6. **Set Up Telegram Bot**  
   - Open **Telegram** and search for **BotFather**.  
   - Create a new bot and get the **API token**.  
   - Add this token to your N8N Telegram node for integration.  

7. **Connect Services**  
   - **Gmail** → Authorize to allow sending, reading, and replying to emails.  
   - **Google Calendar** → Authorize to create, update, and delete events.  
   - **Google Sheets** → Authorize to manage your contact database.  
   - **Calculator Node** → No extra setup needed, just add it in N8N.  

8. **Run the Workflow**  
   - Once all connections are authorized, activate the workflow.  
   - Your **AI Personal Assistant** is now ready 🎉  

---

✅ After setup, you can:  
- Access the assistant via **Telegram**  
- Use both **text & voice inputs**  
- Manage **emails, calendar, contacts**  
- Solve **calculations**  
- Ask **general knowledge questions**  
- Enjoy **basic memory support** for context-based interactions  

## 💡 Why Use This Workflow?  

- 📲 Works entirely inside **Telegram** – no need to switch apps.  
- 🎙 Supports both **text and voice** inputs.  
- 🧑‍💼 Acts like a **smart secretary** for your emails, calendar, contacts, and queries.  
- 🌍 Can also be used as a **personal AI search engine**.  
- 📇 Simple **Google Sheet integration** for easy contact management.  
- 🚀 Expandable – you can add more tools later.  

---

## 🔄 Example Flow  

**Voice Input:**  
🎙 You say → *“Remind me tomorrow to pay my electricity bill at 7 PM.”*  
- Voice → Transcribed → AI detects *reminder* → Creates a calendar event.  

**Text Input:**  
💬 You type → *“What are my unread emails?”*  
- AI → Fetches unread mails → Returns inside Telegram.  

**General Query:**  
💬 You type → *“How many countries are there in the world?”*  
- AI → Replies with **“There are 195 countries in the world.”**  

---

## 🛠 Future Improvements  

- 🔗 Integration with task management apps (Notion, Trello)  
- 🏷 Smart priority tagging for emails  
- 🌐 Multi-language voice support  
- 🔔 Notifications for important calendar events  

---

## 📌 Summary  

The **AI Agent Workflow** is a single assistant that can:  
✔ Manage your **emails**  
✔ Organize your **calendar**  
✔ Maintain your **contacts**  
✔ Solve **math problems**  
✔ Answer **general knowledge questions**  

All inside **Telegram**, with support for both **chat & voice commands** 🎉  
