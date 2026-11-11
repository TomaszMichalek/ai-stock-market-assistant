# Product Requirements Document (PRD)

## Product
AI-Powered Stock Market Assistant — personal research and alerting workflow.

## Problem statement
Manual monitoring across multiple tickers and market indicators creates fragmented context and repetitive work. The user needs concise, timely signals with traceable context while retaining full control of investment decisions.

## Target user
An individual investor monitoring selected US-listed securities. This is a personal-use product concept, not a commercial trading platform.

## Goals
1. Reduce repetitive data collection and indicator review.
2. Identify candidates for further investigation using explicit conditions.
3. Add AI-assisted context without replacing deterministic checks.
4. Deliver actionable, readable notifications to Telegram.
5. Maintain state to support alert evaluation across runs.

## Functional requirements (evidenced in the exported workflow)
- **FR-01** Start via a schedule or manual trigger.
- **FR-02** Maintain a configured list of monitored tickers.
- **FR-03** Retrieve market status, quotes, and market indicators.
- **FR-04** Merge data sources and apply market/alert logic.
- **FR-05** Retrieve and update state using n8n Data Tables.
- **FR-06** Use research and analysis calls to Perplexity API.
- **FR-07** Calculate/handle 15-minute RSI and divergence data.
- **FR-08** Format and send qualifying messages through Telegram.

## Non-functional requirements / product expectations
- **Traceability:** distinguish source market data, deterministic calculations, and AI interpretation.
- **Resilience:** handle API errors, stale/missing fields, and rate limits.
- **Security:** keep API secrets and private identifiers out of public artifacts.
- **Human oversight:** no automated order placement without explicit separate design and approval.

## Acceptance criteria to verify in a live environment
1. Scheduled runs execute only in intended market conditions.
2. Missing or invalid source data do not create misleading alerts.
3. Repeat runs respect intended alert-state behavior.
4. AI-generated claims can be checked against cited or source data.
5. Telegram messages are legible and contain sufficient context.
6. Errors are observable and recoverable.

These are **verification targets**, not claims that all tests have passed.

## Out of scope
Automated brokerage execution, portfolio custody, guaranteed returns, investment recommendations for other users, and independently audited model performance.
