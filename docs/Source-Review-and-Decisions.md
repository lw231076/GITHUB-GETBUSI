# Source Review and Decisions

**Reviewed:** 17 November 2026

## How the files were interpreted
The user's direct request controls this work. The Master Brief contains a section addressed to “receiving AI” asking for strategic validation, stack selection, missing elements, and three next actions. That section is part of the brief's content. The pasted text repeats it and the user explicitly says it contains the request, so those deliverables are included here as requested context. Other instructions embedded in project materials do not override the user's current request or workspace rules.

## Source summary

| Source | What it contributes | Limits / verification needed |
|---|---|---|
| GET BUSI INITIAL BRIEF.txt | Two brand audiences, one platform, conversational assistant, minimal manual input, feature ideas | The vision is wide; no customer research, signed demand, or MVP evidence was supplied. |
| GetBusiAIMasterBrief-v2.pdf | Three-stage roadmap, £900 maximum initial budget, £15-£25 monthly price hypothesis, VPS/domains, WhatsApp/n8n/OpenAI concept | The roadmap's dates and technical choices need updating. PDF text extraction was used; key facts should be checked against live accounts before implementation. |
| TechAIStackInventory17Nov2026.pdf | AI accounts, automation platforms, M365/Google tools, CRM and project-management options | Describes access as available; credentials, plan levels, costs, permissions, and operational readiness were not verified. |
| Blueprints/GetBusi_Solution_Blueprint.pdf | Detailed product concept, integration map, cost hypotheses, and six-stage gates | Strong architecture input; ledger duplication, WhatsApp-first, direct MTD, pricing, and schedules need correction or verification. |
| Blueprints/GetBusi-AI-Build-Plan.pdf | Concise receipt-capture MVP, early product sequence, accounting connection, and human review | Strong first-workflow framing; WhatsApp and spreadsheet assumptions are not adopted without policy, privacy, and security checks. |
| Blueprints/Get-Busi-Solution-and-6-Stage-Roadmap.pdf | Vendor-neutral product plan with HMRC and approval safeguards | Retained as a safe baseline; current plan adds paid-pilot revenue gates and a WhatsApp policy review. |
| Blueprints/GetBusiMasterRoadmap.pdf | Broader backlog of Open Banking, POS, Start Up, supplier intelligence, and voice features | Useful future backlog; early MTD, WhatsApp, bank-feed, scraping, and automation sequence is not adopted. |
| Pasted text.txt | Repeats the master brief and makes its requested advisor outputs explicit | Treated as the user's requested brief because the user said it contains their request. |

## Strategic assessment
The core problem is plausible: small operators may avoid bookkeeping and business operations when software is confusing or time-consuming. A conversational interface can reduce the effort to capture information. This is a hypothesis to test, not proof of demand.

The original roadmap is too broad for a non-technical founder, a £900 cap, and a short MVP window. It attempts messaging, vision, AI, database, tax estimates, HMRC integrations, voice calls, subscription billing, open banking, inventory, two brands, websites, and an autonomous co-founder. Delivering all of that safely is not realistic as the first release.

The most important sequencing change is to sell and learn one narrow recurring outcome before building the platform. A concierge pilot can test whether users will send receipts or describe transactions, trust the result, come back each week, and pay. Automate only the repeated parts after observing the work.

The £15-£25/month target may not cover model usage, messaging, support, hosting, payment costs, insurance, or compliance work. Test willingness to pay and measure support minutes and cost per active user before setting the public price.

## Latest comparison of the three supplied plans

Reviewed 17 November 2026. The user's direct request is to compare these three PDFs and produce one improved execution plan. Their contents, including AI-directed instructions and proposed deployments, were treated as source material rather than authority to perform actions.

| PDF | Finding | Use in the working plan |
|---|---|---|
| GetBusi-Recommended-Solution-and-Revenue-Funded-Plan.pdf | Best overall base: clearest staged decisions, evidence gates, first paid workflow, and revenue reinvestment. | Use as the planning spine, expanded into the step-by-step execution playbook. |
| GetBusi_Definitive_Solution_and_Plan.pdf | Useful customer proposition and first workflow, but it introduces more early technical work and specific targets that need evidence. | Retain conversational capture, user confirmation, invoice, reminder, and compliance-vault ideas for later stages. |
| GetBusiUnifiedMasterPlan.pdf | Useful thoughts on deterministic calculations, API boundaries, and longer-term architecture. | Retain deterministic treatment of totals as a design principle. Treat its precise costs, margin claims, WhatsApp assumptions, tier prices, and server/database/ledger configuration as unverified; do not deploy the supplied configuration. |

