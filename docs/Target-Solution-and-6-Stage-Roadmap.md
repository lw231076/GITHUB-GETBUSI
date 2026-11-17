# Get Busi: Target Solution and Six-Stage Roadmap

> **Superseded on 17 November 2026.** Use [Recommended Solution and Revenue-Funded Plan](Recommended-Solution-and-Revenue-Funded-Plan.md) for current decisions. This earlier draft predates review of all four blueprint PDFs, the current WhatsApp Business terms, and the revenue-funded plan.

**Prepared:** 17 November 2026  
**Purpose:** define the intended product and a commercially sensible route from validation to a two-brand web and app service.

## Recommendation

Build Get Busi as a conversation-first business assistant and workflow layer that connects customers to established systems for accounting, tax filing, payments, banking, and company records. Get Busi should own the simple experience, business context, task orchestration, useful explanations, reminders, and trusted connections. It should not try to recreate every regulated or costly system underneath it.

Use one shared platform and two brand experiences:

- **Get Busi** helps an existing small business keep on top of daily admin, income and costs, upcoming work, and relevant obligations.
- **Get Busi Start Up** takes a new founder from idea to a tested offer, a practical start-up plan, and approved operational set-up.

The second brand should use the same account, conversation, task, finance, integration, and support foundations. Different language, onboarding, and front-end configuration are enough to start. Do not build two separate software products.

The first customer segment is still an open decision. Trades and cleaners are useful candidates to test, not an assumed winner. Choose the launch segment based on customer interviews and the accounting, messaging, and compliance tools those users already use.

**Accounting provider decision:** no accounting engine has been selected. The user's mention of Xero was explicitly an example, not a recommendation. Select a provider only after pilot-user evidence and a commercial/API review.

## What the finished product should do

### 1. A small-business assistant that is easy to talk to
The customer can use a responsive web app, iOS/Android apps, or an approved messaging channel. They can type, speak, or send a document. They see a short conversational response and a small set of clear actions, not a jargon-heavy accounting dashboard.

The main screen should answer:
- What needs my attention today?
- What money came in or went out?
- What is due soon?
- What did Get Busi do, and what needs my approval?

The customer can ask for help in ordinary language, see the source or assumptions behind an important answer, and correct the assistant without re-entering all the information.

### 2. A conversational intake and confirmation flow
For a receipt or transaction, the service:
1. Identifies the customer's business and the correct connected account.
2. Extracts likely date, supplier, amount, tax/VAT details, and document type.
3. Checks required fields, possible duplicates, and confidence.
4. Asks only for missing or uncertain details.
5. Shows a short confirmation before creating or changing a financial record.
6. Sends the confirmed information to the accounting system or a permitted record-keeping product.
7. Shows whether the change succeeded and gives the user a way to correct or undo it.

The AI proposes and explains. Deterministic checks protect totals and required fields. The accounting or tax product remains the financial system of record.

### 3. A useful weekly business view
Get Busi retrieves confirmed records and statuses from connected sources and gives the customer a clear weekly or monthly view: sales, costs, outstanding invoices, recurring bills, missing records, cash position, and next actions.

Any forecast must show the source date and assumptions. Tax estimates should be taken from a suitable accounting or HMRC-compatible product where possible; Get Busi can explain the estimate in plain language. It must not present a rough AI forecast as a definitive tax bill or imply that a reminder guarantees compliance.

### 4. A narrow, sourced compliance and renewal assistant
Each requirement shown to a customer should be tied to:
- their business structure, activity, and location;
- an authoritative source or approved expert rule set;
- an effective date, due date, and last-checked date;
- a confidence level and a named owner; and
- a link to the source or an appropriate human adviser.

Start with a single sector and a limited, reviewed set of obligations. Include user-confirmed training, insurance, accreditation, and renewal dates. Do not promise “all compliance covered” across every UK business type.

### 5. A guided business-start journey
For Start Up users, the assistant can help them:
- test assumptions about customers, competitors, and demand;
- describe an offer and its first target market;
- create a simple cost, price, and cash-flow model with visible assumptions;
- produce a business plan, launch checklist, and near-term priorities;
- connect to an accounting, payment, website, or ecommerce product; and
- draft a website, product listing, or social post for review.

