# 🏛️ Government Contracting (GovCon) Tools

Automation tools supporting McKee2Success LLC's government contracting middleman workflow — from RFP analysis to subcontractor identification and outreach.

---

## Files

| File | Description |
|------|-------------|
| `rfp-analyzer.html` | AI-powered RFP analysis tool — bid/no-bid scoring, red flags, requirements summary |
| `subcontractor-outreach.js` | Automated Gmail outreach to subcontractor prospects via Gmail MCP |
| `bid-pricing-tool.html` | Labor category rate estimator with 15–20% margin formula |
| `middleman-sop.md` | Internal SOPs for the GovCon prime contractor intermediary workflow |

---

## Workflow Overview

```
Step 1: RFP Analysis
  └─ Paste RFP into rfp-analyzer.html
  └─ Get bid/no-bid recommendation + requirements summary

Step 2: Subcontractor Identification
  └─ AI generates list of potential subcontractor prospects
  └─ Filter by NAICS, capability, clearance, location

Step 3: Outreach (Rule of 12)
  └─ subcontractor-outreach.js sends RFQ emails via Gmail MCP
  └─ Track responses, follow up on day 3 and day 7
```

---

## Rule of 12 Outreach Strategy

- Contact **12 subcontractors** per RFP opportunity
- Send initial RFQ email → follow up at day 3 → final follow up at day 7
- Target response rate: 25–30% (3–4 responses per 12 outreach)
- Select best-fit sub based on capability, price, and past performance

---

## Bid Pricing Formula

```
Prime Price = Sub's Quoted Price × (1 + Margin)
Margin Target: 15% – 20%

Example:
  Sub quotes: $500,000
  McKee2Success margin (18%): $90,000
  Total prime bid: $590,000
```

---

## Federal Client Portfolio

| Agency | Focus Area |
|--------|------------|
| U.S. Navy | Cybersecurity / IT Services |
| Department of State | IT Infrastructure |
| FDIC | GRC / Compliance |
| U.S. Army Intelligence | Security Engineering |
| SEC | Cybersecurity Program Management |
| Department of Labor | Cloud Modernization |

---

## Business Info

| Field | Value |
|-------|-------|
| Entity | McKee2Success LLC |
| Type | Minority-Owned SDB |
| CAGE Code | 98EG4 |
| NAICS | 541511 |
| SAM.gov | Active |
| Location | Upper Marlboro, MD |

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

### Run Outreach Script
```bash
node subcontractor-outreach.js --rfp "RFP-2025-001" --naics "541511"
```

---

## Notes

- All outreach emails are saved as **Gmail drafts** before sending — review before dispatch
- RFP analyzer uses Claude Sonnet for cost efficiency on large documents
- Bid pricing tool runs entirely client-side — no data is transmitted
