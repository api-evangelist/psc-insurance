# PSC Insurance (psc-insurance)

PSC Insurance is an Australian insurance broking and intermediary group operating as PSC Insurance Brokers across every Australian state and territory, with a New Zealand arm trading as PSC Broking. It places commercial and SME risk — business packages, construction and civil contracting, public liability, cyber, professional indemnity, directors and officers, management liability, commercial property and industrial special risks, strata, motor and fleet, agribusiness and livestock, workers compensation, financial lines and trade credit, and medical and allied health cover — advising clients rather than carrying underwriting risk itself. Formerly the ASX-listed PSC Insurance Group, the business now sits inside The Ardonagh Group's Australian distribution platform.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/psc-insurance/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/psc-insurance/refs/heads/main/apis.yml)

## Tags

- Insurance
- Australia
- Broker
- Insurance Brokerage
- Property and Casualty
- Commercial Insurance
- Cyber Insurance
- Intermediary
- Partner Gated
- No Public API

## Timestamps

- **Created:** 2026-07-25
- **Modified:** 2026-07-25

## APIs

None. PSC Insurance publishes no public, self-serve API.

This is an honest, deliberate stub. Every conventional developer-portal path and subdomain was probed on 2026-07-25 and none resolved to documentation:

- `developer.`, `developers.`, `docs.` and `api.` subdomains on both `pscinsurance.com.au` and `pscinsurancegroup.com.au` do not resolve in DNS.
- `/developers`, `/developer`, `/api`, `/partners` and `/integrations` all return **HTTP 404**.
- `/openapi.json`, `/swagger.json`, `/api-docs` and `/graphql` all return **HTTP 404**.
- The public sitemap holds 104 URLs, all marketing, product and blog pages, with zero technical documentation.

No OpenAPI or Swagger definition, GraphQL schema, Postman collection, AsyncAPI document, webhook catalog or `.proto` was found. None of the four insurance API verbs — quote, bind, issue, FNOL — is exposed publicly; claims are lodged through a human-facing page and broker contact.

## ACORD posture

**No ACORD reference found.** The public estate was searched for ACORD, AL3, ACORD XML, ACORD certified and NGDS, with zero matches, and no IVANS, agency download, Applied Epic or Vertafore AMS360 reference either. The absence of any published standards posture is itself the finding.

## Auth model

The only machine-facing surface confirmed live is an Auth0 custom-domain OpenID Connect identity endpoint at `login.pscinsurance.com.au`, whose discovery document, JWKS and OAuth authorization-server metadata all return **HTTP 200** anonymously. That is a login wall for a client/broker portal — an authentication boundary, not a developer portal. Its advertised scopes and grant types are Auth0 tenant defaults, not documented PSC API scopes.

## Corporate note

The former corporate group domain `pscinsurancegroup.com.au` returns **HTTP 301** to [https://www.envest.com.au/](https://www.envest.com.au/), and the broking site's `security.txt` names an `@envest.com.au` contact — reflecting the business sitting inside the Ardonagh-owned Envest platform in Australia.

## Market seam

Australia has the legal machinery for open insurance and no live obligation. APRA handles prudential supervision, and the Consumer Data Right that already opened banking and energy was designated to extend to general insurance and then deferred and de-prioritized. No forcing function ever reached brokers, so integration at this tier remains partner-gated and mediated through broker platforms and insurer relationships.

## Links

- [Website](https://www.pscinsurance.com.au/)
- [PSC Broking (New Zealand)](https://www.pscbroking.co.nz/)
- [Blog](https://www.pscinsurance.com.au/blog/)
- [LinkedIn](https://www.linkedin.com/company/psc-insurance-brokers/)
- [Review](review.yml)