Company formation, tax elections, regulated financial services, public publishing, payments, and legally significant submissions should use a qualified or authorised provider where needed and require the founder's approval.

### 6. An operations assistant that acts with permission
As integrations mature, Get Busi can prepare invoices, draft quotes, remind a user about an overdue item, update a task, or suggest a supplier order. Keep a clear review step before sending, publishing, paying, ordering, or filing. The customer should be able to see what was done and revoke access to connected systems.

## Product architecture in plain language

User text, voice, or receipt
→ Get Busi conversation and workflow
→ AI extracts or drafts information
→ deterministic checks and user confirmation
→ existing accounting, company, messaging, or payment product
→ plain-language result, next task, and auditable status

The underlying service should have:

| Layer | Responsibility |
|---|---|
| Two brand experiences | Shared web and app product with Get Busi and Get Busi Start Up language, onboarding, and feature settings. |
| Conversation and workflow | Knows which step the user is on, asks one useful question at a time, and routes approved actions to the right connector. |
| AI services | Extract text and document details, explain confirmed data, draft plans, and summarise. Model choice is based on real accuracy, cost, latency, and data terms. |
| Rules and validation | Calculates from structured data, checks required fields, flags uncertainty, prevents duplicates, and applies reviewed business rules. |
| Business profile and task store | Holds the customer's business profile, consent, preferences, obligations, reminders, workflow status, and audit trail with separate tenant access. |
| Integration layer | Connects to accounting/MTD software, messaging, subscription billing, company records, and later Open Banking or sector tools. Uses user-authorised permissions. |
| Support and administration | Lets the founder or support operator resolve exceptions, see integration failures, respond to data requests, and audit actions without browsing unrelated customer data. |

The product may keep a limited, encrypted cache to make the conversation fast, but the chosen accounting package should remain the source of truth for the customer's financial records. Avoid keeping duplicate receipt and ledger copies unless there is a clear purpose and retention rule.

## Where integrations can reduce build and compliance work

| Capability | Recommended use | Timing and feasibility |
|---|---|---|
| Accounting and record-keeping | Connect one product that the chosen pilot users already use. Read records and invoice status; write only user-confirmed transactions or drafts. Provide an export/import fallback. Do not select the vendor until users, MTD coverage, API terms, support, and per-customer costs are checked. | Highest-value integration. Select during Stage 1; implement one connector in Stage 3. |
| MTD for Income Tax | Prefer an established product in HMRC's software finder, or a commercial partner whose software can form part of a compatible combination. Confirm the digital links and customer authorisation journey before claiming MTD support. | Important now for eligible users. HMRC's developer guide currently says it is no longer accepting production credential requests for new 2026-27 quarterly-update products because the market window has closed. A fresh direct HMRC product is therefore not the fast route. |
| MTD for VAT | Use the accounting provider already filing for the customer, or add a partner after the pilot identifies demand. | Reuse an existing compatible product; do not build VAT filing in the MVP. |
| WhatsApp | Use the Business Platform or a provider that handles onboarding, templates, and delivery. For the first closed pilot, a manually supported channel can test demand before Get Busi becomes a WhatsApp Tech Provider or builds Embedded Signup. | Start manually or with a provider; move to API after the customer flow and message cost are proven. |
| Get Busi subscription billing | The available Payhip account may support an early paid pilot: its webhooks include paid/refunded and subscription started/cancelled events. Its public API is currently limited to coupon and licence-key resources, so it may not be a good long-term SaaS entitlement system. Compare it with a subscription-billing provider before expanding. | Low setup for a small test if the existing account and terms fit; migrate only when required. |
| Customer payments and invoices | Let the customer's accounting or payment provider collect their money. Keep Get Busi subscription fees separate from the customer's business transactions. Do not hold or route customer funds in the MVP. | Avoids payment-service scope and duplicative payments work. |
| Open Banking | If bank reconciliation proves valuable, connect through an FCA-authorised/registered account-information provider with explicit customer consent. Start with read-only transaction data; do not initiate payments. | Later stage. Provider, consent, security, data-use, and commercial terms need review. |
| Companies House | Use the official API to look up and refresh public limited-company information for eligible Start Up or existing-company users. Use a qualified formation partner for incorporation actions. | Read-only lookup is a reasonable Start Up feature; filing or incorporation is later and approval-led. |
| HubSpot | Use for Get Busi's own waitlist, pilot leads, and customer follow-up. | Available now for internal sales; do not store customer's financial ledger or receipts in the CRM. |
| Microsoft 365 / Power Platform | Use Forms, Planner, Teams, SharePoint, Power Automate, and possibly Dataverse for Get Busi's internal pilot operations, support queue, approvals, and founder administration. | Reuses existing access. Do not assume internal Power Apps licensing is suitable for a public multi-tenant SaaS. |
| Zapier / n8n / Pipedream | Use Zapier for quick, low-volume prototypes; Power Automate for internal Microsoft flows; n8n for Get Busi-owned workflows only after licensing and security checks; Pipedream for a technical helper's API experiments. | Do not duplicate a workflow in multiple engines. Confirm n8n's commercial boundary before customer-configurable automation or product resale. |
| Website, ecommerce, and social tools | Use the customer's existing platform API when there is a supported connector. Draft changes and require approval before publishing. | Start with drafts and links; add one integration when customers request it. |
| Supplier and POS data | Connect to the specific POS or supplier systems used in the selected vertical. Compare availability, stock, price, and delivery with a dated source. | Later stage. There is no guaranteed universal supplier API; do not promise best-market prices until coverage is proven. |
| AI runtime | Use a server-side model API for product requests, with spend limits, data minimisation, and a small test set. ChatGPT, Claude, Gemini subscriptions do not themselves grant the product unlimited API use. | Choose one primary API and one fallback only after testing. Keep API keys off devices, prompts, and project files. |

