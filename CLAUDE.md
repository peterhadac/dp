# Timea's Master Thesis — Claude Instructions

## Project Identity

| Field | Value |
|-------|-------|
| Student | Timea Bystričanová |
| Year | 1st → 2nd year Mgr. (2025/2026 → 2026/2027) |
| Institution | Trnavská univerzita v Trnave |
| Faculty | Fakulta zdravotníctva a sociálnej práce |
| Program | Ošetrovateľstvo (Nursing), Mgr. |
| Title (SK) | Využitie moderných technológií a digitálnych nástrojov v ošetrovateľstve |
| Title (EN) | Use of Modern Technologies and Digital Tools in Nursing |
| Deadline | 31 March 2027 (upload to MAIS) |
| Status | Not started — beginning from scratch |

---

## Thesis Scope

### Research Problem
Identify the extent of modern technology use in nursing, factors influencing adoption, and the perceived impact on quality of nursing care.

### Main Goal
Analyze the use of modern technologies and digital tools in nursing practice; evaluate their impact on quality and efficiency of nursing care.

### Partial Goals
1. Determine extent of technology use by nurses in clinical practice
2. Identify most common digital tools used in nursing
3. Examine nurses' attitudes toward digital technology implementation in healthcare facilities
4. Determine impact of digital tools on work efficiency, communication, and quality of care
5. Assess impact of modern technologies on quality, safety, and continuity of nursing care

### Hypotheses
- **H1:** Statistically significant relationship between frequency of digital tool use and nurses' self-assessment of work efficiency
- **H2:** Nurses with higher education (bachelor's, master's, or specialization) use modern technologies more frequently than nurses with secondary education
- **H3:** Statistically significant relationship between years of clinical experience and attitude toward digital technologies
- **H4:** More than 50% of nurses rate electronic health documentation as contributing to improved quality and safety of nursing care

### Research Design
- **Method:** Quantitative — non-standardized questionnaire (own construction)
- **Sample:** 100–200 nurses; inpatient facilities + outpatient clinics in Slovakia; ≥1 year clinical experience; voluntary participation
- **Distribution:** Printed questionnaires + Google Forms (electronic)
- **Statistics:** MS Excel; descriptive (absolute/relative frequencies, means, medians, tables/graphs) + inferential (Chi-square test of independence, significance level p < 0.05)

---

## Formal Requirements

### Document Formatting
| Parameter | Requirement |
|-----------|-------------|
| Length | 50–70 normalized pages (90,000–126,000 chars incl. spaces) |
| Font | Times New Roman 12pt |
| Alignment | Justified (both margins) |
| Line spacing | 1.5 |
| Page numbering | Arabic numerals, bottom center or outer margin |
| Language | Slovak (academic plural, formal register) |
| Voice | 3rd person singular, passive voice, past tense (especially abstract) |

### Required Structure (IMRAD)
1. **Introduction (Úvod)** — topic context, why it matters, goals, research questions/hypotheses, brief literature overview
2. **Methods (Metódy)** — sample selection, research instrument, data collection procedure, statistical methods
3. **Results (Výsledky)** — objective presentation of findings (tables, graphs); no interpretation
4. **Discussion (Diskusia)** — interpretation of results, relation to theory and other studies, hypothesis evaluation, limitations, future research directions
5. **Recommendations for Practice** — 3–4 specific, evidence-based, realistic recommendations (end of Discussion chapter, new page)
6. **Conclusion (Záver)** — summary of the thesis (not research) goals; impersonal form, past tense

### Mandatory Document Sections (in order)
Cover page → Title page → Assignment → Declaration of authorship → Acknowledgements (optional) → Abstract SK + keywords (5) → Abstract EN + keywords (5) → Table of contents → List of tables → List of graphs → List of abbreviations → List of figures → Glossary (if needed) → IMRAD body → References → Appendices

### References
- Minimum 30 scholarly sources
- At least 15 foreign (non-Slovak) sources
- Maximum source age: **5 years** (2021–2026) — stricter than university minimum of 70% ≤10 years
- Always include **3–4 Slovak-language sources**
- International sources are the superset; Slovak sources supplement but do not replace them
- Citation format: **ISO 690** (per Smernica rektora TU Trnava č. 20/2021)
- Bibliography: alphabetically ordered, must match all in-text citations

### Plagiarism
Work submitted to CRZP (Centrálny register záverečných prác) and checked via Antiplagiátorský systém. All sources must be properly cited.

---

## AI Usage Policy

Rules from **Smernica rektora č. 18/2025** (effective 6.10.2025):

### Forbidden
- Presenting AI-generated text as own work
- Using AI to generate entire texts or sections
- Using AI to formulate claims or write summaries

### Allowed — must cite with [UI]
- AI-assisted translation
- AI-generated images or figures

### Allowed — no citation needed
- Grammar and formatting checks

### AI Citation Format
```
[UI] ServiceName (version), dostupné na: URL, [YYYY-MM-DD], prompt: "..."
```

