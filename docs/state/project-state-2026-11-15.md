# Jarvis — Project state (evidence ledger)

Generated: 2026-11-15 11:12 UTC

This is a filtered project-status snapshot, not live telemetry or a software release.
Only facts explicitly marked public are included. Personal conversation history,
credentials, private network identifiers and device addresses are never published.
An item labelled *reported* has not been independently rechecked; an item labelled
*planned* is not installed. Verified items describe the stated check at its date,
not an unconditional guarantee that the service is operational today.

## AI

- **ai.external_provider** [VERIFIED]: The assistant currently uses the external OpenAI Responses API, not an exclusively local language model.
  - Evidence: CT100 ai.py sends authorized requests to the OpenAI Responses API; a live test succeeded on 2026-11-15.
  - As of: 2026-11-15; provenance: system_check
- **ai.local_model** [PLANNED]: Evaluate Ollama for a possible hybrid local/cloud architecture; no local LLM deployment is confirmed.
  - Evidence: Previous Jarvis architecture discussion proposed Ollama; deployment not established.
  - As of: 2026-11-14; provenance: user_report
## Infrastructure

- **infra.jarvis_core** [VERIFIED]: Jarvis Core's local API was active and its health check succeeded.
  - Evidence: Local systemctl service check and local HTTP health endpoint, performed by automated verifier.
  - As of: 2026-11-15; provenance: system_check
- **infra.packard_bell** [VERIFIED]: The public project documents repurposing a Packard Bell desktop as the home server.
  - Evidence: Public README explicitly describes the salvaged Packard Bell and Proxmox installation.
  - As of: 2026-11-15; provenance: project_document
  - Public source: https://github.com/VardoDalgurak/jarvis-homelab
## Memory

- **memory.historical_retrieval** [VERIFIED]: Jarvis can retrieve historical fragments before generating an OpenAI response.
  - Evidence: A real Jarvis AI test in Spanish retrieved relevant MPD/MPV history without changing conversation tables.
  - As of: 2026-11-15; provenance: system_check
- **memory.master_registry** [VERIFIED]: A dedicated, auditable registry separates verified facts, user reports, plans and superseded decisions.
  - Evidence: PostgreSQL master fact/event tables and append-only audit trigger initialized on 2026-11-15.
  - As of: 2026-11-15; provenance: system_check
## Publishing

- **github.progress_document** [VERIFIED]: A development log for 2026-11-05 through 2026-11-10 is published in the public repository.
  - Evidence: GitHub repository tree lists docs/progress/2026-11-05-to-10.md.
  - As of: 2026-11-15; provenance: project_document
  - Public source: https://github.com/VardoDalgurak/jarvis-homelab/blob/main/docs/progress/2026-11-05-to-10.md
- **github.public_journal** [VERIFIED]: The public GitHub repository is currently a project journal, not a downloadable software release.
  - Evidence: Public README and CONTRIBUTING.md clarify the project scope and licensing status.
  - As of: 2026-11-15; provenance: project_document
  - Public source: https://github.com/VardoDalgurak/jarvis-homelab
## Voice

- **voice.wake_word** [PLANNED]: Hands-free wake-word activation and a complete microphone/speaker dialogue pipeline remain pending.
  - Evidence: Public README lists making voice repeatable as a future priority.
  - As of: 2026-11-15; provenance: project_document
  - Public source: https://github.com/VardoDalgurak/jarvis-homelab
## Website

- **web.green_mascot** [REPORTED]: The green Jarvis mascot was applied to the private interface, and the public site was reported updated.
  - Evidence: Private HTML was checked on CT100; user confirmed publication of the public Cloudflare site on 2026-11-15.
  - As of: 2026-11-15; provenance: user_report

## Evidence policy

A fact is marked VERIFIED only after a direct observation or system check.
User-reported outcomes remain REPORTED until independently checked.
Changed or abandoned decisions are SUPERSEDED rather than silently overwritten;
the private ledger retains all revisions and reasons.
