# Oribrix — Construction Materials Marketplace

**Product area:** B2B marketplace, procurement, vendor operations, logistics and settlement  
**Public reference:** [oribrix.com](https://oribrix.com/)

## Product context
Oribrix is a digital marketplace designed around construction-material procurement, connecting customers with suppliers while coordinating fulfilment for products that may require different vehicle types and handling requirements.

## Problem space
Construction procurement can involve multiple suppliers, variable inventory, bulky and heavy materials, fragmented delivery coordination, and limited visibility across order fulfilment. A marketplace needs to coordinate the commercial transaction and the physical movement of goods.

## Product experience

The Oribrix ecosystem is organised around three applications:

- **Customer website and shopping experience:** public-facing discovery and procurement entry point.
- **Admin console:** internal operational workspace for marketplace administration.
- **Vendor application:** supplier-facing workspace for catalogue, inventory and order workflows.

This visual review covers the public website only. The Admin and Vendor applications are not represented in the screenshots below and will be documented separately after their screens are reviewed.

## Public website — visual walkthrough

The supplied website capture (3 pages) shows the following public-facing product story:

### 1. Brand and value proposition
The landing hero uses the message “Plan it. Order it.” and positions Oribrix around requesting quotes, choosing payment methods and keeping orders together. A scrolling category strip highlights construction materials such as cement, TMT steel, aggregates and AAC blocks.

### 2. Customer onboarding and mobile experience
The website introduces a mobile-first experience and displays a sign-in screen with phone/email options. The page describes OTP sign-in and saved site addresses as onboarding capabilities.

### 3. Product discovery
The feature walkthrough shows a material discovery experience with search and category browsing. The examples shown include cement and other construction-product categories.

### 4. Product selection and ordering
The supplied screens illustrate product details, category-level browsing and cart review. The website describes bulk pricing slabs as a way to explore quantity-based pricing.

### 5. Checkout and payments
The website presents GST invoicing and payment choices, including Razorpay or cash on delivery. These are capabilities described on the public website; this visual review does not independently verify payment processing or tax calculations in a live transaction.

### 6. Orders and site-level context
The page shows order history, repeat ordering, scheduled delivery and saved site addresses. The messaging focuses on managing procurement around construction projects and delivery locations.

## Product scope documented

- Customer journey for browsing products, requesting quotes, placing orders, and tracking fulfilment.
- Vendor workflows for catalogue, pricing, stock visibility, and order acceptance.
- Admin operations for order oversight, pricing decisions, settlement, refunds, and exception handling.
- Logistics coordination, including shipment creation, tracking events, vehicle details, ETA, and proof of delivery.
- Commercial rules covering vendor base price, platform commission, shipping, GST treatment, and settlement.

## Key product and operational considerations

1. Separate product price, platform commission, applicable taxes, and transport charges so customer payable and vendor settlement are transparent.
2. Support shipment selection based on consignment characteristics; standard parcel flows may not suit every heavy or oversized item.
3. Consolidate fulfilment where operationally feasible while preserving item-level vendor and shipment traceability.
4. Define settlement and refund states so finance operations can reconcile pending payouts, completed settlements, vendor recoveries, and customer refunds.
5. Treat stock synchronisation with vendor systems as a controlled integration with clear ownership of inventory records.

## Delivery approach

A practical delivery sequence is discovery and commercial-rule validation, customer/vendor/admin journey mapping, integration and data-contract definition, incremental implementation, end-to-end order testing, settlement reconciliation, logistics exception testing, and operational handover.

## Evidence and status

The public website and the supplied three-page website capture were reviewed for this case study. The visual walkthrough describes what is presented on the public website; it does not independently certify every integration, feature, financial rule, shipment workflow, production release, or business outcome.

**Screenshot asset status:** the supplied PDF has been reviewed, but standalone image files have not yet been committed to the public GitHub repository. This case study therefore records the visual walkthrough in text pending approved image assets. No screenshots from the Admin or Vendor applications are included.

## Confidentiality

Detailed source code, internal specifications, credentials, vendor data, customer records, and operational records remain in private project workspaces. Only public-facing material should be used in the visual portfolio.
