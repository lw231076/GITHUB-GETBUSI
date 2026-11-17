# Get Busi Project Memory

**Prepared:** 17 November 2026  
**Status:** Discovery and MVP planning  
**Project home:** GETBUSI folder / Codex project “GET BUSI”

## Vision from the founder
One conversational business-assistant platform for UK businesses. It should feel like a helpful PA, reduce jargon and manual data entry, and grow from a focused service into broader business operations support.

### Brand audiences
- **Get Busi:** existing small businesses such as trades, cleaning, taxi, takeaway, and retail operators.
- **Get Busi Start Up:** aspiring founders who want help validating and starting a business.

The two brands should share data, workflows, and platform components. Their branding, messages, onboarding, and front ends can differ. Do not build two separate products.

## Current recommendation
Start with one segment selected through short customer interviews. A promising hypothesis is UK sole-trader home services, because job income, invoices, receipts, expenses, and periodic records recur. This is not yet a confirmed target; compare it with at least one other group before committing.

Design the final service as a conversation and workflow layer on top of selected accounting, compliance, messaging, and company-information products. Keep the chosen accounting product as the financial system of record where practical. Get Busi should retain the evidence reference, user-confirmed capture, consent, sync status, corrections, and audit trail, not build a second double-entry ledger. No accounting provider has been selected; the founder specifically said the Xero example was not a recommendation.

See docs/Execution-Playbook-and-Paste-Ready-Scripts.md for the current step-by-step operating guide, six-stage plan, go-live gates, tool use, and reusable prompts. The downloadable copy is output/pdf/GetBusi-Execution-Playbook-and-Revenue-Funded-Roadmap.pdf. Of the latest three supplied plans, GetBusi-Recommended-Solution-and-Revenue-Funded-Plan.pdf is the strongest base; its recommendations are expanded in the playbook.

Start with one workflow:
1. A user sends a short text or receipt image describing income or a cost.
2. The assistant drafts a structured record and asks for confirmation when fields or categories are uncertain.
3. The user can correct or delete the entry.
4. The product returns a simple weekly activity and cash view, with any reserve figure clearly labelled as an estimate.

Keep human review in the pilot. Use a responsive web app/PWA as the assumed early channel. Current WhatsApp terms create a material policy risk for an AI-led assistant in the UK, so do not make the WhatsApp Business Platform the launch dependency without written confirmation. Do not submit tax information, move money, make purchases, or present an AI estimate as a tax bill.

Aim to generate the first revenue from a small paid concierge pilot once data handling and support controls are ready. Reinvest contribution after obligations, refunds, direct delivery costs, and operating reserves; keep the £15-£25 monthly amount as a price hypothesis, not a commitment.

## Source-stated assumptions
- The founder states they are non-technical and wants no-code/low-code delivery.
- The master brief states a maximum initial budget of £900. Treat this as a cap to verify against current spend, not a recommended spend.
- A £15-£25 monthly subscription is a pricing hypothesis in the master brief.
- The master brief says the Hostkey VPS is active with Ubuntu 24.04, Docker, 2 vCPU, 4 GB RAM, and 60 GB storage; the technical inventory also lists domains and available tools. These details were not independently tested.
- The user says the product should be marketed under Get Busi and Get Busi Start Up. Naming/capitalisation differs across source files; confirm before public launch.
- The master brief names GetBusi AI Ltd. Verify company and trading-name details before using them in contracts, privacy notices, payment accounts, or public claims.

## Early product boundaries
### Pilot may include
- Plain-language onboarding and a small number of repeated chat commands.
- Receipt/income/expense capture, confirmation, and correction.
- A basic weekly report that shows records received, missing information, totals, and a cash view.
- A neutral service reminder chosen by the user.

### Defer until evidence and review
- HMRC submissions or claims of MTD compatibility.
- Automated tax liability advice or “no surprises” guarantees.
- Automated voice calls, bank feeds, card/payment handling, supplier purchases, or full regulatory coverage.
- POS/inventory integrations, all-business feasibility studies, websites/social publishing, and a broad autonomous co-founder.
- A second fully featured product front end.

## Current decisions and open questions
See docs/Source-Review-and-Decisions.md for the decision log. The largest unanswered question is which customer group has the most urgent repeated problem and will use the service weekly.

## Measures to learn
- Time from sign-up to first useful record.
- Share of records accepted without correction and the error types that need human review.
- Share of pilot users who return weekly.
- Minutes of founder support per user per week.
- Whether the weekly report changes a user's next action.
- Willingness to pay, tested after users experience the workflow.
- Cost per active user across AI, messages, hosting, storage, payment fees, and support.

## Current official reference links
- HMRC MTD ITSA eligibility and start dates: https://www.gov.uk/guidance/use-making-tax-digital-for-income-tax/using-making-tax-digital-for-income-tax-for-the-first-time
- HMRC software production approval journey: https://developer.service.hmrc.gov.uk/guides/income-tax-mtd-end-to-end-service-guide/documentation/how-to-integrate.html
- HMRC MTD ITSA developer guide and current production window: https://developer.service.hmrc.gov.uk/guides/income-tax-mtd-end-to-end-service-guide/
- Meta WhatsApp Business Solution Terms: https://www.whatsapp.com/legal/business-solution-terms/
- Xero developer pricing and API data-use policy: https://developer.xero.com/pricing
- FreeAgent API documentation: https://dev.freeagent.com/docs/introduction?version=2026-09-01
- n8n use-case licensing FAQ: https://support.n8n.io/article/can-i-use-your-license-for-my-use-case
- ICO AI and data protection guidance: https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/artificial-intelligence/
- ICO data-protection complaints process: https://ico.org.uk/for-organisations/how-to-deal-with-data-protection-complaints/
- Meta WhatsApp Business Platform: https://developers.facebook.com/documentation/business-messaging/whatsapp/overview/
