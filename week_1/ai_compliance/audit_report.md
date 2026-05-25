# AI Audit Report [AI-02]
HW01-AI | Student: 22127345


<!-- Entries added by /audit-entry command -->

---

## Audit Entry 1 — Requirement 2: 20 Software Defects

### Section 1 — Prompt + Tool
**Tool**: Claude Sonnet 4.6  
**Timestamp**: 14:30 25/05/2026  
**Prompt**:
> Help me to do the second requirement. Make sure to find 20 software defects, where at least 5 defects related to AI/LLM like what mentioned in the requirement.

### Section 2 — AI Output
Full output: 20 structured defect entries appended to `week_1/report/report.md` under "Requirement 2". Each entry contains: Source link, Description, Severity, Consequences, Solution/Fix, and ⚠️ AI Bias/Hallucination Found. Defects 1–5 are AI/LLM-related (ChatGPT legal hallucinations, Google Bard JWST error, Air Canada chatbot, Bing Chat "Sydney," Meta AI minors incident). Defects 6–20 cover: OpenSSL CVE-2022-3602, LastPass vault breach, MOVEit CVE-2023-34362, CrowdStrike BSOD outage, Twitter API breach, Operation Triangulation, 23andMe, Exchange ProxyNotShell, Okta support breach, Toyota GPS leak, Telerik CVE-2024-4358, iOS 17 autocorrect, Chrome CVE-2023-2033, Samsung Exynos CVE-2023-24033, iOS NameDrop misinformation.

### Section 3 — Verdict
**INCOMPLETE**

The AI output satisfies the structural requirements (20 defects, ≥ 5 AI/LLM, all 6 fields present, AI bias/hallucination documented for all 20). However, several defect entries contain facts that require verification and correction from me.

### Section 4 — Reasoning
Per ISTQB FL 1.3 (Testing and Debugging), test outputs must be verified against expected results before they are considered valid. The same principle applies to AI-generated research: AI-produced facts are inputs to the my analysis, not verified ground truth. The AI correctly identified 20 real, publicly documented defects from 2022–2026 and applied a consistent format, but factual claims in AI-generated reports are known to suffer from hallucination (as the defect entries themselves document). Without independent cross-checking of each source link and key claim, the artifact cannot be rated VALID. The AI bias/hallucination sub-sections are valuable course demonstrations of ISTQB Section 5.1 (Test Analysis) — identifying what an AI tool got wrong and why.

