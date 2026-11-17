# Brandon Gordon

**AI infrastructure · Agent observability · Model evaluation · Retrieval**

My background is in video production. I’m transitioning into AI engineering by building and releasing practical tools for inspecting agent behavior, evaluating model capabilities, and retrieving evidence with clear provenance.

## Selected projects

Three complementary tools, each independently installable and usable.

### [Agent Flight Recorder](https://github.com/Leogy101/agent-flight-recorder) · Observe

Explicit Python instrumentation captures agent, model, and tool operations in portable recordings. A local timeline viewer helps inspect retries, failures, timing, and missing evidence. Metadata-only capture is the default; recorded playback does not re-execute an agent.

**Release verification:** 168 Python tests, 44 viewer tests, and 18 Chromium workflows passed.

[Experimental alpha v0.1.0-alpha.1](https://github.com/Leogy101/agent-flight-recorder/releases/tag/v0.1.0-alpha.1) · [Verification](https://github.com/Leogy101/agent-flight-recorder/actions/runs/43283247673)

### [Governed Capability Broker](https://github.com/Leogy101/governed-capability-broker) · Evaluate

Deterministic Gate 0 handlers execute supported tasks without an LLM. Model research, lightweight benchmarks, and durable capability bios support explainable, policy-aware routing previews. Tested profiling paths include local Ollama and subscription-backed OpenClaw/Codex.

**Published evidence:** 108 benchmark observations across 7 GPT models and 40 requested reasoning configurations. These limited fixtures are not universal capability rankings; effective reasoning was not independently verified.

[Experimental alpha v0.3.2a1](https://github.com/Leogy101/governed-capability-broker/releases/tag/v0.3.2a1) · [Benchmark methodology](https://github.com/Leogy101/governed-capability-broker/blob/v0.3.2a1/docs/public/BENCHMARKS.md)

### [Knowledge Retrieval Engine](https://github.com/Leogy101/knowledge-retrieval-engine) · Retrieve

Local SQLite FTS5 retrieval with exact citations, immutable revisions, scoped access, and revocation. Bounded context and task checkpoints preserve evidence references and revalidate them when work resumes. CLI and optional MCP support work without GCB or a cloud model.

**Release verification:** 313 regression tests passed, with one documented optional skip; 24 lifecycle and MCP checks passed.

[Experimental alpha v0.3.2a1](https://github.com/Leogy101/knowledge-retrieval-engine/releases/tag/v0.3.2a1) · [Known limitations](https://github.com/Leogy101/knowledge-retrieval-engine/blob/v0.3.2a1/docs/LIMITATIONS.md)

## Engineering approach

- Reproducible offline examples, explicit test fixtures, and measured results.
- Privacy boundaries, provenance, negative-path tests, and documented unknowns.
- Independent Python packages, clean-install checks, GitHub Actions, and security checks.

These are experimental alphas with documented support boundaries. GCB’s native OpenClaw/Hermes routing remains preview-only. KRE can miss fragmented evidence; independent semantic review is incomplete, and generalized token or cost savings remain unproven.
