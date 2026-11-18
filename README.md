# Gaza Watermelon — Donation platform prototype

An Arabic-first, RTL, responsive humanitarian donation platform concept for Algerian donors. The interface follows the supplied Gaza Watermelon visual direction: forest green, watermelon red, warm ivory, campaign cards, impact stories, donation flow, transparency center, receipt tracking, and an admin preview.

## Important: demo mode, not a live fundraising service

This project is a functional front-end prototype. **It does not collect or transfer money.** The payment choices (Edahabia / CIB), receipts, donation records, campaign totals, and admin figures are illustrative only. Test donations are stored only in the browser's `localStorage`. No card number or CVV is requested or stored. Never publish this prototype as a live donation service or advertise the demo transactions as real donations.

Before any real fundraising launch, the organization operating the platform must, at minimum:

1. Establish the legal entity / licensed association or formal partnership that is authorized to collect the donations, and have Algerian counsel review the exact operating model and cross-border aid arrangements.
2. Confirm the applicable permissions and documentation for collecting and receiving donations, beneficiary identity checks, donor records, AML / sanctions screening, financial reporting, tax treatment, privacy and data protection.
3. Obtain written acceptance from the acquiring bank / payment provider for this specific charitable use case and complete the relevant SATIM / GIE Monétique onboarding, technical certification and production authorization. Do not assume that a standard merchant account is automatically eligible for donations.
4. Implement a server-side payment adapter with signed callbacks / webhooks, idempotency, reconciliation, refunds and audit trails. Card data must remain with the certified payment page/provider; never collect PAN/CVV in this app.
5. Replace sample campaigns and figures with verified information, signed partner agreements, approved budgets and independently reviewable evidence. Clearly explain administrative fees and refund/failed-campaign policy.
6. Add production authentication / role-based authorization for the admin area, secure sessions, MFA, CSRF protection, rate limiting, logging, backups, monitoring, secrets management and security testing.
7. Replace placeholder contact details and publish reviewed Terms, Privacy, Cookies, Complaints, Refund, Partner Verification and Photo Consent policies.

The current application intentionally labels all seeded amounts and campaign progress as demo data. The `CAPTCHA` checkbox is also a UI placeholder, not a real bot-protection service.

## Run locally

Requires Node.js 20+.

```bash
npm install
npm run dev
```

Open the local URL printed by Vite (usually `http://localhost:5173`).

Production build:

```bash
npm run build
npm run preview
```

## Main routes

- `/` — home page
- `/campaigns` — campaign directory with filters/search
- `/campaigns/:id` — campaign detail
- `/transparency` — transparency / reporting framework
- `/stories` — sourced humanitarian photo stories
- `/about` — about / launch requirements
- `/faq` — frequently asked questions
- `/privacy` — preliminary privacy and payment-data notes
- `/track` — local demo receipt lookup
- `/admin` — non-secured admin UI preview; never expose as a production admin panel

## Open-source libraries

- React + React Router — component UI and routing
- Framer Motion — progressive reveal and card transitions
- Radix UI Dialog — accessible donation modal semantics, focus management and escape handling
- Lucide React — icon set
- Vite — development server and production bundler

The stylesheet includes keyboard focus visibility, semantic landmarks, form labels, accessible names, progressbar values, `prefers-reduced-motion` handling and responsive breakpoints. This is not a formal WCAG audit; test with screen readers, keyboard-only navigation, automated checks and real devices before launch.

## Photo sources and attribution

These images are remote embeds, not original campaign documentation. They are shown for context only and must not be represented as proof of work by Gaza Watermelon:

- World Food Programme (WFP), Gaza food assistance image: https://wfpusa.org/news/wfp-reaches-hundreds-thousands-people-gaza-ceasefire/
- UNICEF Sweden, Gaza water distribution coverage: https://unicef.se/amne/gaza
- World Food Programme (WFP), diary / aid truck coverage: https://www.wfp.org/stories/diary-gaza-theres-no-time-mourn-anyone-or-anything

Check the rights, attribution and hotlinking terms with each source before public/commercial deployment. Prefer media supplied under written permission by the vetted implementation partners, with informed consent and safeguarding review.

## Design tokens

- Deep forest green: `#073b2b` / `#0b4934`
- Watermelon red: `#df4b50`
- Warm ivory: `#fbfaf5`
- Soft green surfaces: `#edf5ee`

The Arabic RTL layout is the default. English and French localizations can be added after the legal and payment content has been finalized.
