# Appendix A — AI Prompt Log
HW01-AI | Student: [Your Student ID]
Tool(s) declared: [list tools used, e.g., Claude Sonnet 4.6, ChatGPT-4o]

> Every prompt sent to any AI tool during this homework must be logged here with a real timestamp.
> Format: ## [HH:MM dd/mm/yyyy] — [Tool Name]
> Use `/plog` command to append entries.

---

<!-- Add entries below using /plog command -->

## [14:00 25/05/2026] — Claude Sonnet 4.6
**Purpose**: R1 — Draft Requirement 1 section (QA/QC job market); format 10 job postings from raw OCR text into structured report entries with job description summary, required skills, salary, and AI Impact Analysis skeleton
**Prompt**:
> currently I'm doing the first requirement. I've copied and pasted 10 images of job postings on @week_1/artifacts/job_screenshots. For jds and info, I've written in the plain text in the report file. Help me to write the first replace it with the first requirement, and leave the skeleton for AI Impact Analysis so that later I will fill myself

**Artifact produced**: `week_1/report/report.md` — Requirement 1 section with all 10 job postings formatted (summary, skills, salary, AI Impact Analysis skeleton for each)

---

## [14:10 25/05/2026] — Claude Sonnet 4.6
**Purpose**: R1 — Add inline image references to job postings and fill in AI Impact Analysis for all 10 jobs
**Prompt**:
> Help me to create reference to the corresponding images as well so that it can be displayed in md file. Also, help me to fill the impact analysis, I'll just edit it later

**Artifact produced**: `week_1/report/report.md` — Added `![Job Posting N](../artifacts/job_screenshots/N.png)` tags to all 10 entries; filled AI Impact Analysis paragraphs for all 10 jobs (student to review and personalise)

---

## [14:20 25/05/2026] — Claude Sonnet 4.6
**Purpose**: R1 — Reformat inconsistent Link and Location fields across all 10 job entries
**Prompt**:
> Help me to reformat the md, especially in link and location section

**Artifact produced**: `week_1/report/report.md` — Standardised all links to `[View posting](URL)` format; removed redundant `**Screenshot**:` lines; added missing Link fields for Jobs 4 and 6; added ⭐ AI/LLM label to Job 9 heading

---

## [14:30 25/05/2026] — Claude Sonnet 4.6
**Purpose**: R2 — Draft Requirement 2 section: 20 software defects 2022–2026, with ≥ 5 AI/LLM-related defects; each entry includes source, description, severity, consequences, solution/fix, and documented AI bias/hallucination found when explaining that defect
**Prompt**:
> Help me to do the second requirement. Make sure to find 20 software defects, where at least 5 defects related to AI/LLM like what mentioned in the requirement.

**Artifact produced**: `week_1/report/report.md` — Requirement 2 section with all 20 defects (Defects 1–5 AI/LLM: ChatGPT legal citations, Google Bard JWST, Air Canada chatbot, Bing Chat Sydney, Meta AI minors; Defects 6–20: OpenSSL CVE-2022-3602, LastPass vault breach, MOVEit CVE-2023-34362, CrowdStrike BSOD, Twitter API breach, Operation Triangulation, 23andMe, Exchange ProxyNotShell, Okta support breach, Toyota data leak, Telerik CVE-2024-4358, iOS 17 autocorrect, Chrome CVE-2023-2033, Samsung Exynos CVE-2023-24033, iOS NameDrop misinformation)

---

## [11:33 25/05/2026] — Claude Sonnet 4.6
**Purpose**: R3 — Generate 15 ISTQB-aligned test cases for Senko DTS1607 stand fan (Challenge Mode: with self-documented hallucinations and intentionally omitted edge cases for student analysis)
**Prompt**:
> Act as an ISTQB Test Analyst. I am testing a physical product: Senko DTS1607.
> 1. Test Design: Generate exactly 15 test cases for this device. Format them in a table with exactly these 6 columns: Objective | Input | Steps | Expected | Actual | Verdict.
> 2. ISTQB Alignment: Use formal test design techniques (e.g., Equivalence Partitioning for temperature/speed settings, Boundary Value Analysis for timers).
> 3. AI Audit Report: Immediately following the table, provide the mandatory 5-section [AI-02] AI Audit Report for this artifact. In section (1), use this exact prompt with the current timestamp. In section (4), provide 2-5 sentences of reasoning citing specific ISTQB Foundation Level sections. Leave sections (3) and (5) blank for my manual review.

**Artifact produced**: `week_1/report/report.md` — Requirement 3 section: device declaration table + 15 test cases (TC-01–TC-15) with EP/BVA technique application, 4 self-documented hallucinations (H1: fabricated airflow spec; H2: wrong ISTQB section ref; H3: unverified timer max; H4: uncertain safety standard). Audit Entry 3 added to `ai_compliance/audit_report.md`. (Defects 1–5 AI/LLM: ChatGPT legal citations, Google Bard JWST, Air Canada chatbot, Bing Chat Sydney, Meta AI minors; Defects 6–20: OpenSSL CVE-2022-3602, LastPass vault breach, MOVEit CVE-2023-34362, CrowdStrike BSOD, Twitter API breach, Operation Triangulation, 23andMe, Exchange ProxyNotShell, Okta support breach, Toyota data leak, Telerik CVE-2024-4358, iOS 17 autocorrect, Chrome CVE-2023-2033, Samsung Exynos CVE-2023-24033, iOS NameDrop misinformation)