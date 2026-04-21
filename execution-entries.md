---
title: "Execution Entries"
description: "Review transport execution statuses, proof-of-delivery data, pictures, and attachments."
---

# Execution Entries

Use **Execution Entries** to review status events and proof-of-delivery facts for a Transport Order.

Execution entries can come from:

- manual user updates,
- proof-of-delivery workflows,
- telematics synchronization,
- API integrations.

![Execution Entries page](resources/execution-entries/screenshot-execution-entries.png)

## What an entry can show

An execution entry can include:

- status,
- date and time,
- route stop or request reference,
- driver or vehicle context,
- comments,
- pictures,
- attachments,
- provider or API-originated data.

## Open execution entries

1. Open a [Transport Order](transportorder.md) or [Posted Transport Order](posted-transport-orders.md).
2. Choose **Execution Entries**.
3. Review the event list.
4. Open attachments or pictures when available.

## Attachments and pictures

Use attachments for evidence such as:

- proof-of-delivery image,
- signed document,
- damage photo,
- delivery note scan.

Integration accounts can also use the API attachment endpoints to upload or download execution-entry attachments. See [API](api.md).

## Status setup

Execution statuses use the status model selected in **Transport Execution Status Profile** in [TMS Setup](setup.md).

For status setup, see [Statuses and Status Profiles](statuses.md).

## Good to know

- Execution entries help dispatchers answer “what happened?” after a delivery event.
- Telematics providers may update execution facts when the provider supports the data.
- Attachments should not contain unnecessary personal data.

## Related

- [Transport Order](transportorder.md)
- [Posted Transport Orders](posted-transport-orders.md)
- [Telematics](telematics.md)
- [Statuses and Status Profiles](statuses.md)
- [API](api.md)
