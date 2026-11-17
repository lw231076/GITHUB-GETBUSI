# Get Busi: Staged Plan to Go Live

**Prepared:** 17 November 2026  
**Planning constraint:** the master brief states a maximum initial budget of £900.  
**Approach:** get one useful, safe customer workflow into an invited pilot quickly; automate and expand only after evidence.

**Current operating guide:** use [Execution Playbook and Paste-Ready Scripts](Execution-Playbook-and-Paste-Ready-Scripts.md) for the detailed steps, current gates, tool prompts, and go-live checklist. This launch outline is retained as supporting context; where details differ, follow the newer playbook and the decision log.

## Strategic recommendation
The vision has a clear appeal: make business admin feel like a conversation, and reduce the effort of turning everyday activity into usable records and decisions. Its current scope is too large for one early release. The two brands, broad compliance coverage, tax forecasts, regulatory renewals, text and voice escalation, supply sourcing, open banking, POS, and autonomous business setup should not all be in the first build.

Build one shared foundation and validate a single first audience. A promising candidate is sole-trader home services (for example, trades or cleaning), but choose it only after interviews. The first paid problem should be simple to explain and frequent: “Tell us what you earned or spent, send the receipt, confirm the record, and get a clear weekly view.”

Use a concierge MVP: the customer sees a simple chat-led product, while the founder reviews uncertain entries and produces or checks the report. The aim is to learn whether customers use it and value it, not to pretend a broad autonomous product already exists.

## The first release

### Include
- One segment and one plain-English onboarding.
- A short text conversation and receipt/image capture.
- Draft income/expense entries with a user confirmation and easy correction.
- A weekly summary of entered transactions, missing details, and a simple cash view.
- A neutral, user-chosen reminder for missing information.
- A clear “estimate” label wherever a reserve or forecast is shown.
- A way to contact support, correct or delete information, and raise a data-protection complaint.

### Exclude from the first release
- HMRC filing, MTD compatibility claims, or tax advice.
- Automated determination of a precise tax bill.
- AI voice calls, customer bank feeds, open banking, payment initiation, or automated purchases.
- Supplier price monitoring, POS/inventory, training/accreditation coverage across many sectors.
- Fully autonomous business plans, website publishing, social posting, or broad co-founder functionality.
- Separate back ends for both brands.

## Go-live stages and gates

The authoritative roadmap is [Get Busi: Recommended Solution and Revenue-Funded Plan](Recommended-Solution-and-Revenue-Funded-Plan.md). It defines the final product, integration principles, customer-revenue gates, and six stages. The dates are working targets, not guarantees; customer evidence, privacy readiness, and integration terms can affect them. The WhatsApp Business Platform is a policy gate for this AI-led UK product, not an assumed first channel.

## Work to complete this week

### 1. ChatGPT/Codex: choose the pilot and freeze the smallest useful product
**Instruction to give:**  
“Read the Get Busi project files. Create a one-page MVP brief, an interview script, and draft landing-page copy. Compare two reachable customer groups, such as tradespeople and cleaners. Do not assume a winner. Give me five interview questions about what they do now, time spent, mistakes, and willingness to try or pay. Define one conversation that captures an income item and a receipt, asks the user to confirm the details, and produces a weekly summary. Mark all unverified claims. Do not publish the page or contact anyone.”

**Completion check:** five interviews are booked or completed; a first segment and one core workflow are logged with evidence; the MVP brief has clear in-scope and out-of-scope items.

### 2. Codex or a technical operator: audit and prepare the VPS safely
**Instruction to give:**  
“Inspect the Hostkey VPS, DNS, Docker, current n8n/PostgreSQL/Caddy status, backups, software versions, and public ports. Return a plain-English findings report and a staging deployment plan for the smallest required stack. Prepare configuration files with placeholders only, TLS, restricted admin access, webhook-only public routes, encrypted backup and restore steps, monitoring, patching, and a rollback plan. Do not put credentials in project files. Do not change DNS, expose the editor/database, or process real customer data. Ask me to review before applying changes. Check n8n's license FAQ and flag anything that needs written approval.”

**Completion check:** the actual server state is recorded; staging configuration is reviewable; backups can be restored; only the intended webhook can be reached publicly; license questions are recorded. If the VPS is not correctly secured, keep using a manual concierge pilot.

### 3. Claude plus ChatGPT/Codex: build one synthetic-data chat workflow
**Instruction to give:**  
"Use the MVP brief to design one controlled web-intake test workflow: receive a text description or receipt, extract candidate fields, ask the user to confirm or correct them, and produce a simple weekly summary. Use synthetic examples first. Include duplicate prevention, low-confidence handling, retries, failures, correction/deletion, and a human-support route. Keep any structured record as a temporary workflow record, not a second accounting ledger. Do not calculate a precise tax bill, submit anything to HMRC, make payments or purchases, or start automated voice calls. Treat WhatsApp Business Platform access as a policy gate; only include it after a written review confirms the exact UK AI-led use. Prepare a privacy notice, data flow, retention plan, access controls, and data-protection complaint route for review before real customer data is used."

**Completion check:** the end-to-end test passes with synthetic data; uncertain fields stop for confirmation; errors do not silently create records; a founder can review and correct the output. Only then invite a small number of pilot users, after the privacy, security, access, and complaint-process gates are met.

Use Microsoft Copilot/Power Automate for the internal pilot checklist and reminders after the flow is approved. Keep that work administrative; do not put transaction records in a marketing CRM or a broad AI chat.

## Current gaps to solve before real customer data

