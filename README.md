# Kenjo (kenjo)

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
