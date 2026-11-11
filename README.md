# AI-Powered Stock Market Assistant

**Product portfolio case study | n8n · market data APIs · Perplexity AI · Telegram**

A personal, experimental stock-market research and alerting workflow. This repository demonstrates how I translate a problem into product requirements, orchestrate data and AI-assisted analysis, and structure a system for iterative improvement.

> **Scope and transparency:** The source is an exported n8n workflow. The export contains 49 nodes, including test/debug nodes. The exported workflow is marked `active: false`; this repository does **not** claim verified live production operation or independently validated investment performance. No trading execution is shown in the workflow.

## The problem

Monitoring several securities requires collecting prices, checking market conditions, comparing indicators, researching context, and deciding when an alert is worth attention. Repeating those steps manually is time-consuming and inconsistent.

## Product approach

- **Automate collection:** market status, stock quotes, and Yahoo market indicators.
- **Apply deterministic logic:** evaluate market data, state, and alert conditions before escalating.
- **Enrich selectively:** request AI-supported research and analysis for candidates that pass workflow gates.
- **Keep a human in control:** deliver a research-oriented Telegram notification; the investor makes the decision.
- **Iterate:** use test and debug nodes to examine edge cases and refine alert logic.

## Workflow at a glance

![n8n workflow overview](images/workflow-overview.png)

1. Scheduled or manual trigger initiates a market-monitoring cycle.
2. Market status and configured tickers are read; quotes and indicators are fetched.
3. Data are merged, evaluated, and checked against stored alert state.
4. Qualifying cases move through research, 15-minute RSI/divergence calculations, and AI analysis.
5. Results are formatted for Telegram notification.

See [architecture](docs/ARCHITECTURE.md), [product requirements](docs/PRODUCT_REQUIREMENTS.md), [agent design](docs/AGENT_DESIGN.md), and [validation](docs/VALIDATION_AND_SAFETY.md).

## Portfolio artefacts

| Artefact | Purpose |
|---|---|
| [Product requirements](docs/PRODUCT_REQUIREMENTS.md) | Problem, users, scope, acceptance criteria |
| [Architecture](docs/ARCHITECTURE.md) | System boundaries and data flow |
| [AI-assisted analysis](docs/AGENT_DESIGN.md) | Research and analysis responsibilities |
| [Validation and safety](docs/VALIDATION_AND_SAFETY.md) | Data quality, human oversight, testing |
| [Roadmap](docs/ROADMAP.md) | Current evidence vs proposed improvements |
| [Workflow structure](workflow/workflow-structure.json) | Safe, non-importable structural overview of nodes and connections |

## Privacy and reproducibility

This public portfolio intentionally excludes the original importable workflow, executable code-node content, credentials, account identifiers, webhook URLs, private portfolio positions, and personal messaging destinations. The included JSON is a **structural representation, not an importable n8n workflow**.

## Disclaimer

This is a product/engineering portfolio project, **not investment advice**. AI output can be inaccurate, delayed, or incomplete; investment decisions require independent verification.
