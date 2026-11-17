# Get Busi: Recommended Solution and Revenue-Funded Plan

**Reviewed:** 17 November 2026  
**Status:** Recommended plan for founder review; no vendor or build commitment made  
**Project principle:** prove one paid outcome, then use customer revenue to fund the next useful capability.

## Executive decision

Build Get Busi as a simple conversational business-operations assistant that connects to established products. Own the customer experience, workflow, evidence trail, plain-English explanations, and support. Use an appropriate accounting product for the formal ledger and tax filing; use authorised providers for banking and payments; use existing company and communications services where their terms fit.

Use one shared platform for the two experiences:

- **Get Busi** helps an existing micro-business keep records and routine work moving.
- **Get Busi Start Up** helps a founder test an idea, plan a launch, and move into business operations.

Do not build two products or attempt an all-purpose autonomous co-founder in the first release. Start with one customer segment and one recurring job.

### First segment and workflow to test

**Recommended segment hypothesis:** sole traders who provide home services, such as tradespeople or cleaners. Interview people in no more than two candidate groups before deciding; this group is not yet validated.

**Recommended first workflow:** a customer sends a receipt or describes income; Get Busi drafts the date, supplier or customer, amount, and category; the customer confirms or corrects it; Get Busi returns a clear weekly activity and cash view.

That is the smallest useful part of the original vision. Invoicing, tax reminders, business renewals, supplier sourcing, calls, Open Banking, POS, and Start Up remain in the plan, but follow evidence and release gates.

## Review of the four blueprints

| Blueprint | Best contribution | What to retain | What to change before using it |
|---|---|---|---|
| **GetBusi_Solution_Blueprint.pdf** | The clearest full product concept, modular architecture, integration map, customer stories, and stage gates. | Build the customer experience; rent specialist engines; keep a human-help route; expand from Get Busi to Start Up only after retention. | Do not create a duplicate accounting ledger. Keep a product evidence and workflow record, while the chosen accounting package remains the ledger. Rework WhatsApp-first, direct MTD, pricing, and cost assumptions against current terms. |
| **GetBusi-AI-Build-Plan.pdf** | The simplest explanation of the receipt-to-weekly-summary loop and the most approachable stage sequence. | The narrow first workflow, user confirmation, invoice drafts later, and accounting integration after evidence. | Do not make WhatsApp or Google Sheets the assumed production channel or financial record store. Confirm privacy, security, licensing, and vendor terms first. |
| **Get-Busi-Solution-and-6-Stage-Roadmap.pdf** | The strongest vendor-neutral integration stance, human-approval rules, and current HMRC warning. | Keep one shared platform, one accounting connector at first, staged approvals, explicit cost controls, and no compliance promises. | Add an explicit paid-pilot and revenue-reinvestment mechanism; account for the current WhatsApp AI terms and the source blueprints' useful late-stage features. |
| **GetBusiMasterRoadmap.pdf** | A useful backlog of Open Banking, POS, supply intelligence, invoicing, Start Up research, and operational reminders. | Keep those ideas as optional modules after a repeated customer need appears. | Do not place direct MTD, bank feeds, voice calls, scraping, supplier ordering, websites, or tax forecasts into early stages. Treat its vendor and price claims as unverified. |

**Best combined approach:** use the Solution Blueprint for the product and integration map, the AI Build Plan for the first workflow, the previous six-stage roadmap for safe product boundaries, and the Master Roadmap as a deferred feature backlog. None of the four should be adopted unchanged.

## The finished product

### Get Busi for existing businesses

1. **Talk to Get Busi:** use a clear, mobile-friendly web app first. The customer can type, add a receipt, and later use voice where it is useful.
2. **Capture and confirm:** AI drafts transaction details and asks about uncertain fields. The user can edit, confirm, or remove a draft. Confirmed records keep a link to their evidence and sync status.
3. **See the week clearly:** show confirmed money in and out, outstanding invoices, bills due, missing information, and next actions. Use figures from the accounting source or verified calculations. Label estimates and show their assumptions.
4. **Move work along:** later, prepare invoices, quotes, neutral reminders, and renewal tasks. The user approves sending, publishing, paying, ordering, or filing.
5. **Track selected obligations:** keep a narrow, sourced list for the chosen business type, with source, effective date, last review date, due date, and a clear route to a qualified adviser.
6. **Get help:** provide a human support route, exception queue, correction, export, disconnect, deletion request, and data-protection complaint route.