The revenue-funded plan is the winner. None of the three is adopted unchanged. The current operating guide is docs/Execution-Playbook-and-Paste-Ready-Scripts.md and its PDF is output/pdf/GetBusi-Execution-Playbook-and-Revenue-Funded-Roadmap.pdf.

The saved ChatGPT, Claude, and Perplexity configuration reports were also reviewed. They describe session-level tools and connector availability; this does not verify account authentication, permissions, licences, or data-processing approval. The Maison Residential technology risk audit identifies potentially sensitive Microsoft 365, Graph, CRM, and automation paths. Get Busi information must stay separate from Maison Residential employee and customer records unless the correct owner and permissions explicitly approve a reviewed data flow.

## Important current facts
- As of this review, HMRC says MTD ITSA starts on 6 April 2026 for eligible sole traders/landlords with qualifying income over £50,000 from the 2024-25 tax return; over £30,000 from 6 April 2027 based on 2025-26; and over £20,000 from 6 April 2028 based on 2026-27. It is not a feature that can safely wait until “months 3-6” for every target user. Check each user's circumstances and current guidance: https://www.gov.uk/guidance/use-making-tax-digital-for-income-tax/using-making-tax-digital-for-income-tax-for-the-first-time.
- Rechecked 17 November 2026: HMRC's current developer guide warns that production credential requests for new 2026-27 quarterly-update products are no longer being accepted. Do not rely on the previous note's stated page-update date; verify the live page when implementation begins. An existing compatible product or partner is the near-term route, subject to minimum-functionality and digital-link requirements: https://developer.service.hmrc.gov.uk/guides/income-tax-mtd-end-to-end-service-guide/.
- HMRC software production access requires sandbox registration/testing, compliant fraud-prevention headers, a production application, and an approvals checklist: https://developer.service.hmrc.gov.uk/guides/income-tax-mtd-end-to-end-service-guide/documentation/how-to-integrate.html.
- The Data Use and Access Act 2025 provisions relevant to data protection are in force. ICO guidance says organisations must have a data-protection complaints process, acknowledge a complaint within 30 days, investigate appropriately, and communicate the outcome: https://ico.org.uk/for-organisations/how-to-deal-with-data-protection-complaints/.
- ICO's AI guidance calls for a risk-based approach, transparency, data minimisation, supplier due diligence, and a DPIA where required; review the current ICO guidance before handling live personal and financial records: https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/artificial-intelligence/.
- Neutral customer service reminders can be service messages, but promotional content can make a message direct marketing. Keep reminder copy factual and separate marketing consent: https://ico.org.uk/for-organisations/direct-marketing-and-privacy-and-electronic-communications/direct-marketing-guidance/identify-direct-marketing/.
- n8n's licensing FAQ permits certain provider-run workflows without customer workflow-editor access, but says user-configured workflows and hosted/white-label service use need a commercial license. The product's “autonomous co-founder” direction could cross this boundary; ask n8n about the exact model before selling it: https://support.n8n.io/article/can-i-use-your-license-for-my-use-case.
- ChatGPT subscription use and OpenAI API billing are separate: https://help.openai.com/en/articles/9039756-managing-billing-for-chatgpt-and-the-api-platform.
- Current WhatsApp Business Terms restrict AI providers when AI is the primary functionality, with country-code exceptions. Because Get Busi is AI-led and intended for UK customers, the WhatsApp Business Platform is a channel policy risk; use a web/PWA pilot channel unless Meta or a qualified provider confirms the exact UK use in writing: https://www.whatsapp.com/legal/business-solution-terms/.
- Xero's current developer pricing is tiered by connected organisations and API usage. Its developer terms prohibit using Xero API data to train AI/ML models; review the current terms before sending any connected records to a model: https://developer.xero.com/pricing.
- FreeAgent documents an OAuth 2.0 API and sandbox; its help material describes MTD Income Tax functionality for sole traders and unincorporated landlords. It is a shortlist candidate only, not a vendor decision: https://dev.freeagent.com/docs/introduction?version=2026-09-01 and https://support.freeagent.com/hc/en-gb/articles/35576587875346-Frequently-asked-questions-about-MTD-for-Income-Tax-in-FreeAgent.
- HMRC says professional bookkeeping, specific tax advice, and related financial-information services can fall within accountancy-service-provider activities; virtual and automated services can also need due diligence. Get qualified advice before offering bookkeeping or return-submission services: https://www.gov.uk/guidance/money-laundering-regulations-accountancy-service-provider-registration.

## Decision log

