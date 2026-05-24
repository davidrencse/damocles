# RelayJack

## Summary

 A browser-based operator console that coordinates real-world NTLM relay workflows for authorized assessments, managing targets, relays, and post-auth actions from one interface.

## Category

 Credential Relay Orchestrator

## Difficulty

 Advanced

## Safe Scope

 Only use against systems you are explicitly authorized to assess. The project must include clear guardrails for consent, target allowlists, and non-production defaults; it must not automate abuse of third-party services.

## Features

 - Import and manage an explicit target allowlist
- Queue and coordinate relay jobs against approved internal endpoints
- Track live session state, capture metadata, and record operator actions
- Plugin hooks for post-auth modules with strict scope checks
- Artifact export for engagement notes and evidence bundles
- Role-based operator controls and audit logging
- One-click shutdown and cleanup for active jobs
- Offline-first UI for field use during assessments

## Tech Stack

 - React
- TypeScript
- Vite
- Tailwind CSS
- IndexedDB
- WebSocket
- Node.js
- Express

## File Structure

 - src/
- src/components/
- src/pages/
- src/state/
- src/api/
- src/lib/
- src/plugins/
- src/styles/
- public/
- docs/

## Acceptance Criteria

 - Can create, edit, and revoke an approved target list
- Can start, pause, and terminate relay jobs from the UI
- Can display job status, timestamps, and operator audit events
- Can export a structured report of actions and captured metadata
- Rejects any action outside the configured allowlist
- Builds successfully as a static GitHub Pages portfolio project

## Documentation Requirements

 - README with purpose, scope boundaries, and authorization warning
- Architecture overview describing frontend, API, and plugin boundaries
- Setup guide for local development and static deployment
- Operator workflow documentation for approved engagement use
- Security notes covering allowlist enforcement and audit logging
- Changelog and contribution guidelines
