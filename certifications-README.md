# 📝 Certifications & Practice Tests

Interactive certification study tools built with React, designed for active prep toward CMMC CPC, CISSP, and other professional credentials.

---

## Files

| File | Description |
|------|-------------|
| `cmmc-practice-test.jsx` | Full CMMC 2.0 / NIST SP 800-171 interactive practice test (React) |

---

## CMMC 2.0 Practice Test

### Coverage

| Domain | NIST Controls Covered |
|--------|-----------------------|
| Access Control (AC) | AC.1.001 – AC.2.006 |
| Audit & Accountability (AU) | AU.2.041 – AU.3.045 |
| Configuration Management (CM) | CM.2.061 – CM.3.068 |
| Identification & Authentication (IA) | IA.1.076 – IA.3.083 |
| Incident Response (IR) | IR.2.092 – IR.2.093 |
| Maintenance (MA) | MA.2.111 – MA.2.114 |
| Media Protection (MP) | MP.1.118 – MP.2.120 |
| Personnel Security (PS) | PS.2.127 – PS.2.128 |
| Physical Protection (PE) | PE.1.131 – PE.1.133 |
| Risk Assessment (RA) | RA.3.145 – RA.5.155 |
| Security Assessment (CA) | CA.2.157 – CA.3.161 |
| System & Comm. Protection (SC) | SC.1.175 – SC.3.187 |
| System & Info. Integrity (SI) | SI.1.210 – SI.3.219 |

### Features
- Timed quiz mode (90 questions / 90 minutes)
- Immediate feedback with domain-level scoring
- Progress tracker — see which domains need more work
- Randomized question order on each attempt
- Export results as summary report

---

## Setup

### Prerequisites
- Node.js 18+
- npm or yarn

### Run Locally
```bash
npx create-react-app cmmc-test
cd cmmc-test
cp /path/to/cmmc-practice-test.jsx src/App.jsx
npm start
```

### Build for Production
```bash
npm run build
```
Deploy the `/build` folder to Vercel, Cloudflare Pages, or GitHub Pages.

---

## Deploy to Vercel (Free)

```bash
npm install -g vercel
vercel
```

Follow the prompts — Vercel auto-detects React and deploys in ~60 seconds.

---

## Planned Additions

- [ ] CISSP domain practice test (8 domains, 125 questions)
- [ ] CEH v13 scenario-based questions
- [ ] Azure AZ-305 architecture review quiz
- [ ] Flashcard mode for acronyms and definitions

---

## Notes

- All question data is embedded in the component — no backend required
- Results are stored in React state only (not persisted between sessions)
- CMMC Level 2 requires 110 practices from NIST SP 800-171 — all 110 are represented
