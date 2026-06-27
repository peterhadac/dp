# Thesis Writing Plan — Roadmap

**Thesis (SK):** Využitie moderných technológií a digitálnych nástrojov v ošetrovateľstve
**Thesis (EN):** Use of Modern Technologies and Digital Tools in Nursing
**Student:** Timea Bystričanová · TU Trnava, Fakulta zdravotníctva a sociálnej práce · Ošetrovateľstvo, Mgr.
**Deadline:** 31 March 2027 (upload to MAIS)
**Status:** Starting from scratch.

> See `CLAUDE.md` for full scope, formal requirements, and AI usage policy.

---

## Recurring Rules (apply to every phase)

- **Language:** Claude works in **English** → Timea translates to Slovak. Translation is Timea's own work.
- **Sources:** maximum age **5 years** (2021–2026); always include **3–4 Slovak** sources; min **30 total**, ≥15 foreign.
- **AI policy (Smernica č. 18/2025):** no AI-generated Slovak thesis text submitted directly; disclose AI use with `[UI]` citation. Grammar/format checks need no citation.
- **Format:** IMRAD · Times New Roman 12 · justified · 1.5 spacing · 50–70 normalized pages · ISO 690 citations.
- **Version control:** commit drafts and research outputs to git as work progresses.

---

## Skills & Tools

### Already installed (Claude skills + agents)
| Skill / Agent | Use |
|---------------|-----|
| `/gpt-researcher` | Autonomous web research, cited reports |
| `academic-researcher` | Literature reviews, paper analysis, citations |
| `deep-research` | Multi-source fact-checked research |
| `/thesis-advisor` | Orchestrator for the whole pipeline |
| `topic-explorer` (agent) | Research gaps, question/hypothesis formulation |
| `literature-analyst` (agent) | Systematic review, theoretical framework |
| `methodology-expert` (agent) | Research design, validity |
| `writing-coach` (agent) | Structure, drafting, argumentation |
| `proofreader` (agent) | Grammar, format, citation, consistency |
| `academic-writing-style` (skill) | Academic register, hedging, metadiscourse |
| `research-methodology` (skill) | Quantitative/qualitative design, validity |

### To install (system tools — the only real gap)
```bash
sudo apt-get install -y poppler-utils pandoc
```
- `poppler-utils` (`pdftotext`) — extract text from the 14 example theses + rules PDFs.
- `pandoc` — convert finished Markdown chapters → DOCX (Times New Roman 12, 1.5) for submission.

No new Claude skills required. ISO 690 citations handled manually by Claude.

---

## 12-Phase Roadmap

Each phase: **goal · tool/agent · output.**

### Phase 0 — Setup
- Install `poppler-utils` + `pandoc`.
- Create `docs/{chapters,questionnaire,bibliography,research}/`.
- `pdftotext` the 14 example theses → `docs/research/_examples/` (reference for length, depth, Slovak register, citation style).

### Phase 1 — Research landscape
- **Goal:** map WHERE to search.
- **Tool:** `/gpt-researcher`.
- **Output:** `docs/research/00-sources-map.md` — databases (PubMed, CINAHL, Scopus, Web of Science, IEEE Xplore, ScienceDirect) + Slovak journals/repositories.

### Phase 2 — Literature research (8 topic areas)
- **Goal:** gather evidence across all sub-topics (EHR, telemedicine, mHealth, smart monitoring, nurses' attitudes, care quality/safety, education vs. adoption, experience vs. attitudes).
- **Tools:** `/gpt-researcher` + `literature-analyst` agent per area. Sources ≤5 yrs, 3–4 Slovak.
- **Output:** `docs/research/01..08-*.md` + running bibliography.

### Phase 3 — Topic & theoretical framework
- **Goal:** validate research questions & H1–H4 against the literature; build theoretical framework.
- **Agents:** `topic-explorer`, `literature-analyst`.
- **Output:** confirmed hypotheses + framework outline.

### Phase 4 — Methodology finalize
- **Goal:** lock sample (100–200 nurses, ≥1 yr experience), instrument, statistics (Chi-square, p<0.05).
- **Tools:** `methodology-expert` agent + `research-methodology` skill.
- **Output:** `docs/chapters/02-methods.md`.

### Phase 5 — Questionnaire
- **Goal:** full instrument operationalizing H1–H4 (Likert + categorical → enables Chi-square).
- **Tool:** Claude drafts in English → Timea translates → Google Forms → pilot 5–10 nurses.
- **Output:** `docs/questionnaire/`.

### Phase 6 — Theoretical part (Introduction / literature review)
- **Goal:** write theoretical chapters.
- **Tools:** `writing-coach` agent + `academic-writing-style` skill.
- **Output:** `docs/chapters/01-introduction.md`.

### Phase 7 — Data collection *(Timea's real-world task)*
- **Goal:** distribute printed + Google Forms; gather 100–200 responses.
- **Note:** Claude cannot do this. Milestone gate before analysis.

### Phase 8 — Data analysis
- **Goal:** descriptive (frequencies, means, medians) + inferential (Chi-square) stats; tables/graphs.
- **Tools:** MS Excel (per methodology); `python3` optional cross-check helper.
- **Output:** analysis tables/graphs.

### Phase 9 — Results + Discussion
- **Goal:** objective results (no interpretation) → discussion (interpretation, hypothesis verdicts, limitations, future research) → 3–4 recommendations for practice.
- **Tool:** `writing-coach` agent.
- **Output:** `docs/chapters/03-results.md`, `docs/chapters/04-discussion.md`.

### Phase 10 — Conclusion + front/back matter
- **Goal:** conclusion (ties to thesis goals); abstract SK+EN (100–200 words, 5 keywords each); lists (tables/graphs/abbreviations/figures); references in **ISO 690** (≥30, ≥15 foreign).
- **Output:** `docs/chapters/05-conclusion.md`, `docs/bibliography/`.

### Phase 11 — Proofread & compliance
- **Goal:** grammar, ISO 690 consistency, IMRAD flow, length 50–70 pages, formal formatting, plagiarism risk.
- **Tool:** `proofreader` agent.

### Phase 12 — Assemble & submit
- **Goal:** final document.
- **Tool:** `pandoc` Markdown → DOCX (Times New Roman 12, justified, 1.5).
- **Steps:** Timea finalizes in Word, adds AI-disclosure `[UI]` statement, cover/title/declaration, uploads to MAIS by **31 March 2027**.

---

## Command Reference

```bash
# One-time setup
sudo apt-get install -y poppler-utils pandoc

# Extract an example thesis to text
pdftotext "assets/google/older/<file>.pdf" docs/research/_examples/<name>.txt

# Export a finished chapter to DOCX
pandoc docs/chapters/01-introduction.md -o introduction.docx
```

## Skill Trigger Cheat Sheet

```
/thesis-advisor      # full pipeline orchestrator
/gpt-researcher      # autonomous research on a topic
/deep-research       # multi-source fact-checked report
```
Agents (`topic-explorer`, `literature-analyst`, `methodology-expert`, `writing-coach`, `proofreader`) are dispatched via the Agent tool, individually or by the `thesis-advisor` orchestrator.
