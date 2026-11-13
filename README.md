# Awesome-Developer-Sandbox-Testing-Environment

## Top Developer Sandbox & Testing Environment Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Ephemeral Preview Environments, Isolated Sandboxes & Cloud Emulation*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Developer Sandbox & Testing Environments**. These tools provide isolated, disposable copies of applications and their dependencies—enabling safe testing, feature previews, and sales demos without risking production data or creating conflicts between teams sharing a staging environment.

**Examples** include Salesforce Sandboxes, Zoho CRM Developer Edition, Okteto, Release.com, Bunnyshell, Uffizzi, LocalStack, and open-source alternatives like fakecloud and Floci (the category leaders).

**Open-source emphasis**: This section highlights every major active project for self-hosted ephemeral environments, open-source cloud emulation, and community-driven sandbox orchestration—ideal for organizations seeking data sovereignty and predictable costs over per-preview SaaS billing. The open-source landscape has shifted significantly: **LocalStack Community Edition is no longer free** (March 2026 change requires auth token), and **fakecloud** (AGPL-3.0) has emerged as the migration target for teams needing commercial-use freedom [citation:4][citation:15].

Contributions welcome! Open an PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [Sector Overview & Market Dynamics](#sector-overview--market-dynamics)
- [SaaS/Hosted Platforms](#saashosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## Sector Overview & Market Dynamics

The Test Environment-as-a-Service (TEaaS) and Environments-as-a-Service (EaaS) sector is estimated at **$17.7B to $20B+** globally, projected to reach over **$40B–$60B+ by the early 2030s** at an estimated CAGR of 14%–19%. The sector remains **highly fragmented**, characterized by open-core platforms, specialized startups targeting ephemeral pull-request previews and local cloud emulation, and competing native capabilities offered by hyperscalers and DevOps git-hosts.

## SaaS/Hosted Platforms

| Product | Company Size (Valuation / Revenue) | Description | Starting Pricing | Free Tier / Free Trial Limits |
|---------|------------------------------------|-------------|------------------|-------------------------------|
| **[Salesforce Sandboxes](https://www.salesforce.com/platform/sandboxes-environments/pricing/)** | ~$180B Market Cap / ~$41.5B Revenue | Four sandbox types: **Developer** (metadata only, included with core CRM licenses), **Developer Pro** (5% of net spend), **Partial Copy** (20% of net spend), **Full Copy** (30% of net spend). Scratch Orgs start at $25/org/month. Base Salesforce CRM Starter Suite begins at $25/user/month. | **Included Free**: 1 to 100 Developer Sandboxes (200 MB test data, daily refresh) bundled per CRM license edition; **Free Trial**: 30-day free trial on Starter Suite. |
| **[Zoho CRM Developer Edition](https://www.zoho.com.cn/crm/developer/developer-edition.html)** | ~$12.5B Valuation / ~$1.4B Revenue | Dedicated, full-featured development environment for Zoho CRM to test custom modules, Deluge functions, and workflows. Paid production Zoho CRM tiers start at $14/user/month (billed annually) or $20/user/month (monthly). | **Free Forever**: 1 developer user account, up to 5,000 records, 10 MB data storage (strictly isolated for testing/development). |
| **[LocalStack](https://localstack.cloud/)** | ~$100M–$250M Valuation (~$28.2M Funded) / ~$7M ARR | Local AWS and Snowflake cloud emulator for rapid testing and CI/CD offloading without cloud spend. | **Base Tier**: $39/user/month (AWS emulator, annual billing) or $45/user/month (monthly billing). | **Hobby Plan (Free Forever)**: 30+ core emulated AWS services, non-commercial personal use only, requires account & auth token; **Free Trial**: 45-day free trial for paid tiers. |
| **[Release.com](https://releasehub.webflow.io/pricing)** | ~$80M Valuation (~$22.9M Funded) / ~$5M ARR | Environments-as-a-Service (EaaS) platform spinning up full-stack ephemeral environments directly inside your cloud (AWS/GCP) on every commit. | **Custom / Enterprise**: Tailored quotes based on cloud architecture and environment scale (runs BYOC in customer AWS/GCP). | **Free Trial / Sandbox Tier**: 5 free environment/compute hours upon registration; free sandbox tier includes 100 managed pre-production environment hours/month. |
| **[Okteto](https://www.okteto.com/pricing/)** | ~$50M–$100M Valuation (~$18.1M Funded) / ~$4M ARR | Kubernetes-native development platforms with automated preview environments for pull requests and development sandboxes. | **Scale Plan**: Custom quote per user seat (billed annually; previous Developer Pro tier started at $19/user/month). | **Starter Plan (Free Forever)**: Free for up to 5 users, unlimited ephemeral and dev environments on self-hosted Kubernetes, community support. |
| **[Bunnyshell](https://www.bunnyshell.com/staging-management/)** | ~$10M–$15M Valuation (~$10M Funded) / ~$3M ARR | Self-service staging and preview environments with auto-sleep functionality reducing idle infrastructure spend by 40–60%. | **Startup Plan**: $0.007 per active environment minute (~$0.42/active hour, $0/month idle cost); Scaleup/Enterprise quotes for teams >20 users. | **Free Trial**: 14-day fully featured free trial with unlimited users and no credit card required; free Starter tier includes 5 ephemeral environments. |
| **[Uffizzi](https://www.uffizzi.com/)** | ~$10M Valuation (~$2.8M Funded) / ~$2M ARR | Ephemeral environments and internal developer platform providing full-stack preview clusters per pull request with service and database dependencies. | **Pro Plan**: ~$9 to $20/seat/month based on infrastructure deployment model; custom for Dedicated/Enterprise. | **Starter Plan (Free Forever)**: 2 concurrent ephemeral preview environments, unlimited team member accounts, version control integration. |
| **[Shipyard](https://shipyard.build/pricing/)** | Seed-stage (~$2.3M Funded, Acquired by StackGen) / ~$1M ARR | Automated preview environments and disposable ephemeral stacks for pull requests and AI agents. | **Startup Tier**: $500/month flat rate (includes 3 concurrent Drydock environments; additional Drydocks at $100/month). | **Free Trial**: 30-day free proof-of-concept trial with full feature and integration access (no permanent free tier). |

## Open-Source GitHub Projects

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[fakecloud](https://github.com/faiscadev/fakecloud)** | [![Stars](https://img.shields.io/github/stars/faiscadev/fakecloud?style=social&color=white)](https://github.com/faiscadev/fakecloud/stargazers) | **The AGPL-licensed migration target for LocalStack Community users.** Single binary, **no account, no auth token, no paid tier**. Covers services teams relied on LocalStack Community for, plus RDS, ElastiCache, Cognito User Pools, SES v2, and API Gateway v2 (which moved to LocalStack Pro). **~300ms startup vs ~3s for LocalStack**; ~30 MiB idle memory vs ~150 MiB. **Commercial use free** under AGPL-3.0 [citation:4]. |
| **[Floci](https://github.com/topics/aws-emulator)** | — | **MIT-licensed AWS emulator, no authentication required.** Free Cognito (which is Pro-only on LocalStack). **Startup measured at 0.012–0.016 seconds**. Newer project (started February 2026, ~1,200 stars as of March 2026)—edge-case compatibility unknown, but functional for CI/CD and commercial local development [citation:15]. |

### Additional Strong Open-Source Options

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[AWS Innovation Sandbox](https://github.com/aws-samples/aws-innovation-sandbox)** | — | AWS solution for provisioning isolated, self-contained environments for evaluating AWS services and third-party applications. Designed for security professionals and infrastructure teams building proof-of-concepts [citation:11]. |

**Frameworks for building custom systems**: For **AWS emulation** (the most common sandbox need), choose **fakecloud** for AGPL-licensed commercial freedom with a single binary and fast startup, or **Floci** for MIT-licensed Cognito support. For **ephemeral PR environments**, **Okteto** (free for 5 users) provides Kubernetes-native previews, while **Release.com** (100 free hours/month) and **Bunnyshell** (5 free environments) offer hosted alternatives. For **Salesforce-specific sandboxes**, Scratch Orgs at $25/org/month provide disposable CLI-driven environments, while **Zoho CRM Developer Edition** is genuinely free for testing.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Sandbox environments often contain production-like data or credentials; enforce strict data anonymization (Salesforce Data Mask & Seed costs 10% of net spend [citation:12]), network isolation, and automatic teardown policies.
- **Free tier terms change without notice.** Vercel's Hobby plan tightened deployment retention in October 2026—old deployments beyond 10GB are deleted immediately, and only the last 3 production deployments are kept per project (down from 10) [citation:5]. **LocalStack Community Edition is no longer free for commercial use**—the March 2026 change requires an auth token, and fakecloud is the recommended open-source migration path [citation:4]. **Salesforce sandbox costs scale with net spend**—Full Copy at 30% of net spend can become expensive for large orgs [citation:1]. Always validate current terms against vendor pages before committing.

---

**Made for developers, platform engineers, QA teams, and organizations building safe testing infrastructure.**  
Let's make developer sandboxes and testing environments more open, ephemeral, and cost-predictable.
