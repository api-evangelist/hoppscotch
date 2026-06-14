# Hoppscotch FinOps

This document provides FinOps guidance for managing costs when using Hoppscotch's
cloud-hosted Organization or Enterprise plans.

## Billing Model

| Attribute | Value |
|---|---|
| Pricing category | Seat-based (per user/month) |
| Billing frequency | Monthly or Annual |
| Billing currency | USD |
| Overage model | Not publicly defined |

## Plan Cost Summary

| Plan | Price | Notes |
|---|---|---|
| Free | $0 | Unlimited users, community support only |
| Organization | $6/user/month (annual) | ~$72/user/year; monthly rate higher |
| Enterprise | Custom | Contact sales for volume/self-host pricing |

## Cost Optimization Strategies

### Right-size Seat Count
- Audit active users quarterly; remove inactive seats before renewal.
- Use the Admin Dashboard (Organization+) to identify low-activity accounts.

### Annual vs Monthly Billing
- Annual billing provides approximately 25% savings over monthly.
- Commit annually only when headcount is stable.

### Self-Hosted Deployment
- Hoppscotch is open source; self-hosting eliminates per-seat SaaS fees.
- Weigh infrastructure and maintenance costs against SaaS subscription cost.
- Enterprise self-host includes support and SLA; evaluate TCO accordingly.

## Unit Economics

| Metric | Formula |
|---|---|
| Cost per developer | total_seats × seat_price / active_developers |
| Cost per API test run | total_spend / monthly_test_executions |

## Notes

- Hoppscotch does not publish metered (per-request) pricing for its cloud service.
- On-premises/self-hosted deployments incur infrastructure costs outside of licensing.
- Monitor usage via the Admin Dashboard to optimize seat utilization.

Source: https://hoppscotch.com/pricing