### Accounting-engine selection: no vendor chosen

The accounting engine is a product category decision, not a brand decision yet. Start by asking pilot users what they already use and whether they would authorise a connection. Score candidates before selecting one:

| Selection factor | What to check |
|---|---|
| Customer fit | How many target users already use it? Can a complete novice authorise it without help? |
| MTD scope | Does it support the user's actual income source, accounting period, VAT status, and end-of-year needs? Is it listed by HMRC for the relevant combination? |
| API quality | Can it read/write the required transactions, receipts, invoices, contacts, and reconciliation status? Are OAuth, scopes, webhooks, rate limits, sandbox, and error recovery clear? |
| Commercial terms | Connection limits, developer/partner tiers, app review or certification, reseller or embedded permission, per-connection costs, support, and minimum commitments. |
| Data control | Customer authorisation/revocation, export, deletion, data location, processor terms, incident support, and AI use restrictions. |
| Operational fit | Availability, API version policy, support for accountants/bookkeepers, and a path to switch providers without losing records. |

Select one provider for the first product connector and maintain a clean internal adapter so another provider can be added later. Do not build five accounting integrations before proving the first workflow. Do not assume that access to a vendor API automatically permits resale, embedding, or use in AI features; confirm partner terms in writing.

## Six-stage roadmap

