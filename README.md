# CAVA

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
