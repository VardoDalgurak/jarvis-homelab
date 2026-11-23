# Jarvis Homelab versus quick-start assistants: comparative SWOT
Date: November 23, 2026 (Europe/Oslo)

## Executive assessment
Quick installation and a custom homelab answer different questions. A ready-made assistant can reduce time to first conversation; developing a maintainable personal system includes integration, recovery, permissions, and ongoing operation. Neither approach is inherently safer or more capable.

Jarvis Homelab has value as a learning project and a documented experiment in persistent context. Its public evidence does not establish superiority over packaged assistants, a finished hands-free experience, or a reproducible software release. Continuing is worthwhile if the next effort produces useful, measurable workflows. Past effort alone is not a reason to keep every custom component.

This report supplements the [W47 report](../weekly-reports/2026-W47.md); it does not rewrite historical reports or approve an architectural migration.

## Method and evidence boundaries
Reviewed on November 23: public project documents and the primary sources linked below. This is a documentation comparison, not a hands-on benchmark, code/security audit, or verification of particular Instagram videos. No competitor was installed, no setup time was measured, and no private Jarvis host or database was accessed.

- **Document checked:** the cited public material contains the statement.
- **Historically verified:** Jarvis's public ledger records a dated successful check; this review did not repeat it.
- **Reported:** an outcome or defect is described without independent retesting.
- **Planned/unverified:** implementation or acceptance is not established.
- Competitor capabilities below are **author-documented**, not independently demonstrated here. Missing evidence does not prove a missing feature.

