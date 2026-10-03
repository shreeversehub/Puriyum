# 🩺 Puriyum (புரியும்)

> Your lab report, explained in your language.

Puriyum explains lab reports on WhatsApp in the patient's own language (English, Tamil, Hindi), with safe color-coded results and questions to ask the doctor. Built for the **Graphiques Innovation Challenge** (Healthcare & Wellbeing).

🎥 **Demo video:** _add your YouTube link here_

## The problem
Patients leave labs with reports full of numbers they can't read, often in English. They panic, ignore abnormal values, or turn to unreliable sources while waiting for a doctor.

## The solution
Send a report, get a plain-language explanation:
- 🟢 Normal · 🟡 Keep an eye · 🔴 See a doctor soon
- Short "what this means" for each abnormal value
- Questions to ask the doctor
- Voice playback
- **Never diagnoses, never suggests medicines**

**Safety by design:** a fixed rules engine decides severity. AI (in the planned full version) only explains.

## Run the prototype
No installation needed.

**Option 1:** double-click `index.html` (opens in your browser).

**Option 2:** local server
```bash
python -m http.server 8000
# open http://localhost:8000
```

### Try it
1. Click **Sample: Meenakshi** (or edit any value).
2. Choose English / தமிழ் / हिन्दी.
3. Click **Send report on WhatsApp**.
4. Click **🔊 Listen** to hear the summary (browser voice support varies).

## What's in the prototype
- WhatsApp-style chat UI
- Rules engine for 7 tests: HbA1c, fasting sugar, TSH, total cholesterol, hemoglobin, creatinine, SGPT
- Multilingual explanations (English, Tamil, Hindi)
- Text-to-speech via the Web Speech API

> OCR (reading a photo of the report) and the WhatsApp Business API are part of the planned architecture. In this prototype, the editable form stands in for OCR.

## Planned architecture
WhatsApp Business API → OCR + table parser → rules-based severity engine → AI explanation layer (validated output) → escalation to partner clinic / teleconsult.

## Tech
HTML · CSS · JavaScript · Web Speech API

## Project structure
```
puriyum/
├── index.html        # working prototype
├── README.md
├── LICENSE
└── docs/
    └── SUBMISSION.md # full project write-up
```

## Roadmap
- 0-3 months: lab pilot with ~200 patients
- 3-9 months: more tests/languages, voice-first mode, trend tracking
- 9-18 months: teleconsult and health-record integration

## Disclaimer
Puriyum is an educational tool, not a medical device. It does not diagnose or treat. Always consult a qualified doctor.

## License
MIT
