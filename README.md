# Christopher O’Keefe

### Applied AI · software · business workflows — St. Louis, remote

I turn business problems into useful software and workflows: figuring out what people need, building and testing the solution, and explaining it so the people using it trust it. Most of my code is written with AI coding tools; the ticket contracts, verification gates and documentation around them are the part I own.

**Portfolio:** [keystonecollective.io](https://keystonecollective.io) · **LinkedIn:** [chrisokeefe-ai](https://linkedin.com/in/chrisokeefe-ai) · chris@keystonecollective.io

## Currently building — Keystone platform (private)

A multi-tenant backend and operator console for real-estate investors: lead generation from public notices, market imports and inbound sites; follow-up in one CRM; an evidence-backed offer range from county public records; a photo-based property brief after the walk; buyers matched to what comes through. Python 3.11 / FastAPI / Pydantic on Cloud Run, Next.js 16 / React 19 / TypeScript on Vercel, Firestore with a staged PostgreSQL research schema, Gemini for extraction and photo analysis, keyless Vercel-OIDC-to-GCP identity.

What I’d point a technical reader at, on request: closed Pydantic contracts that forbid person-identifying keys; a deterministic comp spine with a three-comp floor and printed confidence factors; offline-by-default tests with sockets fenced, run locally and as a GitHub Actions release gate on every pull request (about 5,500 passing across the backend, database and console); row-level security on every tenant table, proven with a synthetic concurrency corpus; a 480-ticket delivery history with approval envelopes and closeouts that state what is not claimed.

Built and operated by one person; the first tenant was a client engagement that has ended. No paying customers, no production PostgreSQL, no public deployment. The case study, with a recorded replay of the research console, is at [keystonecollective.io/projects/keystone-platform](https://keystonecollective.io/projects/keystone-platform). I can walk through the code on a screen share.

## Delivered work

- **Public-notice pipeline** (paid engagement): notices → LLM extraction into validated schemas → property enrichment → explicit rules and human review → same-day alerts; 30+ qualified leads a month from the notice stream the client chose.
- **Three client websites, one CRM** — Next.js / React / TypeScript, audience-specific guidance with official-source links, GTM / Analytics / Meta Pixel events, handed off with documentation. The engagement has ended and the sites are offline; the code is private.
- **Deal Hunter** — normalization, deduplication and cross-source matching of distress lists with deterministic buy-box ranking; 2,934 leads and 6,092 closed-sale records organized in the client’s Sheets workspace.
- **Scout** — inbound email and photo intake to repair estimate, PDF brief and CRM record. Ran end to end in practice on well over the 17 photos in the documented test; accuracy was never measured as a percentage.
- **Clinic digitization** — website, HubSpot CRM, online booking, telehealth setup and opt-in follow-up; an opt-in SMS campaign generated $6,000+ in booked appointments on its first send.

## How I work

Tickets as contracts: scope lock, approval envelope, and a closeout that says what shipped and what is not claimed. Context engineering for AI-assisted delivery: durable orientation files with pointers, replaceable snapshots, agent-harness constraints, a do-not-claim file that overrides everything, and checks that surface drift. Notes on both at [keystonecollective.io/notes](https://keystonecollective.io/notes).

Open to remote roles in applied AI, AI implementation and product engineering.
