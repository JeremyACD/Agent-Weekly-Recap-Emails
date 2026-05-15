[README.md](https://github.com/user-attachments/files/27808698/README.md)
# 📋 Weekly Recap Generator
**ACD Direct — Primerica Program**

A browser-based tool that converts weekly call center reports into formatted agent performance recap emails. No installation, no server, no login — open the link and it works.

---

## 🔗 Live Tool
👉 **[Open the Recap Generator](https://jeremyacd.github.io/OPs-Dashboard/weekly-recap-generator.html)**

---

## 🔒 Privacy
All data processing happens entirely in your browser. CSV files are never uploaded to any server or stored anywhere externally. Close the tab and the data is gone.

---

## 📂 What Files It Accepts

Upload any combination of the following CSV exports from your call center platform:

| File | Where to Export From | What It Provides |
|---|---|---|
| **CDR / Call Detail Report** | Callcorp → Reports → CDR Daily Download | Calls, Handle Time, Denied Calls, Days Worked |
| **QA Evaluations** | Callcorp → Quality → All Evaluations | QA Score, Evaluator, Call Date |
| **User State Detail** | Callcorp → Reports → User State Detail | ACW, Hold Time, Not Ready Time |
| **Agent Roster** | Your internal roster spreadsheet | Maps agents to their Team Lead |
| **Schedule** *(optional, coming soon)* | Scheduling system export | Attendance & punctuality data |

The tool auto-detects each file type by its column headers — no renaming required.

---

## ⚙️ Performance Goals (Defaults)

These are pre-loaded and editable inside the tool each session:

| Metric | Goal |
|---|---|
| QA Score | ≥ 85% |
| Avg Handle Time | ≤ 7:30 (7.5 min) |
| Denied Calls | < 4 per week |
| After Call Work | < 1:30:00 per week |
| Hold Time | < 1:00:00 per week |
| Not Ready | < 20:00 per week |

---

## 🚀 How to Use It

1. **Upload your files** — drag and drop the weekly CSV exports onto the upload zone
2. **Set the week** — enter the start and end date for the reporting period
3. **Confirm goals** — adjust thresholds if needed (changes apply to that session only)
4. **Generate** — the tool processes all agents found across the files
5. **Copy & send** — expand any agent card, preview their email, and click **Copy Formatted Email** to paste directly into Outlook

> **Tip:** Use the search bar to find a specific agent quickly when you have a large team.

---

## 📧 Email Output

Each generated email includes:
- Color-coded metrics table (green = passing, amber = needs attention)
- QA review section with evaluator details
- Automatic coaching note (passing acknowledgment or 1:1 scheduling notice)
- Areas needing attention (only flagged items)
- Highlights section (only genuine wins)
- Navy branded header and footer

**Copy Formatted Email** pastes as rich HTML into Outlook, preserving all colors and formatting.
**Copy as Plain Text** is available as a fallback.

---

## 🗂 Roster File Format

The tool will auto-detect your roster if it contains columns matching these patterns:

- **Agent name column** — any column named `Agent`, `Employee`, or `Name`
- **Team Lead column** — any column named `Team Lead`, `Supervisor`, or `TL`

If your roster uses different column names, contact the tool owner to update the detection logic.

---

## 🛠 Making Updates

The entire tool is a single HTML file: `weekly-recap-generator.html`

To update it:
1. Edit the file locally (or directly in GitHub's editor)
2. Commit to the `main` branch
3. Changes are live on GitHub Pages within ~60 seconds

Key sections inside the file:
- **`compute()`** — metrics calculation logic
- **`buildEmailHTML()`** — generates the formatted email HTML
- **`detect()`** — file type auto-detection by column headers
- **`DEFAULT_GOALS / getGoals()`** — performance threshold logic

---

## 👤 Owner & Support

**Jeremy Jacobs** — Operations Manager, ACD Direct  
For questions about the tool, updates to goals or logic, or roster column mapping issues, reach out directly.

---

*Built for the ACD Direct Primerica Program. Part of the Megastars Operations Hub.*
