# BeaconSnare

## Summary

 A red-team style browser beacon capture tool that detects, fingerprints, and correlates real outbound callback patterns from controlled targets during authorized assessments, focusing on webhooks, DNS over HTTPS, and blind SSRF-style exfil paths.

## Category

 Offensive Web Recon

## Difficulty

 Advanced

## Safe Scope

 Only use on systems you own or have explicit written permission to test. The project must include guardrails to restrict targets to approved domains, block public IP ranges, and log every action for auditability. No live exploitation payloads, credential theft, persistence, or unauthorized access features.

## Features

 - Authorized target allowlist with domain and CIDR restrictions
- Beacon endpoint generator for controlled callback testing
- Callback correlation engine for HTTP, DNS, and webhook events
- Request fingerprinting with headers, timing, and payload metadata
- Session timeline of observed outbound connections
- Rules for detecting blind SSRF-style egress behavior in approved assets
- Exportable evidence bundle for reporting and incident follow-up
- Operator audit log with immutable action history
- Rate limiting and safety checks to prevent misuse
- Optional browser-based control panel for campaign setup and review

## Tech Stack

 - React
- TypeScript
- Vite
- Tailwind CSS
- Node.js
- Express
- PostgreSQL
- Prisma
- Docker

## File Structure

 - src/
- src/components/
- src/pages/
- src/hooks/
- src/api/
- src/utils/
- server/
- server/routes/
- server/services/
- server/middleware/
- prisma/
- docs/
- public/

## Acceptance Criteria

 - User can create an approved target list before any testing begins
- System rejects non-allowlisted domains and private/internal abuse paths outside scope
- User can generate a controlled callback endpoint and view resulting events
- Captured callbacks are grouped into sessions with timestamps and metadata
- Evidence export includes raw events, summaries, and operator actions
- All actions are written to an audit trail
- Project runs cleanly as a GitHub Pages portfolio frontend with documented backend requirements
- No destructive actions, credential harvesting, or stealth persistence features are included

## Documentation Requirements

 - README with project purpose, authorized-use warning, and scope controls
- Architecture overview explaining frontend, backend, and callback ingestion flow
- Setup guide with environment variables and local run steps
- Usage guide showing how to define an allowlist and review callbacks
- Security section describing anti-abuse safeguards and logging
- API documentation for callback ingestion and event retrieval endpoints
- Evidence export format documentation
- Changelog and roadmap