| Stage and target | Build and deliver | Integrations | Exit gate |
|---|---|---|---|
| **1. Choose the wedge and partners** — Weeks 1-2 | Interview 8-12 reachable businesses across at most two candidate groups. Pick one group and one recurring job. Map current manual work, existing software, willingness to try, and willingness to pay. Draw the data flow and price/cost model. | Check the HMRC software finder for needed tax coverage; ask users which accounting, messaging, POS, and payment tools they already use. Ask vendors about API and embedded terms. | Evidence of a repeated problem, reachable pilot users, one clear message, and at least one viable record-keeping route. No accounting provider is assumed in advance. |
| **2. Concierge alpha** — Weeks 2-6 | Create one landing page and one conversational test. Capture income, expenses, and receipts for a single niche. AI prepares drafts; the founder reviews uncertain entries and creates a weekly summary. Use the least data possible and synthetic data until privacy and access controls are ready. | Manual WhatsApp Business or a controlled web route; a restricted internal pilot log; one low-risk automation. Use an accounting sandbox or a selected partner only after its terms and data flow are understood. | 5-10 invited testers can complete the workflow, correct errors, and explain what is valuable. Track accuracy, time saved, repeat use, support time, and cost. |
| **3. Paid core beta** — Months 2-4 | Build the shared tenant/user profile, responsive web app, conversation workflow, confirmation and correction path, support console, notification preference, and first brand theme. Test recurring subscription and costs. | One accounting connector chosen from pilot evidence; one subscription-billing route; HubSpot or M365 for Get Busi's own lead and support process. | Real customers pay or commit to a paid test; per-user support/API/message cost and retention are acceptable; data export and disconnect work. |
| **4. Accounting and compliance connections** — Months 3-6, with MTD planning now | Build sourced obligation tracking for the chosen sector and entity type. Add a user-authorised accounting/MTD partner connection, digital record links, and reviewed report explanations. Offer help from a bookkeeper/accountant for exceptions. | Existing HMRC-compatible software or an approved partner; Companies House read-only lookup for limited companies. Track current threshold and product eligibility. | The connected path covers the target customer's full required journey. Product claims match the partner's permissions and HMRC requirements. Errors, revocation, and support are tested. |
| **5. Proactive operations** — Months 6-9 | Add event-based reminders, invoice and quote drafts, renewal tasks, and an exception queue. Add voice only if users ask for it and opt in. Add supplier/POS capability for the chosen niche only. | WhatsApp Cloud API or a provider after Tech Provider/customer-onboarding requirements and pricing are understood; later, a regulated Open Banking AIS provider for read-only reconciliation; selected POS/supplier connector. | Users prefer and use the automations, opt-outs work, the service handles delivery failures, and variable costs remain within the paid plan economics. |
| **6. Second brand and scale** — Months 9-12+ | Launch the Start Up journey on the shared platform: idea validation, transparent financial scenarios, a launch checklist, company data lookup, and user-approved website/ecommerce/social drafts. Add native iOS/Android apps when usage proves the responsive app is not enough. Move to managed, monitored production hosting and support arrangements based on measured load. | Companies House API; selected formation, web/ecommerce, payment, and accounting partners; app-store and messaging integrations as justified. | Existing-business users retain and pay; Start Up users complete the guided journey; operating costs, security, support, and app maintenance are funded by revenue. |

The stages are gates, not promises about a fixed launch date. Stage 2 can begin manually as soon as privacy, access, and support controls are ready. Do not wait for native apps or an exhaustive integration catalogue before validating the core conversation.

### Stage ownership and completion checks

Named people have not been assigned yet. The roles below are proposed owners; the founder should name an individual for each role before that stage starts. One person may hold more than one role in the early stages.

| Stage | Proposed owner | Tangible outcome | Simple completion check |
|---|---|---|---|
| 1. Choose the wedge and partners | Founder / product owner | Interview notes, selected segment and workflow, partner shortlist, initial cost model | 8-12 interviews are recorded; the chosen problem repeats across users; the first workflow and excluded features are written down. |
| 2. Concierge alpha | Founder / service operator, with a privacy adviser as needed | A working human-reviewed service and pilot operating checklist | 5-10 invited testers can submit and correct a record; a weekly summary is delivered; privacy, complaint, access, retention, and deletion steps are documented before live personal data is used. |
| 3. Paid core beta | Technical product owner / delivery partner, with founder approval | Responsive product, first connector, support process, and paid pilot | A user can onboard, confirm/correct a record, export data, disconnect, and pay; the pilot's cost per active user and support time are measured. |
| 4. Accounting and compliance connections | Integration owner plus qualified bookkeeping/accounting and privacy review | Tested connection to the selected accounting/MTD product and sourced obligation tracker | A target user completes the required journey in a test environment; consent, digital links, errors, revocation, and product claims are reviewed and recorded. |
| 5. Proactive operations | Product owner and integration owner | Opt-in reminders and approved drafts for the chosen vertical | Users can pause or opt out; failures reach the support queue; no payment, purchase, filing, or publishing happens without explicit approval. |
| 6. Second brand and scale | Founder / product owner with technical and specialist reviewers | Start Up experience on the shared platform and a funded support/hosting plan | Start Up users complete the defined journey; retention, support, security, and per-customer economics justify expansion. |

At each gate, the founder records the decision (continue, revise, or stop), evidence, remaining risks, and next owner in `docs/Source-Review-and-Decisions.md` before committing to the following stage.

## Costs and commercial controls

The £900 in the master brief is suitable as a validation ceiling, not a budget for a complete public mobile product with direct MTD, banking, messaging, and multi-sector compliance. The cost can stay lower by:

