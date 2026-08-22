# PSC Insurance (psc-insurance)

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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
