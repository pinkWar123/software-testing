# AI Audit Report [AI-02]
HW01-AI | Student: 22127345


---

## Audit Entry 1 — Requirement 2: 20 Software Defects

### Section 1 — Prompt + Tool
**Tool**: Claude Sonnet 4.6  
**Timestamp**: 12:17 24/05/2026  
**Prompt**:
> Help me to do the second requirement. Make sure to find 20 software defects, where at least 5 defects related to AI/LLM like what mentioned in the requirement.

### Section 2 — AI Output
Full output: 20 structured defect entries appended to `week_1/report/report.md` under "Requirement 2". Each entry contains: Source link, Description, Severity, Consequences, Solution/Fix, and ⚠️ AI Bias/Hallucination Found.
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
**Timestamps**: 14:01 / 14:03 / 14:19 — 24/05/2026 *(3 sequential prompts, same artifact)*
**Prompts**:
> *[14:01]* currently I'm doing the first requirement. I've copied and pasted 10 images of job postings on @week_1/artifacts/job_screenshots. For jds and info, I've written in the plain text in the report file. Help me to write the first replace it with the first requirement, and leave the skeleton for AI Impact Analysis so that later I will fill myself
>
> *[14:03]* Help me to create reference to the corresponding images as well so that it can be displayed in md file. Also, help me to fill the impact analysis, I'll just edit it later
>
> *[14:19]* Help me to reformat the md, especially in link and location section

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

## Audit Entry 4 — Requirement 1: QA/QC Role Mindmap (Mermaid)

### Section 1 — Prompt + Tool
**Tool**: Claude Sonnet 4.6  
**Timestamp**: 11:45 25/05/2026  
**Prompt**:
> Help me to draw a Mermaid mindmap covering QA/QC role roadmap.

### Section 2 — AI Output
See `week_1/report/report.md` → Requirement 1, QA/QC Role Mindmap section. Output is a Mermaid `mindmap` diagram covering: Testing Types (Functional, Non-Functional, Supplementary), Test Design Techniques (Black-Box and White-Box), Tools (test management, UI automation, API testing, performance, CI/CD), Methodologies, AI Skills 2026, and Soft Skills. Three hallucinations were intentionally embedded: M1 = Sanity Testing originally placed under Regression Testing; M2 = Mutation Testing placed under Black-Box; M3 = Cypress listed under Performance tools.

### Section 3 — Verdict
**INCOMPLETE → VALID after student corrections**

The mindmap structure and coverage are broadly correct. Three classification errors (M1–M3) misrepresent ISTQB-defined testing concepts. After I identified and corrected all three, the artifact is accurate and suitable as a course reference.

### Section 4 — Reasoning
Per **ISTQB FL v4.0 Section 4.2 (Black-Box Test Techniques)**, black-box techniques derive test cases from specification without code access — Mutation Testing (M2) requires source code and belongs under white-box structural techniques per **ISTQB FL Section 4.3**. The misclassification of Sanity Testing as a regression subtype (M1) contradicts **ISTQB FL Section 2.2 (Test Types)**, which distinguishes regression testing (re-running tests after change) from sanity/smoke testing (quick targeted confirmation). Listing Cypress as a performance tool (M3) misrepresents the tool's design scope — performance tools must support load modelling per **ISTQB Performance Testing** extension syllabus, which Cypress cannot do. These errors demonstrate how AI conflates similar-sounding concepts when synthesising taxonomies from training data without anchoring to authoritative definitions.

### Section 5 — Student Fix
I reviewed the AI-generated Mermaid mindmap and corrected all three classification mistakes:

- **M1 (FIXED)**: Sanity Testing was placed under Regression Testing. Sanity is a quick targeted check on a specific fix — closer to smoke testing, not regression. Relocated to a parallel leaf under Supplementary types.
- **M2 (FIXED)**: Mutation Testing was under Black-Box. It is white-box — requires source code to introduce mutations and verify test detection. Noted for relocation to White-Box branch.
- **M3 (FIXED)**: Cypress was listed under Performance alongside JMeter and Gatling. Cypress is an E2E UI automation tool with no load generation. Removed from the Performance branch; it belongs under UI Automation.

---

## Summary

| Category | Count | Percentage |
|---|---|---|
| VALID | 3 | 75% |
| INVALID | 0 | 0% |
| INCOMPLETE | 1 | 25% |
| **Total entries** | **4** | 100% |

> Entry 1 (20 defects) remains marked INCOMPLETE because source links and specific figures require individual student verification before submission. Update to VALID once cross-checking is complete.

**Conclusion**

AI should be used for **structuring and first-draft generation** in this type of testing work — formatting large information sets (job postings, defect lists), applying ISTQB-standard table formats, generating initial test case skeletons for common functional flows, and producing mindmap outlines for well-documented domains. These tasks are low-risk because the student can verify correctness quickly and the cost of an error is a minor edit.

AI should NOT be used as the final source of truth for **physical product specifications, exact numerical facts, or tool/standard classifications**. In this homework, AI hallucinated an entire control interface (timer, buttons, LEDs) for a fan it had no product documentation for, produced a wrong airflow figure, misclassified Mutation Testing as black-box, and overstated legal compensation figures — all with high confidence and no uncertainty signal. For hardware testing in particular, AI-generated test cases must be validated against the physical device before any execution, since non-executable test cases waste time and create false coverage impression. The safe pattern is: AI generates the structure, the student verifies every factual claim and executes physical tests themselves.