### Get Busi Start Up

Add this on the same platform after the existing-business workflow has repeat users and viable economics. Guide a founder through idea validation, customer research, a clear offer, pricing and cash-flow scenarios, a launch checklist, and weekly operating priorities. Use public company lookups and existing providers for specialist tasks. Create business-plan, website, ecommerce, or social drafts for the founder to approve; do not publish or register automatically.

### What the product owns and what it connects to

| Product layer | Get Busi responsibility | Use an existing product for |
|---|---|---|
| Experience | Plain-English onboarding, chat, review cards, reminders, approvals, and support | Messaging delivery or app distribution where suitable |
| Workflow | Fixed steps, validation, exception handling, consent, status, and audit history | Workflow infrastructure only when licence, security, and operating cost fit |
| AI | Receipt extraction, intent classification, drafting, and explanations from confirmed facts | Model API selected by accuracy, privacy terms, latency, and measured usage cost |
| Business records | Customer profile, evidence reference, confirmed capture details, consent, workflow status, external IDs, and audit trail | Formal bookkeeping ledger, VAT, payroll, bank reconciliation, statutory records, and filing |
| Payments and banking | Explain status and prepare approved actions | Subscription checkout, invoice collection, and regulated bank access through suitable providers |
| Support | Exception review and complaint handling | Accountants, bookkeepers, or other qualified partners for specialist review |

**Data design:** keep a small, auditable record of what Get Busi received, what the user confirmed, and whether it synced. Do not create a second double-entry ledger. The customer-authorised accounting system remains the financial source of truth where practical. A manual pilot log is temporary intake and review, not a production ledger. Keep evidence only for a defined purpose and retention period.

## API and partner strategy

| Capability | Recommendation | Timing and decision rule |
|---|---|---|
| **Accounting** | Build a vendor-neutral connector boundary and select one product based on pilot users' current software, workflows, permission scopes, MTD needs, export options, support, and commercial terms. FreeAgent is worth shortlisting if sole traders dominate; Xero is worth shortlisting if the target group already uses it. Xero remains unselected. | Decide in discovery; build one connector only after the paid workflow is proven. Consider a unified API such as Codat, Apideck, or Chift only if users demonstrably need several accounting systems and its added fee is lower than maintaining direct connectors. |
| **MTD for Income Tax and VAT** | Prefer an existing HMRC-compatible product or partner. Make sure the actual combination meets HMRC minimum functionality and digital-link rules, and that the user authorises the software. Do not imply that an accounting API alone makes Get Busi MTD-compatible. | Plan now for eligible users. HMRC's current developer guide warns it is not accepting production credential requests for new 2026-27 quarterly-update products because that market window has closed. Direct production integration is not the fast route. |
| **WhatsApp** | Do not make the WhatsApp Business Platform the default product channel yet. Current WhatsApp terms restrict AI providers where AI is the primary functionality, with stated exceptions for some country codes. UK users are not included in that stated exception. Because Get Busi is AI-led, get written confirmation from Meta or a qualified provider before making WhatsApp API a dependency. | Use a responsive web/PWA intake as the pilot front door. Test whether users actually need WhatsApp. Review the current business terms, messaging policy, consent, templates, provider onboarding, and pricing before adding it. This is a material channel risk, not a settled legal conclusion. |
| **Open Banking** | First use bank feeds already available through a customer's accounting product, if that meets the need. If direct transaction data becomes valuable, use an FCA-authorised or registered AISP with explicit consent; keep payment initiation out of the early product. | Later, after paid users and a cost-benefit case. Do not store credentials or act as a bank. |
| **Get Busi subscriptions** | Test an existing checkout such as Payhip if the current account and webhook limits fit. Compare Stripe or another billing provider before scale. Keep Get Busi subscription billing separate from customers' own sales and payments. | Paid concierge/pilot stage; verify fees, cancellation, refunds, tax handling, and entitlement events before selecting. |
| **Customer invoice payments** | Let the customer's accounting/payment provider collect the money. Get Busi may prepare an invoice or link for approval and read back status. Do not hold client funds. | Add only after customers request it and the payment provider's permitted use, fees, and approval path are clear. |
| **Companies House** | Use the official API for read-only public company information. Use an appropriate formation provider for incorporation or filings. | A focused Start Up capability; do not automate legal formation decisions. |
| **Documents and calendars** | Reuse a customer's existing authorised cloud store/calendar where it helps. For Get Busi's internal planning, use the existing Microsoft 365 tools. Keep business documents out of CRM and unapproved personal AI chats. | Internal use now; customer integrations only after tenant, consent, privacy, and commercial checks. |
| **AI APIs** | Choose one primary model after evaluating receipt accuracy, correction rate, response time, and cost on a representative test set. Use only the data needed for the task, and verify every provider's contract, retention, and data-use settings. API use is billed separately from consumer chat subscriptions. | Prototype with synthetic data; start a product API only after the privacy and budget controls are in place. Do not train a model on customer data. Check Xero's current terms before sending Xero API data to an AI service; its published developer terms prohibit using API data to train AI/ML models. |
| **n8n and automation** | Use Microsoft 365/Power Automate for Get Busi's internal tasks if existing licences and permissions fit. n8n may run fixed Get Busi workflows only after a security review and written licence check for this exact product model. | Do not let customers or an AI configure n8n workflows unless the correct commercial licence is in place. Keep one workflow engine, not a duplicate in every automation tool. |
| **POS, suppliers, voice, and publishing** | Add one vertical-specific connection at a time. Start supplier intelligence from the user's own receipts, then consider opt-in aggregate comparisons or partner deals. Prepare drafts and purchase suggestions; require approval. | Late stages only, after repeat use, dependable data, confirmed customer savings, and positive unit economics. Do not rely on scraping as a stable or authorised supplier API. |

