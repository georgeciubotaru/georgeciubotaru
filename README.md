# George Ciubotaru

**Fullstack engineer** · TypeScript / React / Svelte · Node.js / Go / Python · data pipelines & cloud (AWS / GCP)

I've spent 9+ years owning production systems end-to-end, from database schema to shipped UI. EU citizen, no sponsorship needed, based in Chisinau, Moldova (Remote).

> **Why this profile looks quiet:** almost everything I build lives in private employer and client repositories. The public repos here are small experiments and package tests. The work below is the real record, and I'm glad to walk through any of it in detail.

---

## Selected work

### Economic data pipeline: Truflation (2024–2026)
**The problem:** inflation and economic indexes are only worth something if they're accurate and on time, and once published they feed dashboards and external consumers. Errors have to be caught *before* publication, not after.

- **One Python/FastAPI pipeline** computes CPI, PCE, labor, wage and rent indexes for the US, UK, India and Argentina. Data from 10+ third-party sources is normalized and averaged in a single core, with raw and processed data kept in S3 so results can be traced back to inputs.
- **15+ custom index products** run on the same foundation. Each has its own rebalancing logic and weight revisions, so a new index means new rules, not a new system.
- **Quality control was built in as a first-class system:** scheduled health checks, anomaly alerting and zero-delay checks that caught data errors before they were published.
- **On-chain publishing:** I led the migration of index publishing to TrufNetwork/Kwil, handling batch inserts, query retries and connector limits so publishing stayed reliable at volume.
- **30+ FastAPI endpoints** serve internal dashboards and external consumers. Delivery runs on Prefect, Docker, Jenkins and Sentry, with staging/production database mirroring so changes are tested against realistic data.

### Platform & internal tooling: Holdex (2017–present)
**The problem:** a distributed team loses hours to manual triage, invoicing and access control, and every one of those is a place for mistakes.

- **Billing and HR automation** covering contributor pay, billed hours and invoicing end to end, replacing manual processes with one traceable flow.
- **Engineering workflow automation:** issue triage and contributor tracking run automatically, so the team's time goes to building.
- **Secure by design:** the automated integrations are built to reject untrusted or forged requests before they reach the application.
- **A shared engineering foundation:** consistent tooling and quality standards, so every new product starts from the same baseline.
- **Multi-tenant platforms for partner brands:** white-label token-sale and checkout products, with admin tooling for compliance, billing and shareholder management.

### DeFi lending ecosystem: Clearpool (2022–2024, technical lead)
**The problem:** institutions and open-market participants need different things from the same protocol: institutions want gated, compliant liquidity, and open markets want permissionless access.

- **Two pool models in one ecosystem:** permissionless pools for open decentralized market-making and permissioned pools for gated institutional liquidity, plus vault contracts for yield optimization and staking for governance-token incentives.
- **Cross-chain liquidity** through LayerZero bridge contracts, so liquidity isn't stuck on a single chain.
- **Real-time data layer:** Subsquid and The Graph indexing plus backend services that aggregate contract and indexed data into APIs. The frontend reads indexed data rather than querying chain state directly.
- **Frontend:** SvelteKit with Tailwind, a custom Apollo GraphQL client, a custom svelte-store for wallet state, and Chromatic for a shared component library.
- **Led a team of 3–5 engineers** across contracts, indexing and frontend, owning technical direction end to end. The full stack was prepared for an external security audit.

---

## How I work

- **Own the whole path.** I'm comfortable taking a feature from schema to UI, and I prefer to, because that's where the integration bugs hide.
- **Check data and inputs before they ship.** The Truflation QC layer and the security checks on Holdex's automations come from the same principle: validate at the boundary.
- **Automate the recurring work,** but keep the result traceable and auditable.

## Stack

| | |
|---|---|
| **Frontend** | TypeScript, React, SvelteKit / Svelte, Vue, Tailwind, GraphQL / Apollo |
| **Backend** | Node.js, Go, Python (FastAPI, Pandas / NumPy), REST, GraphQL |
| **Data & infra** | PostgreSQL, MongoDB, Drizzle, Supabase, AWS (S3), GCP (Cloud Run, Cloud SQL, BigQuery), Docker, Cloudflare Workers, Vercel |
| **Web3** | Solidity, Hardhat / Foundry, ethers.js, The Graph, Subsquid, LayerZero |

## Get in touch

[LinkedIn](https://linkedin.com/in/george-ciubotaru) · [geeku96@gmail.com](mailto:geeku96@gmail.com) · [X @geeku96](https://twitter.com/geeku96)
