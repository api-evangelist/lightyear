# Lightyear

Lightyear is a European retail investing platform founded by former Wise (TransferWise) employees Martin Sokk and Mihkel Aamer, offering commission-light access to roughly 6,000 stocks, ETFs, money market funds, bonds and crypto, plus interest-bearing cash "Vaults" managed with BlackRock and J.P. Morgan money market funds. Lightyear UK Ltd is authorised by the UK Financial Conduct Authority (FRN 987226) and Lightyear Europe AS is regulated by the Estonian Financial Supervision Authority, with operations in London and Tallinn.

Website: https://lightyear.com — Status: https://status.lightyear.com/ — Backed by: 500-global, lightspeed-venture-partners

## API surface

Lightyear publishes **no public developer API**, developer portal, API documentation or SDKs. `api.lightyear.com` serves the first-party mobile and web apps and returns HTTP 403 from the edge for every path except its `/.well-known/` documents — one of which is a real RFC 8414 OAuth 2.0 authorization server metadata document advertising an `mcp` scope for an internal MCP integration (captured in `well-known/`, `authentication/`, `scopes/` and `mcp/`).

## Artifacts

| Dir | File | Method |
|---|---|---|
| `well-known/` | `lightyear-well-known.yml`, `lightyear-oauth-authorization-server.json` | searched |
| `authentication/` | `lightyear-authentication.yml` | searched |
| `scopes/` | `lightyear-scopes.yml` | searched |
| `mcp/` | `lightyear-mcp.yml` (status: not-public) | searched |
| `lifecycle/` | `lightyear-lifecycle.yml` | searched |
| `changelog/` | `lightyear-changelog.yml` | searched |
| `conformance/` | `lightyear-conformance.yml` | searched |
| `security/` | `lightyear-domain-security.yml` | probed |
| `llms/` | `lightyear-llms.txt` | generated |

> Identity note: the originating VC-portfolio stub carried `https://lightyear.io`, which does not resolve to a Lightyear property (parked on Netlify, certificate mismatch, HTTP 404 as of 2026-07-19). The company was re-identified as lightyear.com (formerly golightyear.com; the Android package is still `com.golightyear.mobile`), whose About page names Lightspeed Venture Partners as an investor — matching the portfolio signal.
