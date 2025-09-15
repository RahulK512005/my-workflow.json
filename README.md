# Daily Random Quote Generator & Logger in n8n

A simple yet powerful workflow that uses n8n to generate a motivational quote every day and log it as an event in Google Calendar.

---

## 🚀 Overview

This n8n workflow triggers daily at midnight, picks a random quote from a curated list via a JavaScript code node, and creates a calendar event in Google Calendar with the quote. A clean “set-and-forget” automation for daily motivation.

---

## 📋 Features

- **Scheduled trigger**: Runs daily at `00:00` (midnight).  
- **Quote selection**: Random quote selected from a static list using a JavaScript node.  
- **Logging**: Creates a “Motivational Quote” event in Google Calendar, with the quote in the event description and timestamp.  
- No external APIs required for quote generation—everything is contained within the workflow.

---

## 🔧 Workflow Components (Nodes)

| Node | Purpose |
|---|---|
| **Schedule Trigger** | Fires the workflow each day at midnight using cron (`0 0 * * *`). |
| **Code (JavaScript)** | Holds a static array of quotes; picks one randomly and attaches a timestamp. |
| **Google Calendar** | Creates an event with summary "Motivational Quote" and description "Quote of the Day: <quote>". |

---

## ⚙️ Setup Instructions

1. Clone this repository or download the workflow JSON.  
2. In your n8n instance, go to **Workflows → Import**, and select the JSON file.  
3. Set up Google Calendar OAuth2 credentials in n8n so the “Create an event” node can authenticate.  
4. Adjust the list of quotes in the Code node if you want to customize.  
5. Activate the workflow.  
6. Make sure the timezone of your n8n instance is set correctly so the midnight trigger works as expected in your local time.

---

## 📅 Schedule & Timing

- The workflow uses a cron expression `0 0 * * *` which means it will run **every day at midnight**.  
- If you want a different time, change the cron expression in the Schedule Trigger node.

---

## 🎯 Use Cases

- Personal daily motivation — seeing a “quote of the day” event in your calendar.  
- Team or shared calendars — everyone gets reminded with the same quote.  
- Learning tool — add quotes on leadership, resilience, etc., to inspire daily reflection.  
- Extendable: could add email or Slack notifications, or pull quotes from a remote source instead of hardcoding.

---

## 🛠 Potential Improvements

- Store quotes in a database or Google Sheet to allow easier addition or editing.  
- Categorize quotes (e.g. “Leadership”, “Growth”, “Perseverance”) and rotate categories.  
- Add notifications: send the daily quote via email, Slack, Microsoft Teams, or messaging platforms.  
- Add a UI or webhook so users can fetch the quote on demand.

---

## 🔐 Security & Credential Notes

- Make sure your Google Calendar credentials are stored securely in n8n.  
- Limit permissions: the calendar service account should have only permissions needed to create events.  
- Be mindful of timezone settings — misaligned timezone config can trigger events at unexpected times.

---

## 📝 License

This project is licensed under the MIT License — feel free to use, modify, and share.

---

## 🤝 Contributing

Contributions are very welcome! Here’s how you can help:

- Add more quotes or better quote sources.  
- Add translations or multi-language support.  
- Improve documentation or add more deployment examples.  
- Submit pull requests with clear descriptions of additions.

---

## 📂 File Structure

