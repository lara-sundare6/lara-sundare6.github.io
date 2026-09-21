---
layout: page
title: "Fly Island"
permalink: /fly-island/
---

*A solo-built AgentOps platform for watching CI failures, costing them, and remediating only inside hard bounds.*

<figure style="margin: 1.75rem -12% 1.25rem; max-width: none;">
  <img
    src="/assets/fly-island/fly-island-architecture.svg"
    alt="Fly Island architecture: GitHub Actions telemetry enters a Rust control plane where Hoverfly observes, a bounded worker reserves budget and plans, and only an ephemeral Bee can execute a brokered repository-scoped GitHub write."
    style="width: 100%; height: auto; display: block;"
  />
  <figcaption style="margin-top: 0.85rem; font-size: 0.95rem; line-height: 1.45; color: #555;">
    <em>Hoverfly stays long-lived and observant. A separate remediation worker times the failing run, reserves SCI/USD/token budget, and produces a typed plan. Bee is the only component that can act: it runs once, performs one brokered repository-scoped REST write, then exits. Between plan and act sit hard gates: fail-closed pre-effect governance, scoped principals, a path allowlist, a circuit breaker, and an admin kill switch.</em>
  </figcaption>
</figure>

Design essay: [Biomimetic engineering: capping the physical cost of unbounded AI](/category/2026/07/10/biomimetic-engineering-capping-the-physical-cost-of-unbounded-ai.html). A deeper architecture walkthrough is available on request or in an interview.

[Download the diagram as PNG](/assets/fly-island/fly-island-architecture.png) for slides or email.
