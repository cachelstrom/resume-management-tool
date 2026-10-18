# Resume Management Tool

An evolving, personal workspace for organizing verified career information and using AI assistance to create accurate, job-specific resume content. The repository currently consists of Markdown source material, existing resume files, and GitHub Copilot instructions, a custom agent, and a prompt. It is not currently a standalone application: there is no resume-generation service, job tracker, command-line tool, build, or automated test suite.

The setup is intended to be adjusted as job-search needs change. The documented workflow describes the current state, not a fixed product design.

## Current workflow

1. Maintain experience facts and their verification status in the professional experience master.
2. Provide a target role and its job description to Copilot Chat, either directly to the **Resume Writer** agent or through the **Tailor Resume** prompt.
3. The agent compares the job requirements with the relevant documented experience, selects only supported claims, and drafts the requested resume content.
4. Review the draft and its evidence map. Confirm unresolved details, correct mistakes, and decide whether to keep or adapt the content for a particular application.

The current AI workflow produces drafts and evidence in chat. It does not automatically create or update a tailored resume file, submit applications, or track job-search activity.

## Repository contents

```text
.
├── .github/
│   ├── agents/
│   │   └── resume-writer.agent.md
│   ├── prompts/
│   │   └── tailor-resume.prompt.md
│   └── copilot-instructions.md
├── experience_context/
│   ├── professional_experience_master.md
│   └── tools-technologies_master-list.md
├── resumes/
│   ├── baseline_resumes/
│   │   └── Caleb_Chelstrom_Platform_Eng_2026.md
│   └── historical/
│       ├── historical_resume_review.md
│       └── historical resume files (PDF and DOCX)
└── README.md
```

### Experience context

- [`experience_context/professional_experience_master.md`](experience_context/professional_experience_master.md) is the **single source of truth for experience context**. It contains role-based notes, projects, education, certifications, military service, and resume-wide positioning. Keep separate jobs and periods distinct. Placeholders, conflicting details, and unconfirmed claims are not ready to use as facts.
- [`experience_context/tools-technologies_master-list.md`](experience_context/tools-technologies_master-list.md) is the controlled skills inventory. Its **Resume-Approved Skills — Use for Core Skills** section is the only permitted source for a resume's Core Skills section. Choose a relevant subset, and still verify that experience claims are supported by the master.
- [`resumes/historical/historical_resume_review.md`](resumes/historical/historical_resume_review.md) is a temporary review document containing unverified claims and variants found in older resumes. It is an index of leads to investigate, **not** a second source of truth. Do not use a claim from it as a resume fact until it is confirmed and incorporated into the experience master.

### Resume examples

- [`resumes/baseline_resumes/Caleb_Chelstrom_Platform_Eng_2026.md`](resumes/baseline_resumes/Caleb_Chelstrom_Platform_Eng_2026.md) provides previously used resume structure and phrasing. Claims found only in the baseline are not automatically verified.
- `resumes/historical/` holds earlier PDF and DOCX resume versions. These may help locate original wording or explain discrepancies, but they do not override the experience master.

### Copilot guidance

- [`.github/copilot-instructions.md`](.github/copilot-instructions.md) supplies workspace-wide accuracy, voice, and source-handling rules.
- [`.github/agents/resume-writer.agent.md`](.github/agents/resume-writer.agent.md) defines the task-specific Resume Writer agent workflow, guardrails, and response format.
- [`.github/prompts/tailor-resume.prompt.md`](.github/prompts/tailor-resume.prompt.md) is a reusable, parameterized starting point for tailoring content to a specific opportunity.

The instructions apply broadly to Copilot work in this workspace; use the agent or prompt when doing resume-specific drafting. Keep their paths and behavior aligned with the real repository structure as it evolves.

## Tailor content in Copilot Chat

### Use the prompt

1. Open this repository as the VS Code workspace and start Copilot Chat.
2. Choose **Tailor Resume** from the prompt picker (or invoke `/tailor-resume` if available in the current Copilot Chat experience).
3. Supply the target role, full job description, and requested content, such as a summary and a specified number of experience bullets.
4. Review the requested draft, evidence map, and questions. Ask for a revision if the target, length, emphasis, or format needs adjustment.

### Use the agent directly

Select **Resume Writer** from the agent picker and provide a target role, job description, desired resume sections, and any format or length constraints. If no job description is available, say so; the agent can only tailor against the information provided.

### Expected output

The agent is instructed to return:

1. A clean, resume-ready draft.
2. A separate evidence map linking claims to their supporting experience notes.
3. Focused questions for missing or conflicting facts that could materially affect accuracy or tailoring.

Unsupported claims should be omitted rather than filled with guesses. Review the output before using it; the repository's guidance is intended to reduce errors, not replace the user's verification.

## Source-of-truth and accuracy rules

Use the following order when sources differ:

1. **Confirmed experience master:** the authoritative source for work-history facts.
2. **Skills inventory:** controls eligibility for the Core Skills section; it does not prove that a skill was used in a particular role.
3. **Baseline resume:** a source for structure and previously used phrasing, not independent verification.
4. **Historical review and older resumes:** unverified references that may help resolve or investigate a claim.

Do not invent or infer dates, titles, employers, tools, scope, ownership, outcomes, metrics, or credentials. Do not combine separate roles in a way that implies the work occurred in one job or period. Treat placeholders, estimates, pending outcomes, and unresolved conflicts as incomplete. Ask for confirmation rather than silently choosing a version.

## Maintaining and adapting the workspace

### Update experience facts

- Add or revise role details in `experience_context/professional_experience_master.md` after confirming them. Keep the relevant role, timeframe, level of ownership, and outcome clear.
- Preserve uncertainty explicitly while a fact is being checked. Once resolved, update the master and remove or revise the corresponding open question in the historical review.
- When older resumes disagree, retain the discrepancy as an open question until resolved; do not promote one variant to fact merely because it appears in a resume.
- Keep `historical_resume_review.md` clearly marked as unverified. It can be reorganized, shortened, or eventually retired as claims are reviewed and migrated.

### Manage skills

- Add a skill to the approved Core Skills list only when it is appropriate for resume use and supported by the experience notes.
- Keep reference-only terms separate from approved Core Skills. A term in the inventory is not by itself evidence of proficiency or role-specific use.
- Tailor each resume's skills to the target job instead of copying the entire inventory.

### Adjust AI behavior

- Edit `.github/copilot-instructions.md` for rules that should apply workspace-wide.
- Edit the Resume Writer agent for changes to the resume-specific workflow, boundaries, tools, or response format. Keep its `description` useful for discovery and its frontmatter valid.
- Edit the Tailor Resume prompt when its inputs or output request should change. Keep it focused on one tailoring task and aligned with the agent and workspace instructions.
- Update this README whenever files, supported workflows, or actual capabilities change. Describe implemented behavior as current and label proposals as future possibilities.

### Add job-search capabilities over time

This repository does not currently provide application tracking, job-description storage, automatic document generation, or application submission. If those needs are added, document the new workflow and data sources, decide where generated or job-specific files should live, and update the Copilot guidance to match. Keep sensitive personal information and employer-provided job materials in mind when deciding what belongs in version control.

## Validation and limitations

This is currently a documentation and source-content repository. There are no build, test, or lint commands defined. Validate content changes by checking file paths, Markdown structure, and consistency between the README, source notes, and Copilot guidance. Any resume draft still requires human fact-checking and review.
