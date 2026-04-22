---
title: "Telematics Troubleshooting"
description: "Resolve common telematics setup, dispatch, mapping, webhook, and synchronization issues."
---

# Telematics Troubleshooting

Use this page when telematics setup, dispatch publication, webhook processing, or execution synchronization does not behave as expected.

## Common issues

| Problem | What to check |
|---|---|
| Publish action fails | Provider setup is enabled, credentials are valid, carrier has setup code, route stops exist, and vehicle or driver mapping is complete |
| No vehicle location appears | Vehicle mapping exists, current positions sync is enabled, and the provider has returned a recent position |
| Dispatch is published to the wrong provider record | Review **Telematics Entity Mapping** for duplicate or stale vehicle and driver mappings |
| Webhook is not received | API URL, OAuth or provider authentication, telematics setup API permission set, and provider webhook registration |
| Inbound message is received but no execution entry appears | Check inbound message status, route or stop matching, status profile setup, and execution-entry logs |
| Sync keeps retrying | Review sync state, last error category, provider rate limits, credentials, and next poll time |
| Admin API action fails | Confirm the selected setup is the right provider, and the account has `TMAS Tel. Admin API` permission |
| Provider secret is visible in a screenshot | Rotate the secret and replace the screenshot with a masked version |

## Safe retry process

1. Fix the obvious setup or mapping issue first.
2. Retry the smallest affected sync stream or dispatch action.
3. Review the log entry created by the retry.
4. Confirm execution entries, dispatch status, or mappings changed as expected.
5. Avoid repeated full syncs until the error category is understood.

## Escalation checklist

Collect this information before escalating to support:

- telematics setup code and provider,
- Transport Order number if dispatch-related,
- vehicle and driver numbers,
- provider external IDs,
- latest telematics log entry message,
- latest sync state error category and result message,
- sanitized webhook or provider response sample.

Do not include API keys, passwords, OAuth tokens, or provider secrets in the escalation package.

## Related

- [Telematics overview](telematics-overview.md)
- [Telematics setup](telematics-setup.md)
- [Telematics provider mapping](telematics-provider-mapping.md)
- [Telematics sync and logs](telematics-sync-and-logs.md)
