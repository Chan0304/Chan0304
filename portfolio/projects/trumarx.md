# Trumarx — IP & Brand Operations Platform

> A multi-workspace platform concept and application for coordinating intellectual-property client onboarding, proposal generation, billing, filing operations, and client communication.

## Executive summary

Trumarx brings client-facing and internal workflows for an IP and brand-services practice into one application. The source archives supplied for review contain a shared application foundation with client onboarding and account views, internal lead and matter coordination, proposal and quotation tools, invoice and payment screens, pre-filing and DSC workflows, approvals, tasks, deadlines, communications, and reporting.

The three supplied ZIPs are closely related snapshots of the same application, not three independent products. The Admin Workspace and Client Portal archives share the same core route and feature structure. The Class Generator & Quick Quote archive includes the additional staff-facing `/staff/quick-quote` workspace and related pricing, calculation, and proposal handoff logic.

This case study describes the product and delivery evidence in the supplied source. It does not claim that every screen is connected to production services or that the complete operating lifecycle is production-ready.

## Problem and product goal

IP and brand-services work can span multiple handoffs: enquiry and lead qualification, client and applicant information, service selection, quotation and proposal, invoice and payment, document collection, filing preparation, DSC-related processing, status updates, and ongoing client communication.

The product goal is to create a more traceable workflow across these stages, reduce repeated data entry, make client document requirements visible, and give internal teams a common operational view.

## User groups

- **Prospective and existing clients:** submit applicant and business details, review their account or brand information, and respond to document requests.
- **Sales and client-facing staff:** qualify enquiries, prepare class-based quotations, and initiate proposal drafts.
- **Operations and filing teams:** coordinate clients, matters, pre-filing tasks, deadlines, approvals, and supporting records.
- **Management and authorised approvers:** review controlled records, approvals, activity, and operational reporting.

Exact production roles and access assignments remain subject to the organisation's approval process.

## Product areas evidenced in the source

### 1. Client onboarding and portal
- Multi-step IP application form with applicant, company, contact, entity, service, business, and document-availability information.
- Review-and-submit experience with validation and inline error handling.
- Document request and upload presentation, including Requested, Uploaded, and Accepted states.
- Client dashboard with application summary, process pipeline, document cards, team/activity areas, and account portfolio or brand views.
- Responsive checks recorded across phone, tablet, and desktop widths.

**Boundary:** the roadmap records that parts of the client form and dashboard use browser-local sample state. Cross-device sharing and real email-code delivery were not verified in the documented checks.

### 2. Lead, client, and matter coordination
- Lead board and searchable client/people records.
- Client and company details with matter-draft creation.
- Separate handling for existing-client matters rather than automatically creating a new lead.
- A newer Cloud operations foundation introduces authenticated staff access, role checks, linked client/matter records, and insert audit events.

**Boundary:** the documented Cloud foundation supports a limited set of saved client and matter-draft operations. It does not replace every legacy browser-based workflow.

### 3. Proposal and service quotation
- Proposal editor with client and service selection, class descriptions, fee lines, discounts, validity, scope, and terms.
- Shared A4 proposal document and PDF preview/export.
- Saved proposal snapshots and version-oriented data structures in the newer implementation.
- Source workbook mapping for proposal fields and service data, including a preserved set of 65 original MASTER references.
- Agreement selection and draft appendices for supported service templates.

**Boundary:** the source notes identify remaining workbook formula, tax, legal wording, and historical-data reconciliation. Exact workbook layout and complete formula parity are not claimed.

### 4. Class Generator & Quick Quote
- Dedicated staff route at `/staff/quick-quote`.
- Four-step sales flow, service and subtype selection, manual Nice class review, fee calculation, and live quote presentation.
- AI-assisted class suggestion integration in the code.
- Quote history, pricing controls, audit-oriented data structures, and proposal-draft handoff logic.

**Boundary:** live AI behaviour, authorised pricing administration, saved quote reload, PDF acceptance, and end-to-end proposal transfer still require verification with an appropriately authorised staff account and approved pricing configuration.

### 5. Billing, approvals, and payment operations
- Invoice creation and billing ledger screens.
- Proforma invoice presentation and document preview.
- Payment and collection views, approval panels, and payment-gate concepts.
- DSC fee and payment management screens with supporting approval and audit-oriented controls.

**Boundary:** the project records explicitly distinguish demonstrations and prototype stores from verified operational payment, approval, signing, or delivery evidence. Do not treat a displayed status as proof of a real payment or filing event.

### 6. Filing operations and work management
- Pre-filing and registry workflow screens.
- DSC management and fee/payment views.
- Tasks, deadlines, activity, communications, reports, report builder, integrations, settings, and audit-trail routes.

**Boundary:** the complete IP India filing, verification, DSC signing, acknowledgement, and registration lifecycle is not certified as an end-to-end production workflow in the supplied evidence.

## Delivery and technical approach

The application uses a TypeScript and React stack with TanStack Start and file-based routing. The package manifest also identifies Vite, Supabase client/auth integration, Tailwind CSS, Drizzle tooling, React Query, and PDF/document-generation libraries.

The implementation direction separates:
- client-facing presentation and onboarding,
- internal operational workspaces,
- authenticated server-side operations,
- role-based data access and database row-level security,
- proposal and quotation calculation rules,
- document snapshots and audit history.

The documented security foundation uses authenticated server functions, database roles, and row-level security for selected saved operations. Legacy local persona selection is not intended to grant access to protected Cloud records.

## Validation evidence recorded in the project

The supplied roadmap and implementation notes record:
- 73 calculation, proposal, catalogue, and phone-rule tests for the sales quick-quote workstream;
- 10 quote tests and a clean build for the quotation presentation update;
- responsive browser checks across widths from 320px to 1280px for key client and quotation journeys;
- 46 client-form rule tests covering validation, uploads, review, and local sample submission;
- 24 existing DSC tests and 7 new authenticated integration tests for the limited Cloud operations foundation;
- browser checks for selected staff and client flows, including access-denial and persistence checks for the new foundation.

These are project-recorded results from the supplied documentation; they were not re-executed as part of this ZIP review.

## Current delivery status

**Status: substantial prototype and partial operational foundation; full production readiness not established.**

The source shows meaningful implementation across the application, and selected calculations, responsive flows, and access controls have documented tests. However, the project notes also identify incomplete integrations, legacy browser-local stores, pending authorised staff setup, outstanding source-workbook and legal/tax reconciliation, and the need for full-system acceptance, backup/restore exercises, and operational cutover.

## Product-management considerations

- Maintain a clear distinction between demo data, browser-local state, and authenticated persisted records.
- Define role ownership and approval authority before enabling real client, financial, or filing operations.
- Reconcile source workbooks and approved legal/commercial terms before treating pricing and proposal outputs as authoritative.
- Establish a controlled document lifecycle with consent, access, retention, and audit requirements.
- Validate every external integration and status transition with real end-to-end evidence.
- Use staged release gates for onboarding, proposals, billing, filing, DSC, and client communications.

## Confidentiality and evidence boundaries

This public summary intentionally excludes source code, environment files, database credentials, client records, client logos, internal workbooks, and private operational details. No customer names, financial metrics, adoption figures, or client acceptance claims are included.

The source archives contain environment configuration files. They were not inspected or reproduced in this public case study. Keep these files out of source control and rotate any credentials that may have been exposed.

## Related project materials

The original application source remains private. This page is a documentation-only case study and does not provide a public source-code mirror.
