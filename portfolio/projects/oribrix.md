# Oribrix — Construction Materials Marketplace

**Product area:** B2B marketplace, procurement, vendor operations, logistics and settlement  
**Public reference:** [oribrix.com](https://oribrix.com/)

## Product context
Oribrix is a digital marketplace concept designed around construction-material procurement, connecting customers with suppliers while coordinating fulfilment for products that may require different vehicle types and handling requirements.

## Problem space
Construction procurement can involve multiple suppliers, variable inventory, bulky and heavy materials, fragmented delivery coordination, and limited visibility across order fulfilment. A marketplace needs to coordinate the commercial transaction and the physical movement of goods.

## Product scope documented
- Customer journey for browsing products, placing orders, and tracking fulfilment.
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
This page summarises documented product scope and delivery considerations. It does not independently certify every integration, feature, financial rule, shipment workflow, production release, or business outcome. Public screenshots and detailed commercial examples should be added only after client approval and redaction.

## Further documentation
Detailed source code, internal specifications, credentials, vendor data, and operational records remain in private project workspaces.
