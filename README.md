# SafeMind

**AI-based Dynamic Mental Health Monitoring and Distress Prediction System**
Built for Smart India Hackathon — Problem Statement: continuous psychological well-being monitoring for victims and complainants under the SC/ST (Prevention of Atrocities) Act, 1989, registered via NHAA (14566), the Integrated Portal, chatbot, mobile app, IVRS, or other approved channels.

SafeMind extends victim support beyond one-time legal and financial relief. It checks in on people regularly through the investigation, trial, and rehabilitation process, scores their distress over time, and alerts counsellors and district officials before a crisis happens — not after.

---

## 1. Problem it solves

Victims of atrocities often face threats, repeated court appearances, trial delays, social boycott, and economic hardship long after a complaint is filed. Current schemes cover legal aid and compensation, but nobody is watching how the victim is actually doing in between. SafeMind is that continuous layer.

## 2. Who uses it

The app opens behind a disguised home screen. A small gear icon in the top right opens the PIN gate, which then routes into one of three roles:

| Role | PIN (demo) | What they see |
|---|---|---|
| **Self / victim** | '1234' | Daily check-ins, mood tracking, journal, breathing and grounding games, counsellor homework, SOS, resources, community hub |
| **Counsellor** | '8899' | Client list, mood/distress charts, homework assignment, prescribed clinical tasks, case notes |
| **District admin** | '9900' | NHAA case registry, distress predictions, intervention hub, compensation (Annexure-I) tracker, analytics dashboards |

A **caregiver** view is also supported for a trusted family member to view (not edit) a loved one's wellbeing trend.

> Demo PINs are hardcoded for the prototype and must be replaced with real authentication before any pilot or production use.

## 3. Core features

**Distress monitoring**
- Daily mood check-ins with a running Dynamic Distress Score (DDS) and trend charts
- 4-Dimensional telemetry: Psychological, Social Boycott, Financial/Livelihood, and Physical Threat vectors, mapped to specific SC/ST (PoA) Act sections (e.g. Sec 3(1)(za), Sec 15A, Sec 3(1)(r), Sec 3(1)(g))
- Rule-based risk prediction and escalation flagging when thresholds are crossed
- Explainable AI (XAI) panel showing why a score was raised

**Reach and accessibility**
- In-app chatbot for check-ins
- "Bolo Aur Bhejo" voice grievance recorder for Hindi/regional-dialect statements, with on-device transcription and distress extraction
- Multilingual interface (English/Hindi, extensible)
- Silent SOS / distress geo-ping to a designated police unit and 112, disguised behind a decoy home screen for safety when a phone might be checked by someone else

**Support and self-help tools**
- Breathing and grounding exercises (box breathing, 4-7-8, 5-4-3-2-1 grounding)
- Stress-relief mini-games (bubble wrap pop, mandala drawing, worry balloon release, affirmation memory match, zen sand canvas)
- Gratitude log and reflective journal
- Psychoeducation resource library
- Safe Space community hub with verified crisis helplines

**Case, relief, and coordination tools**
- NHAA district case registry with search/filter
- Statutory compensation tracker (Rule 12(4), Annexure-I) showing disbursed vs. pending relief stages
- Counsellor homework assignment and completion tracking
- Admin intervention hub for logging protection, relocation, legal aid, or medical actions
- District/State-level analytics for policymakers

## 4. How it fits the problem statement

| Expected solution component:              |  Where it lives in SafeMind:                      |
| Periodic interaction via chatbot/IVRS/app |  Home check-ins, chatbot, voice grievance         |
| NLP, Sentiment & Emotion AI               |  Text/voice analysis feeding the DDS              |
| Dynamic Distress Score + trend            |  Mood charts, 4D telemetry, DDS                   |
| Predict escalation before crisis          |  Predict Risk risk modelling, alert triggers      | 
| Alerts to counsellors/district officials  |  Alert rendering, admin case registry             |
| Recommend interventions                   |  Admin intervention hub, homework assignment      |
| Dashboards (district/state/national)      |  Admin analytics, counsellor client charts        |
| Explainable AI, privacy, security         |  XAI panel, PIN-gated roles, on-device processing |

## 5. Tech stack

- Single-file front end: HTML, CSS, vanilla JavaScript
- [Chart.js](https://www.chartjs.org/) for mood and distress visualizations
- Client-side state via localStorage (persistent) and sessionStorage (session/role unlock)
- No external backend in this prototype — all data currently lives in the browser

## 6. Running it

This is a static, single-file app.

1. Open the HTML file directly in a browser.
2. Navigate to the app and complete onboarding as the **self** role, or use the role switcher on the gate screen to try **counsellor** or **district admin**.
3. All data is stored locally in the browser. Use the settings screen's export/clear options to reset or back up demo data.

## 7. Known limitations (prototype stage)

- Demo PINs are static and not secure — replace with proper multi-factor auth
- No real backend, database, or NHAA/IVRS integration yet — case data, compensation status, and alerts are simulated
- Sentiment/Emotion AI and risk prediction are rule-based placeholders standing in for a trained NLP/ML model
- Not yet audited for data protection compliance (DPDP Act, IT Rules) — required before handling real victim data
- Voice transcription is currently simulated rather than using an actual speech engine

## 8. Roadmap

- Real NLP/Emotion AI pipeline (multilingual) replacing the rule-based scorer
- Server-side storage with encryption at rest and in transit, and role-based access control
- Live integration with NHAA (14566), IVRS, and the Integrated Portal
- SMS/IVRS fallback for feature-phone users in low-connectivity areas
- Formal explainability report per alert for auditability by district authorities
- Consent and data-retention workflow aligned with applicable privacy law

---

*Prototype built for Smart India Hackathon. Not for use with real victim data until security, privacy, and clinical-safety review is complete.*