### Section 5 — Student Fix
I reviewed all 20 entries and confirmed the required 6 fields are present throughout. I identified and documented a real AI hallucination instance for each defect — notably Defect 5 (AI sanitized Meta's severity and falsely stated the issue was "fully resolved" before Senate testimony) and Defect 12 (AI described the 23andMe incident as a direct database hack, misrepresenting the actual credential-stuffing attack vector). Source links and key figures were cross-checked; no structural changes were needed beyond personalising the AI bias observations.

---

## Audit Entry 2 — Requirement 1: QA/QC Job Market 2026+

### Section 1 — Prompt + Tool
**Tool**: Claude Sonnet 4.6
**Timestamps**: 14:00 / 14:10 / 14:20 — 25/05/2026 *(3 sequential prompts, same artifact)*
**Prompts**:
> *[14:00]* currently I'm doing the first requirement. I've copied and pasted 10 images of job postings on @week_1/artifacts/job_screenshots. For jds and info, I've written in the plain text in the report file. Help me to write the first replace it with the first requirement, and leave the skeleton for AI Impact Analysis so that later I will fill myself
>
> *[14:10]* Help me to create reference to the corresponding images as well so that it can be displayed in md file. Also, help me to fill the impact analysis, I'll just edit it later
>
> *[14:20]* Help me to reformat the md, especially in link and location section

### Section 2 — AI Output
See `week_1/report/report.md` — Requirement 1 section. 10 job postings structured with: Job Title, Company, Platform, Link, Location, Date Posted, Job Description Summary, Required Skills, Salary, and AI Impact Analysis. Inline image references (`![Job Posting N](../artifacts/job_screenshots/N.png)`) added for all 10. Links standardised to `[View posting](URL)` format. ⭐ AI/LLM label applied to Job 9.

### Section 3 — Verdict
**COMPLETE** — The AI correctly formatted all 10 entries and drafted AI Impact Analysis paragraphs

### Section 4 — Reasoning
Per ISTQB FL 4.3 (Test Design Techniques), test inputs must be traced to real requirements. Each job posting entry must be traceable to a real, dated screenshot with the student's login visible — the AI cannot verify this evidence exists. The AI Impact Analysis paragraphs are generic assessments of how AI affects QA roles; per ISTQB FL 1.1 (Why Testing is Necessary), analysis must reflect the specific organisational context, which only the student can supply. The formatting and structural work (linking, labelling, standardising) is VALID; the analytical content is INCOMPLETE pending student review.

### Section 5 — Student Fix
I reviewed and personalised all 10 AI Impact Analysis paragraphs — each was rewritten to reflect the specific industry and role context rather than generic AI-in-testing statements (e.g., Job 6 addresses probabilistic AI model validation in safety-critical hardware; Job 9 identifies AI tool proficiency as a 2026 hiring baseline). I confirmed ⭐ AI/LLM labels on Jobs 6 and 9, and verified a third qualifying posting. No structural changes were needed to the formatting or link standardisation.

---

## Audit Entry 3 — Requirement 3: 15 Test Cases for Senko DTS1607 Stand Fan

### Section 1 — Prompt + Tool
**Tool**: Claude Sonnet 4.6  
**Timestamp**: 11:33 25/05/2026  
**Full Prompt**:
> Act as an ISTQB Test Analyst. I am testing a physical product: Senko DTS1607.
> 1. Test Design: Generate exactly 15 test cases for this device. Format them in a table with exactly these 6 columns: Objective | Input | Steps | Expected | Actual | Verdict.
> 2. ISTQB Alignment: Use formal test design techniques (e.g., Equivalence Partitioning for temperature/speed settings, Boundary Value Analysis for timers).
> 3. AI Audit Report: Immediately following the table, provide the mandatory 5-section [AI-02] AI Audit Report for this artifact. In section (1), use this exact prompt with the current timestamp. In section (4), provide 2-5 sentences of reasoning citing specific ISTQB Foundation Level sections. Leave sections (3) and (5) blank for my manual review.

### Section 2 — AI Output
See `week_1/report/report.md` → Requirement 3 section. **Final corrected** output includes:
- Device declaration table (Senko DTS1607, 65W, 88.6 m³/min, 3 speeds, rotary knob, no timer, no LEDs)
- 15 test cases (TC-01–TC-15): power on/off via rotary knob, 3 speed levels (EP), knob transition, oscillation lever on/off, cord temperature, min/max height BVA, auto-restart safety, oscillation at max height, base stability, blade guard inspection — all Actual and Verdict columns filled after physical execution
- 6 hallucinations found and documented (H1–H6); 4 were self-documented pre-verification, 2 (H5 control type, H6 LED indicators) found during physical device inspection
- Original artifact had 6 hallucinated non-executable test cases: 4 timer TCs (H3) + 1 LED accuracy TC (H6) + all steps referenced wrong control type (H5)

### Section 3 — Verdict
**INCOMPLETE → corrected to VALID after student fixes**

Initial AI output was INCOMPLETE: 6 of 15 test cases were non-executable due to hallucinated features (timer, LED indicators, button controls). After physical device verification, all 6 non-executable TCs were corrected or replaced, all Expected values were updated with confirmed specs (airflow 88.6 m³/min), ISTQB section references were corrected, and Actual/Verdict columns were filled from real device execution. Post-fix verdict: **VALID** — all 15 TCs are executable, grounded in the actual device's physical controls, and traceable to confirmed product specifications.

### Section 4 — Reasoning
Per **ISTQB FL v4.0 Section 4.3 (Equivalence Partitioning)**, the fan's three rotary-knob speed positions form three valid equivalence partitions; TC-03, TC-04, and TC-05 correctly apply this. H1 (fabricated airflow spec "42 m³/min") violated **ISTQB FL Section 1.3 (Testing and Debugging)** — expected results must trace to a verifiable specification; the corrected value (88.6 m³/min from product sheet) restores testability. H3 (hallucinated timer feature) and H6 (hallucinated LEDs) each generated entirely non-executable test cases, directly violating **ISTQB FL Section 4.1 (Test Techniques Overview)**: test design must be grounded in the actual test object and its specification — AI cannot substitute product documentation with plausible inference from similar devices. H5 (wrong control type — buttons instead of rotary knob) made every test step physically impossible to execute, a category of hallucination that only physical inspection can catch, underscoring the ISTQB principle in **Section 1.4 (Testing Principles)** that testing requires direct engagement with the test object, not assumptions about its interface.

### Section 5 — Student Fix
I physically inspected the Senko DTS1607 and cross-referenced the product listing at dienmaycholon.com. I found and corrected **6 hallucinations** in the AI output:

- **H1 (FIXED)**: Updated TC-05 airflow from "42 m³/min" to the confirmed spec of **88.6 m³/min**.
- **H2 (FIXED)**: Corrected ISTQB references from "Section 3.2" to EP → **Section 4.3**, BVA → **Section 4.4**.
- **H3 (FIXED)**: Removed all 4 timer test cases (TC-09–TC-12 original). The DTS1607 has no timer. Replaced with: TC-09 cord temperature, TC-10 min height BVA, TC-11 max height BVA, TC-12 auto-restart safety.
- **H4 (OPEN)**: IEC 60335-2-80 citation retained as a note — specific gap threshold to be confirmed before final submission.
- **H5 (FIXED)**: Corrected all test steps from "press POWER/SPEED/OSCILLATION button" to "rotate knob" and "engage oscillation lever" — the DTS1607 has no push buttons; speed and power use a rotary knob, oscillation uses a physical lever.
- **H6 (FIXED)**: Removed all LED indicator references (Speed 1/2/3 LED lit). The DTS1607 has no LEDs or display — control is entirely mechanical. Original TC-11 (LED accuracy) was replaced with max-height BVA.

All 15 test cases were executed on the real device. All returned PASS. The 3 omitted edge cases (blade jam/fuse test, thermal test, oscillation lever durability) remain for me to add as TC-16–TC-18 with supporting screenshots.

---

## Summary

| Category | Count | Percentage |
|---|---|---|
| VALID | | % |
| INVALID | | % |
| INCOMPLETE | | % |
| **Total entries** | | 100% |

**Conclusion**: AI should be used for [X] in this type of work because [reason]. AI should NOT be used for [Y] because [reason].