---

## Claude's Role in This Project

**Language:** Claude always communicates in **English**. Claude reads and understands Slovak. The thesis is written in Slovak by Timea. Claude drafts in English; Timea translates (translation is her work, not AI-generated thesis text).

**Claude assists with:**
- Structural guidance and chapter outlining
- Drafting content in English (for Timea to translate)
- Research assistance via `/gpt-researcher`
- Full questionnaire design (English, to be translated)
- Bibliography compilation and ISO 690 citation formatting
- Feedback on chapter drafts for structure, logic, coverage
- Checking compliance with formal requirements

**Claude must NOT:**
- Write Slovak text intended for direct submission
- Generate summaries or claims to be presented as Timea's own formulations without [UI] disclosure

---

## Research Phase

### Step 1: Identify Where to Search
Use `/gpt-researcher` first to map the research landscape — identify the best databases, journals, and repositories:

**International:**
- PubMed / MEDLINE
- CINAHL (Cumulative Index to Nursing and Allied Health Literature)
- Scopus
- Web of Science
- IEEE Xplore (for technology/health informatics angle)
- ScienceDirect

**Slovak:**
- Slovak nursing journals (Sestra, Ošetrovateľstvo a pôrodná asistencia)
- CRZP (for orientation on Slovak academic coverage)
- University repositories (TU Trnava, UK Bratislava, UPJŠ Košice)

### Step 2: Research Topic Areas
Run `/gpt-researcher` on each area, sources max 5 years old:

1. Electronic health records (EHR) — adoption and impact in nursing
2. Telemedicine and nursing practice
3. Mobile health applications in nursing
4. Smart monitoring and wearable systems in clinical settings
5. Nurses' attitudes toward digital technology
6. Impact of digitalization on care quality, safety, and continuity
7. Education level vs. technology adoption in nursing (links to H2)
8. Clinical experience vs. technology attitudes in nursing (links to H3)

**Output:** Save all research outputs to `docs/research/` as separate Markdown files.

---

## Questionnaire Design

Claude creates the full questionnaire in English. Timea translates to Slovak for distribution.

**Structure:**
- **Part 1 — Demographics:** education level, years of experience, workplace type (inpatient/outpatient), ward type
- **Part 2 — Technology Use:** frequency of digital tool use, tool types, barriers to adoption
- **Part 3 — Perceived Impact:** quality, safety, efficiency, communication

**Design constraints:**
- Items must operationalize H1–H4 for Chi-square testing
- Likert scale (5-point) for frequency/attitude items
- Categorical/binary items for demographic grouping
- Pilot test on 5–10 nurses before full distribution (per methodology)

**Save to:** `docs/questionnaire/`

---

## Repository Structure

```
dp/
├── CLAUDE.md                    # This file
├── .gitignore                   # Excludes assets/google/**
├── assets/google/               # Symlink → Google Drive: /mnt/g/My Drive/Timea DP/
│   ├── older/                   # 14 example master's theses (reference)
│   ├── rules/                   # University rules PDFs
│   │   ├── Usmernenie-k-Mgr-pracam-2025.pdf      # Thesis writing guidelines
│   │   └── smernica-o-vyuzivaní-AI-v-pracach-18_2025.pdf  # AI usage policy
│   └── theme/                   # Research design DOCX (Bystričanová)
├── docs/
│   ├── chapters/                # Draft chapters in English
│   │   ├── 01-introduction.md
│   │   ├── 02-methods.md
│   │   ├── 03-results.md
│   │   ├── 04-discussion.md
│   │   └── 05-conclusion.md
│   ├── questionnaire/           # Questionnaire drafts and final version
│   ├── bibliography/            # ISO 690 formatted references
│   └── research/                # /gpt-researcher output files
└── README.md
```

### Example Theses (`assets/google/older/`)
14 hash-named PDFs — previous nursing master's theses from the same faculty. Use as reference for:
- Appropriate length, depth, and complexity per chapter
- Slovak academic register and nursing terminology
- Faculty-specific structural conventions
- Citation style and bibliography formatting

> **Note:** Reading these PDFs requires `poppler-utils` (`sudo apt-get install poppler-utils`). Currently not installed.

---

## Workflow Summary

1. **Research** → `/gpt-researcher` per topic area → save to `docs/research/`
2. **Outline** → Claude drafts chapter structure → review with Timea
3. **Questionnaire** → Claude creates English version → Timea translates → pilot → distribute
4. **Chapters** → Claude drafts in English → Timea translates to Slovak → saved in `docs/chapters/`
5. **Bibliography** → Claude formats in ISO 690 → save to `docs/bibliography/`
6. **Data analysis** → MS Excel (descriptive + Chi-square) → results documented in `docs/chapters/03-results.md`
7. **Final review** → check IMRAD flow, reference count, formal requirements, length
8. **Submission** → upload final Slovak document to MAIS by 31 March 2027
