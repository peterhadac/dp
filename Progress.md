# Thesis Progress Tracker

**Thesis:** Use of Modern Technologies and Digital Tools in Nursing
**Student:** Timea Bystričanová · TU Trnava · Ošetrovateľstvo, Mgr.
**Deadline:** 31 March 2027

---

## Decisions Log

| # | Date | Phase | Decision | Rationale |
|---|------|-------|----------|-----------|
| 1 | 2026-06-26 | Setup | Writing full thesis in English | User goal; translation to Slovak is Timea's task |
| 2 | 2026-06-26 | Setup | Using IMRAD structure | Required by TU Trnava methodology guidelines |
| 3 | 2026-06-26 | Setup | Quantitative design, non-standardized questionnaire | Matches seminar paper research design |
| 4 | 2026-06-26 | Setup | Chi-square test, p<0.05 | Standard for H1–H4 hypothesis testing |
| 5 | 2026-06-26 | Setup | Sources ≤5 years (2021–2026), ≥30 total, ≥15 foreign, 3-4 Slovak | Stricter than university minimum; ensures currency |
| 6 | 2026-06-26 | Setup | ISO 690 citation format | Per Smernica rektora TU Trnava č. 20/2021 |
| 7 | 2026-06-26 | Scope | Sample: 100–200 nurses, inpatient + outpatient, Slovakia, ≥1yr experience | From seminar paper design |
| 8 | 2026-06-26 | Scope | Hypotheses H1–H4 unchanged from seminar paper | Research design already validated |
| 9 | 2026-06-27 | Writing | Results/Discussion written with [DATA PENDING] placeholders | Data collection requires real survey deployment by Timea |
| 10 | 2026-06-27 | Writing | Chapters written in English; Slovak translation is Timea's task for MAIS submission | Per AI policy Smernica 18/2025 + user goal |
| 11 | 2026-06-27 | Research | 8 parallel literature-analyst agents covered all topic areas | TAM, UTAUT, EHR, telemedicine, mHealth, monitoring, attitudes, care quality, education vs adoption, experience vs attitudes |
| 12 | 2026-06-27 | Writing | Chapter files extracted from _workspace/04_draft_manuscript.md (117KB) | Agents used thesis-advisor harness _workspace convention |

---

## Phase Status

| Phase | Name | Status | Output |
|-------|------|--------|--------|
| 0 | Setup | ✅ Complete | `docs/` structure, poppler-utils, pandoc |
| 1 | Research landscape | ✅ Complete | 8 research reports in `docs/research/` |
| 2 | Literature research | ✅ Complete | `docs/research/01..08-*.md` (8 files, 28-42KB each) |
| 3 | Theoretical framework | ✅ Complete | TAM, UTAUT, Diffusion of Innovations in Chapter 1 |
| 4 | Methodology | ✅ Complete | `docs/chapters/02-methods.md` (35KB) |
| 5 | Questionnaire | ✅ Complete | `docs/questionnaire/questionnaire-en.md` (60KB) |
| 6 | Introduction / Lit review | ✅ Complete | `docs/chapters/01-introduction.md` (21KB) |
| 7 | Data collection | ⏸️ Blocked | Real-world task — Timea distributes to 100-200 nurses |
| 8 | Data analysis | ⏸️ Blocked | Depends on Phase 7 |
| 9 | Results + Discussion | ✅ Template complete | `docs/chapters/03-results.md`, `04-discussion.md` (with [DATA PENDING]) |
| 10 | Conclusion + front/back matter | ✅ Complete | `docs/chapters/05-conclusion.md` |
| 11 | Proofread & compliance | ⏳ Pending | Run proofreader agent when ready |
| 12 | Assemble & submit | ⏳ Pending | pandoc → DOCX after data collection |

---

## Chapter Status

| File | Status | Size |
|------|--------|------|
| `docs/chapters/01-introduction.md` | ✅ Draft complete | 21KB |
| `docs/chapters/02-methods.md` | ✅ Draft complete | 35KB |
| `docs/chapters/03-results.md` | ✅ Template (needs real data) | 19KB |
| `docs/chapters/04-discussion.md` | ✅ Template (needs real data) | 35KB |
| `docs/chapters/05-conclusion.md` | ✅ Draft complete | 4.4KB |
| `docs/questionnaire/questionnaire-en.md` | ✅ Complete (needs Slovak translation) | 60KB |
| `docs/bibliography/references.md` | ✅ Compiled from 8 research reports | 24KB |
| `thesis-draft-en.md` | ✅ Full draft assembled | 115KB |
| `docs/research/01..08-*.md` | ✅ 8 research reports | 28-42KB each |

---

## Research Log

*(Populated as /gpt-researcher runs complete)*

---

## Notes

- Phases 7–9 require real data collection — thesis framework complete without them; Results/Discussion written as template pending data.
- poppler-utils required to read 14 example theses in `assets/google/older/`.
- pandoc required for Markdown → DOCX export at Phase 12.
