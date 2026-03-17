# LabelSync Monitor

> Gives IT admins and compliance teams real-time alerting and audit-ready reports on Microsoft Purview sensitivity label policy sync status — so they never fly blind after a policy change.

## Overview

LabelSync Monitor is a PowerShell module paired with a lightweight scheduled task that continuously polls the Microsoft Purview API for sensitivity label publishing policy sync status and fires alerts via Teams, email, or webhook when propagation completes, stalls, or fails. It generates timestamped audit logs and PDF/HTML compliance reports proving when a policy change was confirmed as synced — critical evidence for regulated industries. An optional SaaS dashboard tier aggregates sync telemetry across multiple tenants for MSPs managing multiple clients.

## Problem This Solves

After modifying a sensitivity label publishing policy, admins have no reliable way to confirm propagation completed — leading to compliance gaps, support tickets, and audit failures when labels silently fail to reach users in time-sensitive regulatory scenarios

## Target Audience

IT admins and compliance officers in regulated industries (finance, healthcare, legal) managing Microsoft Purview at 500+ user scale, and MSPs managing multiple M365 tenants

## Tech Stack

PowerShell, Microsoft Graph API, Next.js, Node.js, SQLite, Lemon Squeezy API

## Installation

```powershell
# Clone the repository
git clone https://github.com/labelsync-monitor.git
cd labelsync-monitor

# Review the script before running
Get-Content scripts/labelsync-monitor.ps1

# Run with appropriate permissions
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
.\scripts\{labelsync-monitor}.ps1
```

## Usage

Poll the Microsoft Purview / Security & Compliance PowerShell API for sensitivity label publishing policy sync status on a configurable interval and send a Teams or email alert when a policy transitions to synced, pending, or error state, while appending a timestamped entry to a local audit log CSV for compliance reporting.

## Monetization Strategy

Tiered model: (1) Core PowerShell module sold on Gumroad for $29 one-time — single tenant, alerting + basic reports; (2) Pro license at $79 one-time — multi-tenant support + compliance PDF exports; (3) MSP SaaS dashboard at $19/tenant/month on a self-hosted or Vercel-hosted app, sold via Lemon Squeezy subscription. Upsell consulting engagement for deployment and custom alert integration at $150/hr.

| Metric | Value |
|--------|-------|
| Revenue Potential | HIGH |
| Estimated Effort  | 1-3months |

## Contributing

1. Fork this repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'feat: add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

MIT License — see [LICENSE](LICENSE) for details.

---

*Generated from the article: [Microsoft Purview: How to Monitor Sensitivity Label Policy Sync Status in the Purview Portal](http://localhost/msendpoint/articles/microsoft-purview-how-to-monitor-sensitivity-label-policy-sync-status-in-the-purview-portal) on 2026-03-17*
*Blog: [MSEndpoint.com](https://msendpoint.com)*