## What a quick start actually covers
| Project / primary source | Documented starting point and advantage | Prerequisites, limitations and relevance |
|---|---|---|
| [CodesbyRohit/JARVIS tutorial](https://github.com/CodesbyRohit/JARVIS_/blob/main/docs/TUTORIAL.md) | Advertises a five-minute ZIP/launcher route to a voice assistant, plus a developer route. This lowers onboarding effort. | Requires a supported computer, microphone permission and a Gemini key with Live API access; the tutorial notes billing may need enabling. Cloud access and first-run success do not establish household integration, operating cost or long-term reliability. |
| [sam3gp8/jarvis-aio](https://github.com/sam3gp8/jarvis-aio) | Documents a five-minute start through HACS, conversation, Home Assistant voice integration, memory and optional vision. It offers substantial reusable functionality, not merely a visual shell. | Assumes Home Assistant and a configured model provider. Cameras, voice hardware and advanced features are subsequent setup. Local Ollama is an option; actual privacy depends on the chosen providers and configuration. Its documented memory means persistent context is not unique to our project. |
| [OpenJarvis](https://github.com/open-jarvis/OpenJarvis) | Documents local-first agents, installers, a starter model and task presets. The README estimates about three minutes on broadband. | Larger downloads continue afterwards. Hardware suitability, model quality and service authorization remain separate questions. Local-first does not mean every configuration avoids cloud services. It is a candidate for reuse, not a measured replacement for this homelab. |
| [Home Assistant Assist](https://www.home-assistant.io/voice_control/) | Documents a reusable voice architecture with local or cloud speech processing and conversation agents. | Included as a component baseline, not as a five-minute marketing claim. Microphone/speaker setup, language support and performance still need evaluation on the actual installation. |

The fair comparison separates time to install, time to first useful task, time to safe integrated operation, and maintenance time. These sources do not establish equal scope or equal prerequisites. A fast setup claim is neither proof of deception nor evidence that all deployment work is finished.

## Jarvis: evidence versus ambition
| Area | Publicly supported status | What remains unproven |
|---|---|---|
| Core and AI | November 15 ledger records a successful local API health check and external OpenAI response test. [State snapshot](../state/project-state-2026-11-15.md) | Current uptime, availability guarantees, and fully local AI. Local-model evaluation remains planned. |
| Memory | November 15 ledger records retrieval of relevant historical fragments and initialization of an auditable fact/event registry. [State snapshot](../state/project-state-2026-11-15.md) | Reliable recall across broad tasks, correct supersession handling under conflicting records, and recovery across restarts need dedicated acceptance evidence. Existing retrieval must not be mislabeled as entirely absent. |
| Voice | README records browser voice input tests and reported Piper integration. W47 records reported playback/formatting defects. [README](../../README.md), [W47](../weekly-reports/2026-W47.md) | Complete repeatable hands-free dialogue, wake-word activation and reliable interruption. Speech synthesis alone does not prove these. |
| Recovery | README documents historical database recovery testing. [README](../../README.md) | Current backup coverage, unattended operation and a fresh full recovery drill. A past restore is useful evidence, not a permanent guarantee. |
| Home automation | README documents Home Assistant setup; W47 identifies end-to-end integration and authorization work. [README](../../README.md), [W47](../weekly-reports/2026-W47.md) | A safely authorized household action completed from Jarvis, including denial and failure cases. |
| Security | W47 records an authorization review and requests for reproducible validation. [W47](../weekly-reports/2026-W47.md) | Completed remediation or a security assurance claim. Owning the server does not establish stronger security. |
| Distribution | Public documentation explicitly identifies this repository as a journal; source release, installer and license selection remain pending. [Contribution guide](../../CONTRIBUTING.md) | Reproducible installation by an independent user. |

## SWOT: Jarvis Homelab
This matrix is an assessment inferred from the evidence above, not a ranking based on measured competitor performance.

| Category | Assessment | Practical consequence |
|---|---|---|
| **Strengths — internal** | Dated evidence distinguishes tests from plans; persistent retrieval and a fact registry have historical test evidence; reused hardware supports hands-on learning; custom integration allows project-specific behavior. | Preserve the evidence ledger and learning record. Demonstrate usefulness rather than equating architectural complexity with maturity. |
| **Weaknesses — internal** | No distributable source product or installer; incomplete voice experience; unresolved authorization validation; multiple integration surfaces; external AI dependency. | Reduce scope and finish one workflow. Maintenance, electricity, API use and operator time belong in the cost assessment. |
| **Opportunities — external** | Existing voice stacks, assistants and model runtimes may replace custom plumbing. Community review can improve documentation and reproducibility. | Evaluate reuse in isolation, check component licenses before redistribution, and publish measured acceptance results. |
| **Threats — external** | Provider/API changes, outages, dependency vulnerabilities, model errors, malicious input influencing actions, hardware limits and maintainer availability can undermine operation. | Bound action permissions, keep rollback/recovery paths, test denied actions, and measure resource use before adding workloads. These are risk scenarios, not claims of observed breaches. |

Quick-start alternatives have their own trade-offs: packaged setup may deliver useful interaction sooner and reduce custom maintenance, while introducing dependency on upstream design and updates. Local inference can reduce cloud exposure but requires suitable resources. A custom homelab offers flexibility but transfers integration and operating responsibility to its maintainer. Neither “local” nor “open source” alone guarantees privacy, quality or safety.

## Proposed next experiments — not approved decisions or completed work
1. **Authorization acceptance:** use sanitized test identities to demonstrate allowed and denied actions across supported interfaces. Record expected/actual outcomes, date and version; do not publish sensitive enforcement details.
2. **One voice loop:** compare the current path with Assist in an isolated trial. Measure task success, response latency, interruption, recovery after restart, and resource use under the same conditions.
3. **Memory correctness:** save a non-sensitive fact, correct it, restart, and verify the active correction is retrieved while the earlier value remains historical. Include an unrelated query to detect irrelevant recall.
4. **One household workflow:** start with a read-only device-state request; add a reversible action only after authorization and confirmation behavior pass.
5. **Reproducibility and cost:** record prerequisites, setup time from a clean environment, operator interventions, API usage and resource consumption. Set acceptance thresholds before testing. Evaluate a component replacement if it achieves those thresholds with lower maintenance effort.

No benchmark results, savings, release dates or completed migrations are claimed. Learning is a legitimate benefit; future engineering choices should still be judged by usefulness and maintainability.

## Publication and privacy
This report uses public, sanitized documentation and public upstream sources. It contains no private conversation export, credentials, personal notes, private service locations or device identifiers. Source pages may change; their claims were reviewed on November 23, 2026. Jarvis evidence is explicitly dated, with the latest inspected state snapshot from November 15 and subsequent findings through November 22.

GitHub publication and Discord delivery are separate outcomes. This document does not assert that a Discord message was delivered. Recommendations here are proposals, not new entries in the approved decision register.
