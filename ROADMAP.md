# Product Roadmap

## Present in the exported design
- Scheduled/manual monitoring triggers.
- Multi-source market-data retrieval and technical-indicator processing.
- Stateful alert evaluation via n8n Data Tables.
- Two-stage Perplexity-assisted research/analysis.
- Telegram alert formatting and sending.
- Dedicated test/debug nodes.

## Proposed next improvements (not claimed as implemented)
1. Add structured event logs and per-stage latency/error metrics.
2. Create repeatable test fixtures for price/indicator edge cases.
3. Introduce a consistent confidence and evidence format for AI outputs.
4. Measure alert precision, duplication rate, and user usefulness.
5. Improve rate-limit handling, retries, and failure notifications.
6. Add versioned release notes and a lightweight decision log.

## Product success metrics to define and measure
- False/duplicate alert rate.
- Percentage of alerts with valid and sufficiently recent source data.
- Median workflow completion time.
- Human-rated usefulness of research summaries.

No metric results are asserted here without supporting measurements.
