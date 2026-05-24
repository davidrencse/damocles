# RedirectForge

## Summary

 A single-purpose offensive utility that crawls an authorized target and finds open redirect and redirect-chaining abuse paths, then automatically builds weaponized redirect URLs for controlled phishing, traffic pivoting, and token leakage checks against your own infrastructure or authorized targets.

## Category

 HTTP Redirect Abuse Tool

## Difficulty

 Advanced

## Safe Scope

 Use only on systems you own or have explicit written permission to assess. The project must include hard limits to prevent third-party abuse, enforce target allowlisting, and block credential collection or live exfiltration.

## Features

 - URL crawler focused on redirect endpoints, callback URLs, and next/return/path parameters
- Redirect chain resolver that traces multi-hop redirects and flags trust boundary breaks
- Payload builder for safe redirect abuse strings and parameter permutations
- Allowlist-based target control with domain and CIDR restrictions
- Request replay engine with rate limiting and audit logs
- Heuristic scoring for exploitable redirect patterns
- Exportable findings package with reproduction steps and raw evidence
- CLI-first workflow with optional GitHub Pages documentation frontend

## Tech Stack

 - React
- TypeScript
- Vite
- Tailwind CSS
- Node.js
- Playwright
- Axios

## File Structure

 - src/
- src/components/
- src/pages/
- src/lib/
- src/lib/redirects/
- src/lib/replay/
- src/data/
- public/
- docs/
- docs/README.md
- docs/usage.md
- docs/ethics.md

## Acceptance Criteria

 - Detects redirect parameters in URLs and forms with a configurable crawler
- Correctly resolves and records redirect chains up to a defined hop limit
- Generates reproducible proof strings without sending data to unapproved hosts
- Blocks any request outside the configured allowlist
- Produces a clean findings report with severity, evidence, and remediation notes
- Builds successfully as a GitHub Pages-ready portfolio project
- Includes a documented threat model and authorization boundary

## Documentation Requirements

 - README with project purpose, authorization warning, and setup instructions
- Architecture section explaining crawler, resolver, and replay flow
- Usage guide with example inputs and expected outputs
- Ethics and authorization document describing allowed use only
- Security notes covering allowlisting, rate limits, and logging
- Deployment notes for GitHub Pages build and static hosting
