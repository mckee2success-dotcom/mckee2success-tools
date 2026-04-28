# 🔍 Job Search Automation

Tools for scanning Gmail, classifying job requisitions, and auto-generating tailored cover letters using the Claude API and Gmail MCP integration.

---

## Files

| File | Description |
|------|-------------|
| `gmail-job-scanner.js` | Connects to Gmail via MCP, scans inbox for recruiter emails and job requisitions |
| `job-classifier.js` | Uses Claude API to classify roles by type, seniority, and alignment with resume |
| `cover-letter-generator.js` | Generates tailored cover letters and saves them as Gmail drafts for review |

---

## How It Works

1. **Scanner** — Connects to Gmail MCP and pulls recent recruiter emails from inbox
2. **Classifier** — Sends email content to Claude API; returns role type, seniority, confidence score, and match notes
3. **Generator** — Builds a tailored cover letter based on the job description and saves it as a Gmail draft

---

## Target Role Profile

- **Titles:** Senior Cybersecurity Engineer, ISSO, CISO, Security Architect, Program Manager
- **Focus Areas:** Vulnerability Management, GRC, Cloud Security (Azure), Incident Response
- **Clearance:** Secret (Active)
- **Certifications:** CISSP, PMP, CEH, Azure Solutions Architect Expert

---

## Active Prospects (as of 2025)

| Company | Role | Status |
|---------|------|--------|
| Quzara LLC | Senior Cybersecurity | Draft sent |
| VT Group | Security Architect | Draft sent |
| BryceTech | PM / Security | Draft sent |
| DLA Piper | Cybersecurity Counsel Support | Draft sent |
| eTeam Inc. | Federal Cyber Analyst | Recruiter engaged |
| Nova Staffing | Azure Cloud Security | Recruiter engaged |

---

## Setup

### Prerequisites
```bash
npm install @anthropic-ai/sdk
```

### Environment Variables
```
ANTHROPIC_API_KEY=your_key_here
GMAIL_MCP_URL=https://gmailmcp.googleapis.com/mcp/v1
```

### Run
```bash
node gmail-job-scanner.js
node job-classifier.js
node cover-letter-generator.js
```

---

## Notes

- Cover letters are saved as **Gmail drafts** — always review before sending
- Classifier confidence score threshold: **70%+** to auto-draft, below 70% flagged for manual review
- Scanner filters by common recruiter keywords: `"opportunity"`, `"role"`, `"position"`, `"requisition"`, `"clearance"`
