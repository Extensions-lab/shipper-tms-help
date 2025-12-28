# Posted Forwarding Order

The Posted Forwarding Order represents the historical and finalized version of a [Forwarding Order](forwardingorder.md) in the Transportation Management System (TMS) extension for Microsoft Dynamics 365 Business Central. It serves as an immutable record of a completed transportation request that has been posted or archived in the system.
The Posted Forwarding Order captures all essential transportation details including:

- the ordering party (customer/vendor/company)
- shipper and consignee information with complete address details
- transportation planning data (requested/planned/actual pickup and delivery dates)
- freight documentation (waybills, consolidation numbers)
- and financial settlement information.

It maintains a comprehensive audit trail with creation and modification timestamps, user tracking, and supports multiple posted versions of the same order through versioning.

The entity includes extensive logistics data such as weights, volumes, freight charges, carrier assignments, vehicle and driver information, and integrates with Business Central's document attachment system for supporting documentation.

As a read-only historical record, it provides complete visibility into past transportation operations while preserving the integrity of completed transactions and enabling detailed reporting and analysis of transportation performance, costs, and execution patterns. The Posted Forwarding Order is designed primarily for the Logistics Service Provider (LSP) scenario, serving as the definitive record of transportation services delivered to customers.

## Post

A Posted Forwarding Order appears only after the Forwarding Order has been posted.

The permissions—that is, when posting is allowed—are controlled by the [status system](statuses.md). For example, statuses can be used to block the posting of a Forwarding Order if customer invoices or carrier invoices related to that order have not yet been processed.

## Use cases

This table is used when a transport history for a customer/client is needed. Typically, the customer is the party paying for the transport, meaning the value is stored in Order Party No. (Order Party Name).
