# Get Busi Technology Stack: Roles and Guardrails

**Inventory source:** TechAIStackInventory17Nov2026.pdf and GetBusiAIMasterBrief-v2.pdf.  
**Verified status:** This file records what the founder says is available; accounts, permissions, costs, versions, and infrastructure health have not been independently tested.

## Recommended small working stack

| Need | Use first | Keep out of scope for now |
|---|---|---|
| Product planning, decisions, deliverables | Current Codex “GET BUSI” project and this OneDrive folder | Duplicating the same plan across Jira, Asana, ClickUp, Trello, Nifty, and Smartsheet |
| Founder action tracking | One Microsoft Planner board, shared through Teams | A second task board |
| Working documents | GETBUSI folder; share approved files through SharePoint/OneDrive | Parallel copies in Google Drive and M365 without a rule for which is current |
| Customer discovery and waitlist | One landing page on getbusi.co.uk plus one simple form and one CRM list | Full marketing automation before demand is proven |
| Internal Microsoft workflows | Power Automate for Forms, SharePoint, Planner, and Teams tasks | Using it as the customer-facing product runtime |
| Early cross-tool prototypes | Zapier, using a small number of approved workflows and test data | Building the same automation in Zapier, Power Automate, Pipedream, and n8n |
| Product workflow engine | Private n8n only after security and licensing checks | Giving customers access to the n8n editor or letting AI configure customer workflows before license review |
| AI-assisted planning and artifacts | ChatGPT/Codex as the project workspace; Claude as an independent reviewer | Treating model output as legal, tax, or accounting approval |
| Current web research | Perplexity for discovery, followed by official primary-source verification | Citing an AI summary as the final authority |
| Long documents and data tables | Gemini or Copilot where the file's approved storage and privacy terms permit | Uploading live customer receipts or bank data to unapproved personal AI chats |
| Design and brand experiments | Canva; Adobe for finished assets where needed | Building separate brand systems before the proposition is validated |
| Customer relationship tracking | HubSpot or one M365 list; choose one | Storing customer ledger data in the CRM |
| API work | A technical partner/contractor can use Pipedream for isolated experiments if needed | Making the non-technical founder maintain code-only integrations |
| Robotic process automation | UiPath only if a proven workflow has no suitable API | Automating clicks in systems that provide a stable API |

## Product channel and financial data boundaries
- Use a responsive web app/PWA as the assumed first product channel. Current WhatsApp Business Platform terms restrict AI providers when AI is the primary functionality, with stated exceptions for some country codes. Because Get Busi is AI-led and targets UK users, confirm the current Meta terms and permitted use in writing before making WhatsApp API the core channel: https://www.whatsapp.com/legal/business-solution-terms/.
- Keep an evidence and workflow record in Get Busi (user-confirmed capture, source reference, external record ID, consent, sync status, corrections, audit events). Do not build a duplicate double-entry accounting ledger. The customer-authorised accounting package remains the financial source of truth where practical.
- Select one accounting connection from actual pilot-user tools and commercial terms. Xero is not preselected. Its developer pricing is tiered by connections and API usage, and its current terms prohibit using Xero API data to train AI/ML models: https://developer.xero.com/pricing.
- FreeAgent is a shortlist candidate if sole traders are the selected group; verify API scopes, sandbox, product terms, and the user's precise HMRC software needs: https://dev.freeagent.com/docs/introduction?version=2026-09-01.
- Do not make MTD API access, bank feeds, payments, or a spreadsheet ledger assumptions in the MVP. Use an existing HMRC-compatible product/partner for the near-term filing route and review the complete digital-link journey.

## AI division of work
- **ChatGPT/Codex:** maintain this project, turn decisions into specifications, prototype copy and forms, generate implementation plans, and review project files. The ChatGPT subscription is for the ChatGPT application; product API use has its own billing and must be budgeted separately. Check the current account plan and billing page.
- **Claude:** second-opinion review of requirements, prompts, failure cases, and clear user language. Ask it to identify unsupported claims and edge cases; return the review to this folder.
- **Perplexity Pro:** competitor and current-source discovery. Require links and verify claims against the original HMRC, ICO, Meta, or vendor source.
- **Microsoft Copilot:** use within M365 for internal meeting notes, document summaries, and action extraction, subject to company data permissions.
- **Gemini:** use for long-document review or spreadsheet analysis only where the selected workspace/data terms are appropriate.
- **OpenAI API:** possible product runtime, subject to evaluation, privacy review, pricing controls, and separate API billing. Choose model by testing real pilot tasks, not by assuming a model name in an older brief remains current.

## n8n licensing and hosting
The master brief proposes n8n as the backend workflow engine. n8n's current FAQ says building and running workflows for clients on the operator's own instance can be allowed under its Sustainable Use License if clients only receive outputs and cannot access or change the workflows. It says external users configuring workflows, a hosted n8n service, or white-labelling need a commercial license. Get Busi's autonomous/configurable features make the exact boundary important. Before public commercial use, send the proposed data flow and customer controls to license@n8n.io and get written guidance. See https://support.n8n.io/article/can-i-use-your-license-for-my-use-case.

The inventory lists a single 2 vCPU / 4 GB VPS. Treat this as a limited beta environment, not a proven high-availability production system. Before real customer records are processed, establish TLS, restricted admin access, two-factor authentication where available, encrypted backups with restore checks, monitoring, patching, a security contact, and a way to respond to incidents. Run the n8n security audit: https://docs.n8n.io/deploy/host-n8n/configure-n8n/security/run-security-audits/.

Use getbusi.app for only the endpoints that need to receive webhooks. Never expose the workflow editor, database, or admin interfaces publicly. Store credentials in the platform's secret controls, not in project files, screenshots, prompts, or shared spreadsheets.

## Financial and tax integrations
- Do not treat OpenAI API access as included with a ChatGPT subscription. OpenAI states that ChatGPT and API billing are separate: https://help.openai.com/en/articles/9039756-managing-billing-for-chatgpt-and-the-api-platform.
- The MTD plan is not “add an API bridge and launch.” HMRC's MTD ITSA integration guide requires sandbox registration and testing, compliant fraud-prevention headers, production application steps, and an approvals checklist: https://developer.service.hmrc.gov.uk/guides/income-tax-mtd-end-to-end-service-guide/documentation/how-to-integrate.html.
- Prefer integrating with existing HMRC-recognised software or a qualified provider first. Do not claim MTD compatibility until the actual product has passed the applicable process.
- Delay Open Banking and payment initiation. If added later, select a UK-authorised provider and review permissions, customer consent, security, support, and commercial terms.

## Don't add another tool unless
1. A repeated customer or founder problem is being blocked.
2. The current tool cannot handle it safely.
3. A named owner will maintain the connection.
4. Cost, data access, and exit/export paths are understood.

## Configuration and tenant boundary
The ChatGPT, Claude, and Perplexity configuration snapshots report session-level tool availability; that does not prove account authentication, permissions, licences, or approval to process Get Busi customer data. The Maison Residential technology risk audit identifies potentially sensitive Microsoft 365, Graph, CRM, and automation paths. Keep Get Busi work separate from Maison Residential employee and customer records unless the data owner approves a reviewed and restricted flow. Confirm the correct tenant, permissions, processor terms, and access controls before using Forms, SharePoint, Power Automate, CRM, or AI connectors for a Get Busi pilot.
