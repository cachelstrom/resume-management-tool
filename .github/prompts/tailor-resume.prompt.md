---
name: Tailor Resume
description: "Draft or tailor resume content to a specific job description using documented experience and evidence from experience_context."
agent: "Resume Writer"
argument-hint: "Paste the job description and specify the target role and resume section or format."
---

Tailor my resume content to the role described below. Follow the project instructions and the Resume Writer agent's accuracy and evidence requirements.

## Target role

${input:targetRole:Enter the job title or target role}

## Job description

${input:jobDescription:Paste the full job description}

## What to draft

${input:requestedContent:For example, a professional summary and 4-6 experience bullets; mention any length or format constraints}

Use `resumes/baseline_resumes/Caleb_Chelstrom_Platform_Eng_2026.md` as a starting point, then read `experience_context/professional_experience_master.md`, `experience_context/tools-technologies_master-list.md`, and the relevant role sections to verify claims and find the strongest evidence for this specific role. Do not combine distinct jobs or invent missing details. Treat claims present only in the baseline as unverified, and flag any conflicts for confirmation. The `experience_context/historical_resume_review.md` file is pending my accuracy review; do not use claims from it as facts unless I confirm them.

If you include a `## Core Skills` section, use only a concise, job-relevant subset of **Resume-Approved Skills — Use for Core Skills** in the master list. Ignore **Reference-Only Skills — Do NOT Use for Core Skills** for that section unless I explicitly approve and move a skill to the approved section. Verify any experience bullet against the relevant role notes; the master list alone is not evidence.

Return:

1. A clean, resume-ready draft.
2. A separate evidence map linking each claim to its source file and note.
3. Any focused questions about unverified or missing facts that could materially improve the draft.

Leave unsupported claims out of the draft. Do not treat placeholders, estimates, or pending outcomes as confirmed facts. If a useful draft cannot be made from the available notes, explain what additional information is needed.