### MTD and dates to keep visible

HMRC's current schedule says eligible sole traders and landlords with qualifying income over £50,000 from the 2024-25 return start MTD for Income Tax from 6 April 2026; the threshold reduces to over £30,000 from 6 April 2027 based on 2025-26, then over £20,000 from 6 April 2028 based on 2026-27. The customer's income type, previous return, exemptions, software combination, and authorisation matter. Check HMRC's live guidance for each case.

The current HMRC developer guide also says production credential requests for new 2026-27 quarterly-update products are no longer being accepted because that product market window has closed. HMRC permits compatible combinations, but the combination must meet its requirements, including digital links. Treat an established compatible product or partner as the immediate MTD route.

## Six-stage roadmap

Timings are indicative gates. Revenue, customer evidence, security readiness, and partner terms determine pace. The founder owns product decisions; assign a named delivery owner for technical, privacy, and integration work before each stage.

| Stage and target | Work and owner | Exit check and funding trigger |
|---|---|---|
| **1. Choose the first paid problem - Weeks 1-2** | **Owner:** Founder/product owner. Interview 8-12 reachable businesses across at most two groups. Map repeated tasks, current tools, pain, willingness to try/pay, channel preference, and accounting package. Choose one segment and workflow; write a one-page scope and data flow. | **Done when:** evidence supports one frequent problem and a reachable pilot group; accounting and channel assumptions are recorded; one offer and its exclusions are clear. **Spend:** remain within the stated £900 validation ceiling unless the founder explicitly changes it. |
| **2. Concierge alpha and first revenue - Weeks 2-6** | **Owner:** Founder/service operator, with privacy/security support as needed. Build a controlled web intake and review process. Use synthetic data for demonstrations. After the data flow, access, retention, support, complaint, and deletion controls are ready, invite 5-10 testers. Manually review uncertain captures and deliver a weekly view. Test the source price hypothesis of £15 and £25 per month as options, not promises; the customer's accounting subscription may be separate. | **Done when:** testers can submit, confirm/correct, and understand the record; errors reach review; repeat use, founder minutes, cost per user, and willingness to pay are measured. **Funding trigger:** charge for the concierge outcome once the pilot is ready, and use paid demand to decide whether to productise. |
| **3. Productise the repeatable core - Months 2-4** | **Owner:** Founder/product owner plus a technical delivery partner. Build a responsive web app/PWA with onboarding, account separation, confirmation/correction, support queue, export/disconnect, usage limits, and subscription billing. Add invoice drafts and status only if pilot users request them. Maintain a product cost dashboard. | **Done when:** a paid user can use the workflow without the founder rebuilding each record; exceptions are visible; support load and variable cost per user are known; paid use repeats. **Funding trigger:** only productise the parts that reduced support or increased paid retention in the pilot. |
| **4. Connect accounting and a narrow compliance pack - Months 3-6** | **Owner:** Integration owner with an accountant/bookkeeper and privacy reviewer. Choose one existing accounting engine from user evidence. Read or write only the required authorised fields; write confirmed data, track external IDs and failures, and preserve a clear audit trail. Add a small source-reviewed renewal calendar for the selected group. Use a compatible MTD product/partner where required. | **Done when:** the test customer journey meets the chosen provider's terms and relevant HMRC requirements; access can be revoked; data can be exported; exceptions and support are clear; all claims are checked. **Funding trigger:** connector usage and partner costs fit customer pricing. |
| **5. Add proactive operations - Months 6-9** | **Owner:** Product and integration owners. Add opted-in factual reminders, invoice chasing drafts, accountant sharing, and one value-proven connection such as an accounting bank feed, POS, or supplier. Consider direct read-only Open Banking through an authorised provider only if the accounting feed is inadequate. Voice calls remain optional and late. | **Done when:** customers use the specific automation, can pause it, delivery failures are handled, and the measurable benefit exceeds its fee and support cost. Do not initiate payments, make purchases, file, or publish without customer approval. |
| **6. Launch Start Up and scale - Months 9-18+** | **Owner:** Founder/product owner with technical, privacy, and specialist reviewers. Add the Start Up onboarding, idea and offer validation, transparent scenario models, launch tasks, Companies House lookups, and approved website/ecommerce/social drafts on the same platform. Move from a pilot VPS to suitable managed hosting and add native apps only when the use data supports it. | **Done when:** the existing-business service has repeat paid use and viable support economics; Start Up has its own validated offer; hosting, security, support, and regulatory review are funded. **Funding trigger:** reinvest from proven contribution, or consider external funding only for an evidenced return. |

