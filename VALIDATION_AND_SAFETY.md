# Validation, Risk and Safety

## Current evidence
The export contains named test/debug nodes (including alert-check, research, analysis, date, and Telegram tests). This shows test instrumentation exists, but **does not demonstrate passing tests, measured accuracy, or live reliability**.

## Validation checklist
- [ ] Verify market hours and trading-date handling, including holidays and time zones.
- [ ] Check missing, stale, inconsistent, and delayed quote/indicator inputs.
- [ ] Confirm RSI/divergence calculations against a trusted independent reference.
- [ ] Test alert-state persistence, duplicates, and repeated schedule executions.
- [ ] Simulate API rate limits, timeouts, and malformed AI responses.
- [ ] Inspect AI outputs for unsupported assertions and missing source context.
- [ ] Confirm Telegram formatting and recipient configuration without exposing IDs.
- [ ] Check whether every error path fails safely and is logged.

## Security and privacy
Never commit API keys, authorization headers, personal chat IDs, account identifiers, private positions, credentials, or production webhook endpoints. A public repository must use mock values and diagrams, not a raw n8n export.

## Financial safety
This system supports research and alerting. AI output must not be treated as a verified signal, and the workflow does not establish a track record or guaranteed profitability. The human retains final control.
