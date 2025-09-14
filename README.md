# my-workflow.json
n8n workflow for sending daily updates
# 🧠 Daily Random Quote Generator in n8n

This project is an automated **Daily Random Quote Generator** built entirely using [n8n](https://n8n.io/)'s built-in nodes — no third-party services or APIs required.

---

## 📌 Overview

This workflow is designed to run **automatically every day at 9:00 AM**. It selects a random motivational quote from a predefined list using JavaScript and outputs it as JSON. Optionally, it can log the quote to a local file or return it through a webhook for testing.

---

## 🚀 Features

- ⏰ **Daily Scheduled Trigger** using Cron node  
- ✨ **Random Quote Selection** using Function node  
- 📤 **JSON Output** of the selected quote  
- 💾 Optional: **Log quote to file** using Write File node  
- 🌐 Optional: Test via **Webhook**

---

## 🧱 Nodes Used

- `Cron` – Triggers the workflow every day at 9 AM  
- `Function` – Contains JavaScript to randomly select a quote  
- `Set` or `Respond to Webhook` – Outputs the selected quote (optional)  
- `Write Binary File` – (Optional) Logs the quote to a text file (local only)

---

## 📂 File Included

| File Name                  | Description                           |
|---------------------------|---------------------------------------|
| `daily-quote-workflow.json` | n8n workflow export file for import   |

---

## 🛠️ How to Use

1. Open your [n8n](https://n8n.io/) instance (local or cloud)
2. Go to **Settings → Import Workflow**
3. Upload the file: `daily-quote-workflow.json`
4. Adjust the time in the `Cron` node if needed
5. (Optional) Add a `Webhook` trigger to manually test
6. Click **Activate**

---

## ✍️ Example Output

```json
{
  "quote": "Your time is limited, so don't waste it living someone else's life.",
  "timestamp": "2025-09-15T09:00:00.000Z"
}