At every gate, write down the decision to continue, revise, or stop, the evidence, open risks, spend to date, and next owner in `docs/Source-Review-and-Decisions.md`.

## Revenue-funded build-out

The goal is to earn revenue early by delivering a valuable service, then automate only the work customers already value.

1. **Earn before expanding:** after the privacy and support gates, offer the receipt-to-weekly-view service as a small paid concierge pilot. The existing £15-£25 monthly amount is a hypothesis to test, not a final price. Keep the customer's accounting subscription separate unless a partner bundle is negotiated.
2. **Measure contribution per customer:** record cash collected, refunds, payment fees, model and message costs, storage, connector fees, partner costs, and support time. Do not rely on the PDFs' rough per-user cost estimates; measure actual usage and obtain current vendor quotes.
3. **Protect liabilities and operating cash:** set aside amounts the company owes and maintain a sensible refund, support, and continuity reserve before committing the remaining contribution to new features. Confirm tax/VAT treatment and reserves with the company's accountant; this plan does not calculate them.
4. **Reinvest against evidence:** use available contribution for the next feature only when users have asked for it, it reduces manual work or improves paid retention, and its expected ongoing cost is clear. Avoid committing to fixed hiring or infrastructure costs before recurring income supports them.
5. **Keep outside funding optional:** grants, loans, investment, or an integration partner can accelerate later stages, but the base plan should not require them before the paid service is proven.

## Costs, risks, and safeguards

- Treat £900 from the Master Brief as a validation cap to confirm, not a budget for a finished app. If a safety requirement cannot fit within it, keep activity to discovery and synthetic-data work until the scope or funding changes.
- Use already-paid subscriptions only after checking the account, licence, data terms, and permissions. Do not assume that a tool in the inventory is live, secure, or permitted for product use.
- Xero's published developer model now varies by app connections and API data usage, and its terms restrict training AI/ML models on Xero API data. Its own user subscription is another cost for customers. Compare the full customer price and data-use terms, not only an API fee.
- FreeAgent's developer documentation describes an OAuth API and sandbox; its current help material describes MTD Income Tax functionality for sole traders and unincorporated landlords. Check the specific customer case and HMRC software finder; do not treat this as a selection decision.
- Do not provide bookkeeping, specific tax advice, or filings on behalf of customers until qualified advice confirms the applicable AML supervision, agent authorisation, and service requirements.
- Before processing real financial records, assign a data owner; map purposes and processors; minimise data; agree retention and deletion; prepare access controls, backup/restore, incident response, complaint handling, and customer notices. The ICO says organisations must provide a data-protection complaint route, acknowledge within 30 days, investigate, and communicate an outcome.
- Keep reminder messages factual and user-enabled. Promotional content can make a message direct marketing under ICO guidance; handle marketing separately.
- Never place passwords, API keys, recovery codes, or private customer records in project files or prompts. Use a managed secrets store and least-privilege access.

## First 30 days

