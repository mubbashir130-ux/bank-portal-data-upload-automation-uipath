# 🏦 Bank Portal Data Upload Automation — UiPath

> UiPath bot reads Excel from email, securely logs into 
> bank portal using card credentials, uploads customer 
> data with human-like actions, builds upload status 
> report and sends to team manager automatically.

---

## 🔄 Workflow Overview
```
📧 Email Received
   (Excel file attachment)
      ↓
📊 Bot Saves Excel Temporarily
   → Reads All Customer Records
      ↓
🏦 Bank Portal Login
   → Enters Card Credentials
   → Clicks & Navigates Securely
      ↓
📋 Data Entry Page
   → Bot Types Customer Data
   → Uploads Each Record
   → Logs Success ✅ or Failure ❌
      ↓
📊 Build Upload Report
   → Which data uploaded ✅
   → Which data failed & why ❌
      ↓
📧 Send Report to Team Manager
```

---

## ⚙️ Features

- 📧 **Email Trigger** — Reads incoming email with Excel attachment
- 📊 **Excel Processing** — Extracts all customer records
- 🔐 **Secure Login** — Card credentials via UiPath Orchestrator
- 🖱️ **Full UI Automation** — Types, clicks & navigates portal
- ⬆️ **Bulk Data Upload** — Uploads all customer records
- 📋 **Smart Reporting** — Logs what uploaded and what failed with reasons
- ✉️ **Manager Notification** — Sends full report to team manager
- 🔒 **Secure Processing** — No credentials stored in code

---

## 📊 Upload Report Structure

| Column | Description |
|--------|-------------|
| Customer ID | Unique identifier |
| Customer Name | Full name |
| Upload Status | ✅ Success / ❌ Failed |
| Failure Reason | Why it failed (duplicate, missing field, etc.) |
| Timestamp | When it was processed |
| Processed By | Bot name / ID |

---

## 🤖 UI Actions Performed

| Action | Purpose |
|--------|---------|
| ⌨️ Typing | Enter card credentials & customer data |
| 🖱️ Clicking | Navigate portal buttons & menus |
| 📜 Scrolling | Navigate data entry pages |
| ⬆️ Uploading | Submit customer records |
| 📸 Screenshot | Capture errors for report |

---

## 🛠️ Technologies Used

| Tool | Purpose |
|------|---------|
| UiPath Studio | Main automation platform |
| UiPath UI Automation | Human-like portal interaction |
| UiPath Mail Activities | Email reading & sending |
| UiPath Excel Activities | Excel data processing |
| UiPath Orchestrator | Secure credential storage |
| UiPath Error Handling | Capture & log failures |

---

## 🚀 How to Run

1. Open `project.json` in UiPath Studio
2. Configure `Config.xlsx`:
   - Bank portal URL
   - Card credentials (via Orchestrator Assets)
   - Email account settings
   - Manager email address
3. Send trigger email with Excel attachment
4. Run `Main.xaml`

---

## 📁 Project Structure
```
├── Main.xaml
├── project.json
├── Config.xlsx
├── Workflows/
│   ├── ReadEmailAndExcel.xaml
│   ├── Portal_SecureLogin.xaml
│   ├── Portal_NavigateDataPage.xaml
│   ├── UploadCustomerData.xaml
│   ├── BuildUploadReport.xaml
│   └── SendReportToManager.xaml
└── README.md
```

---

## 💼 Business Value

| Before Automation | After Automation |
|-------------------|-----------------|
| Staff logs in manually | Bot handles secure login |
| Manual data entry per customer | Bulk upload automatically |
| No tracking of failures | Full report with failure reasons |
| Hours of data entry work | Minutes for full upload |
| Manager waits for updates | Instant report via email |
| Human errors in entry | Consistent accurate uploads |

---

## 🔒 Security & Compliance

- No real credentials stored in repository
- Card details managed via UiPath Orchestrator Assets
- No real customer financial data in codebase
- Built following banking security best practices
- PCI DSS compliance considerations applied

---

## 👨‍💻 About the Developer

**RPA & AI Automation Developer** specializing in UiPath,
banking/financial automation & secure data processing.

📩 **Available for freelance projects!**

---

⭐ If you find this useful, please star the repo!
