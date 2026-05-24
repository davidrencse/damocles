# SSTI Beacon Forge: Outbound Canary Exfiltration Recon

## Summary

 A security operations tool that performs authorized server-side template injection validation against your own controlled targets by planting unique canary beacons in templated content, then detecting whether those beacons are rendered, transformed, or echoed back through outbound callbacks. It is designed to help red teams and pentesters prove template injection impact in a controlled environment, while producing a polished GitHub Pages portfolio with report generation and replayable attack traces.

## Category

 Offensive Security

## Difficulty

 Advanced

## Safe Scope

 Use only on systems you own or have explicit written permission to test. The project must restrict execution to whitelisted targets, avoid payloads that perform destructive actions, and focus on controlled validation of template-rendering behavior and outbound callback verification within authorized environments.

## Features

 - Whitelisted target manager with explicit authorization notes
- Template probe generator for controlled SSTI verification strings
- Outbound canary callback listener to confirm rendering paths
- Request correlation IDs and evidence capture for each test attempt
- Replayable attack trace timeline with raw HTTP request/response storage
- Risk scoring for observed template behavior and injection indicators
- Exportable findings bundle in JSON and Markdown
- Target-specific notes for common template engines and payload families
- One-click GitHub Pages case-study mode with sanitized demo data
- Role-based access gating for operator actions

## Tech Stack

 - React
- TypeScript
- Vite
- Tailwind CSS
- Node.js
- Express
- SQLite
- Zod
- Playwright
- Markdown

## File Structure

 - src/
- src/components/
- src/pages/
- src/features/
- src/features/probes/
- src/features/evidence/
- src/features/reports/
- src/lib/
- src/types/
- public/
- server/
- server/routes/
- server/services/
- server/db/
- docs/
- docs/case-studies/
- tests/

## Acceptance Criteria

 - User can create and save an authorized target with scope notes and contact details
- User can generate controlled SSTI probes for at least three template engines
- User can register a callback endpoint and observe inbound canary hits
- User can view each test as a trace with timestamps, request IDs, and evidence artifacts
- User can export a complete findings report in Markdown and JSON
- User can run the app locally with a documented setup flow
- GitHub Pages version renders a polished portfolio case-study without exposing unsafe automation details
- All operator actions are blocked unless the target is marked authorized
- Evidence storage preserves raw results for later review
- Project includes tests for probe generation, evidence logging, and report export

## Documentation Requirements

 - README with project purpose, authorization boundaries, and setup steps
- Architecture overview explaining frontend, API, evidence storage, and callback flow
- Threat model and safety section describing allowed use only
- Operator guide for creating targets, generating probes, and exporting reports
- Developer guide covering local development, environment variables, and testing
- API documentation for target management, probe execution, callback ingestion, and report export
- Case study write-up suitable for GitHub Pages showcasing the workflow with sanitized examples
- Changelog and versioning notes for future additions
