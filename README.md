# Christopher O’Keefe

### Applied AI · software · business workflows — St. Louis, remote

I build software that removes friction from real work. Most of it started in my own: I’ve worked in real estate since 2017, as a Realtor and then on the wholesale side of investing. I write the requirements and review every change. AI coding tools do most of the typing.

**Portfolio:** [keystonecollective.io](https://keystonecollective.io) · **Technical detail:** [keystonecollective.io/receipts](https://keystonecollective.io/receipts) · **LinkedIn:** [chrisokeefe-ai](https://linkedin.com/in/chrisokeefe-ai) · chris@keystonecollective.io

## Keystone platform (private, current work)

**What it does:** turns scattered property information into organized research, repair estimates and clear next steps for real estate investors.

**How it’s built:**

- Python 3.11, FastAPI and Pydantic backend on Cloud Run. Next.js 16, React 19 and TypeScript console on Vercel.
- Firestore is the runtime store. A PostgreSQL research schema with row-level security on every tenant table is built and proven offline. It is not provisioned in production.
- Gemini reads notices, emails and photos. Written rules decide qualification, ranking and offer ranges. A person reviews before anything is written.
- The console reaches the backend with Vercel OIDC exchanged for a short-lived Google identity. No long-lived keys.

**Worth a look if you’re an engineer:**

- Closed Pydantic contracts that reject person-identifying keys.
- A value range from county records that returns no dollar figure below three comparable sales, with the confidence factors printed.
- About 5,500 offline tests with sockets fenced, run locally and as a GitHub Actions release gate on every pull request. The gate verifies. It never deploys.
- More than 460 shipped tickets, each with a locked scope, a review and a closeout that states what isn’t claimed.

**Status:** one operator. A paid client was the first user, and that engagement has ended. No paying customers, no production PostgreSQL, no public deployment. The code is private, and I’m happy to walk through it on a call. Case study with recorded lookups: [keystonecollective.io/projects/keystone-platform](https://keystonecollective.io/projects/keystone-platform).

## Tools I’ve built

| Tool | What it did | How |
|---|---|---|
| [Foreclosure lead alerts](https://keystonecollective.io/projects/document-to-decision) | Same-day alerts for a paid client; 30+ qualified leads a month from the notices he chose. | Python pipeline. LLM extraction into Pydantic schemas, property enrichment, deduplication, written qualification rules, human review for uncertain records, email delivery. |
| [Deal Hunter](https://keystonecollective.io/projects/intake-and-prioritization) | My own lead research: one ranked list of 2,934 distressed-property leads, backed by 6,092 closed sales. | Normalization and cross-source matching of distress lists. Deterministic signal rules plus a buy box. Results in Google Sheets. |
| [Scout](https://keystonecollective.io/projects/email-photo-intake) | Email and photos in; repair estimate, PDF brief and CRM record out. | Structured extraction, photo analysis, a tiered repair catalog, PDF and CRM output. Estimates flagged for review. Verified end to end on a 17-photo test; accuracy not measured. |
| [Three websites, one CRM](https://keystonecollective.io/projects/customer-intake) | Foreclosure, probate and investor sites for one brand, every inquiry in one CRM. | Next.js, React, TypeScript. GTM dataLayer events, Analytics and Meta Pixel. RentCast API for seller reports. Handed off with docs; sites now offline, code private. |
| [Clinic digitization](https://keystonecollective.io/projects/clinic-workflow) | A clinic moved from paper to digital; $6,000+ booked in the first week of the campaign. | Website, HubSpot CRM, online booking, telehealth and opt-in SMS. Through ICI Marketing, 2019–2021. |

Stack by project, architecture and limits for each: [keystonecollective.io/receipts](https://keystonecollective.io/receipts).

## How I work with AI

- Every task starts as a written ticket I approve: the goal, the limits and how we’ll know it’s done.
- Larger batches get a separate review. Fixes repeat until it passes.
- Structured “brains” give the model the goals, evidence, rules and a list of things it must never claim. One prompt orients a session.
- An end-of-day sync writes the day’s work, lessons and next ticket back into the brains.

Notes: [How I keep AI work on track](https://keystonecollective.io/notes/tickets-as-contracts) · [Giving AI the right context](https://keystonecollective.io/notes/context-engineering) · [I review before anything changes](https://keystonecollective.io/notes/human-review-before-the-write)

Open to remote implementation, business-systems and applied-AI work.
