# sevdesk (sevdesk)

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

sevdesk is a German cloud accounting, invoicing, and bookkeeping platform for freelancers and small businesses. Its RESTful API (base `https://my.sevdesk.de/api/v1`) exposes everything the web application does - contacts, invoices, orders, credit notes, vouchers (receipts), bank check accounts and transactions, parts (inventory), tags, plus DATEV and CSV exports.

## Access model

**Self-serve, paid SaaS.** sevdesk is a subscription product (a free trial is available). Any paying account administrator can generate an **API token** in the web app's user settings - a **32-character hexadecimal string** - with no separate application, partner program, or approval step. The token is passed as the **raw value of an `Authorization` header** (no `Bearer` prefix), for example:

```
Authorization: b7794de0085f5cd00560f160f290af38
```

Tokens have an infinite lifetime and can be regenerated (password-confirmed) to revoke a previous token. The API is included in every subscription tier at no additional charge - there is no separate API plan or per-call fee.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/sevdesk/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/sevdesk/refs/heads/main/apis.yml)

## Tags

- Accounting
- Invoicing
- Bookkeeping
- Finance
- Germany
- Vouchers
- Contacts
- SaaS
- ERP
- Financial Software

## Timestamps

- **Created:** 2026-07-12
- **Modified:** 2026-07-12

## APIs

The OpenAPI, Postman collection, and Open Collection in this repository are a grounded, representative subset authored from sevdesk's official OpenAPI specification (openapi 3.0.0, reported version 2.0.0). Paths, HTTP methods, operationIds, and the apiKey security scheme come directly from that specification; request/response body schemas are simplified. See `review.yml` for confirmed-vs-modeled detail.

### sevdesk Contacts API

Create, retrieve, update, and delete contacts - customers, suppliers, and partners - along with helpers such as the next free customer number.

- **Human URL:** [https://api.sevdesk.de/](https://api.sevdesk.de/)
- **Base URL:** `https://my.sevdesk.de/api/v1`

#### Tags

- Contacts
- Customers
- CRM

#### Properties

- [Documentation](https://api.sevdesk.de/)
- [API Reference](https://api.sevdesk.de/)
- [OpenAPI](openapi/sevdesk-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sevdesk.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sevdesk.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### sevdesk Invoices API

Create invoices with their positions via the saveInvoice factory, list and retrieve invoices, render and download the PDF, fetch e-invoice XML, send invoices by email, and drive the invoice lifecycle (book, enshrine, cancel, reset).

- **Human URL:** [https://api.sevdesk.de/](https://api.sevdesk.de/)
- **Base URL:** `https://my.sevdesk.de/api/v1`

#### Tags

- Invoices
- Billing
- PDF

#### Properties

- [Documentation](https://api.sevdesk.de/)
- [OpenAPI](openapi/sevdesk-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sevdesk.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sevdesk.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### sevdesk Orders API

Manage orders and quotations - create with positions via the saveOrder factory, list, retrieve, update, and delete, fetch positions and discounts, generate packing lists or contract notes, and send orders by email.

- **Human URL:** [https://api.sevdesk.de/](https://api.sevdesk.de/)
- **Base URL:** `https://my.sevdesk.de/api/v1`

#### Tags

- Orders
- Quotations
- Sales

#### Properties

- [Documentation](https://api.sevdesk.de/)
- [OpenAPI](openapi/sevdesk-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sevdesk.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sevdesk.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### sevdesk Credit Notes API

Issue credit notes with the saveCreditNote factory or derive them from an existing invoice or voucher, then list, retrieve, render the PDF, send by email, book, and enshrine them.

- **Human URL:** [https://api.sevdesk.de/](https://api.sevdesk.de/)
- **Base URL:** `https://my.sevdesk.de/api/v1`

#### Tags

- Credit Notes
- Refunds
- Accounting

#### Properties

- [Documentation](https://api.sevdesk.de/)
- [OpenAPI](openapi/sevdesk-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sevdesk.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sevdesk.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### sevdesk Vouchers API

Book expense and revenue vouchers (receipts) - upload the receipt file, create the voucher with positions via saveVoucher, retrieve and update vouchers, and use receipt-guidance helpers to pick the correct booking account.

- **Human URL:** [https://api.sevdesk.de/](https://api.sevdesk.de/)
- **Base URL:** `https://my.sevdesk.de/api/v1`

#### Tags

- Vouchers
- Receipts
- Bookkeeping

#### Properties

- [Documentation](https://api.sevdesk.de/)
- [OpenAPI](openapi/sevdesk-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sevdesk.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sevdesk.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### sevdesk Bank and Transactions API

Manage bank and clearing check accounts and the transactions booked against them - list and create accounts, import and create transactions, fetch account balance at a date, and enshrine transactions for audit safety.

- **Human URL:** [https://api.sevdesk.de/](https://api.sevdesk.de/)
- **Base URL:** `https://my.sevdesk.de/api/v1`

#### Tags

- Banking
- Transactions
- Reconciliation

#### Properties

- [Documentation](https://api.sevdesk.de/)
- [OpenAPI](openapi/sevdesk-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sevdesk.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sevdesk.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### sevdesk Parts API

Manage parts / articles used on invoices and orders - create, list, retrieve, and update parts, and read current stock levels for inventory-aware workflows.

- **Human URL:** [https://api.sevdesk.de/](https://api.sevdesk.de/)
- **Base URL:** `https://my.sevdesk.de/api/v1`

#### Tags

- Parts
- Inventory
- Catalog

#### Properties

- [Documentation](https://api.sevdesk.de/)
- [OpenAPI](openapi/sevdesk-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sevdesk.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sevdesk.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### sevdesk Tags API

Create tags and relate them to resources, then list, retrieve, update, and delete tags and inspect tag relations across the account.

- **Human URL:** [https://api.sevdesk.de/](https://api.sevdesk.de/)
- **Base URL:** `https://my.sevdesk.de/api/v1`

#### Tags

- Tags
- Labels
- Organization

#### Properties

- [Documentation](https://api.sevdesk.de/)
- [OpenAPI](openapi/sevdesk-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sevdesk.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sevdesk.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### sevdesk Export and Reports API

Export accounting data for the tax advisor - start DATEV CSV/XML ZIP export jobs, track progress and download, export invoices, credit notes, vouchers, transactions, and contacts as CSV/ZIP, and pull invoice, order, contact, and voucher report lists.

- **Human URL:** [https://api.sevdesk.de/](https://api.sevdesk.de/)
- **Base URL:** `https://my.sevdesk.de/api/v1`

#### Tags

- Export
- DATEV
- Reports

#### Properties

- [Documentation](https://api.sevdesk.de/)
- [OpenAPI](openapi/sevdesk-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sevdesk.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sevdesk.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Domain Security](security/sevdesk-domain-security.yml)
- [Authentication](authentication/sevdesk-authentication.yml)
- [GitHub Organization](https://github.com/sevdesk)
- [LinkedIn](https://www.linkedin.com/company/sevdesk)
- [Website](https://sevdesk.de)
- [Documentation](https://api.sevdesk.de/)
- [Plans](plans/sevdesk-plans-pricing.yml)
- [Rate Limits](rate-limits/sevdesk-rate-limits.yml)
- [Fin Ops](finops/sevdesk-finops.yml)
- [Blog](https://tech.sevdesk.com/)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