### 1. MTD is not a simple formatting bridge
HMRC's current schedule says MTD ITSA started on 6 April 2026 for eligible users whose qualifying income exceeded £50,000 based on the 2024-25 tax return. The next thresholds are over £30,000 from 6 April 2027 and over £20,000 from 6 April 2028, based on the respective previous tax years. Eligibility and exemptions are user-specific. Source: [HMRC: using MTD ITSA for the first time](https://www.gov.uk/guidance/use-making-tax-digital-for-income-tax/using-making-tax-digital-for-income-tax-for-the-first-time).

HMRC production access requires sandbox testing, fraud-prevention headers and a Production Approvals Checklist. It is not equivalent to adding an API key. Source: [HMRC developer integration guide](https://developer.service.hmrc.gov.uk/guides/income-tax-mtd-end-to-end-service-guide/documentation/how-to-integrate.html).

**Recommendation:** at first, help users organise records and export them. If users need MTD, partner with recognised compatible software or an experienced provider. Do not say “HMRC compliant” or “MTD ready” until the exact flow has approval and has been checked against live requirements.

### 2. Privacy and complaints operations
Before live receipts or financial records are processed, map what data is collected, why, who can see it, each supplier that processes it, where it is stored, how long it is retained, how it is deleted, and what happens after a security incident. Use current ICO guidance and obtain advice for the actual data flows. A DPIA should be completed if required by the processing risk.

The Data Use and Access Act 2025 data-protection provisions are now in force. ICO guidance says every organisation needs a clear data-protection complaints process, must acknowledge complaints within 30 days, investigate appropriately, and communicate an outcome. Add a dedicated contact route, owner, and tracking workflow before collecting personal information. Sources: [ICO AI and data protection](https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/artificial-intelligence/) and [ICO complaints guidance](https://ico.org.uk/for-organisations/how-to-deal-with-data-protection-complaints/).

### 3. n8n licence and operating model
n8n's FAQ says fixed workflows built and operated for clients can be allowed if clients only receive outputs and cannot change or access the workflows. Its FAQ says customer-configured workflows, hosted n8n services, or white-labelling need a commercial license. Ask n8n in writing about Get Busi's planned conversational and autonomous workflows before public commercial use. Source: [n8n license use-case FAQ](https://support.n8n.io/article/can-i-use-your-license-for-my-use-case).

The VPS can support an early technical pilot only if it is secured and maintained. Confirm the current software version, restrict the admin panel, expose only required webhooks, configure backups and test restore, and run the [n8n security audit](https://docs.n8n.io/deploy/host-n8n/configure-n8n/security/run-security-audits/). Keep a human technical owner for patching and recovery.

### 4. WhatsApp and reminder setup
Meta's Business Platform supports messaging and calling, but it has onboarding, templates, permissions and pricing requirements. Its current business terms also restrict some AI-primary uses and list exceptions that do not name UK numbers. Verify the exact use in writing before making it a dependency: [Meta WhatsApp Business Platform](https://developers.facebook.com/documentation/business-messaging/whatsapp/overview/) and [WhatsApp Business Solution Terms](https://www.whatsapp.com/legal/business-solution-terms/).

Begin with inbound user messages and reminders users deliberately enable. Keep reminders factual and non-promotional. If a message promotes a product or upgrade, separate it from service reminders and meet marketing rules. Source: [ICO service messages and direct marketing](https://ico.org.uk/for-organisations/direct-marketing-and-privacy-and-electronic-communications/direct-marketing-guidance/identify-direct-marketing/).

### 5. AI API cost and controls
ChatGPT Go/Plus access does not provide an unlimited OpenAI API for the public product. OpenAI bills ChatGPT and API separately. Budget product API calls separately, set spend alerts and per-user limits, and compare models on receipt accuracy, latency, and price before choosing. Source: [OpenAI billing for ChatGPT and API](https://help.openai.com/en/articles/9039756-managing-billing-for-chatgpt-and-the-api-platform).

Use an API key on a server-side secret store, not in a browser or a prompt. Do not pass full customer histories to every model call. Send only the information required for the task, explain AI use to users, and provide correction and human support.

### 6. Financial boundaries and assurance
- Define what the product records versus what it calculates.
- Present forecasts as estimates with visible assumptions, dates, and caveats; allow the user or accountant to correct them.
- Confirm accounting and tax categories with a qualified accountant before use in tax workflows.
- Separate sole trader, limited company, VAT, payroll, and property situations instead of giving one universal answer.
- Obtain appropriate terms, privacy notices, processor agreements, retention rules, support commitments, and insurance advice before public launch.
- Add secure backups, change logs, access controls, monitoring, recovery, and an incident runbook.
- Consider accessibility, plain language, consent, opt-out, correction, export, and deletion from the first design.

## Budget control
The source brief says £900 maximum. First list already-paid annual/monthly subscriptions and direct incremental costs; do not buy another AI or PM platform. Prioritise customer interviews, the smallest landing and workflow test, API/message usage caps, and essential privacy/security review. Keep a written cost per active pilot user. If the £900 limit cannot cover a required safety step, reduce scope or extend the test instead of quietly exceeding it.

## First release acceptance checklist
- [ ] One chosen segment, supported by customer conversations.
- [ ] One clear job-to-be-done and one landing-page offer.
- [ ] Onboarding explains data use and support.
- [ ] Data-protection complaint route has a named owner.
- [ ] Each record is user-confirmed or clearly marked uncertain.
- [ ] User can correct, export, or request deletion.
- [ ] No autonomous tax filing, payment, purchase, or public posting.
- [ ] Synthetic-data workflow succeeds before real data is collected.
- [ ] Access control, backup, restore, security and incident procedures are in place for the pilot.
- [ ] Cost, error rate, founder support minutes, repeat use, and willingness to pay are measured.
- [ ] Every public product claim is checked and approved.
