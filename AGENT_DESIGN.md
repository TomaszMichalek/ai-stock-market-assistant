# AI-Assisted Research Design

## Why separate research and analysis?
The exported workflow contains two distinct Perplexity API request stages: **Perplexity Deep Research** and **Perplexity Analysis**, each followed by processing steps. This separation can help distinguish gathering context from interpreting it.

## Responsibilities visible in the workflow
1. **Research input preparation:** structure market context for an AI research request.
2. **Research retrieval:** call Perplexity and parse the response.
3. **Technical indicator processing:** collect and calculate 15-minute RSI/divergence signals in code nodes.
4. **Analysis request:** combine available context and request a second AI interpretation.
5. **Message formatting:** convert the result into a Telegram-readable output.

## Human / machine responsibility split
- **Deterministic code:** fetching/parsing data, calculating indicators, screening conditions, handling alert state.
- **AI:** contextual research and interpretation, subject to possible errors.
- **Human:** assess credibility and decide whether any trade is appropriate.

## What this is not
The presence of multiple AI calls does not by itself prove independent autonomous agents, tool-using agent loops, or self-learning. Those would require separate implementation evidence. The project is best described as an **AI-assisted multi-stage workflow**.