| When | Owner | Action | Completion check |
|---|---|---|---|
| Days 1-7 | Founder | Choose two reachable candidate groups; schedule and conduct initial interviews; record current tools and recurring work. | At least five interview notes; no customer group has been assumed from a PDF alone. |
| Days 8-14 | Founder/product owner | Complete 8-12 interviews; select one segment and one workflow; draft the one-page pilot offer, data flow, price tests, and exclusions. | Decision and evidence entered in the source review log; pilot scope fits the validation cap. |
| Days 15-21 | Founder + technical/privacy owner | Test the web intake with synthetic data; decide how it will be stored; review product terms, security, consent, access, retention, complaint and deletion process. Confirm channel strategy, including WhatsApp policy risk. | Synthetic workflow is reviewable; named owners and unresolved risks are visible; no real customer data is processed before readiness. |
| Days 22-30 | Founder/service operator | If readiness checks pass, invite a very small pilot, deliver the workflow manually, and offer the first paid trial. Record time, corrections, repeat use, support, and actual cost. | A continue/revise/stop decision uses pilot evidence; any revenue is recorded against its delivery cost and obligations. |

## Official sources checked 17 November 2026

- HMRC, [MTD Income Tax first-time guidance and thresholds](https://www.gov.uk/guidance/use-making-tax-digital-for-income-tax/using-making-tax-digital-for-income-tax-for-the-first-time).
- HMRC, [MTD Income Tax developer guide and production window](https://developer.service.hmrc.gov.uk/guides/income-tax-mtd-end-to-end-service-guide/).
- HMRC, [how to integrate with MTD APIs](https://developer.service.hmrc.gov.uk/guides/income-tax-mtd-end-to-end-service-guide/documentation/how-to-integrate.html).
- HMRC, [compatible software finder](https://www.gov.uk/guidance/find-software-that-works-with-making-tax-digital-for-income-tax).
- HMRC, [accountancy service provider and AML supervision guidance](https://www.gov.uk/guidance/money-laundering-regulations-accountancy-service-provider-registration).
- HMRC, [how to get authorised to act as a tax agent](https://www.gov.uk/guidance/how-to-get-authorised-to-act-as-a-tax-agent-on-behalf-of-your-clients).
- Meta, [WhatsApp Business Platform overview](https://developers.facebook.com/documentation/business-messaging/whatsapp/overview/) and [WhatsApp Business Solution Terms](https://www.whatsapp.com/legal/business-solution-terms/).
- Xero, [developer pricing, API usage tiers, and developer terms](https://developer.xero.com/pricing) and [pricing and AI policy FAQs](https://developer.xero.com/faq/pricing-and-policy-updates).
- FreeAgent, [API introduction](https://dev.freeagent.com/docs/introduction?version=2026-09-01) and [MTD for Income Tax FAQ](https://support.freeagent.com/hc/en-gb/articles/35576587875346-Frequently-asked-questions-about-MTD-for-Income-Tax-in-FreeAgent).
- FCA, [account information and payment initiation services](https://www.fca.org.uk/consumers/account-information-payment-initiation-services).
- OpenAI, [business and API data use](https://help.openai.com/en/articles/7039943-how-openai-handles-data-in-consumer-services) and [API billing](https://help.openai.com/en/articles/9039756-managing-billing-for-the-api-platform).
- n8n, [licence FAQ for commercial use cases](https://support.n8n.io/article/can-i-use-your-license-for-my-use-case).
- ICO, [AI and data protection](https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/artificial-intelligence/), [complaints handling](https://ico.org.uk/for-organisations/how-to-deal-with-data-protection-complaints/), and [identifying direct marketing](https://ico.org.uk/for-organisations/direct-marketing-and-privacy-and-electronic-communications/direct-marketing-guidance/identify-direct-marketing/).

## Source files reviewed

- `GET BUSI INITIAL BRIEF.txt`
- `GetBusiAIMasterBrief-v2.pdf`
- `TechAIStackInventory17Nov2026.pdf`
- `Blueprints/GetBusi_Solution_Blueprint.pdf`
- `Blueprints/GetBusi-AI-Build-Plan.pdf`
- `Blueprints/Get-Busi-Solution-and-6-Stage-Roadmap.pdf`
- `Blueprints/GetBusiMasterRoadmap.pdf`
- `docs/Source-Review-and-Decisions.md`, `memory/projects/get-busi.md`, and `memory/context/technology-stack.md`

