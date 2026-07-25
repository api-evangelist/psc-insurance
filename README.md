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

The first machine-facing surface confirmed live is an Auth0 custom-domain OpenID Connect identity endpoint at `login.pscinsurance.com.au`, whose discovery document, JWKS and OAuth authorization-server metadata all return **HTTP 200** anonymously. That is a login wall for a client/broker portal — an authentication boundary, not a developer portal. Its advertised scopes and grant types are Auth0 tenant defaults, not documented PSC API scopes.

## Content Lake (found 2026-07-25)

The marketing site is a Next.js front end over a **Sanity Content Lake** dataset — project `tw8a70my`, dataset `production` — configured for public read. The GROQ query endpoint, single-document endpoint, full NDJSON dataset export and Server-Sent Events mutation stream all return **HTTP 200** to an anonymous request; only the mutate path (405 on GET) and project administration (401) are gated. Live introspection yields the real content model: 11 document types, 84 pages, 86 blog articles, 34 office locations, 819 image assets, 108 file assets, and a `website` discriminator showing the dataset also serves WorkRisk IQ.

This is standard headless-CMS configuration rather than a deliberate API, PSC documents it nowhere, and it carries **marketing content only** — no policy, quote, claim, client or premium entity exists in it. Sanity's GraphQL API is not deployed for this project, so there is still no GraphQL surface.

## Artifacts

| Artifact | File |
|---|---|
| Well-known index | [`well-known/psc-insurance-well-known.yml`](well-known/psc-insurance-well-known.yml) |
| security.txt (verbatim) | [`well-known/psc-insurance-security.txt`](well-known/psc-insurance-security.txt) |
| OIDC discovery (verbatim) | [`well-known/psc-insurance-openid-configuration.json`](well-known/psc-insurance-openid-configuration.json) |
| OAuth AS metadata (verbatim) | [`well-known/psc-insurance-oauth-authorization-server.json`](well-known/psc-insurance-oauth-authorization-server.json) |
| JWKS (verbatim) | [`well-known/psc-insurance-jwks.json`](well-known/psc-insurance-jwks.json) |
| Authentication profile | [`authentication/psc-insurance-authentication.yml`](authentication/psc-insurance-authentication.yml) |
| OAuth scopes | [`scopes/psc-insurance-scopes.yml`](scopes/psc-insurance-scopes.yml) |
| Conformance + regulatory posture | [`conformance/psc-insurance-conformance.yml`](conformance/psc-insurance-conformance.yml) |
| API conventions | [`conventions/psc-insurance-conventions.yml`](conventions/psc-insurance-conventions.yml) |
| Data model | [`data-model/psc-insurance-data-model.yml`](data-model/psc-insurance-data-model.yml) |
| AsyncAPI (content mutation stream) | [`asyncapi/psc-insurance-content-lake-asyncapi.yml`](asyncapi/psc-insurance-content-lake-asyncapi.yml) |
| Lifecycle | [`lifecycle/psc-insurance-lifecycle.yml`](lifecycle/psc-insurance-lifecycle.yml) |
| Domain security | [`security/psc-insurance-domain-security.yml`](security/psc-insurance-domain-security.yml) |
| Vulnerability disclosure | [`security/psc-insurance-vulnerability-disclosure.yml`](security/psc-insurance-vulnerability-disclosure.yml) |
| llms.txt | [`llms/psc-insurance-llms.txt`](llms/psc-insurance-llms.txt) |

Not emitted, because they genuinely do not exist: `openapi/`, `graphql/`, `packages/`, `mcp/`, `skills/`, `cli/`, `sandbox/`, `changelog/`, `components/`, `errors/`, `overlays/`, `grpc/`.

## Compliance posture

PSC publishes no security certifications (no SOC 2, ISO 27001 or trust centre), but it does publish a substantial Australian financial-services regulatory posture at [industry memberships](https://www.pscinsurance.com.au/industry-memberships/): NIBA membership, AFCA membership, the Insurance Brokers Code of Practice, BrokersLink, and six named AFSL licences (305491, 342385, 247417, 234421, 234502, 239041). The [privacy statement](https://www.pscinsurance.com.au/privacy-statement/) names the Privacy Act 1988 (Cth) and the Australian Privacy Principles.

## Corporate note

The former corporate group domain `pscinsurancegroup.com.au` returns **HTTP 301** to [https://www.envest.com.au/](https://www.envest.com.au/), and the broking site's `security.txt` names an `@envest.com.au` contact — reflecting the business sitting inside the Ardonagh-owned Envest platform in Australia.

## Market seam

Australia has the legal machinery for open insurance and no live obligation. APRA handles prudential supervision, and the Consumer Data Right that already opened banking and energy was designated to extend to general insurance and then deferred and de-prioritized. No forcing function ever reached brokers, so integration at this tier remains partner-gated and mediated through broker platforms and insurer relationships.

## Links

- [Website](https://www.pscinsurance.com.au/)
- [PSC Broking (New Zealand)](https://www.pscbroking.co.nz/)
- [Insights / blog](https://www.pscinsurance.com.au/insights/)
- [LinkedIn](https://www.linkedin.com/company/psc-insurance-brokers/)
- [Contact](https://www.pscinsurance.com.au/contact-us/)
- [Complaints](https://www.pscinsurance.com.au/complaints/)
- [Industry memberships](https://www.pscinsurance.com.au/industry-memberships/)
- [Financial Services Guide](https://www.pscinsurance.com.au/financial-services-guide/)
- [Privacy statement](https://www.pscinsurance.com.au/privacy-statement/)
- [Terms of use](https://www.pscinsurance.com.au/terms-of-use-statement/)
- [Review](review.yml)
