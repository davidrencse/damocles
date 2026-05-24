# HeaderRift

## Summary

 A focused HTTP request manipulation tool that crafts and replays custom header-borne attack chains against exposed web apps and APIs, with modules for header smuggling variants, auth bypass attempts, cache poisoning probes, and WAF evasion payload rotation.

## Category

 HTTP attack tooling

## Difficulty

 advanced

## Safe Scope

 Use only on systems you own or have explicit authorization to assess. The tool must ship with hard safety controls, target allowlisting, rate limiting, and a default block on public IP ranges unless explicitly enabled.

## Features

 - Custom raw request builder for headers, cookies, and edge-case encodings
- Replay engine for chaining multiple crafted requests in sequence
- Module set for request smuggling, header injection, cache poisoning, and auth-header abuse
- Target allowlist with domain/IP pinning and mandatory confirmation prompts
- Payload profile rotation for different proxies, CDN edges, and backend parsers
- Response diffing to compare status codes, headers, body length, and timing
- Exportable attack traces in JSON and HAR-like formats
- CLI mode plus a React control panel for managing profiles and runs

## Tech Stack

 - React
- TypeScript
- Vite
- Tailwind CSS
- Node.js
- Express
- PostgreSQL
- Prisma

## File Structure

 - src/
- src/components/
- src/pages/
- src/modules/
- src/utils/
- src/types/
- server/
- server/routes/
- server/services/
- server/db/
- public/
- docs/
- README.md

## Acceptance Criteria

 - Users can define a target profile with hostname, method set, and allowed paths
- Users can build and save raw HTTP payload chains with custom headers and body templates
- The app can send replayed requests and show response differences across attempts
- The app includes at least three attack modules focused on header-level abuse cases
- The app enforces allowlist validation before any outbound request is sent
- The app records run history with timestamps, payload names, and outcomes
- The GitHub Pages front-end works as a polished portfolio UI for showcasing the project

## Documentation Requirements

 - README with purpose, scope limits, and authorization disclaimer
- Installation and local development instructions
- Architecture overview for the frontend, API, and module system
- Module reference documenting each attack technique at a high level
- Safe-use section describing allowlisting, rate limits, and blocked targets
- Example workflows showing how to create a profile, run a chain, and export results
- Changelog and roadmap
- License file
