# Hoppscotch Rate Limits

Hoppscotch is primarily a client-side API development tool; explicit published rate limits
for its cloud service are not publicly documented as of 2026-06-14.

The information below reflects scaffold defaults derived from the provider's plan tiers.
Confirm current limits with the Hoppscotch team or documentation before relying on these values.

## Response Headers

| Header | Description |
|---|---|
| `X-RateLimit-Limit` | Maximum requests allowed in the window |
| `X-RateLimit-Remaining` | Requests remaining in the current window |
| `X-RateLimit-Reset` | UTC timestamp when the window resets |
| `Retry-After` | Seconds to wait after being throttled |

## HTTP Status Codes

| Code | Meaning |
|---|---|
| `429 Too Many Requests` | Rate limit or monthly quota exceeded |
| `503 Service Unavailable` | Service temporarily unavailable |

## Tier Limits (Scaffold — Not Officially Published)

### Free Tier
- **Rate:** 10 requests/minute (burst up to 20)
- **Monthly quota:** 1,000 requests

### Organization / Professional Tier
- **Rate:** 100 requests/minute (burst up to 200)
- **Monthly quota:** 100,000 requests

### Enterprise Tier
- **Rate:** Negotiated (default scaffold: 1,000 requests/minute, burst 5,000)
- **Monthly quota:** Uncapped (subject to fair use)

## Policies

- **Backoff:** Clients should implement exponential backoff with jitter and honor `Retry-After`.
- **Burst:** Short bursts above steady-state are tolerated up to the documented burst ceiling.
- **Quota reset:** Monthly quotas reset at the start of each calendar month (UTC).
- **Fair use:** Enterprise tiers are still subject to fair-use throttling under sustained high load.
