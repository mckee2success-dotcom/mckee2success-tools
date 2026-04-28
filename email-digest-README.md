# 📧 Email Digest

A Google Apps Script that runs automatically every few days, summarizes your Gmail inbox, and surfaces the most important emails — delivered like a morning briefing.

---

## Files

| File | Description |
|------|-------------|
| `digest-script.gs` | Main Apps Script — scans Gmail, summarizes threads, and sends digest |

---

## How It Works

1. Runs on a **time-driven trigger** (every 3 days at 7:30 AM)
2. Pulls recent unread threads from Gmail
3. Summarizes each thread by sender, subject, and key action items
4. Sends a consolidated digest email to your inbox
5. Flags emails requiring a reply or follow-up action

---

## Setup Instructions

### Step 1: Open Google Apps Script
Go to [script.google.com](https://script.google.com) and create a new project.

### Step 2: Paste the Script
Copy and paste the contents of `digest-script.gs` into the editor.

### Step 3: Set the Trigger
1. Click **Triggers** (clock icon) in the left sidebar
2. Click **+ Add Trigger**
3. Configure:
   - Function: `sendEmailDigest`
   - Event source: **Time-driven**
   - Type: **Day timer** or **Week timer**
   - Time: **7:30 AM – 8:30 AM**

### Step 4: Authorize
Run the script once manually to grant Gmail read/send permissions.

---

## Configuration (inside the script)

```javascript
const CONFIG = {
  MAX_THREADS: 50,          // How many Gmail threads to scan
  DAYS_BACK: 3,             // How far back to look
  DIGEST_SUBJECT: "📬 Your McKee2Success Morning Digest",
  FLAG_KEYWORDS: ["urgent", "action required", "deadline", "respond by", "interview"],
};
```

---

## Sample Digest Output

```
📬 YOUR MORNING DIGEST — April 28, 2025

ACTION REQUIRED (3)
─────────────────────────────────────
• [eTeam Inc.] RE: Cybersecurity Role — Reply requested by Friday
• [SAM.gov] RFP Notice — Solicitation closes May 5
• [Contracting Officer] RFQ Response Needed — McKee2Success

INFORMATIONAL (7)
─────────────────────────────────────
• [LinkedIn] 5 people viewed your profile
• [Nova Staffing] Azure Cloud Security — New position available
• [Google] Security alert — New sign-in from Chrome
...
```

---

## Notes

- No API key required — runs entirely inside Google's ecosystem
- Gmail read/send permissions are granted via Google OAuth during first run
- To pause the digest, simply delete or disable the trigger in Apps Script
