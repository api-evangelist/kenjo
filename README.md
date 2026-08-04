# Kenjo (kenjo)

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

Kenjo is an all-in-one human resources (HRIS) software platform for small and mid-sized companies, with a particular focus on deskless and shift-based teams. It covers the full employee lifecycle: employee database, attendance and time tracking, absence and time-off management, document management, payroll and compensation, shift planning, performance reviews, and recruiting. Kenjo is based in Germany and Spain and serves 1,000+ companies.

Kenjo exposes a documented REST API for reading and writing HR data. **Access is gated:** the API is available on Kenjo's top-tier **Connect** plan and must first be activated for your account (sandbox or production) by the Kenjo Customer Success team. You then generate an API key in the Kenjo web app under **Settings > Integrations > API**, exchange it for a bearer token via `POST /auth/login`, and send that token in the `Authorization` header on every request.

- **Production base URL:** `https://api.kenjo.io/api/v1`
- **Sandbox base URL:** `https://sandbox-api.kenjo.io/api/v1`
- **Authentication:** Bearer token (API key exchanged via `POST /auth/login`)
- **API reference:** [https://kenjo.readme.io/reference](https://kenjo.readme.io/reference)

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/kenjo/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/kenjo/refs/heads/main/apis.yml)

## Tags

- Human Resources
- HRIS
- Employee Management
- HR Software
- Time Tracking
- Absence Management
- Payroll
- Recruiting

## Timestamps

- **Created:** 2026-07-11
- **Modified:** 2026-07-11

## APIs

### Kenjo Employees API

Create, list, and read employees and update their profile sections - account, personal, work, work schedule, address, financial, home, and emergency contact - plus activate and deactivate employees. New employees are created deactivated by default. The core HRIS surface for keeping an external system of record in sync with Kenjo.

- **API Reference:** [https://kenjo.readme.io/reference/post_employees](https://kenjo.readme.io/reference/post_employees)
- **Base URL:** `https://api.kenjo.io/api/v1`

### Kenjo Attendance API

Record and manage attendance and time tracking - create, retrieve, update, and delete attendance entries, track a clock-in/clock-out by user email or external id, list attendance categories, and return expected working time per user for a date range. Built for deskless and shift-based workforce time capture.

- **API Reference:** [https://kenjo.readme.io/reference/post_attendances](https://kenjo.readme.io/reference/post_attendances)
- **Base URL:** `https://api.kenjo.io/api/v1`

### Kenjo Time Off and Absences API

Manage absences and time off - create time-off requests, create pre-approved (processed) requests, list requests, list time-off types and statuses, and set an employee's balance for a given time-off type.

- **API Reference:** [https://kenjo.readme.io/reference/post_time-off-requests](https://kenjo.readme.io/reference/post_time-off-requests)
- **Base URL:** `https://api.kenjo.io/api/v1`

### Kenjo Documents API

Return a paginated list of company documents stored in Kenjo.

- **API Reference:** [https://kenjo.readme.io/reference/get_documents-company](https://kenjo.readme.io/reference/get_documents-company)
- **Base URL:** `https://api.kenjo.io/api/v1`

### Kenjo Compensation and Payroll API

Read compensation and payroll-adjacent data - contracts, contract types, salaries, additional payments, and additional payment types - to feed payroll runs and compensation reporting.

- **API Reference:** [https://kenjo.readme.io/reference/get_compensation-contracts](https://kenjo.readme.io/reference/get_compensation-contracts)
- **Base URL:** `https://api.kenjo.io/api/v1`

### Kenjo Organization API

Manage the organizational structure behind the HRIS - companies, offices, departments, teams, areas, and calendars - with full CRUD on offices, departments, teams, and areas.

- **API Reference:** [https://kenjo.readme.io/reference/get_companies](https://kenjo.readme.io/reference/get_companies)
- **Base URL:** `https://api.kenjo.io/api/v1`

### Kenjo Recruiting API

Applicant tracking surface - list public job positions, create and manage candidates and their attachments and documents, and create and update applications tying a candidate to a position. Also powers custom career sites built on top of Kenjo's public positions endpoint.

- **API Reference:** [https://kenjo.readme.io/reference/get_recruiting-positions](https://kenjo.readme.io/reference/get_recruiting-positions)
- **Base URL:** `https://api.kenjo.io/api/v1`

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/kenjohr)
- [Website](https://www.kenjo.io/)
- [Documentation](https://kenjo.readme.io/reference)
- [Support Email](mailto:support@kenjo.io)
- [Plans](plans/kenjo-plans-pricing.yml)
- [Rate Limits](rate-limits/kenjo-rate-limits.yml)
- [Fin Ops](finops/kenjo-finops.yml)
- [Blog](https://www.kenjo.io/blog)

## Access Model

The Kenjo API is not open self-service. To use it you must:

1. Be on the **Connect** plan (Kenjo's top tier; APIs and integrations are a Connect-only capability).
2. Request API activation from the Kenjo Customer Success team for your sandbox and/or production account.
3. Generate an API key in **Settings > Integrations > API** (each key needs a unique alias; copy it immediately, it is shown once).
4. Call `POST /auth/login` with the API key to obtain a bearer token, then authorize all calls with that token.

A test/sandbox environment (`https://sandbox-api.kenjo.io/api/v1`) is provided and recommended before enabling the integration against production data.

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