- reusing the subscriptions and connections already active;
- choosing one customer segment, one workflow, one accounting integration, and one messaging route;
- keeping human review in the alpha instead of buying voice automation, inventory, or multiple AI agents;
- using an existing accounting/MTD product rather than building a ledger and filing service;
- testing a paid pilot through a tool already available, subject to its webhook and business terms;
- capping model and message spend per user and checking costs weekly;
- pricing from measured support time, connected-account fees, API use, storage, failed transactions, refunds, and payment fees.

Before selecting an integration, get written answers to: setup or certification fees, fee per customer/account, included API calls, data volume limits, revenue share, support fees, minimum contract, customer data export, and contract termination. Re-check the commercial model at 5, 20, 100, and 500 active customers.

## Product rules that minimise manual work safely

- Ask one missing question at a time; prefill from user-authorised connected records.
- Confirm any low-confidence amount, date, tax treatment, recipient, or category.
- Use deterministic calculations for totals and forecasts; AI explains them rather than inventing the numbers.
- Automate reminders and drafts first. Require review for filing, payment, purchases, public publishing, and high-impact compliance changes.
- Track action status: pending, confirmed, sent, failed, cancelled, or needs review.
- Offer pause, opt-out, disconnect, correction, export, and deletion routes.
- Route exceptions to one founder/support queue instead of making the customer repeat the entire story.

## Current constraints to keep visible

- HMRC says MTD ITSA is already live for eligible users whose qualifying income was over £50,000 for the 2024-25 tax year, with the threshold reducing to over £30,000 from 6 April 2027 (based on 2025-26) and over £20,000 from 6 April 2028 (based on 2026-27). Eligibility and exemptions are user-specific; check the current HMRC guidance for each customer.
- HMRC's current developer guide warns it is no longer accepting production credential requests for new 2026-27 quarterly-update products. Use an existing HMRC-compatible product or partner for the immediate route. HMRC also allows compatible software combinations, subject to minimum functionality and digital-link requirements. See the authoritative review in docs/Recommended-Solution-and-Revenue-Funded-Plan.md.
- An accounting API does not make Get Busi MTD-compatible automatically. Validate the complete customer journey, software permissions, and customer authorisation.
- Open Banking and payment initiation are regulated areas. Use an authorised provider and explicit customer consent; do not become a financial provider in the early product.
- Meta's platform has provider onboarding and Embedded Signup steps for offering messaging services to customers. Verify these and price by actual expected message volume before choosing it as the only channel.
- Payhip is already in the stack and can emit paid/refund/subscription webhooks, but its public API has limited resources; use it for a simple paid test only if that limitation is acceptable.
- The single VPS is a test/early-pilot asset until backups, access, monitoring, patching, and recovery are verified. Do not use a public n8n editor or a spreadsheet as the production ledger.

## Official references checked 17 November 2026

- HMRC, MTD ITSA developer guide and current market-window warning: https://developer.service.hmrc.gov.uk/guides/income-tax-mtd-end-to-end-service-guide/
- HMRC, compatible software finder: https://www.gov.uk/guidance/find-software-that-works-with-making-tax-digital-for-income-tax
- HMRC, API minimum functionality and production approval: https://developer.service.hmrc.gov.uk/guides/income-tax-mtd-end-to-end-service-guide/documentation/how-to-integrate.html
- FCA, account information/payment initiation provider authorisation: https://www.fca.org.uk/firms/account-information-services-payment-initiation-services
- FCA, authorisation/registration application guidance updated 2 November 2026: https://www.fca.org.uk/firms/apply-emoney-payment-institution
- Meta, WhatsApp Business Platform and partner onboarding: https://developers.facebook.com/documentation/business-messaging/whatsapp/overview/
- Companies House, API overview: https://developer.company-information.service.gov.uk/
- Payhip, webhook events: https://help.payhip.com/article/115-webhooks
- Payhip, API resources: https://payhip.com/api-reference
- Stripe, Billing: https://stripe.com/gb/billing
- n8n, licensing FAQ: https://support.n8n.io/article/can-i-use-your-license-for-my-use-case
- OpenAI, ChatGPT and API billing: https://help.openai.com/en/articles/9039756-managing-billing-for-the-api-platform
- ICO, data protection and AI: https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/artificial-intelligence/
