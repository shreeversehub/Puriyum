# Puriyum — Your Lab Report, Explained in Your Language

**Theme:** Healthcare & Wellbeing
**Tagline:** Understand your health report in 60 seconds, on WhatsApp, in your own language.

---

## 1. The Problem

Every day, millions of people in India walk out of a diagnostic lab holding a report full of numbers, units and abbreviations (HbA1c, TSH, SGPT, Creatinine) that nobody explained to them. The doctor's appointment is often days away, and the report is in English.

What happens next:
- **Panic:** a value flagged "High" sends families into fear and late-night Googling.
- **Neglect:** a slightly abnormal value is ignored because "the lab didn't call me".
- **Misinformation:** forwarded WhatsApp advice and unverified websites fill the gap.
- **Language barrier:** patients who are most vulnerable (rural, elderly, first-generation literate) are least able to read English medical reports.

**What is not working well enough?** The last mile between a lab result and a patient's understanding.

> *Add 2-3 verified statistics here with sources (e.g., health literacy, doctor-to-patient ratio, share of English-literate population) before submitting.*

## 2. Persona

**Meenakshi, 58, a small-town tailor.** She gets a diabetes and thyroid panel done. The report says "HbA1c 8.1%, TSH 6.4". Her son works in another city, her doctor is booked for 4 days. She doesn't know if this is urgent. She sends the photo of the report to Puriyum on WhatsApp and gets a voice and text explanation in Tamil within a minute: what each value means, which ones need attention, and what to ask the doctor.

## 3. The Solution

**Puriyum** (Tamil: *"it will be understood"*) is a WhatsApp-based assistant that turns any lab report into a simple, safe, personalised explanation.

**How it works**
1. **Send:** the user sends a photo or PDF of the report to the Puriyum WhatsApp number.
2. **Read:** OCR extracts test names, values, units and reference ranges.
3. **Check:** a rules layer compares each value with standard reference ranges (adjusted for age and sex if provided) and classifies it as 🟢 Normal, 🟡 Watch, or 🔴 See a doctor soon.
4. **Explain:** an AI model writes a plain-language summary in the user's chosen language (Tamil, Hindi, Telugu, English and more), in text and an optional voice note.
5. **Prepare:** it suggests 3-5 questions to ask the doctor and general lifestyle pointers, never a prescription.
6. **Escalate:** critically abnormal values trigger an urgent "please see a doctor today" message, with an option to connect to a partner clinic or teleconsult.

**What it will never do**
- Diagnose a disease.
- Recommend or change medication.
- Replace a doctor.

Every message carries a clear disclaimer, and the rules layer (not the AI) decides the severity colour, so the safety-critical part is deterministic and auditable.

## 4. What Makes It Original

- **No new app:** it lives in WhatsApp, where users already are.
- **Language-first design:** built for regional languages and voice, not just English text.
- **Safety by architecture:** the AI only explains, while verified reference ranges and escalation rules decide severity.
- **Doctor-ready output:** it improves the consultation instead of replacing it, which builds trust with the medical community.
- **Explainability:** each flag shows *why* (the value, the normal range and what it generally indicates).

## 5. Feasibility

| Component | Approach |
|---|---|
| Channel | WhatsApp Business API |
| Report reading | OCR plus a table parser for common lab formats |
| Severity logic | Curated reference-range database, reviewed by medical advisors |
| Explanation | LLM with strict prompt rules and output validation |
| Languages | Start with Tamil and English, then expand |
| Voice | Text-to-speech for voice notes |
| Privacy | Reports deleted after processing, minimal data stored, consent on first message, personal data masked before AI processing |

**Pilot plan (first 90 days)**
- Month 1: build a prototype for the 10 most common tests (CBC, lipid, blood sugar, HbA1c, thyroid, liver, kidney).
- Month 2: pilot with 2-3 local diagnostic labs and 200 patients, with doctor review of samples.
- Month 3: measure accuracy, comprehension and satisfaction, then refine and expand.

## 6. Business Model

- **B2B2C (primary):** diagnostic labs pay a small per-report fee to offer Puriyum as a value-added service, which gives them retention and a differentiator.
- **Free for patients:** a basic explanation of every report.
- **Premium (optional):** trend tracking across reports, family profiles and teleconsult referrals.
- **Referral revenue:** partner clinics and teleconsult services for escalated cases.

## 7. Impact

- **Patients:** less panic and neglect, better-informed doctor visits, and earlier action on abnormal values.
- **Doctors:** shorter consultations because patients arrive with prepared questions.
- **Labs:** better patient experience at very low cost.
- **Society:** a step toward health literacy that is inclusive of language and literacy gaps.

**Success metrics:** report-comprehension score before and after, share of abnormal reports followed by a doctor visit, user satisfaction, and accuracy of severity classification against doctor review.

## 8. Risks and Mitigations

| Risk | Mitigation |
|---|---|
| Wrong or misleading explanation | Rules-based severity, validated reference ranges, output checks, mandatory disclaimer |
| OCR errors | Show extracted values back to the user for confirmation, and refuse to explain low-confidence reads |
| Privacy of health data | Consent, encryption, deletion after processing, compliance with India's DPDP Act |
| Over-reliance on the tool | Constant nudge to consult a doctor, with no diagnosis or treatment advice |
| Language quality | Native-speaker review of templates and testing with real users |

## 9. Roadmap

1. **Now:** concept, flow and safety design (this submission).
2. **0-3 months:** prototype and lab pilot.
3. **3-9 months:** more languages, voice-first mode, trend tracking.
4. **9-18 months:** teleconsult integration, ABDM/health-record integration, expansion across states.

## 10. Closing Line

Healthcare shouldn't end at the lab counter. **Puriyum makes sure every patient understands their own health, in the language they think in.**

---

### Submission checklist
- [ ] Add 2-3 sourced statistics in Section 1
- [ ] Pick the theme **Healthcare & Wellbeing** on Devpost
- [ ] Paste sections into the Devpost fields (or upload as PDF)
- [ ] Add a flow diagram or 3-4 slides as an image or file if allowed
- [ ] Submit at least 30 minutes before the Oct 4, 2:30 am IST deadline
