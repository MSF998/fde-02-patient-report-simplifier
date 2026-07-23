# Business Requirements Document (BRD)

## Patient Report Simplifier

|            |          |
| ---------- | -------- |
| **Status** | Draft v1 |
| **Owner**  | Product Team |
| **Date**   | July 22, 2026 |
| **Type**   | Consumer Web Application |

## 1. Purpose

This document defines the business requirements for the Patient Report Simplifier — a free, web-based, self-service tool that allows patients to upload their medical reports and receive a plain-language explanation of the contents, along with a structured dashboard of conditions, tests, and risk indicators. The purpose of this BRD is to align stakeholders on scope, requirements, and success criteria ahead of a fast MVP build.

## 2. Background / Problem Statement

Patients regularly receive medical reports — lab results, radiology/imaging reports, discharge summaries, and clinical notes — that are written in dense medical terminology intended for clinicians, not laypeople. This creates confusion, anxiety, and a reliance on waiting for a doctor's appointment just to understand basic findings. There is no simple, free, self-service way for patients to upload a report and immediately get a clear, structured, plain-language explanation of what it means. The Patient Report Simplifier addresses this gap by using OCR and LLM-based summarization to translate medical jargon into layman's terms and surface key insights automatically.

## 3. Objectives

1. Improve patient health literacy by translating medical jargon into plain language
2. Reduce patient anxiety/confusion caused by not understanding their own reports
3. Drive user engagement and repeat usage through longitudinal report tracking (trends across multiple reports)
4. Establish a free, high-engagement consumer tool as a lead-generation/brand-awareness asset (no direct monetization in this phase)
5. Build a scalable foundation for potential future premium features or partnerships

## 4. Target User

**Primary: Self-service Patient** — Individuals who receive medical reports (from labs, hospitals, diagnostic centers) and want to understand them without waiting for a doctor's appointment. They need simple explanations, visual clarity, reassurance, and the ability to track their health over time.

**Secondary: Caregiver/Family Member** — Individuals managing reports on behalf of an aging parent, child, or dependent, with the same needs as above plus multi-report management for another person.

This product is explicitly **not** designed for clinicians, hospital admins, or insurance staff in this phase.

## 5. Scope

### In scope

- Patient-facing web application (self-service, no clinician/admin portal)
- Upload of medical reports as PDF or scanned image files
- OCR-based text extraction from uploaded files
- LLM-based summarization and simplification of medical content into plain language
- Structured extraction of conditions, tests/results, and risk indicators
- Dashboard visualization of extracted insights
- Support for multiple report types: lab/blood tests, radiology/imaging reports, discharge summaries, and general clinical notes
- Trend tracking across multiple reports uploaded over time (e.g., cholesterol trending over 6 months)
- Conversational chatbot for patient follow-up questions about their own report(s)
- Basic informational disclaimer (not a substitute for professional medical advice)
- Clean/clinical dashboard design direction (calming blues/greens, minimal, trust-focused)

### Out of scope

- Mobile native applications (iOS/Android) — web-only for this phase
- Clinician-facing or admin portal/dashboard — no plans for future phases either; product remains patient-only for the foreseeable future
- Direct EHR/HL7/FHIR system integrations
- HIPAA/GDPR-grade compliance infrastructure (audit trails, BAAs, etc.) — basic privacy disclaimer only
- FDA/CE regulatory clearance as a medical device
- Monetization features (subscriptions, payments, premium tiers)
- Multi-language support — English-only

## 6. Success Criteria

| Metric | Target (illustrative — to be finalized with stakeholders) |
| --- | --- |
| Report uploads per month | Track growth trend |
| User return rate (repeat uploads) | Indicator of trend-tracking value |
| Chatbot engagement rate | % of sessions using follow-up Q&A |
| Average processing time per report | < 60 seconds |
| User-reported clarity/satisfaction (survey) | e.g., >80% "easy to understand" |

## 7. Constraints & Assumptions

**Constraints**
- No mobile app in Phase 1 (web-only)
- No clinician or administrative portal in Phase 1; product remains patient-only for the foreseeable future, with no clinician-facing views or EHR/system integrations planned in upcoming phases
- No formal healthcare regulatory certification (not positioned as a medical device)
- Compliance limited to standard privacy disclaimers, not full HIPAA/GDPR infrastructure
- English-only; no multi-language support planned

**Assumptions**
- Users will self-upload their own reports; no direct integration with hospital/lab systems
- OCR quality is dependent on the clarity of the uploaded scan/PDF; extremely poor-quality scans may reduce accuracy
- LLM output will be reviewed periodically for quality/safety, but this is not a clinically validated diagnostic system
- No monetization strategy is required for Phase 1; this is a free engagement/lead-gen tool
- Uploaded reports and account data will be retained indefinitely until the user explicitly deletes them

## 8. Stakeholders

| Role | Who |
| ---- | --- |
| Business Sponsor | TBD |
| Product Owner | Product Team |
| Engineering Lead | TBD |
| Design Lead | TBD |
| End Users | Patients / Caregivers |

## 9. Risks

| Risk | Mitigation |
| ---- | ---------- |
| LLM misinterprets or oversimplifies critical medical findings | Strong disclaimers, conservative language, flagging "consult your doctor" on any abnormal/critical findings |
| OCR inaccuracies on poor-quality scans | Quality checks on upload, prompt user to re-upload clearer scans |
| Users mistaking the tool for medical advice | Persistent, unavoidable disclaimers at upload, summary, and chatbot touchpoints |
| Sensitive health data handling without full regulatory compliance | Clear privacy policy, data encryption, minimal friction for account/data deletion |
| Low user trust in AI-simplified medical content | Transparency about AI-generated content, option to view original report side-by-side |

## 10. High-Level Timeline

Target: **fast MVP launch within a 4-8 week window**. No phased rollout is planned beyond this initial release at this time; scope for the MVP is defined entirely by Section 5 (Scope) above.
