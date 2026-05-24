# PhishKey

## Summary

 A high-precision credential interception platform that fingerprints target login flows, recreates them locally, and captures submitted secrets with auto-validation, replay checks, and delivery chaining for real-world phishing operations.

## Category

 Credential Capture

## Difficulty

 Advanced

## Safe Scope

 Use only on systems you own or have explicit authorization to assess. The project may emulate credential interception logic and workflow automation for security research and defensive validation, but must not include instructions for unauthorized access or evasion.

## Features

 - Target login flow profiler that records form structure, field names, cookies, redirects, and post-auth behavior
- Credential submission relay with exact field mapping and response handling
- Replay detection for submitted credentials to identify reused passwords across multiple captured flows
- Session-token extraction and normalization from common auth patterns
- Template generator for cloning login entry points from captured metadata
- Automated credential triage that labels valid, invalid, MFA-protected, or locked responses
- Encrypted local secret store for captured data with export controls
- Operator notes and campaign tagging for multi-target engagement tracking
- Rate-aware request scheduling to reduce lockouts during authorized assessments
- Import/export of target profiles as portable JSON bundles

## Tech Stack

 - React
- TypeScript
- Vite
- Tailwind CSS
- Node.js
- Express
- SQLite
- Playwright
- Zod

## File Structure

 - src/
- src/components/
- src/pages/
- src/lib/
- src/hooks/
- server/
- server/routes/
- server/services/
- server/storage/
- public/
- docs/
- README.md

## Acceptance Criteria

 - Can create and manage target profiles with captured login metadata
- Can generate a working credential relay flow from a stored profile
- Can classify authentication outcomes from server responses
- Can store captured secrets locally in encrypted form
- Can export and import target bundles as JSON
- Can run as a static GitHub Pages frontend with a documented backend deployment path for full functionality
- Includes clear authorization safeguards and scope warnings in the UI

## Documentation Requirements

 - README with project purpose, scope limitations, and authorized-use warning
- Setup guide for frontend and backend
- Architecture overview covering capture flow, storage, and replay handling
- Configuration reference for target profiles and secret storage
- Usage guide with example authorized workflows
- Security notes describing data handling, encryption, and retention
- Deployment guide for GitHub Pages frontend and optional server hosting
- Changelog and contribution guidelines
