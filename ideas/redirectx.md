# RedirectX

## Summary

 A redirection-hijack assessment tool that maps open redirect chains, token leaks, and OAuth callback abuse paths in public targets, then generates actionable takeover paths and proof links for authorized operators.

## Category

 Offensive Web Utility

## Difficulty

 Advanced

## Safe Scope

 Use only on assets you are explicitly authorized to assess. Focus on externally visible redirect endpoints, callback parameters, and URL-based trust flaws; do not include credential theft, persistence, or destructive actions.

## Features

 - Crawl a target domain for redirect-capable endpoints and extract parameterized bounce paths
- Detect chained redirects, mixed-domain hops, and reflected token leakage in query strings and fragments
- Identify OAuth callback and SSO handoff URLs that accept attacker-controlled destinations
- Generate reproducible exploit URLs for authorized validation of redirect abuse
- Track findings by severity, affected endpoint, and exploitability
- Export concise operator-ready reports with evidence and remediation notes

## Tech Stack

 - React
- TypeScript
- Vite
- Tailwind CSS
- Node.js
- Playwright
- Zod

## File Structure

 - src/
- src/components/
- src/pages/
- src/features/
- src/lib/
- src/types/
- src/styles/
- public/
- docs/
- README.md

## Acceptance Criteria

 - Can ingest a URL or domain and enumerate redirect-related endpoints
- Can display redirect chains with parameters and final destinations
- Can flag likely open redirect and callback abuse issues with clear evidence
- Can generate a shareable report containing findings and remediation guidance
- Must run as a GitHub Pages portfolio project with no backend dependency for the UI

## Documentation Requirements

 - README with project overview, authorized-use notice, installation, and build steps
- Usage guide explaining input format, scan workflow, and report export
- Architecture section describing the redirect analysis pipeline
- Security and ethics section limiting use to authorized targets only
- Example output section showing a sample finding and remediation note
- Contribution guide and release/versioning notes
