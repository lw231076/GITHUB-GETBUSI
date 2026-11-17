# Collaboration and Tool Operating Model

**Goal:** use the subscriptions already available while keeping one source of truth and reducing repeated manual work.

## One project home
- Keep product decisions, drafts, research notes, specs, and the action list in the GETBUSI folder.
- Use the Codex “GET BUSI” project for work that changes these files. The current chat is in the “Get Busi Build” sidebar section.
- Use one Planner board as the action board if the founder wants a shared team task view. Each task should link back to a file in this folder.
- Use Teams for calls and discussion. Save decisions in the decision log, not only in meeting chat.
- Use SharePoint/OneDrive permissions and version history for approved business files. Do not keep a second “master” copy in Google Drive.

## Use an AI handoff card
For each task given to an AI, provide:
1. **Outcome:** what must exist when the task is done.
2. **Source files:** exact project files or official links.
3. **Boundaries:** what must not be sent, published, purchased, or changed.
4. **Deliverable:** file, draft, workflow diagram, or checklist.
5. **Acceptance check:** how the founder can tell it is complete.
6. **Review needed:** who checks financial, tax, legal, data, or customer-facing claims.

Ask each AI to return its output as a file or concise decision note in this folder, not an untraceable chat answer. Record the chosen answer once in Source-Review-and-Decisions.md.

## Best use of the available tools

| Tool | Use it for | Don't use it for |
|---|---|---|
| ChatGPT/Codex | Product requirements, implementation drafts, project files, structured launch artifacts, and iterative work against this folder | Treating generated tax or legal content as professional approval |
| Claude | Independent critique of flows, prompts, edge cases, accessibility, and user-friendly explanations; consult CLAUDE.md and memory/ | Maintaining a second competing master plan |
| Perplexity Pro | Fast competitor and vendor research with direct links | Final legal, HMRC, or security authority without opening official sources |
| Copilot + Microsoft 365 | Internal meeting notes, action extraction, Forms/Lists, Teams, Planner, and SharePoint tasks | The public product's AI engine unless a deliberate product/API decision is made |
| Gemini | Long-document review and spreadsheet exploration where the data terms fit | Live financial data in an unapproved account |
| Power Automate | Internal workflows that begin and end in Microsoft 365 | Duplicating every Zapier workflow |
| Zapier | Fast low-volume prototype connections across the existing 20 connected apps | Permanent product backend before cost, security, and ownership are understood |
| n8n | Private, founder-managed product workflows after licensing, security, backup, and maintenance checks | Public editor access or user-configurable automations before n8n confirms licensing |
| HubSpot | Waitlist, discovery, and sales follow-up if already active | Transaction ledger, receipt storage, or tax records |
| Canva/Adobe | Brand experiments and launch materials after message validation | Two full design systems before one audience is validated |
| Pipedream | Technical API experiments with a technical helper | A founder-maintained code dependency |
| UiPath | A proven internal process with no reliable API | The first version of customer-facing product automation |

## Automation sequence
1. Automate founder admin: meeting notes to actions, new waitlist entry to CRM, and approved beta onboarding checklist.
2. Automate one customer workflow only after a founder has performed it manually several times.
3. Measure exceptions and correction rate. Keep a human approval step where an error could affect money, taxes, customer rights, or a public post.
4. Give every workflow an owner, test account, failure alert, retry/recovery path, and short plain-English runbook.

## Weekly working rhythm
- **Monday, 20 minutes:** choose the three most important outcomes and set owners.
- **After each discovery call:** capture the user's words, what they do today, time/cost of the problem, and evidence of willingness to try or pay.
- **Friday, 30 minutes:** review pilot metrics, failures, spend, decisions, and the next week's three outcomes.
- At each review, update the memory files and source links. Archive only completed decisions; do not keep a large untriaged chat history as the only memory.

## Suggested project workstreams
- Product discovery and customer language.
- MVP workflow and data model.
- Privacy, compliance, and operational readiness.
- Go-to-market and pilot measurement.

Use separate Codex or Claude conversations only when they produce independent work. Bring the result back into this project folder and keep this chat as the project coordination thread.
