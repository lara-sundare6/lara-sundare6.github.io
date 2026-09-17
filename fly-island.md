---
layout: page
title: "Fly Island"
permalink: /fly-island/
---

*A solo-built AgentOps platform for watching CI failures, costing them, and remediating only inside hard bounds.*

Hoverfly stays long-lived and observant. A separate remediation worker turns detections into a typed plan. Bee is the only component that can act, and it runs once, does one bounded write through MCP (with a controlled REST fallback), then exits. Between plan and act sit hard gates: shadow mode by default, path allowlists, token and carbon budgets, a circuit breaker, and an admin kill switch.

![Fly Island architecture: GitHub Actions telemetry enters a Rust control plane where Hoverfly observes, a bounded worker plans, and only an ephemeral Bee can execute through gated MCP tools.](/assets/fly-island/fly-island-architecture.svg)

Design essay: [Biomimetic engineering: capping the physical cost of unbounded AI](/category/2026/07/10/biomimetic-engineering-capping-the-physical-cost-of-unbounded-ai.html). A deeper architecture walkthrough is available on request or in an interview.

[Download the diagram as PNG](/assets/fly-island/fly-island-architecture.png) for slides or email.
