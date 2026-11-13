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
- [SaaS/Hosted Platforms](#saas-products)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

| Product | Description | Pricing (Starting) | Free Tier / Trial Limits |
|---------|-------------|-------------------|--------------------------|
| **[Salesforce Sandboxes](https://www.salesforce.com/platform/sandboxes-environments/pricing/)** | Four sandbox types: **Developer** (metadata only, included with CRM licenses), **Developer Pro** (collaborative, 5% of net spend), **Partial Copy** (sample data, 20% of net spend), **Full Copy** (complete replica, 30% of net spend). **Scratch Orgs** available at $25/org/month—source-driven, CLI-accessible, disposable environments [citation:1][citation:12]. | Developer: included; Developer Pro: 5% of net spend; Partial Copy: 20%; Full Copy: 30%; Scratch Org: $25/org/month | **Developer Sandbox**: included with CRM licenses; **Scratch Org**: $25/org/month (no free tier) |
| **[Zoho CRM Developer Edition](https://www.zoho.com.cn/crm/developer/developer-edition.html)** | Free, full-featured development environment for Zoho CRM. Provides access to all highest-tier features for testing customizations, Deluge functions, and automation workflows. Invited developers work in an isolated sandbox without access to production data [citation:2]. | **Free** | **Free forever**: full-featured developer account with specific limits (intended for practice and testing, not production) |
| **[Okteto](https://www.okteto.com/pricing/)** | Kubernetes development environments with preview environments for PRs. **Starter tier free for up to 5 users**—run as many development, preview, and agent environments as needed. Pay per user, never per environment [citation:6]. | Starter: **Free** (up to 5 users); Scale/Enterprise: per-user pricing | **Free (Starter)**: up to 5 users, unlimited environments, no credit card required |
| **[Release.com](https://releasehub.webflow.io/pricing)** | Ephemeral environments for development, QA, and demos. **Free tier includes 100 pre-production environment hours per month**. Runs in your cloud; automatic environment creation with every code commit [citation:7]. | Free: **$0** (100 hours/month); Pay-as-you-go available | **Free**: 100 pre-production environment hours/month, no cloud or credit card required |
| **[Bunnyshell](https://www.bunnyshell.com/staging-management/)** | Self-service staging environments with auto-sleep to cut cloud spend 40–60%. **Free tier includes 5 environments**. Stopped/sleeping environments cost $0 [citation:8]. | Free: **$0** (5 environments); Paid tiers available | **Free**: 5 environments, no credit card required, white-glove onboarding |
| **[Uffizzi](https://www.uffizzi.com/)** | Ephemeral environments for full-stack applications. **Both Personal and Team tiers are completely free** as of September 2026 verification. Creates preview environments per PR with database and service dependencies [citation:10]. | **Free** (Personal and Team tiers) | **Free forever**: Personal and Team tiers both free, no subscription required |
| **[Shipyard](https://shipyard.build/pricing/)** | Ephemeral environments platform. **Startup tier: $500/month** with a 30-day free trial for proof-of-concept. No free tier listed [citation:9]. | Startup: **$500/month**; Business: custom | **30-day free trial** (technical proof-of-concept) |
| **[LocalStack](https://localstack.cloud/)** | Local AWS cloud emulator. **Critical: Community Edition replaced by proprietary image in March 2026**—requires account and auth token. **Commercial use not allowed on free tier**; paid plans required for commercial use [citation:4]. | Base: **$39/month** (commercial); Pro: higher tiers | **Hobby (non-commercial)**: 30+ services; **Commercial use requires paid plan** [citation:15] |

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
