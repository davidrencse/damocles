# CookieForge

## Summary

 A browser-driven session replay and token-harvesting tool that detects exposed auth flows, replays edge-case requests, and captures reusable session artifacts from target-owned web properties with strict operator-controlled scope rules.

## Category

 offensive web automation

## Difficulty

 advanced

## Safe Scope

 Only use against systems you own or have explicit written authorization to assess. The project must enforce allowlisted target domains, block credential stuffing behavior, log all actions locally, and include a hard safety gate that prevents third-party misuse.

## Features

 - Allowlisted target manager with per-domain authorization notes
- Browser automation flow recorder for login and session transitions
- HTTP request replay engine for authenticated endpoints
- Token and cookie extraction from permitted flows
- Session expiry detection and refresh chaining
- Exportable artifact bundle for authorized reporting
- Operator command log with immutable timestamps
- Configurable rate limiting and abort conditions

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
- src/hooks/
- src/lib/
- src/rules/
- src/types/
- public/
- docs/
- docs/usage.md
- docs/scope-policy.md
- docs/authorization.md
- README.md

## Acceptance Criteria

 - Project blocks execution unless at least one explicit allowlisted domain is configured
- Recorded browser flows can be replayed against the same authorized domain
- Cookies, session headers, and tokens are captured only from approved targets
- Rate limiting and kill-switch controls are enforced in the UI and runtime
- Exported bundles include timestamps, scope metadata, and operator notes
- The app builds successfully for GitHub Pages deployment

## Documentation Requirements

 - README with purpose, scope boundaries, and deployment steps
- Usage guide showing authorized workflow setup and replay process
- Scope policy document explaining allowed and disallowed use
- Authorization template for operator sign-off before use
- Security notes covering logging, data handling, and safety gates
