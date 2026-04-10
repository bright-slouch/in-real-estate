# Changelog

All notable changes to the real-estate-plugin will be documented in this file.

## [0.1.0] - 2026-03-30

### Added
- `.claude-plugin/plugin.json` with plugin metadata and user config schema.
- `agents/orchestrator.md` — orchestrator agent coordinating all 19 skills.
- `settings.json` pointing to orchestrator as default agent.
- `CLAUDE.md` with plugin-level instructions, config system, agent registry, and skill catalog.
- `README.md` with user-facing overview and installation guide.
- `test-manifest.yaml` with 6-tier testing hierarchy.
- `LICENSE` (MIT).
- This `CHANGELOG.md`.
- `config/_template/` — 7 YAML config templates with inline documentation.
- `references/` — 8 substantive Indiana law, MIBOR, and Central Indiana reference documents.
- `templates/` — 7 transaction and presentation templates.
- `re-agent-setup/` — foundational skill for agent onboarding and config generation.
- `scheduled/README.md` — placeholder for future scheduled tasks.

## [0.5.0] - 2026-03-31

### Added
- `re-transaction-manager/` — Phase 4 transaction management skill. Post-contract command
  center from acceptance through clear-to-close. Deadline calendar generation, Google Calendar
  integration, party coordination emails, weekly status updates, and mid-transaction issue
  management (inspection extensions, appraisal delays, financing extensions, title issues,
  amendment tracking). Includes `references/deadline-checklist.md`.
- `re-closing-coordinator/` — Phase 4 closing coordination skill. Final-mile skill from
  clear-to-close through post-closing follow-up. Pre-closing checklist, Central Indiana utility
  transfer list, Closing Disclosure review guide, final walkthrough checklist, closing day prep
  for buyers and sellers, and full post-closing sequence (gift, review request, homestead
  exemption reminder, anniversary scheduling). Includes `references/closing-checklist.md`.
