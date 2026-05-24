# CookieRift

## Summary

 A browser-based offensive testing utility for identifying weak session handling on authorized targets by probing cookie scope, token rotation gaps, and replayable auth flows, then packaging findings into a clean attack report for pentest portfolios.

## Category

 HTTP Session Hijack Tool

## Difficulty

 Advanced

## Safe Scope

 Use only on systems you own or have explicit written permission to test. Focus on controlled targets, sanctioned bug bounty programs, or internal environments with authorization.

## Features

 - Target URL intake with auth-flow mapping
- Session cookie scope and attribute inspection
- Token reuse detection across requests
- Auth endpoint replay analysis
- Header tampering tester for weak session controls
- Exportable attack-chain report
- Notes for manual verification of findings
- Session lifecycle timeline for authorized assessments

## Tech Stack

 - React
- TypeScript
- Vite
- Tailwind CSS
- Playwright
- Node.js

## File Structure

 - src/
- src/components/
- src/pages/
- src/lib/
- src/tests/
- public/
- docs/
- README.md

## Acceptance Criteria

 - Can load a target and record observed session cookies and auth responses
- Can detect repeated or unchanged session tokens across sequential requests
- Can identify insecure cookie attributes such as missing HttpOnly, Secure, or SameSite
- Can generate a concise offensive findings report in Markdown
- Can run against an authorized target without requiring any third-party service
- Can be deployed as a GitHub Pages portfolio project with a polished UI
- Can clearly separate tested targets, findings, and evidence

## Documentation Requirements

 - README with project purpose, authorized-use warning, setup, and build steps
- Threat model section explaining what session weaknesses the tool looks for
- Usage guide showing safe, permission-based testing workflow
- Report example section with sample findings output
- Architecture notes covering React UI, request handling, and report generation
- Ethics and authorization policy stating the tool is for permitted testing only