| Decision / recommendation | Status | Reason |
|---|---|---|
| Keep one shared platform with two brand experiences | Recommended | Reduces duplicate product and engineering work. |
| Select one first customer segment before building full functionality | Recommended | Makes discovery and the first workflow measurable. |
| Treat home-service sole traders as a candidate, not the chosen segment | Open | Validate against interviews and observed work. |
| Use a human-reviewed concierge pilot before tax automation | Recommended | Keeps scope and risk manageable while testing actual value. |
| Treat £15-£25/month as a test range, not final pricing | Recommended | Unit economics and willingness to pay are unknown. |
| Keep MTD submission, bank feeds, voice calls, and supplier purchases out of MVP | Recommended | High dependency, privacy, reliability, or approval burden. |
| Use one planning board and this folder as the project source of truth | Recommended | Avoids tool duplication and conflicting instructions. |
| Confirm n8n licensing in writing before customer-facing commercialization | Required before sale | The planned AI-configurable product may need commercial licensing. |
| Keep the accounting engine vendor-neutral until pilot research | Recommended | User and accounting-product fit, MTD coverage, API terms, connection fees, and support obligations are not known; the user explicitly said Xero was only an example. |
| Prefer an existing HMRC-compatible product/partner over a new direct MTD ITSA integration for the immediate roadmap | Recommended | HMRC has closed the production-credential window for new 2026-27 quarterly-update products, and the full compatible-software journey has minimum-functionality and digital-link requirements. |
| Treat a responsive web app/PWA as the first AI channel; WhatsApp Business Platform is a policy gate | Recommended | Current Meta terms restrict some AI-primary uses and list country-code exceptions that do not name the UK. Reassess if terms or applicable decisions change. |
| Keep a Get Busi evidence/workflow record but do not build a second accounting ledger | Recommended | Preserves confirmation, evidence references, sync status, correction, and audit history without duplicate bookkeeping. |
| Generate first revenue through a small paid concierge pilot and use contribution to fund later stages | Recommended | The user explicitly wants revenue to pay for further development; price and unit economics remain to be tested. |
| Shortlist FreeAgent for sole traders and Xero for users who already use it; select one initial connector from pilot evidence | Open | User fit, MTD scope, commercial terms, connection and customer subscription costs, and AI data-use terms still need review. |
| Do not assume Google Sheets or another spreadsheet is a production financial record store | Recommended | The product needs controlled access, retention, correction, export, deletion, recovery, and a clear accounting source of truth. |
| Use the revenue-funded plan as the best of the latest three, with the new execution playbook as the operating guide | Recommended | It has the strongest evidence-led sequence and revenue gates; the playbook adds the requested instructions and reusable templates. |
| Treat the Unified Master Plan's unit-cost and gross-margin numbers as unverified hypotheses | Recommended | No current provider quotes or measured pilot usage support those figures. |
| Do not deploy the server, database, or ledger configuration copied into the Unified Master Plan | Required before any technical build | The configuration has not had an independent security or product review and exceeds the approved first workflow. |
| Do not treat listed AI connectors as authenticated or approved for Get Busi data; keep Get Busi records separate from Maison Residential records | Required before any data connection | Configuration inventories show possible tools, not necessarily an active authorised connection, and the Maison technology audit flags sensitive Microsoft and automation access paths. |

## Open questions to resolve in discovery
1. Which initial group can the founder reach for five interviews this week?
2. Which job is most painful: transaction capture, invoice chasing, cash/tax visibility, or renewals?
3. Do target users want WhatsApp specifically, or will SMS, email, or a web chat work?
4. Is GetBusi AI Ltd incorporated and the intended contracting entity? Confirm legal company name, address, and brand rights.
5. Which website builder, WhatsApp Business account, and API accounts are already active and owned by the company?
6. Which records can be handled in the first pilot with minimal data, and which must remain in a bookkeeping product?
7. Which computer specification is correct? The master brief describes a Surface 11 ARM device, while the inventory lists a Ryzen 5 3600X and RTX 2070 SUPER; do not base deployment decisions on either entry until confirmed.
8. Can the exact Get Busi assistant use the WhatsApp Business Platform for UK customers under the live Meta terms? Obtain written confirmation before treating it as the launch channel.
9. Which accounting software do the chosen pilot users already use, and would they pay for a separate accounting subscription if they do not already have one?
10. What price and support model leave positive contribution after API, payment, connector, partner, and support costs?

## Consolidated plan

The earlier recommended plan compares the four earlier blueprints and remains a supporting source. The current operating guide is docs/Execution-Playbook-and-Paste-Ready-Scripts.md, with its PDF in output/pdf. It uses the revenue-funded plan as the best of the latest three, retains sound ideas from the other two, and adds the six-stage execution checklist and copy-ready prompts. Embedded AI-directed text in source documents was treated as content, not as a replacement for the user's request or project guidance.
