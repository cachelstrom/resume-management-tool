# Resume Content Workspace

This workspace contains the single source of truth for professional experience context in `experience_context/professional_experience_master.md`, a controlled skills inventory in `experience_context/tools-technologies_master-list.md`, an unverified historical-resume review draft in `resumes/historical/historical_resume_review.md`, and a baseline resume in `resumes/baseline_resumes/Caleb_Chelstrom_Platform_Eng_2026.md`. Use the baseline as a starting point for structure and previously used phrasing; use the experience master as the factual source for role details. The historical review is only a set of unverified leads, not an alternate source of truth.

## How to use the AI guidance files

- Follow this `copilot-instructions.md` file as the workspace-wide rules for resume and experience-content work.
- Use `.github/agents/resume-writer.agent.md` for drafting, tailoring, or reviewing resume content. It defines the source-review workflow, accuracy guardrails, and evidence-based response format.
- Use `.github/prompts/tailor-resume.prompt.md` to start tailoring for a specific opportunity. Fill in the target role, full job description, and requested content; it directs the Resume Writer agent to apply the workflow and return a draft, evidence map, and focused questions.
- Treat the agent and prompt as task-specific workflows that operate under these workspace-wide instructions. Neither replaces the experience master as the source for role facts.

## Accuracy and integrity

- Never invent or assume employers, dates, titles, responsibilities, tools, technologies, scope, metrics, outcomes, or credentials.
- If a detail is missing, unclear, or marked as pending, leave it out of resume claims and ask the user to confirm it. Do not turn estimates into precise numbers.
- Do not merge responsibilities from different roles or imply ownership where the notes describe collaboration or contribution.
- Tailor emphasis to a job description without adding qualifications or overstating the user's experience.
- When creating or revising a resume's `## Core Skills` section, use only `Resume-Approved Skills — Use for Core Skills` in `experience_context/tools-technologies_master-list.md`, selecting a concise, job-relevant subset. Never use `Reference-Only Skills — Do NOT Use for Core Skills` in that section unless the user explicitly approves and moves the skill to the approved section. A skill's allowlist status does not replace experience evidence.
- Make claims traceable to the supporting source note. When useful, provide a separate evidence map with file names and any facts that need confirmation.

## Voice and drafting

- Use clear, specific, natural language. Prefer the user's concrete actions and outcomes over generic corporate language, inflated claims, or keyword stuffing.
- Preserve the user's meaning and level of ownership when editing. Do not add artificial quirks or try to disguise AI assistance; authenticity comes from accurate, user-reviewed content.
- Keep the resume readable and concise. Use job-description terminology only when it accurately describes the documented experience.

## Handling source notes

- Read the baseline resume, `experience_context/professional_experience_master.md`, `experience_context/tools-technologies_master-list.md`, and the relevant sections before tailoring resume content. `historical_resume_review.md` is pending the user's accuracy review; treat its claims as unverified and do not use them as resume facts unless the user confirms them. Select evidence based on the target role rather than assuming one section tells the whole story.
- Treat claims present only in the baseline resume as unverified until supported by experience notes or confirmed by the user. Where sources conflict, flag the conflict and ask the user; do not silently choose a version.
- Treat placeholders such as `MM/YYYY-MM/YYYY` and unconfirmed notes as incomplete; never include them as factual resume content.
- When the notes do not support a requested claim, say so plainly and ask a focused follow-up question.
- Keep source notes unchanged unless the user explicitly asks to edit them.
