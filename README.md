# sevdesk (sevdesk)

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
