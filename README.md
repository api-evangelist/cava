# CAVA

CAVA Group, Inc. (NYSE: CAVA) is a Washington, D.C.-headquartered Mediterranean fast-casual restaurant
company operating the CAVA brand — customizable bowls, pitas, salads and sides built on house-made dips,
spreads and dressings — alongside a grocery CPG line, digital ordering and delivery, catering, and the
CAVA Rewards loyalty program delivered through its iOS and Android apps.

- Website: https://cava.com/
- Support: https://support.cava.com/
- Careers: https://cava.com/careers
- Investors: https://investor.cava.com/overview/default.aspx
- GitHub: https://github.com/cavagrill

## API surface

CAVA publishes **no public developer program, API documentation, or machine-readable API contract.**
Contract discovery was run against `cava.com`, `catering.cava.com`, `investor.cava.com` and
`cavacatering.com` — OpenAPI/Swagger paths, GraphQL, MCP `tools/list`, and both A2A agent-card
well-known paths all missed. No agent card was found, so none is recorded.

What CAVA *does* publish machine-readably, and what this repo captures:

| Artifact | Method | Source |
|---|---|---|
| `well-known/cava-security.txt` | searched | https://cava.com/.well-known/security.txt (RFC 9116) |
| `well-known/cava-well-known.yml` | searched | full `/.well-known/` probe index across four hosts |
| `llms/cava-llms.txt` | searched | https://cava.com/llms.txt (verbatim) |
| `security/cava-domain-security.yml` | probed | TLS/HSTS/DNSSEC/CAA/SPF/DMARC |
| `security/cava-vulnerability-disclosure.yml` | searched | security.txt `Contact:` |

> Probe note: the `cava.com` edge (Cloudflare in front of CloudFront/S3) answers HTTP/2 requests with a
> 403 challenge. All probes above were made over **HTTP/1.1**. Unpublished `/.well-known/*` keys return a
> 403 `application/xml` AccessDenied from the origin bucket rather than a 404.
