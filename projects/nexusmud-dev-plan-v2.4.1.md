---
title: "NexusMUD Development Plan — v2.4.1"
layout: page
---

# NexusMUD Development Plan (v2.4.1)

Generated: 2026-06-13
Repository referenced: hn3tdevops-jpg/workforce-nexusmud
Status: in_progress
Completion: 74%

This page is an auto-generated, human-readable summary of the dev plan JSON (nexusmud-dev-plan-v2.4.1.json). Use it as a public/internal project status and roadmap reference.

## Quick summary

- Current milestone: v2.4.1 (phase: Workforce & Agents)
- Target date for v2.4.1: 2026-06-30
- Overall completion: 74%
- Test coverage: 61% (goal in Phase 5: 80%)
- Open issues in the plan: 12

## Phases (from plan)

1. Foundation — completed (milestone v2.0.0) — packages: core, economy — completed 2026-03-15
2. API & World Engine — completed (v2.2.0) — gateway_api, world_engine — completed 2026-04-20
3. Territory System — completed (v2.3.0) — territory — completed 2026-05-10
4. Workforce & Agents — in_progress (v2.4.1) — packages: workforce, agent_core, zocomputer — target 2026-06-30
5. Audit Resolution & Hardening — planned (v2.5.0) — target 2026-08-01

## Phase-4 tasks (current focus)

- task-401: Fix agent_core deadlock in TaskScheduler — in_progress — priority: critical — assignee: agent_core_team — estimate: 3d
- task-402: Resolve workforce hot-reload role conflicts — open — priority: critical — assignee: workforce_team — estimate: 2d
- task-403: Complete agent_core API documentation — open — priority: medium — estimate: 1d
- task-404: ZoComputer queue overflow signal — open — priority: low — estimate: 0.5d

## Dependencies (summary)

- workforce and agent_core depend on core and world_engine and economy and territory; gateway_api depends on many pieces including workforce.
- Keep integration test focus on cross-package interactions between core, world_engine, workforce, gateway_api, and agent_core.

## Metrics

- Total LOC: 41,100
- Test coverage: 61%
- Open issues: 12
- Resolved issues: 34
- Packages stable: 5
- Packages in progress: 3

## Recommended uses for this page

1. Public roadmap entry: link this page from the project README so contributors and stakeholders can see status and timeline.
2. Issue triage dashboard: link tasks to GitHub issues and a Project board; mark critical tasks as blockers for the v2.4.1 milestone.
3. Release checklist: use these phase tasks as a release checklist for v2.4.1 — close task-401/402 before cutting the release.
4. CI gating: add a CI job to block merges to v2.4.1 branch if agent_core TaskScheduler deadlock reproduces in CI.
5. Documentation portal: convert task-403 into a checklist and publish generated API docs (Sphinx/ MkDocs) under /docs or the site.

## Immediate actionables (what you can make live now)

- Share this page on your GitHub Pages site (this file) — done: this markdown file added under /projects.
- Create a lightweight Project board named "NexusMUD v2.4.1" and add the tasks above as cards (recommended next step).
- Add a status badge or link to this page from the main repo README: `projects/nexusmud-dev-plan-v2.4.1.md`.
- Publish agent_core API docs (task-403) as a docs site (MkDocs/Sphinx) under the GitHub Pages repo — recommended content/CI scaffolding below.

## Suggested next steps and checks

1. Prioritize and assign any missing owners for task-402/404 and create GitHub issues if not present.
2. Add a CI job (or reproduce locally) that runs the TaskScheduler stress test to catch the deadlock (task-401).
3. Add a hot-reload integration test that exercises role changes while services are active (task-402).
4. Raise test coverage toward 80% for Phase-5 — start by adding integration tests for world_engine >500 entities.
5. Add a CHANGELOG.md entry and a short release note template for v2.4.1.

## Example files & CI bits to make life easier (templates)

- A GitHub Actions workflow (example) to run unit + integration tests and publish docs on push to main.
- A CONTRIBUTING.md and ROADMAP.md that link back to this page.

---

Generated from plan id: nexusmud-dev-plan-v2 (version 2.4.1)
